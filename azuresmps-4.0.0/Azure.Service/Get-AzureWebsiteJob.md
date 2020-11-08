---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6B406310-287F-4BD3-BA38-A9C97E8EDC45
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9f68ca1667e7b028c7646bf5a569e4e467c1b03
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076273"
---
# <span data-ttu-id="51916-101">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="51916-101">Get-AzureWebsiteJob</span></span>

## <span data-ttu-id="51916-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51916-102">SYNOPSIS</span></span>
<span data-ttu-id="51916-103">Возвращает веб-задания, связанные с веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="51916-103">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="51916-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51916-104">SYNTAX</span></span>

```
Get-AzureWebsiteJob [-JobName <String>] [-JobType <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="51916-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51916-105">DESCRIPTION</span></span>
<span data-ttu-id="51916-106">Возвращает веб-задания, связанные с веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="51916-106">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="51916-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51916-107">EXAMPLES</span></span>

### <span data-ttu-id="51916-108">Пример 1: получение конкретных сведений о веб-задании</span><span class="sxs-lookup"><span data-stu-id="51916-108">Example 1: Get specific web job info</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="51916-109">Возвращает веб-задание с именем MyWebJob из MyWebsite производственного слота.</span><span class="sxs-lookup"><span data-stu-id="51916-109">Gets a web job called MyWebJob from MyWebsite production slot.</span></span>

### <span data-ttu-id="51916-110">Пример 2: получение всех веб-заданий для веб-сайта</span><span class="sxs-lookup"><span data-stu-id="51916-110">Example 2: Get all web jobs for a website</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite
```

<span data-ttu-id="51916-111">Возвращает все веб-задания, связанные с производственным слотом MyWebsite.</span><span class="sxs-lookup"><span data-stu-id="51916-111">Gets all web jobs associated with MyWebsite production slot.</span></span>

### <span data-ttu-id="51916-112">Пример 3: получение всех запущенных веб-заданий</span><span class="sxs-lookup"><span data-stu-id="51916-112">Example 3: Get all triggered web jobs</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -Slot staging -Type Triggered
```

<span data-ttu-id="51916-113">Получает все инициированные веб-задания из промежуточного слота MyWebsite.</span><span class="sxs-lookup"><span data-stu-id="51916-113">Gets all triggered web jobs from staging slot of MyWebsite.</span></span>

## <span data-ttu-id="51916-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51916-114">PARAMETERS</span></span>

### <span data-ttu-id="51916-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="51916-115">-JobName</span></span>
<span data-ttu-id="51916-116">Имя веб-задания</span><span class="sxs-lookup"><span data-stu-id="51916-116">The web job name</span></span>

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

### <span data-ttu-id="51916-117">-JobType</span><span class="sxs-lookup"><span data-stu-id="51916-117">-JobType</span></span>
<span data-ttu-id="51916-118">Тип веб-задания.</span><span class="sxs-lookup"><span data-stu-id="51916-118">The web job type.</span></span>
<span data-ttu-id="51916-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="51916-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51916-120">Активации</span><span class="sxs-lookup"><span data-stu-id="51916-120">Triggered</span></span>
- <span data-ttu-id="51916-121">Продолжитель</span><span class="sxs-lookup"><span data-stu-id="51916-121">Continuous</span></span>

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

### <span data-ttu-id="51916-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="51916-122">-Name</span></span>
<span data-ttu-id="51916-123">Имя веб-сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="51916-123">The name of the Azure website.</span></span>

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

### <span data-ttu-id="51916-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="51916-124">-Profile</span></span>
<span data-ttu-id="51916-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="51916-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51916-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51916-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51916-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="51916-127">-Slot</span></span>
<span data-ttu-id="51916-128">Имя гнезда на веб-сайте Azure.</span><span class="sxs-lookup"><span data-stu-id="51916-128">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="51916-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51916-129">CommonParameters</span></span>
<span data-ttu-id="51916-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51916-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51916-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51916-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51916-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51916-132">INPUTS</span></span>

## <span data-ttu-id="51916-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51916-133">OUTPUTS</span></span>

## <span data-ttu-id="51916-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="51916-134">NOTES</span></span>

## <span data-ttu-id="51916-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51916-135">RELATED LINKS</span></span>

[<span data-ttu-id="51916-136">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="51916-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="51916-137">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="51916-137">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="51916-138">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="51916-138">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="51916-139">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="51916-139">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="51916-140">Остановить-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="51916-140">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


