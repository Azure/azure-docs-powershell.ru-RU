---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 9b6c9b77ae29214c7d998e3d2c859e4ac7521db1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236216"
---
# <span data-ttu-id="53272-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="53272-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="53272-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="53272-102">SYNOPSIS</span></span>
<span data-ttu-id="53272-103">Обновите изменяемые поля для регистрации конфигурации.</span><span class="sxs-lookup"><span data-stu-id="53272-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="53272-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="53272-104">SYNTAX</span></span>

### <span data-ttu-id="53272-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="53272-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53272-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="53272-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53272-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="53272-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53272-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53272-108">DESCRIPTION</span></span>
<span data-ttu-id="53272-109">Обновление указанных свойств автоматической конфигурации управления устройствами IoT.</span><span class="sxs-lookup"><span data-stu-id="53272-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="53272-110">Примечание. содержимое конфигурации является неизменяемым.</span><span class="sxs-lookup"><span data-stu-id="53272-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="53272-111">Свойства конфигурации, которые можно обновить: "метки", "метрики", "приоритет" и "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="53272-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="53272-112"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementДля получения дополнительных сведений ознакомьтесь с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="53272-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="53272-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="53272-113">EXAMPLES</span></span>

### <span data-ttu-id="53272-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="53272-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="53272-115">Изменение приоритета конфигурации устройства и обновление его конечного состояния</span><span class="sxs-lookup"><span data-stu-id="53272-115">Alter the priority of a device configuration and update its target condition</span></span>

## <span data-ttu-id="53272-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="53272-116">PARAMETERS</span></span>

### <span data-ttu-id="53272-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53272-117">-DefaultProfile</span></span>
<span data-ttu-id="53272-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53272-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53272-119">-Force</span><span class="sxs-lookup"><span data-stu-id="53272-119">-Force</span></span>
<span data-ttu-id="53272-120">Объект конфигурации можно заменять, даже если он был обновлен после того, как он был получен в прошлый раз.</span><span class="sxs-lookup"><span data-stu-id="53272-120">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="53272-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53272-121">-InputObject</span></span>
<span data-ttu-id="53272-122">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="53272-122">IotHub object</span></span>

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

### <span data-ttu-id="53272-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="53272-123">-IotHubName</span></span>
<span data-ttu-id="53272-124">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="53272-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="53272-125">-Label</span><span class="sxs-lookup"><span data-stu-id="53272-125">-Label</span></span>
<span data-ttu-id="53272-126">Схема подписей, применяемых к целевой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="53272-126">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="53272-127">-Метрическая система мер</span><span class="sxs-lookup"><span data-stu-id="53272-127">-Metric</span></span>
<span data-ttu-id="53272-128">Коллекция запросов для определения метрик конфигурации.</span><span class="sxs-lookup"><span data-stu-id="53272-128">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="53272-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="53272-129">-Name</span></span>
<span data-ttu-id="53272-130">Идентификатор конфигурации.</span><span class="sxs-lookup"><span data-stu-id="53272-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="53272-131">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="53272-131">-Priority</span></span>
<span data-ttu-id="53272-132">Вес конфигурации устройства в случае использования правил конкурирующих конкурентов (самый высокий WINS-сервер).</span><span class="sxs-lookup"><span data-stu-id="53272-132">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="53272-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53272-133">-ResourceGroupName</span></span>
<span data-ttu-id="53272-134">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="53272-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="53272-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53272-135">-ResourceId</span></span>
<span data-ttu-id="53272-136">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="53272-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="53272-137">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="53272-137">-TargetCondition</span></span>
<span data-ttu-id="53272-138">Целевое условие, к которому применяется конфигурация устройства.</span><span class="sxs-lookup"><span data-stu-id="53272-138">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="53272-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53272-139">-Confirm</span></span>
<span data-ttu-id="53272-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="53272-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53272-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53272-141">-WhatIf</span></span>
<span data-ttu-id="53272-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="53272-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53272-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="53272-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53272-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53272-144">CommonParameters</span></span>
<span data-ttu-id="53272-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="53272-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53272-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53272-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53272-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="53272-147">INPUTS</span></span>

### <span data-ttu-id="53272-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="53272-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="53272-149">System. String</span><span class="sxs-lookup"><span data-stu-id="53272-149">System.String</span></span>

## <span data-ttu-id="53272-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="53272-150">OUTPUTS</span></span>

### <span data-ttu-id="53272-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="53272-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="53272-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="53272-152">NOTES</span></span>

## <span data-ttu-id="53272-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53272-153">RELATED LINKS</span></span>
