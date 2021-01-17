---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: d84d5b172d1a22880b508f8b43f071d5d454cf38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403700"
---
# <span data-ttu-id="f6181-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6181-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="f6181-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6181-102">SYNOPSIS</span></span>
<span data-ttu-id="f6181-103">Добавление конфигурации автоматического управления устройствами из IoT в целевой центр IoT.</span><span class="sxs-lookup"><span data-stu-id="f6181-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="f6181-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f6181-104">SYNTAX</span></span>

### <span data-ttu-id="f6181-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f6181-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6181-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f6181-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6181-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f6181-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6181-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6181-108">DESCRIPTION</span></span>
<span data-ttu-id="f6181-109">Содержимое конфигурации является json и немного различается в зависимости от цели устройства или модуля.</span><span class="sxs-lookup"><span data-stu-id="f6181-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="f6181-110">Конфигурации устройств имеют форму {"deviceContent":{...}}</span><span class="sxs-lookup"><span data-stu-id="f6181-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="f6181-111">Конфигурации модулей имеют форму {"moduleContent":{...}}</span><span class="sxs-lookup"><span data-stu-id="f6181-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="f6181-112">Конфигурации можно определить с учетом предоставленных пользователем метрик для оценки по запросу.</span><span class="sxs-lookup"><span data-stu-id="f6181-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="f6181-113">Метриками пользователей являются json и в виде {"queries":{...}}</span><span class="sxs-lookup"><span data-stu-id="f6181-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="f6181-114">или {"метрики":{"запросы":{...}}}.</span><span class="sxs-lookup"><span data-stu-id="f6181-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="f6181-115">Примечание. Целевое условие для модулей должно начинаться с "from devices.modules where".</span><span class="sxs-lookup"><span data-stu-id="f6181-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="f6181-116">Дополнительные https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management сведения см. в этой области.</span><span class="sxs-lookup"><span data-stu-id="f6181-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="f6181-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f6181-117">EXAMPLES</span></span>

### <span data-ttu-id="f6181-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f6181-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="f6181-119">Создайте конфигурацию устройства с метаданными по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f6181-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="f6181-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f6181-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="f6181-121">Создайте конфигурацию устройства с приоритетом 3, который применяется на условии, если устройство помечено в здании 9 и среда является тестовой.</span><span class="sxs-lookup"><span data-stu-id="f6181-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="f6181-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f6181-122">Example 3</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="f6181-123">Создайте конфигурацию устройства с метриками пользователей.</span><span class="sxs-lookup"><span data-stu-id="f6181-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="f6181-124">Пример 4</span><span class="sxs-lookup"><span data-stu-id="f6181-124">Example 4</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="f6181-125">Создайте конфигурацию устройства с метами.</span><span class="sxs-lookup"><span data-stu-id="f6181-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="f6181-126">Пример 5</span><span class="sxs-lookup"><span data-stu-id="f6181-126">Example 5</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="f6181-127">Создайте конфигурацию устройства с содержимым.</span><span class="sxs-lookup"><span data-stu-id="f6181-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="f6181-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6181-128">PARAMETERS</span></span>

### <span data-ttu-id="f6181-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6181-129">-DefaultProfile</span></span>
<span data-ttu-id="f6181-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6181-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6181-131">-DeviceContent</span><span class="sxs-lookup"><span data-stu-id="f6181-131">-DeviceContent</span></span>
<span data-ttu-id="f6181-132">Конфигурация устройств IotHub.</span><span class="sxs-lookup"><span data-stu-id="f6181-132">Configuration for IotHub devices.</span></span>

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

### <span data-ttu-id="f6181-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6181-133">-InputObject</span></span>
<span data-ttu-id="f6181-134">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="f6181-134">IotHub object</span></span>

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

### <span data-ttu-id="f6181-135">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f6181-135">-IotHubName</span></span>
<span data-ttu-id="f6181-136">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="f6181-136">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f6181-137">-Label</span><span class="sxs-lookup"><span data-stu-id="f6181-137">-Label</span></span>
<span data-ttu-id="f6181-138">Карта меток, которые будут применены к конечной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f6181-138">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="f6181-139">-Метрическая</span><span class="sxs-lookup"><span data-stu-id="f6181-139">-Metric</span></span>
<span data-ttu-id="f6181-140">Набор запросов для определения метрик конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f6181-140">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="f6181-141">-Name</span><span class="sxs-lookup"><span data-stu-id="f6181-141">-Name</span></span>
<span data-ttu-id="f6181-142">Идентификатор конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f6181-142">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="f6181-143">-Priority</span><span class="sxs-lookup"><span data-stu-id="f6181-143">-Priority</span></span>
<span data-ttu-id="f6181-144">Вес конфигурации устройства в случае соревнований правил (самые высокие победы).</span><span class="sxs-lookup"><span data-stu-id="f6181-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="f6181-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6181-145">-ResourceGroupName</span></span>
<span data-ttu-id="f6181-146">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f6181-146">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f6181-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6181-147">-ResourceId</span></span>
<span data-ttu-id="f6181-148">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="f6181-148">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f6181-149">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="f6181-149">-TargetCondition</span></span>
<span data-ttu-id="f6181-150">Целевое условие, к которому применяется конфигурация устройства.</span><span class="sxs-lookup"><span data-stu-id="f6181-150">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="f6181-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6181-151">-Confirm</span></span>
<span data-ttu-id="f6181-152">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6181-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6181-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6181-153">-WhatIf</span></span>
<span data-ttu-id="f6181-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6181-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6181-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f6181-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6181-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6181-156">CommonParameters</span></span>
<span data-ttu-id="f6181-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6181-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6181-158">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6181-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6181-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6181-159">INPUTS</span></span>

### <span data-ttu-id="f6181-160">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f6181-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f6181-161">System.String</span><span class="sxs-lookup"><span data-stu-id="f6181-161">System.String</span></span>

## <span data-ttu-id="f6181-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f6181-162">OUTPUTS</span></span>

### <span data-ttu-id="f6181-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6181-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="f6181-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f6181-164">NOTES</span></span>

## <span data-ttu-id="f6181-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6181-165">RELATED LINKS</span></span>
