---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 07772e7d0cbec3a2cd8241de3afa0100e1c253cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962995"
---
# <span data-ttu-id="035e2-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="035e2-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="035e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="035e2-102">SYNOPSIS</span></span>
<span data-ttu-id="035e2-103">Вызов запроса метрики конфигурации устройства IoT.</span><span class="sxs-lookup"><span data-stu-id="035e2-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="035e2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="035e2-104">SYNTAX</span></span>

### <span data-ttu-id="035e2-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="035e2-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="035e2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="035e2-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="035e2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="035e2-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="035e2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="035e2-108">DESCRIPTION</span></span>
<span data-ttu-id="035e2-109">Оценка целевой настраиваемой или системной метрик, определенной в конфигурации устройства под управлением IoT.</span><span class="sxs-lookup"><span data-stu-id="035e2-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="035e2-110">Существуют предопределяемые системные показатели, которые рассчитываются с помощью IOT-концентратора и не могут быть настроены.</span><span class="sxs-lookup"><span data-stu-id="035e2-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="035e2-111">"Targeted" — количество совпадений устройства, которые соответствуют целевому условию.</span><span class="sxs-lookup"><span data-stu-id="035e2-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="035e2-112">"Применено" — количество устройств, которые были изменены конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="035e2-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="035e2-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="035e2-113">EXAMPLES</span></span>

### <span data-ttu-id="035e2-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="035e2-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="035e2-115">Оцените настраиваемую метрику warningLimit.</span><span class="sxs-lookup"><span data-stu-id="035e2-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="035e2-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="035e2-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="035e2-117">Оцените "примененную" метрическую систему.</span><span class="sxs-lookup"><span data-stu-id="035e2-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="035e2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="035e2-118">PARAMETERS</span></span>

### <span data-ttu-id="035e2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="035e2-119">-DefaultProfile</span></span>
<span data-ttu-id="035e2-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="035e2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="035e2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="035e2-121">-InputObject</span></span>
<span data-ttu-id="035e2-122">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="035e2-122">IotHub object</span></span>

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

### <span data-ttu-id="035e2-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="035e2-123">-IotHubName</span></span>
<span data-ttu-id="035e2-124">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="035e2-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="035e2-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="035e2-125">-MetricName</span></span>
<span data-ttu-id="035e2-126">Целевая метрика для оценки.</span><span class="sxs-lookup"><span data-stu-id="035e2-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="035e2-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="035e2-127">-MetricType</span></span>
<span data-ttu-id="035e2-128">Показывает, какой метрическую коллекцию следует использовать для подытовки метрики.</span><span class="sxs-lookup"><span data-stu-id="035e2-128">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="035e2-129">-Name</span><span class="sxs-lookup"><span data-stu-id="035e2-129">-Name</span></span>
<span data-ttu-id="035e2-130">Идентификатор конфигурации.</span><span class="sxs-lookup"><span data-stu-id="035e2-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="035e2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="035e2-131">-ResourceGroupName</span></span>
<span data-ttu-id="035e2-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="035e2-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="035e2-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="035e2-133">-ResourceId</span></span>
<span data-ttu-id="035e2-134">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="035e2-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="035e2-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="035e2-135">-Confirm</span></span>
<span data-ttu-id="035e2-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="035e2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="035e2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="035e2-137">-WhatIf</span></span>
<span data-ttu-id="035e2-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="035e2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="035e2-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="035e2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="035e2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="035e2-140">CommonParameters</span></span>
<span data-ttu-id="035e2-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="035e2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="035e2-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="035e2-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="035e2-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="035e2-143">INPUTS</span></span>

### <span data-ttu-id="035e2-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="035e2-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="035e2-145">System.String</span><span class="sxs-lookup"><span data-stu-id="035e2-145">System.String</span></span>

## <span data-ttu-id="035e2-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="035e2-146">OUTPUTS</span></span>

### <span data-ttu-id="035e2-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="035e2-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="035e2-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="035e2-148">NOTES</span></span>

## <span data-ttu-id="035e2-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="035e2-149">RELATED LINKS</span></span>
