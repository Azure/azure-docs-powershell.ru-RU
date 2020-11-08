---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: 9ca873736ad86eaac17dd2795ad61716197ceaba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250039"
---
# <span data-ttu-id="b3852-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="b3852-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="b3852-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3852-102">SYNOPSIS</span></span>
<span data-ttu-id="b3852-103">Получение определений метрик.</span><span class="sxs-lookup"><span data-stu-id="b3852-103">Gets metric definitions.</span></span>

## <span data-ttu-id="b3852-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3852-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3852-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3852-105">DESCRIPTION</span></span>
<span data-ttu-id="b3852-106">Командлет **Get-AzMetricDefinition** получает определения метрик.</span><span class="sxs-lookup"><span data-stu-id="b3852-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="b3852-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3852-107">EXAMPLES</span></span>

### <span data-ttu-id="b3852-108">Пример 1: получение определений метрик для ресурса</span><span class="sxs-lookup"><span data-stu-id="b3852-108">Example 1: Get metric definitions for a resource</span></span>
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

<span data-ttu-id="b3852-109">Эта команда получает определения метрик для указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="b3852-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="b3852-110">Пример 2: получение определений метрик с подробным выводом</span><span class="sxs-lookup"><span data-stu-id="b3852-110">Example 2: Get metric definitions with detailed output</span></span>
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

<span data-ttu-id="b3852-111">Эта команда получает определения метрики для website2.</span><span class="sxs-lookup"><span data-stu-id="b3852-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="b3852-112">Вывод будет подробным.</span><span class="sxs-lookup"><span data-stu-id="b3852-112">The output is detailed.</span></span>

### <span data-ttu-id="b3852-113">Пример 3: получение определений метрик по названию</span><span class="sxs-lookup"><span data-stu-id="b3852-113">Example 3: Get metric definitions by name</span></span>
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

<span data-ttu-id="b3852-114">Эта команда получает определения метрик BytesSent и CpuTime.</span><span class="sxs-lookup"><span data-stu-id="b3852-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="b3852-115">Вывод будет подробным.</span><span class="sxs-lookup"><span data-stu-id="b3852-115">The output is detailed.</span></span>

## <span data-ttu-id="b3852-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3852-116">PARAMETERS</span></span>

### <span data-ttu-id="b3852-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3852-117">-DefaultProfile</span></span>
<span data-ttu-id="b3852-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b3852-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3852-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="b3852-119">-DetailedOutput</span></span>
<span data-ttu-id="b3852-120">Указывает на то, что эта операция включает подробный вывод.</span><span class="sxs-lookup"><span data-stu-id="b3852-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="b3852-121">Если этот параметр не указан, выводится сводка.</span><span class="sxs-lookup"><span data-stu-id="b3852-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="b3852-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="b3852-122">-MetricName</span></span>
<span data-ttu-id="b3852-123">Указывает массив имен метрик.</span><span class="sxs-lookup"><span data-stu-id="b3852-123">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="b3852-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="b3852-124">-MetricNamespace</span></span>
<span data-ttu-id="b3852-125">Задает пространство имен метрик для запроса определений метрик.</span><span class="sxs-lookup"><span data-stu-id="b3852-125">Specifies the metric namespace to query metric definitions for.</span></span>

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

### <span data-ttu-id="b3852-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3852-126">-ResourceId</span></span>
<span data-ttu-id="b3852-127">Указывает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b3852-127">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="b3852-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3852-128">CommonParameters</span></span>
<span data-ttu-id="b3852-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3852-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3852-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3852-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3852-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3852-131">INPUTS</span></span>

### <span data-ttu-id="b3852-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b3852-132">System.String</span></span>

### <span data-ttu-id="b3852-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="b3852-133">System.String[]</span></span>

## <span data-ttu-id="b3852-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3852-134">OUTPUTS</span></span>

### <span data-ttu-id="b3852-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="b3852-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="b3852-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3852-136">NOTES</span></span>

<span data-ttu-id="b3852-137">Дополнительные сведения о поддерживаемых метриках можно найти по адресу: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="b3852-137">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="b3852-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3852-138">RELATED LINKS</span></span>

<span data-ttu-id="b3852-139">[Get-AzMetric](./Get-AzMetric.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="b3852-139">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


