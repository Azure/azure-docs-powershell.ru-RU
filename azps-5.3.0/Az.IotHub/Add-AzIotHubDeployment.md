---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 0e3065cb2ee668f6b0ef5b20ac25ee51d922edc7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518497"
---
# <span data-ttu-id="d2346-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="d2346-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="d2346-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2346-102">SYNOPSIS</span></span>
<span data-ttu-id="d2346-103">Добавьте развертывание IoT Edge в целевой центр IoT.</span><span class="sxs-lookup"><span data-stu-id="d2346-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="d2346-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d2346-104">SYNTAX</span></span>

### <span data-ttu-id="d2346-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2346-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2346-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d2346-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2346-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d2346-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2346-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2346-108">DESCRIPTION</span></span>
<span data-ttu-id="d2346-109">Развертывания Edge можно создавать с помощью пользовательских метрик для оценки по запросу.</span><span class="sxs-lookup"><span data-stu-id="d2346-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="d2346-110">Дополнительные https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring сведения см. в этой области.</span><span class="sxs-lookup"><span data-stu-id="d2346-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="d2346-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d2346-111">EXAMPLES</span></span>

### <span data-ttu-id="d2346-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2346-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="d2346-113">Создайте развертывание Edge с метаданными по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d2346-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="d2346-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d2346-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="d2346-115">Создайте развертывание Edge с приоритетом 3, который применяется на условии, если устройство помечено в здании 9 и среда протестирована.</span><span class="sxs-lookup"><span data-stu-id="d2346-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="d2346-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d2346-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="d2346-117">Создайте развертывание Edge с метриками пользователей.</span><span class="sxs-lookup"><span data-stu-id="d2346-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="d2346-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d2346-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="d2346-119">Создайте развертывание Edge с метами.</span><span class="sxs-lookup"><span data-stu-id="d2346-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="d2346-120">Пример 4</span><span class="sxs-lookup"><span data-stu-id="d2346-120">Example 4</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content -TargetCondition "from devices.modules where tags.environment='test'"
```

<span data-ttu-id="d2346-121">Создайте развертывание Edge с контентом.</span><span class="sxs-lookup"><span data-stu-id="d2346-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="d2346-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2346-122">PARAMETERS</span></span>

### <span data-ttu-id="d2346-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2346-123">-DefaultProfile</span></span>
<span data-ttu-id="d2346-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2346-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2346-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2346-125">-InputObject</span></span>
<span data-ttu-id="d2346-126">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="d2346-126">IotHub object</span></span>

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

### <span data-ttu-id="d2346-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d2346-127">-IotHubName</span></span>
<span data-ttu-id="d2346-128">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="d2346-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d2346-129">-Label</span><span class="sxs-lookup"><span data-stu-id="d2346-129">-Label</span></span>
<span data-ttu-id="d2346-130">Карта меток, которые нужно применить к целевому развертыванию.</span><span class="sxs-lookup"><span data-stu-id="d2346-130">Map of labels to be applied to target deployment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2346-131">-Метрическая</span><span class="sxs-lookup"><span data-stu-id="d2346-131">-Metric</span></span>
<span data-ttu-id="d2346-132">Сбор запросов для определения метрик развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="d2346-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2346-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="d2346-133">-ModulesContent</span></span>
<span data-ttu-id="d2346-134">Содержимое развертывания модулей для устройств IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="d2346-134">Deployment content of modules for IoT Edge devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2346-135">-Name</span><span class="sxs-lookup"><span data-stu-id="d2346-135">-Name</span></span>
<span data-ttu-id="d2346-136">Идентификатор развертывания.</span><span class="sxs-lookup"><span data-stu-id="d2346-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="d2346-137">-Priority</span><span class="sxs-lookup"><span data-stu-id="d2346-137">-Priority</span></span>
<span data-ttu-id="d2346-138">Вес развертывания в случае соревнований по правилам (самые высокие победы).</span><span class="sxs-lookup"><span data-stu-id="d2346-138">Weight of deployment in case of competing rules (highest wins).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2346-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2346-139">-ResourceGroupName</span></span>
<span data-ttu-id="d2346-140">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d2346-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d2346-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2346-141">-ResourceId</span></span>
<span data-ttu-id="d2346-142">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="d2346-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d2346-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="d2346-143">-TargetCondition</span></span>
<span data-ttu-id="d2346-144">Целевое условие, к которому относится развертывание Edge.</span><span class="sxs-lookup"><span data-stu-id="d2346-144">Target condition in which an Edge deployment applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2346-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2346-145">-Confirm</span></span>
<span data-ttu-id="d2346-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2346-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2346-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2346-147">-WhatIf</span></span>
<span data-ttu-id="d2346-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2346-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2346-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d2346-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2346-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2346-150">CommonParameters</span></span>
<span data-ttu-id="d2346-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2346-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2346-152">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2346-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2346-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2346-153">INPUTS</span></span>

### <span data-ttu-id="d2346-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d2346-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d2346-155">System.String</span><span class="sxs-lookup"><span data-stu-id="d2346-155">System.String</span></span>

## <span data-ttu-id="d2346-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d2346-156">OUTPUTS</span></span>

### <span data-ttu-id="d2346-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="d2346-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="d2346-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d2346-158">NOTES</span></span>

## <span data-ttu-id="d2346-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2346-159">RELATED LINKS</span></span>
