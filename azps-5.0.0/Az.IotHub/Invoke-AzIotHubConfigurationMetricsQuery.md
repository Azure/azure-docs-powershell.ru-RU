---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 85793ba3097297de646db4695cac36173bb01673
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94257994"
---
# <span data-ttu-id="03938-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="03938-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="03938-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03938-102">SYNOPSIS</span></span>
<span data-ttu-id="03938-103">Вызов запроса метрики конфигурации устройства IoT.</span><span class="sxs-lookup"><span data-stu-id="03938-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="03938-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03938-104">SYNTAX</span></span>

### <span data-ttu-id="03938-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="03938-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03938-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="03938-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03938-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="03938-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03938-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03938-108">DESCRIPTION</span></span>
<span data-ttu-id="03938-109">Оцените целевую пользовательскую или системную метрику, определенную в конфигурации устройства IoT.</span><span class="sxs-lookup"><span data-stu-id="03938-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="03938-110">Существуют предварительно определенные системные показатели, которые рассчитываются центром Интернета вещей и не могут быть настроены.</span><span class="sxs-lookup"><span data-stu-id="03938-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="03938-111">"Targeted" указывает число Twins устройств, соответствующих целевому условию.</span><span class="sxs-lookup"><span data-stu-id="03938-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="03938-112">"Применено" указывает число Twins устройств, измененных конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="03938-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="03938-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03938-113">EXAMPLES</span></span>

### <span data-ttu-id="03938-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="03938-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="03938-115">Оцените пользовательскую определенную метрику "warningLimit".</span><span class="sxs-lookup"><span data-stu-id="03938-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="03938-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="03938-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="03938-117">Оценка метрики "применяется система".</span><span class="sxs-lookup"><span data-stu-id="03938-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="03938-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03938-118">PARAMETERS</span></span>

### <span data-ttu-id="03938-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03938-119">-DefaultProfile</span></span>
<span data-ttu-id="03938-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="03938-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03938-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03938-121">-InputObject</span></span>
<span data-ttu-id="03938-122">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="03938-122">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03938-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="03938-123">-IotHubName</span></span>
<span data-ttu-id="03938-124">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="03938-124">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03938-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="03938-125">-MetricName</span></span>
<span data-ttu-id="03938-126">Целевая метрика для оценки.</span><span class="sxs-lookup"><span data-stu-id="03938-126">Target metric for evaluation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03938-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="03938-127">-MetricType</span></span>
<span data-ttu-id="03938-128">Указывает, какая коллекция метрик должна использоваться для подстановки метрики.</span><span class="sxs-lookup"><span data-stu-id="03938-128">Indicates which metric collection should be used to lookup a metric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricType
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03938-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="03938-129">-Name</span></span>
<span data-ttu-id="03938-130">Идентификатор конфигурации.</span><span class="sxs-lookup"><span data-stu-id="03938-130">Identifier for the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03938-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03938-131">-ResourceGroupName</span></span>
<span data-ttu-id="03938-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="03938-132">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03938-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03938-133">-ResourceId</span></span>
<span data-ttu-id="03938-134">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="03938-134">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03938-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03938-135">-Confirm</span></span>
<span data-ttu-id="03938-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="03938-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03938-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03938-137">-WhatIf</span></span>
<span data-ttu-id="03938-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="03938-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03938-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="03938-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03938-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03938-140">CommonParameters</span></span>
<span data-ttu-id="03938-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="03938-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03938-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03938-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03938-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03938-143">INPUTS</span></span>

### <span data-ttu-id="03938-144">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="03938-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="03938-145">System. String</span><span class="sxs-lookup"><span data-stu-id="03938-145">System.String</span></span>

## <span data-ttu-id="03938-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03938-146">OUTPUTS</span></span>

### <span data-ttu-id="03938-147">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="03938-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="03938-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="03938-148">NOTES</span></span>

## <span data-ttu-id="03938-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03938-149">RELATED LINKS</span></span>