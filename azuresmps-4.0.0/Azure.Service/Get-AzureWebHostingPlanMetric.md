---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2DEF8B3A-4E91-4D39-AD39-1871F9FECE10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a59c93c9de0d2445f2839d9a66f4750751c987f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076510"
---
# <span data-ttu-id="0f6a7-101">Get-AzureWebHostingPlanMetric</span><span class="sxs-lookup"><span data-stu-id="0f6a7-101">Get-AzureWebHostingPlanMetric</span></span>

## <span data-ttu-id="0f6a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f6a7-102">SYNOPSIS</span></span>
<span data-ttu-id="0f6a7-103">Получает метрики для планов размещения на веб-сайтах Azure.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-103">Gets metrics for Azure website hosting plans.</span></span>

## <span data-ttu-id="0f6a7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f6a7-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlanMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f6a7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f6a7-105">DESCRIPTION</span></span>
<span data-ttu-id="0f6a7-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0f6a7-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0f6a7-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0f6a7-108">Командлет **Get-AzureWebHostingPlanMetric** получает метрики для планов размещения веб-сайтов Azure в подписке.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-108">The **Get-AzureWebHostingPlanMetric** cmdlet gets metrics for Azure web hosting plans in a subscription.</span></span>

## <span data-ttu-id="0f6a7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f6a7-109">EXAMPLES</span></span>

### <span data-ttu-id="0f6a7-110">Пример 1: Получение метрик за последние три часа на уровне каждого экземпляра</span><span class="sxs-lookup"><span data-stu-id="0f6a7-110">Example 1: Get metrics for the last three hours at a per-instance level</span></span>
```
PS C:\> Get-AzureWebHostingPlanMetric -WebSpaceName "eastuswebspace" -StartDate (get-date).AddHours(-3) -InstanceDetails $Metrics[1].Data 

Name : CpuPercentage 
Unit : Percent 
StartTime : 8/11/2014 7:00:00 AM 
EndTime : 8/11/2014 5:00:23 PM 
TimeGrain : PT1H 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 8:00:00 AM, Total:2, Min:9, Max:0, 
Time:8/11/2014 9:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 10:00:00 AM, Total:2, Min:8, Max:0...} $metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName
 ----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 8:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 9:00:00 AM 2 9 0 1 RD00155DC24579 
8/11/2014 10:00:00 AM 2 8 0 1 RD00155DC24599 
8/11/2014 11:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 12:00:00 PM 2 6 0 1 RD00155DC24599 
8/11/2014 1:00:00 PM 2 15 0 1 RD00155DC24599 
8/11/2014 2:00:00 PM 3 21 0 1 RD00155DC24599 
8/11/2014 3:00:00 PM 2 13 0 1 RD00155DC24599 
8/11/2014 4:00:00 PM 2 14 0 1 RD00155DC24599
```

<span data-ttu-id="0f6a7-111">Эта команда получает метрики плана размещения веб-сайтов за последние три часа на уровне каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-111">This command gets web hosting plan metrics for last three hours on per-instance level.</span></span>

## <span data-ttu-id="0f6a7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f6a7-112">PARAMETERS</span></span>

