---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 717023DA-AA2D-4F1B-AE46-67ED75AA0D15
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6d8dae704946680dd72ff8227d2a88d55f8b77a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076271"
---
# <span data-ttu-id="53343-101">Get-AzureWebsiteMetric</span><span class="sxs-lookup"><span data-stu-id="53343-101">Get-AzureWebsiteMetric</span></span>

## <span data-ttu-id="53343-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="53343-102">SYNOPSIS</span></span>
<span data-ttu-id="53343-103">Получает метрики для веб-сайта Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="53343-103">Gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="53343-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="53343-104">SYNTAX</span></span>

```
Get-AzureWebsiteMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-SlotView] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="53343-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53343-105">DESCRIPTION</span></span>
<span data-ttu-id="53343-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="53343-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="53343-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="53343-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="53343-108">Командлет **Get-AzureWebsiteMetric** получает метрики для веб-сайта Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="53343-108">The **Get-AzureWebsiteMetric** cmdlet gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="53343-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="53343-109">EXAMPLES</span></span>

### <span data-ttu-id="53343-110">Пример 1: Получение метрик за последние три часа на уровне каждого экземпляра для веб-сайта</span><span class="sxs-lookup"><span data-stu-id="53343-110">Example 1: Get metrics for the last three hours on a per-instance level for a website</span></span>
```
PS C:\> Get-AzureWebsiteMetric -Name "ContosoWebSite" -StartDate (get-date).AddHours(-3) -MetricNames "Requests" -InstanceDetails -SlotView -TimeGrain "PT1M" 
PS C:\> $metrics[1].Data Name : Requests 

Unit : Count 

StartTime : 8/11/2014 7:05:00 AM 

EndTime : 8/11/2014 5:06:01 PM 

