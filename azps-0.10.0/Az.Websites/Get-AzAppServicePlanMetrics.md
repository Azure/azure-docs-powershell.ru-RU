---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
ms.openlocfilehash: c08ae63999582fd220005dde84316a2f4421d7b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910629"
---
# <span data-ttu-id="4048d-101">Get-AzAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="4048d-101">Get-AzAppServicePlanMetrics</span></span>

## <span data-ttu-id="4048d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4048d-102">SYNOPSIS</span></span>
<span data-ttu-id="4048d-103">Получение метрик плана веб-службы Azure.</span><span class="sxs-lookup"><span data-stu-id="4048d-103">Gets Azure Web service plan metrics.</span></span>

## <span data-ttu-id="4048d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4048d-104">SYNTAX</span></span>

### <span data-ttu-id="4048d-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="4048d-105">S1</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4048d-106">S2</span><span class="sxs-lookup"><span data-stu-id="4048d-106">S2</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <AppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4048d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4048d-107">DESCRIPTION</span></span>
<span data-ttu-id="4048d-108">**Get-AzAppServicePlanMetrics** получает метрики плана служб приложений.</span><span class="sxs-lookup"><span data-stu-id="4048d-108">The **Get-AzAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="4048d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4048d-109">EXAMPLES</span></span>

### <span data-ttu-id="4048d-110">1:</span><span class="sxs-lookup"><span data-stu-id="4048d-110">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="4048d-111">Эта команда возвращает процент ЦП для плана служб приложений в минуту (PT1M — время опроса 1 минута) между StartTime и EndTime.</span><span class="sxs-lookup"><span data-stu-id="4048d-111">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="4048d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4048d-112">PARAMETERS</span></span>

### <span data-ttu-id="4048d-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4048d-113">-AppServicePlan</span></span>
<span data-ttu-id="4048d-114">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="4048d-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4048d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4048d-115">-DefaultProfile</span></span>
<span data-ttu-id="4048d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4048d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4048d-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4048d-117">-EndTime</span></span>
<span data-ttu-id="4048d-118">Время окончания в формате UTC</span><span class="sxs-lookup"><span data-stu-id="4048d-118">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4048d-119">-Гранулярность</span><span class="sxs-lookup"><span data-stu-id="4048d-119">-Granularity</span></span>
<span data-ttu-id="4048d-120">Детализации</span><span class="sxs-lookup"><span data-stu-id="4048d-120">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4048d-121">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="4048d-121">-InstanceDetails</span></span>
<span data-ttu-id="4048d-122">Сведения об экземпляре</span><span class="sxs-lookup"><span data-stu-id="4048d-122">Instance Details</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4048d-123">-Метрики</span><span class="sxs-lookup"><span data-stu-id="4048d-123">-Metrics</span></span>
<span data-ttu-id="4048d-124">Метрик</span><span class="sxs-lookup"><span data-stu-id="4048d-124">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4048d-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4048d-125">-Name</span></span>
<span data-ttu-id="4048d-126">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="4048d-126">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4048d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4048d-127">-ResourceGroupName</span></span>
<span data-ttu-id="4048d-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4048d-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4048d-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4048d-129">-StartTime</span></span>
<span data-ttu-id="4048d-130">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="4048d-130">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4048d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4048d-131">CommonParameters</span></span>
<span data-ttu-id="4048d-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4048d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4048d-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4048d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4048d-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4048d-134">INPUTS</span></span>

### <span data-ttu-id="4048d-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="4048d-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="4048d-136">Параметр "AppServicePlan" принимает значение типа "ServerFarmWithRichSku" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4048d-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="4048d-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4048d-137">OUTPUTS</span></span>

## <span data-ttu-id="4048d-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="4048d-138">NOTES</span></span>

## <span data-ttu-id="4048d-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4048d-139">RELATED LINKS</span></span>

