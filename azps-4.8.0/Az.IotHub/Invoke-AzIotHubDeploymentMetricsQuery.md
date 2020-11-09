---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 570caa5d788fae000834a7f3a79230849daf372f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244919"
---
# <span data-ttu-id="7ed7a-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="7ed7a-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="7ed7a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7ed7a-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed7a-103">Вызов запроса метрики развертывания в Интернет – EDGE.</span><span class="sxs-lookup"><span data-stu-id="7ed7a-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="7ed7a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7ed7a-104">SYNTAX</span></span>

### <span data-ttu-id="7ed7a-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7ed7a-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ed7a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7ed7a-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ed7a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7ed7a-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ed7a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ed7a-108">DESCRIPTION</span></span>
<span data-ttu-id="7ed7a-109">Оцените целевую пользовательскую или системную метрику, определенную в развертывании в Интернет-приложении IoT.</span><span class="sxs-lookup"><span data-stu-id="7ed7a-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="7ed7a-110">Существуют предварительно определенные системные показатели, которые рассчитываются центром Интернета вещей и не могут быть настроены.</span><span class="sxs-lookup"><span data-stu-id="7ed7a-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="7ed7a-111">"Targeted" показывает устройства EDGE в IoT, соответствующие условию нацеливания развертывания.</span><span class="sxs-lookup"><span data-stu-id="7ed7a-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="7ed7a-112">"Применено" показывает целевые устройства в Интернет вещей, которые не предназначены для другого развертывания с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="7ed7a-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="7ed7a-113">"Успешная отчетность" — показывает, что модули были успешно развернуты.</span><span class="sxs-lookup"><span data-stu-id="7ed7a-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="7ed7a-114">"Ошибка при составлении отчета" — показывает, что один или несколько модулей не были успешно развернуты.</span><span class="sxs-lookup"><span data-stu-id="7ed7a-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="7ed7a-115">Для дальнейшего изучения ошибки подключитесь к ним удаленно и просмотрите файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="7ed7a-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="7ed7a-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7ed7a-116">EXAMPLES</span></span>

### <span data-ttu-id="7ed7a-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7ed7a-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="7ed7a-118">Оцените пользовательскую определенную метрику "warningLimit".</span><span class="sxs-lookup"><span data-stu-id="7ed7a-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="7ed7a-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7ed7a-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="7ed7a-120">Оценка метрики «сообщение об успехе» системы.</span><span class="sxs-lookup"><span data-stu-id="7ed7a-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="7ed7a-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7ed7a-121">PARAMETERS</span></span>

### <span data-ttu-id="7ed7a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed7a-122">-DefaultProfile</span></span>
<span data-ttu-id="7ed7a-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed7a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ed7a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ed7a-124">-InputObject</span></span>
<span data-ttu-id="7ed7a-125">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="7ed7a-125">IotHub object</span></span>

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

### <span data-ttu-id="7ed7a-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7ed7a-126">-IotHubName</span></span>
<span data-ttu-id="7ed7a-127">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="7ed7a-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7ed7a-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="7ed7a-128">-MetricName</span></span>
<span data-ttu-id="7ed7a-129">Целевая метрика для оценки.</span><span class="sxs-lookup"><span data-stu-id="7ed7a-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="7ed7a-130">-MetricType</span><span class="sxs-lookup"><span data-stu-id="7ed7a-130">-MetricType</span></span>
<span data-ttu-id="7ed7a-131">Указывает, какая коллекция метрик должна использоваться для подстановки метрики.</span><span class="sxs-lookup"><span data-stu-id="7ed7a-131">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="7ed7a-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7ed7a-132">-Name</span></span>
<span data-ttu-id="7ed7a-133">Идентификатор развертывания.</span><span class="sxs-lookup"><span data-stu-id="7ed7a-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="7ed7a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ed7a-134">-ResourceGroupName</span></span>
<span data-ttu-id="7ed7a-135">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7ed7a-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7ed7a-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ed7a-136">-ResourceId</span></span>
<span data-ttu-id="7ed7a-137">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="7ed7a-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7ed7a-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ed7a-138">-Confirm</span></span>
<span data-ttu-id="7ed7a-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7ed7a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ed7a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ed7a-140">-WhatIf</span></span>
<span data-ttu-id="7ed7a-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7ed7a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ed7a-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7ed7a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ed7a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed7a-143">CommonParameters</span></span>
<span data-ttu-id="7ed7a-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7ed7a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed7a-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ed7a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed7a-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7ed7a-146">INPUTS</span></span>

### <span data-ttu-id="7ed7a-147">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7ed7a-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7ed7a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7ed7a-148">System.String</span></span>

## <span data-ttu-id="7ed7a-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ed7a-149">OUTPUTS</span></span>

### <span data-ttu-id="7ed7a-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="7ed7a-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="7ed7a-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="7ed7a-151">NOTES</span></span>

## <span data-ttu-id="7ed7a-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ed7a-152">RELATED LINKS</span></span>