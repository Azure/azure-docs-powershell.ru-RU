---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
ms.openlocfilehash: 8dea2e61d6d64fbb59363d157dc0b8c1096ba259
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732722"
---
# <span data-ttu-id="89ee1-101">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="89ee1-101">Get-AzureRmMetricDefinition</span></span>

## <span data-ttu-id="89ee1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="89ee1-103">Получение определений метрик.</span><span class="sxs-lookup"><span data-stu-id="89ee1-103">Gets metric definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89ee1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89ee1-104">SYNTAX</span></span>

```
Get-AzureRmMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89ee1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89ee1-105">DESCRIPTION</span></span>
<span data-ttu-id="89ee1-106">Командлет **Get-AzureRmMetricDefinition** получает определения метрик.</span><span class="sxs-lookup"><span data-stu-id="89ee1-106">The **Get-AzureRmMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="89ee1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89ee1-107">EXAMPLES</span></span>

### <span data-ttu-id="89ee1-108">Пример 1: получение определений метрик для ресурса</span><span class="sxs-lookup"><span data-stu-id="89ee1-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
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

<span data-ttu-id="89ee1-109">Эта команда получает определения метрик для указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="89ee1-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="89ee1-110">Пример 2: получение определений метрик с подробным выводом</span><span class="sxs-lookup"><span data-stu-id="89ee1-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
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

<span data-ttu-id="89ee1-111">Эта команда получает определения метрики для website2.</span><span class="sxs-lookup"><span data-stu-id="89ee1-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="89ee1-112">Вывод будет подробным.</span><span class="sxs-lookup"><span data-stu-id="89ee1-112">The output is detailed.</span></span>

### <span data-ttu-id="89ee1-113">Пример 3: получение определений метрик по названию</span><span class="sxs-lookup"><span data-stu-id="89ee1-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricNames "BytesSent,CpuTime"
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

<span data-ttu-id="89ee1-114">Эта команда получает определения метрик BytesSent и CpuTime.</span><span class="sxs-lookup"><span data-stu-id="89ee1-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="89ee1-115">Вывод будет подробным.</span><span class="sxs-lookup"><span data-stu-id="89ee1-115">The output is detailed.</span></span>

## <span data-ttu-id="89ee1-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89ee1-116">PARAMETERS</span></span>

### <span data-ttu-id="89ee1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ee1-117">-DefaultProfile</span></span>
<span data-ttu-id="89ee1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="89ee1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ee1-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="89ee1-119">-DetailedOutput</span></span>
<span data-ttu-id="89ee1-120">Указывает на то, что эта операция включает подробный вывод.</span><span class="sxs-lookup"><span data-stu-id="89ee1-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="89ee1-121">Если этот параметр не указан, выводится сводка.</span><span class="sxs-lookup"><span data-stu-id="89ee1-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="89ee1-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="89ee1-122">-MetricName</span></span>
<span data-ttu-id="89ee1-123">Указывает массив имен метрик.</span><span class="sxs-lookup"><span data-stu-id="89ee1-123">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="89ee1-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="89ee1-124">-MetricNamespace</span></span>
<span data-ttu-id="89ee1-125">Задает пространство имен метрик для запроса определений метрик.</span><span class="sxs-lookup"><span data-stu-id="89ee1-125">Specifies the metric namespace to query metric definitions for.</span></span>

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

### <span data-ttu-id="89ee1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89ee1-126">-ResourceId</span></span>
<span data-ttu-id="89ee1-127">Указывает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="89ee1-127">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="89ee1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ee1-128">CommonParameters</span></span>
<span data-ttu-id="89ee1-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89ee1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ee1-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89ee1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ee1-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89ee1-131">INPUTS</span></span>

### <span data-ttu-id="89ee1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="89ee1-132">System.String</span></span>

### <span data-ttu-id="89ee1-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="89ee1-133">System.String[]</span></span>

## <span data-ttu-id="89ee1-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89ee1-134">OUTPUTS</span></span>

### <span data-ttu-id="89ee1-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="89ee1-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="89ee1-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="89ee1-136">NOTES</span></span>

## <span data-ttu-id="89ee1-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89ee1-137">RELATED LINKS</span></span>

<span data-ttu-id="89ee1-138">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [New-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="89ee1-138">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[New-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span></span>


