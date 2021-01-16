---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 40fa5d382972c53de94187c9731748be5b1bfe2a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425964"
---
# <span data-ttu-id="27491-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="27491-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="27491-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27491-102">SYNOPSIS</span></span>
<span data-ttu-id="27491-103">Обновив неавтные поля регистрации конфигурации.</span><span class="sxs-lookup"><span data-stu-id="27491-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="27491-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="27491-104">SYNTAX</span></span>

### <span data-ttu-id="27491-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27491-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27491-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="27491-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27491-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="27491-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27491-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27491-108">DESCRIPTION</span></span>
<span data-ttu-id="27491-109">Обновить указанные свойства автоматической настройки управления устройствами в режиме IoT.</span><span class="sxs-lookup"><span data-stu-id="27491-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="27491-110">Примечание. Содержимое конфигурации является неавтеринимым.</span><span class="sxs-lookup"><span data-stu-id="27491-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="27491-111">Можно обновлять такие свойства конфигурации, как "метки", "метрики", "приоритет" и "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="27491-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="27491-112">Дополнительные https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management сведения см. в этой области.</span><span class="sxs-lookup"><span data-stu-id="27491-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="27491-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="27491-113">EXAMPLES</span></span>

### <span data-ttu-id="27491-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="27491-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="27491-115">Изменение приоритета конфигурации устройства и обновление конечного условия</span><span class="sxs-lookup"><span data-stu-id="27491-115">Alter the priority of a device configuration and update its target condition</span></span>

### <span data-ttu-id="27491-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="27491-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels -Metric $metrics
```

<span data-ttu-id="27491-117">Обновление метрик и меток конфигурации устройства</span><span class="sxs-lookup"><span data-stu-id="27491-117">Update the metrics and labels of a device configuration</span></span>

## <span data-ttu-id="27491-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27491-118">PARAMETERS</span></span>

### <span data-ttu-id="27491-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27491-119">-DefaultProfile</span></span>
<span data-ttu-id="27491-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27491-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27491-121">-Force</span><span class="sxs-lookup"><span data-stu-id="27491-121">-Force</span></span>
<span data-ttu-id="27491-122">Позволяет заменить объект конфигурации, даже если он был обновлен с момента его последнего получения.</span><span class="sxs-lookup"><span data-stu-id="27491-122">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="27491-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27491-123">-InputObject</span></span>
<span data-ttu-id="27491-124">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="27491-124">IotHub object</span></span>

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

### <span data-ttu-id="27491-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="27491-125">-IotHubName</span></span>
<span data-ttu-id="27491-126">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="27491-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="27491-127">-Label</span><span class="sxs-lookup"><span data-stu-id="27491-127">-Label</span></span>
<span data-ttu-id="27491-128">Карта меток, которые будут применены к конечной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="27491-128">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="27491-129">-Метрическая</span><span class="sxs-lookup"><span data-stu-id="27491-129">-Metric</span></span>
<span data-ttu-id="27491-130">Набор запросов для определения метрик конфигурации.</span><span class="sxs-lookup"><span data-stu-id="27491-130">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="27491-131">-Name</span><span class="sxs-lookup"><span data-stu-id="27491-131">-Name</span></span>
<span data-ttu-id="27491-132">Идентификатор конфигурации.</span><span class="sxs-lookup"><span data-stu-id="27491-132">Identifier for the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27491-133">-Priority</span><span class="sxs-lookup"><span data-stu-id="27491-133">-Priority</span></span>
<span data-ttu-id="27491-134">Вес конфигурации устройства в случае соревнований по правилам (самые высокие победы).</span><span class="sxs-lookup"><span data-stu-id="27491-134">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="27491-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27491-135">-ResourceGroupName</span></span>
<span data-ttu-id="27491-136">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="27491-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="27491-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27491-137">-ResourceId</span></span>
<span data-ttu-id="27491-138">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="27491-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="27491-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="27491-139">-TargetCondition</span></span>
<span data-ttu-id="27491-140">Целевое условие, к которому применяется конфигурация устройства.</span><span class="sxs-lookup"><span data-stu-id="27491-140">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="27491-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27491-141">-Confirm</span></span>
<span data-ttu-id="27491-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="27491-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27491-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27491-143">-WhatIf</span></span>
<span data-ttu-id="27491-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27491-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27491-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="27491-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27491-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27491-146">CommonParameters</span></span>
<span data-ttu-id="27491-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27491-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27491-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27491-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27491-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27491-149">INPUTS</span></span>

### <span data-ttu-id="27491-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="27491-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="27491-151">System.String</span><span class="sxs-lookup"><span data-stu-id="27491-151">System.String</span></span>

## <span data-ttu-id="27491-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="27491-152">OUTPUTS</span></span>

### <span data-ttu-id="27491-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="27491-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="27491-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="27491-154">NOTES</span></span>

## <span data-ttu-id="27491-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27491-155">RELATED LINKS</span></span>
