---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: 3e1038fc44acc1e3834ee10a1fd08bb49c35cd82
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979939"
---
# <span data-ttu-id="e9d12-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="e9d12-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="e9d12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9d12-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d12-103">Получает определения метрик.</span><span class="sxs-lookup"><span data-stu-id="e9d12-103">Gets metric definitions.</span></span>

## <span data-ttu-id="e9d12-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e9d12-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9d12-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9d12-105">DESCRIPTION</span></span>
<span data-ttu-id="e9d12-106">Для **этого с помощью cmdlet Get-AzMetricDefinition** будут метрические определения.</span><span class="sxs-lookup"><span data-stu-id="e9d12-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="e9d12-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e9d12-107">EXAMPLES</span></span>

### <span data-ttu-id="e9d12-108">Пример 1. Определение метрик для ресурса</span><span class="sxs-lookup"><span data-stu-id="e9d12-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
Name                   : CpuTime
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Seconds
Name                   : Requests
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="e9d12-109">Эта команда получает определения метрик для указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="e9d12-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="e9d12-110">Пример 2. Получите метрические определения с подробными выходными сведениями</span><span class="sxs-lookup"><span data-stu-id="e9d12-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : Requests
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="e9d12-111">Эта команда получает определения метрик для website2.</span><span class="sxs-lookup"><span data-stu-id="e9d12-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="e9d12-112">Результат будет подробным.</span><span class="sxs-lookup"><span data-stu-id="e9d12-112">The output is detailed.</span></span>

### <span data-ttu-id="e9d12-113">Пример 3. Определение метрик по имени</span><span class="sxs-lookup"><span data-stu-id="e9d12-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricName "BytesSent,CpuTime"
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : BytesSent
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Bytes
```

<span data-ttu-id="e9d12-114">Эта команда получает определения метрик BytesSent и CpuTime.</span><span class="sxs-lookup"><span data-stu-id="e9d12-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="e9d12-115">Результат будет подробным.</span><span class="sxs-lookup"><span data-stu-id="e9d12-115">The output is detailed.</span></span>

## <span data-ttu-id="e9d12-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9d12-116">PARAMETERS</span></span>

### <span data-ttu-id="e9d12-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9d12-117">-DefaultProfile</span></span>
<span data-ttu-id="e9d12-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e9d12-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d12-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="e9d12-119">-DetailedOutput</span></span>
<span data-ttu-id="e9d12-120">Указывает на то, что эта операция содержит подробные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="e9d12-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="e9d12-121">Если этот параметр не указан, выходные данные будут обобщены.</span><span class="sxs-lookup"><span data-stu-id="e9d12-121">If you do not specify this parameter, the output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d12-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="e9d12-122">-MetricName</span></span>
<span data-ttu-id="e9d12-123">Определяет массив имен метрик.</span><span class="sxs-lookup"><span data-stu-id="e9d12-123">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9d12-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="e9d12-124">-MetricNamespace</span></span>
<span data-ttu-id="e9d12-125">Указывает пространство имен метрик, для которого нужно запрашивать определения метрик.</span><span class="sxs-lookup"><span data-stu-id="e9d12-125">Specifies the metric namespace to query metric definitions for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9d12-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9d12-126">-ResourceId</span></span>
<span data-ttu-id="e9d12-127">Определяет ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="e9d12-127">Specifies the resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9d12-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d12-128">CommonParameters</span></span>
<span data-ttu-id="e9d12-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9d12-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d12-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9d12-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d12-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9d12-131">INPUTS</span></span>

### <span data-ttu-id="e9d12-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e9d12-132">System.String</span></span>

### <span data-ttu-id="e9d12-133">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e9d12-133">System.String[]</span></span>

## <span data-ttu-id="e9d12-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e9d12-134">OUTPUTS</span></span>

### <span data-ttu-id="e9d12-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="e9d12-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="e9d12-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e9d12-136">NOTES</span></span>

<span data-ttu-id="e9d12-137">Дополнительные сведения о поддерживаемых показателях можно найти в https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="e9d12-137">More information about the supported metrics may be found at: https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="e9d12-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9d12-138">RELATED LINKS</span></span>

<span data-ttu-id="e9d12-139">[Get-AzMetric](./Get-AzMetric.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="e9d12-139">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


