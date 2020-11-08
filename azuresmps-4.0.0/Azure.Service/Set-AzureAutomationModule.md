---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 9CED6E53-B65C-4D55-8AC7-9E8A8B143544
online version: ''
schema: 2.0.0
ms.openlocfilehash: da8f0e3bdc9e1cf573e9189e49feda85ee8c1b90
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075830"
---
# <span data-ttu-id="faccd-101">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="faccd-101">Set-AzureAutomationModule</span></span>

## <span data-ttu-id="faccd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="faccd-102">SYNOPSIS</span></span>

<span data-ttu-id="faccd-103">Обновляет модуль в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="faccd-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="faccd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="faccd-104">SYNTAX</span></span>

```
Set-AzureAutomationModule -Name <String> [-Tags <IDictionary>] [-ContentLinkUri <Uri>]
 [-ContentLinkVersion <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="faccd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="faccd-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="faccd-106">Командлет **Set-AzureAutomationModule** импортирует новую версию модуля или изменяет конфигурацию модуля в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="faccd-106">The **Set-AzureAutomationModule** cmdlet imports a new version of a module or changes the configuration of the module in Azure Automation.</span></span>

## <span data-ttu-id="faccd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="faccd-107">EXAMPLES</span></span>

### <span data-ttu-id="faccd-108">Пример 1: обновление модуля</span><span class="sxs-lookup"><span data-stu-id="faccd-108">Example 1: Update a module</span></span>
```
PS C:\> Set-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1"
```

<span data-ttu-id="faccd-109">Эта команда импортирует обновленную версию существующего модуля с именем ContosoModule в учетную запись службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="faccd-109">This command imports an updated version of an existing module named ContosoModule into the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="faccd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="faccd-110">PARAMETERS</span></span>

### <span data-ttu-id="faccd-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="faccd-111">-AutomationAccountName</span></span>
<span data-ttu-id="faccd-112">Указывает имя учетной записи автоматизации для модуля.</span><span class="sxs-lookup"><span data-stu-id="faccd-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="faccd-113">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="faccd-113">-ContentLinkUri</span></span>
<span data-ttu-id="faccd-114">Задает путь к файлу модуля.</span><span class="sxs-lookup"><span data-stu-id="faccd-114">Specifies the path to the module file.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faccd-115">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="faccd-115">-ContentLinkVersion</span></span>
<span data-ttu-id="faccd-116">Указывает версию модуля.</span><span class="sxs-lookup"><span data-stu-id="faccd-116">Specifies the version of the module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faccd-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="faccd-117">-Name</span></span>
<span data-ttu-id="faccd-118">Указывает имя модуля.</span><span class="sxs-lookup"><span data-stu-id="faccd-118">Specifies the name of the module.</span></span>

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

### <span data-ttu-id="faccd-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="faccd-119">-Profile</span></span>
<span data-ttu-id="faccd-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="faccd-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="faccd-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="faccd-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="faccd-122">-Теги</span><span class="sxs-lookup"><span data-stu-id="faccd-122">-Tags</span></span>
<span data-ttu-id="faccd-123">Указывает теги для модуля.</span><span class="sxs-lookup"><span data-stu-id="faccd-123">Specifies tags for the module.</span></span>

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

### <span data-ttu-id="faccd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faccd-124">CommonParameters</span></span>
<span data-ttu-id="faccd-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="faccd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faccd-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faccd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faccd-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="faccd-127">INPUTS</span></span>

### <span data-ttu-id="faccd-128">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="faccd-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="faccd-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="faccd-129">OUTPUTS</span></span>

## <span data-ttu-id="faccd-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="faccd-130">NOTES</span></span>

## <span data-ttu-id="faccd-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="faccd-131">RELATED LINKS</span></span>

[<span data-ttu-id="faccd-132">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="faccd-132">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="faccd-133">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="faccd-133">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="faccd-134">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="faccd-134">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)


