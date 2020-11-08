---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: a54bfdb26b7013e490ca36e4ae5608da228d9d70
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065869"
---
# <span data-ttu-id="a32fc-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="a32fc-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="a32fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a32fc-102">SYNOPSIS</span></span>
<span data-ttu-id="a32fc-103">Обновление маршрута в центре Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="a32fc-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="a32fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a32fc-104">SYNTAX</span></span>

### <span data-ttu-id="a32fc-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a32fc-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a32fc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a32fc-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a32fc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a32fc-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a32fc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a32fc-108">DESCRIPTION</span></span>
<span data-ttu-id="a32fc-109">Изменение маршрута.</span><span class="sxs-lookup"><span data-stu-id="a32fc-109">Edit a route.</span></span> <span data-ttu-id="a32fc-110">Вы можете обновить все поля в маршруте, включая источник данных, конечную точку, маршрут запроса, а также включить или отключить маршрут.</span><span class="sxs-lookup"><span data-stu-id="a32fc-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="a32fc-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a32fc-111">EXAMPLES</span></span>

### <span data-ttu-id="a32fc-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a32fc-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="a32fc-113">Обновление сведений о маршруте.</span><span class="sxs-lookup"><span data-stu-id="a32fc-113">Updating the route information.</span></span>

### <span data-ttu-id="a32fc-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a32fc-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="a32fc-115">Обновление сведений о маршруте.</span><span class="sxs-lookup"><span data-stu-id="a32fc-115">Updating the route information.</span></span>

### <span data-ttu-id="a32fc-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a32fc-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="a32fc-117">Обновление сведений о маршруте.</span><span class="sxs-lookup"><span data-stu-id="a32fc-117">Updating the route information.</span></span>

## <span data-ttu-id="a32fc-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a32fc-118">PARAMETERS</span></span>

### <span data-ttu-id="a32fc-119">-Условие</span><span class="sxs-lookup"><span data-stu-id="a32fc-119">-Condition</span></span>
<span data-ttu-id="a32fc-120">Условие, которое оценивается для применения правила маршрутизации</span><span class="sxs-lookup"><span data-stu-id="a32fc-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="a32fc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a32fc-121">-DefaultProfile</span></span>
<span data-ttu-id="a32fc-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a32fc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a32fc-123">-Включено</span><span class="sxs-lookup"><span data-stu-id="a32fc-123">-Enabled</span></span>
<span data-ttu-id="a32fc-124">Включить маршрут</span><span class="sxs-lookup"><span data-stu-id="a32fc-124">Enable route</span></span>

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

### <span data-ttu-id="a32fc-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a32fc-125">-EndpointName</span></span>
<span data-ttu-id="a32fc-126">Имя конечной точки маршрутизации</span><span class="sxs-lookup"><span data-stu-id="a32fc-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="a32fc-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a32fc-127">-InputObject</span></span>
<span data-ttu-id="a32fc-128">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="a32fc-128">IotHub Object</span></span>

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

### <span data-ttu-id="a32fc-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a32fc-129">-Name</span></span>
<span data-ttu-id="a32fc-130">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="a32fc-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a32fc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a32fc-131">-ResourceGroupName</span></span>
<span data-ttu-id="a32fc-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a32fc-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a32fc-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a32fc-133">-ResourceId</span></span>
<span data-ttu-id="a32fc-134">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="a32fc-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a32fc-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="a32fc-135">-RouteName</span></span>
<span data-ttu-id="a32fc-136">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="a32fc-136">Name of the Route</span></span>

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

### <span data-ttu-id="a32fc-137">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="a32fc-137">-Source</span></span>
<span data-ttu-id="a32fc-138">Источник маршрута</span><span class="sxs-lookup"><span data-stu-id="a32fc-138">Source of the route</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource]
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a32fc-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a32fc-139">-Confirm</span></span>
<span data-ttu-id="a32fc-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a32fc-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a32fc-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a32fc-141">-WhatIf</span></span>
<span data-ttu-id="a32fc-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a32fc-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a32fc-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a32fc-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a32fc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a32fc-144">CommonParameters</span></span>
<span data-ttu-id="a32fc-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a32fc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a32fc-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a32fc-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a32fc-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a32fc-147">INPUTS</span></span>

### <span data-ttu-id="a32fc-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a32fc-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a32fc-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a32fc-149">System.String</span></span>

## <span data-ttu-id="a32fc-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a32fc-150">OUTPUTS</span></span>

### <span data-ttu-id="a32fc-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="a32fc-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="a32fc-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="a32fc-152">NOTES</span></span>

## <span data-ttu-id="a32fc-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a32fc-153">RELATED LINKS</span></span>
