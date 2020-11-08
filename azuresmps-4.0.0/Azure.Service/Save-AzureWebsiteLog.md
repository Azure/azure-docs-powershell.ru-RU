---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4696BB05-F507-4FFB-8D96-6BAA2EBB0F0A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03acdfb16c7f1e7e8ee5e6b95902ef1ed056412a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075458"
---
# <span data-ttu-id="b19e5-101">Save-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="b19e5-101">Save-AzureWebsiteLog</span></span>

## <span data-ttu-id="b19e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b19e5-102">SYNOPSIS</span></span>
<span data-ttu-id="b19e5-103">Загружает и сохраняет журналы для указанного веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="b19e5-103">Downloads and saves the logs for a specified website.</span></span>

## <span data-ttu-id="b19e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b19e5-104">SYNTAX</span></span>

```
Save-AzureWebsiteLog [-Output <String>] [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b19e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b19e5-105">DESCRIPTION</span></span>
<span data-ttu-id="b19e5-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b19e5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b19e5-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b19e5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b19e5-108">Командлет **Save-AzureWebsiteLog** загружает журналы для указанного веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="b19e5-108">The **Save-AzureWebsiteLog** cmdlet downloads the logs for a specified website.</span></span>

## <span data-ttu-id="b19e5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b19e5-109">EXAMPLES</span></span>

### <span data-ttu-id="b19e5-110">Пример 1: Загрузка и сохранение журналов для веб-сайта</span><span class="sxs-lookup"><span data-stu-id="b19e5-110">Example 1: Download and save logs for a website</span></span>
```
PS C:\> Save-AzureWebsiteLogs -Name mySite -Output .\logs.zip
```

<span data-ttu-id="b19e5-111">В этом примере выполняется загрузка журналов среды выполнения и развертывания для личного сайта в файл logs.zip в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="b19e5-111">This example downloads the runtime and deployment logs for website mySite to the file logs.zip in the current directory.</span></span>

## <span data-ttu-id="b19e5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b19e5-112">PARAMETERS</span></span>

### <span data-ttu-id="b19e5-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b19e5-113">-Name</span></span>
<span data-ttu-id="b19e5-114">Указывает имя веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="b19e5-114">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="b19e5-115">-Output</span><span class="sxs-lookup"><span data-stu-id="b19e5-115">-Output</span></span>
<span data-ttu-id="b19e5-116">Указывает путь для хранения скачанного файла.</span><span class="sxs-lookup"><span data-stu-id="b19e5-116">Specifies the path to store the downloaded file.</span></span>

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

### <span data-ttu-id="b19e5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b19e5-117">-PassThru</span></span>
<span data-ttu-id="b19e5-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b19e5-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b19e5-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b19e5-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b19e5-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="b19e5-120">-Profile</span></span>
<span data-ttu-id="b19e5-121">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b19e5-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b19e5-122">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b19e5-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b19e5-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="b19e5-123">-Slot</span></span>
<span data-ttu-id="b19e5-124">Указывает имя гнезда.</span><span class="sxs-lookup"><span data-stu-id="b19e5-124">Specifies the slot name.</span></span>

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

### <span data-ttu-id="b19e5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b19e5-125">CommonParameters</span></span>
<span data-ttu-id="b19e5-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b19e5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b19e5-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b19e5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b19e5-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b19e5-128">INPUTS</span></span>

## <span data-ttu-id="b19e5-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b19e5-129">OUTPUTS</span></span>

## <span data-ttu-id="b19e5-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="b19e5-130">NOTES</span></span>

## <span data-ttu-id="b19e5-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b19e5-131">RELATED LINKS</span></span>

[<span data-ttu-id="b19e5-132">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="b19e5-132">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


