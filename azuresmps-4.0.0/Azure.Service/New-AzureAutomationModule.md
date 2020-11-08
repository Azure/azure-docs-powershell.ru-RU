---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1F875179-E3CA-4BBB-822A-600777B2D980
online version: ''
schema: 2.0.0
ms.openlocfilehash: c93a09647e22f9d7f1c69cfd6aafe58799217686
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076223"
---
# <span data-ttu-id="d34de-101">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d34de-101">New-AzureAutomationModule</span></span>

## <span data-ttu-id="d34de-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d34de-102">SYNOPSIS</span></span>

<span data-ttu-id="d34de-103">Импортирует модуль в автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="d34de-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="d34de-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d34de-104">SYNTAX</span></span>

```
New-AzureAutomationModule -Name <String> -ContentLink <Uri> [-Tags <IDictionary>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d34de-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d34de-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="d34de-106">Командлет **New-AzureAutomationModule** импортирует модуль в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d34de-106">The **New-AzureAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="d34de-107">Модуль — это сжатый файл с расширением ZIP, содержащий папку, в которую входит один из следующих типов файлов:</span><span class="sxs-lookup"><span data-stu-id="d34de-107">A module is a compressed file, with a .zip extension, that contains a folder which includes one of the following file types:</span></span>

- <span data-ttu-id="d34de-108">Модуль Windows PowerShell (файл PSM1).</span><span class="sxs-lookup"><span data-stu-id="d34de-108">A Windows PowerShell module (psm1 file).</span></span> 

- <span data-ttu-id="d34de-109">Манифест модуля Windows PowerShell (файл PSD1).</span><span class="sxs-lookup"><span data-stu-id="d34de-109">A Windows PowerShell module manifest (psd1 file).</span></span> 

- <span data-ttu-id="d34de-110">Сборка (DLL-файл).</span><span class="sxs-lookup"><span data-stu-id="d34de-110">An assembly (dll file).</span></span>

<span data-ttu-id="d34de-111">Имена файлов ZIP, папок в ZIP-файлах и файлов в папке (. psm1, PSD. 1 или. dll) должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="d34de-111">The names of the zip file, the folder in the zip file, and file in the folder (.psm1, psd.1, or .dll) must match.</span></span>

## <span data-ttu-id="d34de-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d34de-112">EXAMPLES</span></span>

### <span data-ttu-id="d34de-113">Пример 1: импорт модуля</span><span class="sxs-lookup"><span data-stu-id="d34de-113">Example 1: Import a module</span></span>
```
PS C:\> New-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip"
```

<span data-ttu-id="d34de-114">Эта команда импортирует модуль с именем ContosoModule в учетную запись автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d34de-114">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="d34de-115">Модуль хранится в большом двоичном объекте Azure в учетной записи хранения с именем contosostorage и контейнером с именем modules.</span><span class="sxs-lookup"><span data-stu-id="d34de-115">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="d34de-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d34de-116">PARAMETERS</span></span>

### <span data-ttu-id="d34de-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d34de-117">-AutomationAccountName</span></span>
<span data-ttu-id="d34de-118">Указывает имя учетной записи автоматизации, в которой будет храниться модуль.</span><span class="sxs-lookup"><span data-stu-id="d34de-118">Specifies the name of the Automation account the module will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d34de-119">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="d34de-119">-ContentLink</span></span>
<span data-ttu-id="d34de-120">Общедоступный URL-адрес, например, веб-сайт или хранилище больших двоичных объектов Azure, задающий путь к файлу модуля.</span><span class="sxs-lookup"><span data-stu-id="d34de-120">Public URL such as a website or Azure blob storage specifying the path to the module file.</span></span>
<span data-ttu-id="d34de-121">Это расположение должно быть общедоступным.</span><span class="sxs-lookup"><span data-stu-id="d34de-121">This location must be publically accessible.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d34de-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d34de-122">-Name</span></span>
<span data-ttu-id="d34de-123">Задает имя модуля.</span><span class="sxs-lookup"><span data-stu-id="d34de-123">Specifies a name for the module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d34de-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="d34de-124">-Profile</span></span>
<span data-ttu-id="d34de-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d34de-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d34de-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d34de-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d34de-127">-Теги</span><span class="sxs-lookup"><span data-stu-id="d34de-127">-Tags</span></span>
<span data-ttu-id="d34de-128">Определяет один или несколько тегов, связанных с модулем.</span><span class="sxs-lookup"><span data-stu-id="d34de-128">Specifies one or more tags related to the module.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d34de-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d34de-129">CommonParameters</span></span>
<span data-ttu-id="d34de-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d34de-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d34de-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d34de-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d34de-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d34de-132">INPUTS</span></span>

## <span data-ttu-id="d34de-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d34de-133">OUTPUTS</span></span>

### <span data-ttu-id="d34de-134">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="d34de-134">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="d34de-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="d34de-135">NOTES</span></span>

## <span data-ttu-id="d34de-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d34de-136">RELATED LINKS</span></span>

[<span data-ttu-id="d34de-137">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d34de-137">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="d34de-138">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d34de-138">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="d34de-139">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d34de-139">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


