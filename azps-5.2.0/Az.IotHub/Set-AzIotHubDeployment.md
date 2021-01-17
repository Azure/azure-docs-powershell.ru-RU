---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 947eec246c5dac9543522ade583426246c731d3e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327588"
---
# <span data-ttu-id="c4861-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="c4861-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="c4861-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4861-102">SYNOPSIS</span></span>
<span data-ttu-id="c4861-103">Обновите отключенные поля в развертывании IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="c4861-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="c4861-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c4861-104">SYNTAX</span></span>

### <span data-ttu-id="c4861-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c4861-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4861-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c4861-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4861-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c4861-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4861-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4861-108">DESCRIPTION</span></span>
<span data-ttu-id="c4861-109">Обновление указанных свойств развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="c4861-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="c4861-110">Примечание. Содержимое конфигурации является неавтеринимым.</span><span class="sxs-lookup"><span data-stu-id="c4861-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="c4861-111">Можно обновлять такие свойства конфигурации, как "метки", "метрики", "приоритет" и "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="c4861-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="c4861-112">Дополнительные https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  сведения см. в этой информации.</span><span class="sxs-lookup"><span data-stu-id="c4861-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="c4861-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c4861-113">EXAMPLES</span></span>

### <span data-ttu-id="c4861-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c4861-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="c4861-115">Измените приоритет развертывания IoT Edge и обновите его целевое условие.</span><span class="sxs-lookup"><span data-stu-id="c4861-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

### <span data-ttu-id="c4861-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c4861-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels -Metric $metrics
```

<span data-ttu-id="c4861-117">Обновите метрики и метки развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="c4861-117">Update the metrics and labels of IoT Edge deployment.</span></span>

## <span data-ttu-id="c4861-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4861-118">PARAMETERS</span></span>

### <span data-ttu-id="c4861-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4861-119">-DefaultProfile</span></span>
<span data-ttu-id="c4861-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4861-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4861-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c4861-121">-Force</span></span>
<span data-ttu-id="c4861-122">Позволяет заменить объект развертывания, даже если он был обновлен с момента его последнего получения.</span><span class="sxs-lookup"><span data-stu-id="c4861-122">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="c4861-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4861-123">-InputObject</span></span>
<span data-ttu-id="c4861-124">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="c4861-124">IotHub object</span></span>

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

### <span data-ttu-id="c4861-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c4861-125">-IotHubName</span></span>
<span data-ttu-id="c4861-126">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="c4861-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c4861-127">-Label</span><span class="sxs-lookup"><span data-stu-id="c4861-127">-Label</span></span>
<span data-ttu-id="c4861-128">Карта меток, которые нужно применить к целевому развертыванию.</span><span class="sxs-lookup"><span data-stu-id="c4861-128">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="c4861-129">-Метрическая</span><span class="sxs-lookup"><span data-stu-id="c4861-129">-Metric</span></span>
<span data-ttu-id="c4861-130">Сбор запросов для определения метрик развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="c4861-130">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="c4861-131">-Name</span><span class="sxs-lookup"><span data-stu-id="c4861-131">-Name</span></span>
<span data-ttu-id="c4861-132">Идентификатор развертывания.</span><span class="sxs-lookup"><span data-stu-id="c4861-132">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="c4861-133">-Priority</span><span class="sxs-lookup"><span data-stu-id="c4861-133">-Priority</span></span>
<span data-ttu-id="c4861-134">Вес развертывания в случае соревнований по правилам (самые высокие победы).</span><span class="sxs-lookup"><span data-stu-id="c4861-134">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="c4861-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4861-135">-ResourceGroupName</span></span>
<span data-ttu-id="c4861-136">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c4861-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c4861-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4861-137">-ResourceId</span></span>
<span data-ttu-id="c4861-138">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="c4861-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c4861-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="c4861-139">-TargetCondition</span></span>
<span data-ttu-id="c4861-140">Целевое условие, к которому относится развертывание Edge.</span><span class="sxs-lookup"><span data-stu-id="c4861-140">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="c4861-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4861-141">-Confirm</span></span>
<span data-ttu-id="c4861-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c4861-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4861-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4861-143">-WhatIf</span></span>
<span data-ttu-id="c4861-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4861-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4861-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c4861-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4861-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4861-146">CommonParameters</span></span>
<span data-ttu-id="c4861-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4861-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4861-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4861-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4861-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4861-149">INPUTS</span></span>

### <span data-ttu-id="c4861-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c4861-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c4861-151">System.String</span><span class="sxs-lookup"><span data-stu-id="c4861-151">System.String</span></span>

## <span data-ttu-id="c4861-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c4861-152">OUTPUTS</span></span>

### <span data-ttu-id="c4861-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="c4861-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="c4861-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c4861-154">NOTES</span></span>

## <span data-ttu-id="c4861-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4861-155">RELATED LINKS</span></span>