### <span data-ttu-id="0f6a7-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="0f6a7-113">-EndDate</span></span>
<span data-ttu-id="0f6a7-114">Задает время окончания в виде объекта **DateTime** , из которого возвращаются метрики.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-114">Specifies the end time, as a **DateTime** object, from which to return metrics.</span></span>
<span data-ttu-id="0f6a7-115">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="0f6a7-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="0f6a7-116">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="0f6a7-116">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6a7-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="0f6a7-117">-InstanceDetails</span></span>
<span data-ttu-id="0f6a7-118">Указывает на то, что этот командлет включает подробные сведения о уровне каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="0f6a7-119">Если план размещения веб-сайта работает на нескольких компьютерах, этот командлет возвращает метрики данных для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-119">If the website hosting plan runs on two or more machines, this cmdlet returns details metrics for each machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6a7-120">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="0f6a7-120">-MetricNames</span></span>
<span data-ttu-id="0f6a7-121">Форель массив метрик для получения.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-121">Species an array of metrics to get.</span></span>
<span data-ttu-id="0f6a7-122">Если значение для этого параметра не задано, этот командлет получает все метрики.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-122">If you do not specify a value for this parameter, this cmdlet gets all metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6a7-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f6a7-123">-Name</span></span>
<span data-ttu-id="0f6a7-124">Указывает имя плана в подписке.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-124">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="0f6a7-125">По умолчанию **Get-AzureWebHostingPlanMetric** получает все веб-сайты в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-125">By default, **Get-AzureWebHostingPlanMetric** gets all websites in the current subscription.</span></span>
<span data-ttu-id="0f6a7-126">Этот параметр не поддерживает подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-126">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="0f6a7-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="0f6a7-127">-Profile</span></span>
<span data-ttu-id="0f6a7-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0f6a7-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0f6a7-130">-StartDate</span><span class="sxs-lookup"><span data-stu-id="0f6a7-130">-StartDate</span></span>
<span data-ttu-id="0f6a7-131">Задает время начала в виде объекта **DateTime** , для которого требуется получить метрики.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-131">Specifies the start time, as a **DateTime** object, for which to get metrics.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6a7-132">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="0f6a7-132">-TimeGrain</span></span>
<span data-ttu-id="0f6a7-133">Задает единицу времени, для которой требуется получить метрики.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-133">Specifies the time unit for which to get metrics.</span></span>
<span data-ttu-id="0f6a7-134">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="0f6a7-134">Valid values are:</span></span> 

- <span data-ttu-id="0f6a7-135">PT1M (минута)</span><span class="sxs-lookup"><span data-stu-id="0f6a7-135">PT1M (Minute)</span></span> 
- <span data-ttu-id="0f6a7-136">PT1H (час)</span><span class="sxs-lookup"><span data-stu-id="0f6a7-136">PT1H (Hour)</span></span> 
- <span data-ttu-id="0f6a7-137">P1D (день)</span><span class="sxs-lookup"><span data-stu-id="0f6a7-137">P1D (Day)</span></span>

<span data-ttu-id="0f6a7-138">Значением по умолчанию является PT1H.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-138">The default value is PT1H.</span></span>

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

### <span data-ttu-id="0f6a7-139">-WebSpaceName</span><span class="sxs-lookup"><span data-stu-id="0f6a7-139">-WebSpaceName</span></span>
<span data-ttu-id="0f6a7-140">Указывает имя веб-пространства в подписке.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-140">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="0f6a7-141">По умолчанию **Get-AzureWebHostingPlanMetric** получает все планы в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-141">By default, **Get-AzureWebHostingPlanMetric** gets all plans in the current subscription.</span></span>
<span data-ttu-id="0f6a7-142">Этот параметр не поддерживает подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-142">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6a7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f6a7-143">CommonParameters</span></span>
<span data-ttu-id="0f6a7-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f6a7-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f6a7-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f6a7-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f6a7-146">INPUTS</span></span>

###  
<span data-ttu-id="0f6a7-147">Вы можете передать входные данные этому командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-147">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="0f6a7-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f6a7-148">OUTPUTS</span></span>

###  
<span data-ttu-id="0f6a7-149">Microsoft. WindowsAzure. Commands. Utilities. website. Services. Entities. MetricResponse</span><span class="sxs-lookup"><span data-stu-id="0f6a7-149">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>

<span data-ttu-id="0f6a7-150">По умолчанию **Get-AzureWebHostingPlanMetric** возвращает массив объектов **MetricResponse** .</span><span class="sxs-lookup"><span data-stu-id="0f6a7-150">By default, **Get-AzureWebHostingPlanMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="0f6a7-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f6a7-151">NOTES</span></span>

## <span data-ttu-id="0f6a7-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f6a7-152">RELATED LINKS</span></span>

[<span data-ttu-id="0f6a7-153">Get-AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="0f6a7-153">Get-AzureWebHostingPlan</span></span>](./Get-AzureWebHostingPlan.md)


