---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: 6b4068056607de76380e5ec8457f7a8242a1a0b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074247"
---
# <span data-ttu-id="1d456-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d456-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="1d456-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1d456-102">SYNOPSIS</span></span>
<span data-ttu-id="1d456-103">Добавьте конфигурацию автоматического управления устройствами IoT в конечный центр Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="1d456-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="1d456-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1d456-104">SYNTAX</span></span>

### <span data-ttu-id="1d456-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1d456-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d456-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1d456-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d456-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1d456-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d456-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d456-108">DESCRIPTION</span></span>
<span data-ttu-id="1d456-109">Содержимое конфигурации — это JSON и небольшие значения зависят от намерения устройства или модуля.</span><span class="sxs-lookup"><span data-stu-id="1d456-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="1d456-110">Конфигурации устройства имеют вид {"deviceContent": {...}}</span><span class="sxs-lookup"><span data-stu-id="1d456-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="1d456-111">Конфигурации модулей находятся в форме {"moduleContent": {...}}</span><span class="sxs-lookup"><span data-stu-id="1d456-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="1d456-112">Конфигурации можно определить с помощью метрик, предоставленных пользователем, для оценки спроса.</span><span class="sxs-lookup"><span data-stu-id="1d456-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="1d456-113">Метрики пользователей — JSON и в форме {"запросы": {...}}</span><span class="sxs-lookup"><span data-stu-id="1d456-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="1d456-114">или {"метрики": {"запросы": {...}}}.</span><span class="sxs-lookup"><span data-stu-id="1d456-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="1d456-115">Примечание. конечные условия для модулей должны начинаться с "с устройств. Modules".</span><span class="sxs-lookup"><span data-stu-id="1d456-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="1d456-116"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementДля получения дополнительных сведений ознакомьтесь с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="1d456-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="1d456-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1d456-117">EXAMPLES</span></span>

### <span data-ttu-id="1d456-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1d456-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="1d456-119">Создание конфигурации устройства с метаданными по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1d456-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="1d456-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1d456-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="1d456-121">Создание конфигурации устройства с приоритетом 3, который применяется к условию, когда устройство помечено в здании 9, а среда — "тест".</span><span class="sxs-lookup"><span data-stu-id="1d456-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="1d456-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1d456-122">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="1d456-123">Создание конфигурации устройства с метриками пользователей.</span><span class="sxs-lookup"><span data-stu-id="1d456-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="1d456-124">Пример 3</span><span class="sxs-lookup"><span data-stu-id="1d456-124">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="1d456-125">Создание конфигурации устройства с метками.</span><span class="sxs-lookup"><span data-stu-id="1d456-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="1d456-126">Пример 4</span><span class="sxs-lookup"><span data-stu-id="1d456-126">Example 4</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="1d456-127">Создание конфигурации устройства с содержимым.</span><span class="sxs-lookup"><span data-stu-id="1d456-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="1d456-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1d456-128">PARAMETERS</span></span>

### <span data-ttu-id="1d456-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d456-129">-DefaultProfile</span></span>
<span data-ttu-id="1d456-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1d456-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d456-131">-DeviceContent</span><span class="sxs-lookup"><span data-stu-id="1d456-131">-DeviceContent</span></span>
<span data-ttu-id="1d456-132">Настройка устройств IotHub.</span><span class="sxs-lookup"><span data-stu-id="1d456-132">Configuration for IotHub devices.</span></span>

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

### <span data-ttu-id="1d456-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d456-133">-InputObject</span></span>
<span data-ttu-id="1d456-134">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="1d456-134">IotHub object</span></span>

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

### <span data-ttu-id="1d456-135">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1d456-135">-IotHubName</span></span>
<span data-ttu-id="1d456-136">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="1d456-136">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1d456-137">-Label</span><span class="sxs-lookup"><span data-stu-id="1d456-137">-Label</span></span>
<span data-ttu-id="1d456-138">Схема подписей, применяемых к целевой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1d456-138">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="1d456-139">-Метрическая система мер</span><span class="sxs-lookup"><span data-stu-id="1d456-139">-Metric</span></span>
<span data-ttu-id="1d456-140">Коллекция запросов для определения метрик конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1d456-140">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="1d456-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1d456-141">-Name</span></span>
<span data-ttu-id="1d456-142">Идентификатор конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1d456-142">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="1d456-143">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="1d456-143">-Priority</span></span>
<span data-ttu-id="1d456-144">Вес конфигурации устройства в случае использования правил конкурирующих конкурентов (самый высокий WINS-сервер).</span><span class="sxs-lookup"><span data-stu-id="1d456-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="1d456-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d456-145">-ResourceGroupName</span></span>
<span data-ttu-id="1d456-146">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1d456-146">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1d456-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d456-147">-ResourceId</span></span>
<span data-ttu-id="1d456-148">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="1d456-148">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1d456-149">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="1d456-149">-TargetCondition</span></span>
<span data-ttu-id="1d456-150">Целевое условие, к которому применяется конфигурация устройства.</span><span class="sxs-lookup"><span data-stu-id="1d456-150">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="1d456-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d456-151">-Confirm</span></span>
<span data-ttu-id="1d456-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1d456-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d456-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d456-153">-WhatIf</span></span>
<span data-ttu-id="1d456-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1d456-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d456-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1d456-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d456-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d456-156">CommonParameters</span></span>
<span data-ttu-id="1d456-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1d456-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d456-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d456-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d456-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1d456-159">INPUTS</span></span>

### <span data-ttu-id="1d456-160">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1d456-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1d456-161">System. String</span><span class="sxs-lookup"><span data-stu-id="1d456-161">System.String</span></span>

## <span data-ttu-id="1d456-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d456-162">OUTPUTS</span></span>

### <span data-ttu-id="1d456-163">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d456-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="1d456-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="1d456-164">NOTES</span></span>

## <span data-ttu-id="1d456-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d456-165">RELATED LINKS</span></span>
