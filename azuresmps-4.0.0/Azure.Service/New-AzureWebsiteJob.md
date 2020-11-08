---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1254A28B-F670-44B2-BB0E-BD41B9483E3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1910a0da546bdc4d5b167d82685608669b7565c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076183"
---
# <span data-ttu-id="5f6cb-101">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="5f6cb-101">New-AzureWebsiteJob</span></span>

## <span data-ttu-id="5f6cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5f6cb-102">SYNOPSIS</span></span>
<span data-ttu-id="5f6cb-103">Создание веб-задания для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="5f6cb-103">Creates a web job for a website.</span></span>

## <span data-ttu-id="5f6cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5f6cb-104">SYNTAX</span></span>

```
New-AzureWebsiteJob -JobName <String> -JobType <WebJobType> -JobFile <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5f6cb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f6cb-105">DESCRIPTION</span></span>
<span data-ttu-id="5f6cb-106">Командлет **New-AzureWebsiteJob** создает веб-задание для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="5f6cb-106">The **New-AzureWebsiteJob** cmdlet creates a web job for a website.</span></span>

## <span data-ttu-id="5f6cb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5f6cb-107">EXAMPLES</span></span>

### <span data-ttu-id="5f6cb-108">Пример 1: создание нового веб-задания для веб-сайта</span><span class="sxs-lookup"><span data-stu-id="5f6cb-108">Example 1: Create new web job for a website</span></span>
```
PS C:\> New-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous -JobFile job.bat
```

<span data-ttu-id="5f6cb-109">Создание непрерывного задания для вызова job.bat на веб-сайте MyWebsite.</span><span class="sxs-lookup"><span data-stu-id="5f6cb-109">Creates a continuous job to call job.bat on website MyWebsite.</span></span>

## <span data-ttu-id="5f6cb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5f6cb-110">PARAMETERS</span></span>

### <span data-ttu-id="5f6cb-111">-JobFile</span><span class="sxs-lookup"><span data-stu-id="5f6cb-111">-JobFile</span></span>
<span data-ttu-id="5f6cb-112">Файл веб-задания.</span><span class="sxs-lookup"><span data-stu-id="5f6cb-112">The web job file.</span></span>

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

### <span data-ttu-id="5f6cb-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="5f6cb-113">-JobName</span></span>
<span data-ttu-id="5f6cb-114">Имя веб-задания.</span><span class="sxs-lookup"><span data-stu-id="5f6cb-114">The web job name.</span></span>

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

### <span data-ttu-id="5f6cb-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="5f6cb-115">-JobType</span></span>
<span data-ttu-id="5f6cb-116">Тип веб-задания.</span><span class="sxs-lookup"><span data-stu-id="5f6cb-116">The web job type.</span></span>
<span data-ttu-id="5f6cb-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5f6cb-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f6cb-118">Активации</span><span class="sxs-lookup"><span data-stu-id="5f6cb-118">Triggered</span></span> 
- <span data-ttu-id="5f6cb-119">Продолжитель</span><span class="sxs-lookup"><span data-stu-id="5f6cb-119">Continuous</span></span>

```yaml
Type: WebJobType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6cb-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5f6cb-120">-Name</span></span>
<span data-ttu-id="5f6cb-121">Имя веб-сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="5f6cb-121">The name of the Azure website.</span></span>

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

### <span data-ttu-id="5f6cb-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="5f6cb-122">-Profile</span></span>
<span data-ttu-id="5f6cb-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5f6cb-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5f6cb-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5f6cb-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5f6cb-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="5f6cb-125">-Slot</span></span>
<span data-ttu-id="5f6cb-126">Имя гнезда на веб-сайте Azure.</span><span class="sxs-lookup"><span data-stu-id="5f6cb-126">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="5f6cb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f6cb-127">CommonParameters</span></span>
<span data-ttu-id="5f6cb-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5f6cb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f6cb-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f6cb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f6cb-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5f6cb-130">INPUTS</span></span>

## <span data-ttu-id="5f6cb-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f6cb-131">OUTPUTS</span></span>

## <span data-ttu-id="5f6cb-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="5f6cb-132">NOTES</span></span>

## <span data-ttu-id="5f6cb-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f6cb-133">RELATED LINKS</span></span>

[<span data-ttu-id="5f6cb-134">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5f6cb-134">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="5f6cb-135">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="5f6cb-135">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="5f6cb-136">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="5f6cb-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="5f6cb-137">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="5f6cb-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="5f6cb-138">Остановить-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="5f6cb-138">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


