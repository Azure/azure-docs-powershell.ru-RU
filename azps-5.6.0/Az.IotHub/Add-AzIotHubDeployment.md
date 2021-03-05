---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 80494fd18216ce42883a962920ab78bbc2aa628b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997926"
---
# <span data-ttu-id="994da-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="994da-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="994da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="994da-102">SYNOPSIS</span></span>
<span data-ttu-id="994da-103">Добавьте развертывание IoT Edge в целевой центр IoT.</span><span class="sxs-lookup"><span data-stu-id="994da-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="994da-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="994da-104">SYNTAX</span></span>

### <span data-ttu-id="994da-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="994da-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="994da-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="994da-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="994da-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="994da-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="994da-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="994da-108">DESCRIPTION</span></span>
<span data-ttu-id="994da-109">Развертывания Edge можно создавать с помощью пользовательских метрик для оценки по запросу.</span><span class="sxs-lookup"><span data-stu-id="994da-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="994da-110">Дополнительные https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring сведения см. в этой области.</span><span class="sxs-lookup"><span data-stu-id="994da-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="994da-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="994da-111">EXAMPLES</span></span>

### <span data-ttu-id="994da-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="994da-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="994da-113">Создайте развертывание Edge с метаданными по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="994da-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="994da-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="994da-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="994da-115">Создайте развертывание Edge с приоритетом 3, который применяется на условии, если устройство помечено в здании 9 и среда протестирована.</span><span class="sxs-lookup"><span data-stu-id="994da-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="994da-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="994da-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="994da-117">Создайте развертывание Edge с метриками пользователей.</span><span class="sxs-lookup"><span data-stu-id="994da-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="994da-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="994da-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="994da-119">Создайте развертывание Edge с метами.</span><span class="sxs-lookup"><span data-stu-id="994da-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="994da-120">Пример 4</span><span class="sxs-lookup"><span data-stu-id="994da-120">Example 4</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content -TargetCondition "from devices.modules where tags.environment='test'"
```

<span data-ttu-id="994da-121">Создайте развертывание Edge с контентом.</span><span class="sxs-lookup"><span data-stu-id="994da-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="994da-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="994da-122">PARAMETERS</span></span>

### <span data-ttu-id="994da-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="994da-123">-DefaultProfile</span></span>
<span data-ttu-id="994da-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="994da-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="994da-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="994da-125">-InputObject</span></span>
<span data-ttu-id="994da-126">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="994da-126">IotHub object</span></span>

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

### <span data-ttu-id="994da-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="994da-127">-IotHubName</span></span>
<span data-ttu-id="994da-128">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="994da-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="994da-129">-Label</span><span class="sxs-lookup"><span data-stu-id="994da-129">-Label</span></span>
<span data-ttu-id="994da-130">Карта меток, которые нужно применить к целевому развертыванию.</span><span class="sxs-lookup"><span data-stu-id="994da-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="994da-131">-Метрическая</span><span class="sxs-lookup"><span data-stu-id="994da-131">-Metric</span></span>
<span data-ttu-id="994da-132">Набор запросов для определения метрик развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="994da-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="994da-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="994da-133">-ModulesContent</span></span>
<span data-ttu-id="994da-134">Содержимое развертывания модулей для устройств IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="994da-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="994da-135">-Name</span><span class="sxs-lookup"><span data-stu-id="994da-135">-Name</span></span>
<span data-ttu-id="994da-136">Идентификатор развертывания.</span><span class="sxs-lookup"><span data-stu-id="994da-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="994da-137">-Priority</span><span class="sxs-lookup"><span data-stu-id="994da-137">-Priority</span></span>
<span data-ttu-id="994da-138">Вес развертывания в случае соревнований по правилам (самые высокие победы).</span><span class="sxs-lookup"><span data-stu-id="994da-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="994da-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="994da-139">-ResourceGroupName</span></span>
<span data-ttu-id="994da-140">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="994da-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="994da-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="994da-141">-ResourceId</span></span>
<span data-ttu-id="994da-142">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="994da-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="994da-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="994da-143">-TargetCondition</span></span>
<span data-ttu-id="994da-144">Целевое условие, к которому относится развертывание Edge.</span><span class="sxs-lookup"><span data-stu-id="994da-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="994da-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="994da-145">-Confirm</span></span>
<span data-ttu-id="994da-146">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="994da-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="994da-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="994da-147">-WhatIf</span></span>
<span data-ttu-id="994da-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="994da-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="994da-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="994da-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="994da-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="994da-150">CommonParameters</span></span>
<span data-ttu-id="994da-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="994da-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="994da-152">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="994da-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="994da-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="994da-153">INPUTS</span></span>

### <span data-ttu-id="994da-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="994da-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="994da-155">System.String</span><span class="sxs-lookup"><span data-stu-id="994da-155">System.String</span></span>

## <span data-ttu-id="994da-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="994da-156">OUTPUTS</span></span>

### <span data-ttu-id="994da-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="994da-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="994da-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="994da-158">NOTES</span></span>

## <span data-ttu-id="994da-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="994da-159">RELATED LINKS</span></span>