TimeGrain : PT1M 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:05:00 AM, Total:4, Min:, Max:, Time:8/11/2014 7:06:00 AM, Total:3, Min:, Max:, 
Time:8/11/2014 7:07:00 AM, Total:3, Min:, Max:, Time:8/11/2014 7:08:00 AM, Total:12, Min:, Max:...} 
$metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName 
----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:05:00 AM 4 1 RD00155DC24599 
8/11/2014 7:06:00 AM 3 1 RD00155DC24599 
8/11/2014 7:07:00 AM 3 1 RD00155DC24589 
8/11/2014 7:08:00 AM 12 1 RD00155DC24599
8/11/2014 7:09:00 AM 37 1 RD00155DC24599 
8/11/2014 7:10:00 AM 9 1 RD00155DC24599
```

<span data-ttu-id="53343-111">Эта команда получает метрики за последние три часа на уровне каждого экземпляра для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="53343-111">This command gets metrics for the last three hours on a per-instance level for a website.</span></span>

## <span data-ttu-id="53343-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="53343-112">PARAMETERS</span></span>

### <span data-ttu-id="53343-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="53343-113">-EndDate</span></span>
<span data-ttu-id="53343-114">Указывает время, в виде объекта **DateTime** , для которого нужно прекратить сбор метрик.</span><span class="sxs-lookup"><span data-stu-id="53343-114">Specifies the time, as a **DateTime** object, to stop getting metrics.</span></span>
<span data-ttu-id="53343-115">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="53343-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="53343-116">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="53343-116">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="53343-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="53343-117">-InstanceDetails</span></span>
<span data-ttu-id="53343-118">Указывает на то, что этот командлет включает подробные сведения о уровне каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="53343-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="53343-119">Если план размещения веб-сайтов выполняется на нескольких компьютерах, этот командлет возвращает метрики для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="53343-119">If the web hosting plan runs on two or more computers, this cmdlet returns metrics for each computer.</span></span>

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

### <span data-ttu-id="53343-120">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="53343-120">-MetricNames</span></span>
<span data-ttu-id="53343-121">Задает массив метрик для получения.</span><span class="sxs-lookup"><span data-stu-id="53343-121">Specifies an array of metrics to get.</span></span>
<span data-ttu-id="53343-122">Если этот параметр не указан, командлет получает все метрики.</span><span class="sxs-lookup"><span data-stu-id="53343-122">If you do not specify this parameter, the cmdlet gets all metrics.</span></span>

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

### <span data-ttu-id="53343-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="53343-123">-Name</span></span>
<span data-ttu-id="53343-124">Указывает имя веб-сайта в подписке.</span><span class="sxs-lookup"><span data-stu-id="53343-124">Specifies the name of a website in the subscription.</span></span>
<span data-ttu-id="53343-125">Этот параметр не поддерживает подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="53343-125">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="53343-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="53343-126">-Profile</span></span>
<span data-ttu-id="53343-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="53343-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="53343-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="53343-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="53343-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="53343-129">-Slot</span></span>
<span data-ttu-id="53343-130">Указывает среду развертывания облачной службы.</span><span class="sxs-lookup"><span data-stu-id="53343-130">Specifies the environment of a cloud service deployment.</span></span>
<span data-ttu-id="53343-131">Допустимые значения: "производство" и "промежуточный".</span><span class="sxs-lookup"><span data-stu-id="53343-131">Valid values are: Production and Staging.</span></span>

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

### <span data-ttu-id="53343-132">-SlotView</span><span class="sxs-lookup"><span data-stu-id="53343-132">-SlotView</span></span>
<span data-ttu-id="53343-133">Указывает на то, что этот командлет получает метрики для имен узлов, которые получают трафик в текущем слоте.</span><span class="sxs-lookup"><span data-stu-id="53343-133">Indicates that this cmdlet gets metrics for the host names that receive traffic at the current slot.</span></span>
<span data-ttu-id="53343-134">Если в течение интервала времени возникает замена, метрики объединяются.</span><span class="sxs-lookup"><span data-stu-id="53343-134">If a swap occurs during the time period, the metrics are merged.</span></span>

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

### <span data-ttu-id="53343-135">-StartDate</span><span class="sxs-lookup"><span data-stu-id="53343-135">-StartDate</span></span>
<span data-ttu-id="53343-136">Задает время в виде объекта **DateTime** , с которого начинается сбор метрик.</span><span class="sxs-lookup"><span data-stu-id="53343-136">Specifies the time, as a **DateTime** object, to start getting metrics.</span></span>

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

### <span data-ttu-id="53343-137">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="53343-137">-TimeGrain</span></span>
<span data-ttu-id="53343-138">Указывает единицу времени для метрик.</span><span class="sxs-lookup"><span data-stu-id="53343-138">Specifies the time unit for metrics.</span></span>
<span data-ttu-id="53343-139">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="53343-139">Valid values are:</span></span> 

- <span data-ttu-id="53343-140">PT1M (минута)</span><span class="sxs-lookup"><span data-stu-id="53343-140">PT1M (Minute)</span></span> 
- <span data-ttu-id="53343-141">PT1H (час)</span><span class="sxs-lookup"><span data-stu-id="53343-141">PT1H (Hour)</span></span> 
- <span data-ttu-id="53343-142">P1D (день)</span><span class="sxs-lookup"><span data-stu-id="53343-142">P1D (Day)</span></span>

<span data-ttu-id="53343-143">Значением по умолчанию является PT1H.</span><span class="sxs-lookup"><span data-stu-id="53343-143">The default value is PT1H.</span></span>

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

### <span data-ttu-id="53343-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53343-144">CommonParameters</span></span>
<span data-ttu-id="53343-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="53343-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53343-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53343-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53343-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="53343-147">INPUTS</span></span>

###  
<span data-ttu-id="53343-148">Вы можете передать входные данные этому командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="53343-148">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="53343-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="53343-149">OUTPUTS</span></span>

### <span data-ttu-id="53343-150">Microsoft. WindowsAzure. Commands. Utilities. website. Services. Entities. MetricResponse</span><span class="sxs-lookup"><span data-stu-id="53343-150">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>
<span data-ttu-id="53343-151">По умолчанию **Get-AzureWebsiteMetric** возвращает массив объектов **MetricResponse** .</span><span class="sxs-lookup"><span data-stu-id="53343-151">By default, **Get-AzureWebsiteMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="53343-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="53343-152">NOTES</span></span>

## <span data-ttu-id="53343-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53343-153">RELATED LINKS</span></span>

[<span data-ttu-id="53343-154">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="53343-154">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


