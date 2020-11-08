---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 375e225d4c09368fac82db240988132952a0ada7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236444"
---
# <span data-ttu-id="f292e-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="f292e-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="f292e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f292e-102">SYNOPSIS</span></span>
<span data-ttu-id="f292e-103">Добавьте развертывание по краю IoT в конечный центр Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f292e-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="f292e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f292e-104">SYNTAX</span></span>

### <span data-ttu-id="f292e-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f292e-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f292e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f292e-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f292e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f292e-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f292e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f292e-108">DESCRIPTION</span></span>
<span data-ttu-id="f292e-109">Развертывание пограничного сервера можно создать с помощью метрик, определенных пользователем, для оценки спроса.</span><span class="sxs-lookup"><span data-stu-id="f292e-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="f292e-110"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringДля получения дополнительных сведений ознакомьтесь с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="f292e-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="f292e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f292e-111">EXAMPLES</span></span>

### <span data-ttu-id="f292e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f292e-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="f292e-113">Создание развертывания Edge с метаданными по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f292e-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="f292e-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f292e-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="f292e-115">Создайте развертывание пограничного сервера с приоритетом 3, которое применяется к условию, если устройство помечено в здании 9, а среда — "тест".</span><span class="sxs-lookup"><span data-stu-id="f292e-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="f292e-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f292e-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="f292e-117">Создайте развертывание пограничного сервера с метриками пользователей.</span><span class="sxs-lookup"><span data-stu-id="f292e-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="f292e-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f292e-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="f292e-119">Создайте развертывание пограничного сервера с метками.</span><span class="sxs-lookup"><span data-stu-id="f292e-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="f292e-120">Пример 4</span><span class="sxs-lookup"><span data-stu-id="f292e-120">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content
```

<span data-ttu-id="f292e-121">Создание пограничного развертывания с содержимым.</span><span class="sxs-lookup"><span data-stu-id="f292e-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="f292e-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f292e-122">PARAMETERS</span></span>

### <span data-ttu-id="f292e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f292e-123">-DefaultProfile</span></span>
<span data-ttu-id="f292e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f292e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f292e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f292e-125">-InputObject</span></span>
<span data-ttu-id="f292e-126">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="f292e-126">IotHub object</span></span>

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

### <span data-ttu-id="f292e-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f292e-127">-IotHubName</span></span>
<span data-ttu-id="f292e-128">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="f292e-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f292e-129">-Label</span><span class="sxs-lookup"><span data-stu-id="f292e-129">-Label</span></span>
<span data-ttu-id="f292e-130">Сопоставление меток, применяемых к целевому развертыванию.</span><span class="sxs-lookup"><span data-stu-id="f292e-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="f292e-131">-Метрическая система мер</span><span class="sxs-lookup"><span data-stu-id="f292e-131">-Metric</span></span>
<span data-ttu-id="f292e-132">Коллекция запросов с определением метрик развертывания для EDGE в IoT.</span><span class="sxs-lookup"><span data-stu-id="f292e-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="f292e-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="f292e-133">-ModulesContent</span></span>
<span data-ttu-id="f292e-134">Развертывание модулей для устройств с границами Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="f292e-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="f292e-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f292e-135">-Name</span></span>
<span data-ttu-id="f292e-136">Идентификатор развертывания.</span><span class="sxs-lookup"><span data-stu-id="f292e-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="f292e-137">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="f292e-137">-Priority</span></span>
<span data-ttu-id="f292e-138">Вес развертывания в случае с правилами конкурирующих конкурентов (самый высокий уровень WINS).</span><span class="sxs-lookup"><span data-stu-id="f292e-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="f292e-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f292e-139">-ResourceGroupName</span></span>
<span data-ttu-id="f292e-140">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f292e-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f292e-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f292e-141">-ResourceId</span></span>
<span data-ttu-id="f292e-142">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="f292e-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f292e-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="f292e-143">-TargetCondition</span></span>
<span data-ttu-id="f292e-144">Целевое условие, к которому применяется развертывание Edge.</span><span class="sxs-lookup"><span data-stu-id="f292e-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="f292e-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f292e-145">-Confirm</span></span>
<span data-ttu-id="f292e-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f292e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f292e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f292e-147">-WhatIf</span></span>
<span data-ttu-id="f292e-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f292e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f292e-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f292e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f292e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f292e-150">CommonParameters</span></span>
<span data-ttu-id="f292e-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f292e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f292e-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f292e-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f292e-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f292e-153">INPUTS</span></span>

### <span data-ttu-id="f292e-154">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f292e-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f292e-155">System. String</span><span class="sxs-lookup"><span data-stu-id="f292e-155">System.String</span></span>

## <span data-ttu-id="f292e-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f292e-156">OUTPUTS</span></span>

### <span data-ttu-id="f292e-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="f292e-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="f292e-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="f292e-158">NOTES</span></span>

## <span data-ttu-id="f292e-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f292e-159">RELATED LINKS</span></span>
