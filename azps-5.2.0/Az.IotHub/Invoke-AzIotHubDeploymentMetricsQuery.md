---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 570caa5d788fae000834a7f3a79230849daf372f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396895"
---
# <span data-ttu-id="9e9f9-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="9e9f9-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="9e9f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e9f9-102">SYNOPSIS</span></span>
<span data-ttu-id="9e9f9-103">Вызов запроса метрики развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="9e9f9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9e9f9-104">SYNTAX</span></span>

### <span data-ttu-id="9e9f9-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e9f9-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e9f9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9e9f9-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e9f9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9e9f9-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e9f9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e9f9-108">DESCRIPTION</span></span>
<span data-ttu-id="9e9f9-109">Оценка целевой настраиваемой или системной метрик, определенной в развертывании IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="9e9f9-110">Существуют предопределяемые системные показатели, которые рассчитываются с помощью IOT-концентратора и не могут быть настроены.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="9e9f9-111">Targeted (Целевой) — это устройства IoT Edge, которые соответствуют условию целевого развертывания.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="9e9f9-112">"Применено" показывает целевые устройства IoT Edge, которые не являются целевыми при другом развертывании с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="9e9f9-113">"Отчет об успешном развертывании" — это устройства IoT Edge, которые сообщили об успешном развертывании модулей.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="9e9f9-114">"Сбой отчетов" — это устройства IoT Edge, которые сообщили о том, что один или несколько модулей не были развернуты успешно.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="9e9f9-115">Чтобы изучить ошибку, подключите ее удаленно к этим устройствам и изучите файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="9e9f9-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9e9f9-116">EXAMPLES</span></span>

### <span data-ttu-id="9e9f9-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9e9f9-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="9e9f9-118">Оцените настраиваемую метрику warningLimit.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="9e9f9-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9e9f9-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="9e9f9-120">Оценка успешности системы.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="9e9f9-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e9f9-121">PARAMETERS</span></span>

### <span data-ttu-id="9e9f9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e9f9-122">-DefaultProfile</span></span>
<span data-ttu-id="9e9f9-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e9f9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e9f9-124">-InputObject</span></span>
<span data-ttu-id="9e9f9-125">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="9e9f9-125">IotHub object</span></span>

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

### <span data-ttu-id="9e9f9-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9e9f9-126">-IotHubName</span></span>
<span data-ttu-id="9e9f9-127">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="9e9f9-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9e9f9-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="9e9f9-128">-MetricName</span></span>
<span data-ttu-id="9e9f9-129">Целевая метрика для оценки.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="9e9f9-130">-MetricType</span><span class="sxs-lookup"><span data-stu-id="9e9f9-130">-MetricType</span></span>
<span data-ttu-id="9e9f9-131">Показывает, какой метрическую коллекцию следует использовать для подытовки метрики.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-131">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="9e9f9-132">-Name</span><span class="sxs-lookup"><span data-stu-id="9e9f9-132">-Name</span></span>
<span data-ttu-id="9e9f9-133">Идентификатор развертывания.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="9e9f9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e9f9-134">-ResourceGroupName</span></span>
<span data-ttu-id="9e9f9-135">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9e9f9-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9e9f9-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e9f9-136">-ResourceId</span></span>
<span data-ttu-id="9e9f9-137">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="9e9f9-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9e9f9-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e9f9-138">-Confirm</span></span>
<span data-ttu-id="9e9f9-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e9f9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e9f9-140">-WhatIf</span></span>
<span data-ttu-id="9e9f9-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e9f9-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e9f9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e9f9-143">CommonParameters</span></span>
<span data-ttu-id="9e9f9-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e9f9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e9f9-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e9f9-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e9f9-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e9f9-146">INPUTS</span></span>

### <span data-ttu-id="9e9f9-147">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9e9f9-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9e9f9-148">System.String</span><span class="sxs-lookup"><span data-stu-id="9e9f9-148">System.String</span></span>

## <span data-ttu-id="9e9f9-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9e9f9-149">OUTPUTS</span></span>

### <span data-ttu-id="9e9f9-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="9e9f9-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="9e9f9-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9e9f9-151">NOTES</span></span>

## <span data-ttu-id="9e9f9-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e9f9-152">RELATED LINKS</span></span>
