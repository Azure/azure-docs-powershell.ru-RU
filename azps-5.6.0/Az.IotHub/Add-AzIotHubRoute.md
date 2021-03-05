---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: fbb0801dd586731a938c773711d72847e7a96e50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997811"
---
# <span data-ttu-id="41fb0-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="41fb0-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="41fb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41fb0-102">SYNOPSIS</span></span>
<span data-ttu-id="41fb0-103">Создание маршрутов в центре IoT</span><span class="sxs-lookup"><span data-stu-id="41fb0-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="41fb0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="41fb0-104">SYNTAX</span></span>

### <span data-ttu-id="41fb0-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41fb0-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41fb0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="41fb0-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41fb0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="41fb0-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41fb0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41fb0-108">DESCRIPTION</span></span>
<span data-ttu-id="41fb0-109">Создайте маршрут для отправки определенного источника данных и условия в нужную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="41fb0-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="41fb0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="41fb0-110">EXAMPLES</span></span>

### <span data-ttu-id="41fb0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41fb0-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="41fb0-112">Создать новый маршрут "R1".</span><span class="sxs-lookup"><span data-stu-id="41fb0-112">Create a new route "R1".</span></span>

## <span data-ttu-id="41fb0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41fb0-113">PARAMETERS</span></span>

### <span data-ttu-id="41fb0-114">-Condition</span><span class="sxs-lookup"><span data-stu-id="41fb0-114">-Condition</span></span>
<span data-ttu-id="41fb0-115">Условие, оцениваемое для применения правила маршрутки</span><span class="sxs-lookup"><span data-stu-id="41fb0-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="41fb0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41fb0-116">-DefaultProfile</span></span>
<span data-ttu-id="41fb0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41fb0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41fb0-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="41fb0-118">-Enabled</span></span>
<span data-ttu-id="41fb0-119">Включить маршрут</span><span class="sxs-lookup"><span data-stu-id="41fb0-119">Enable route</span></span>

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

### <span data-ttu-id="41fb0-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="41fb0-120">-EndpointName</span></span>
<span data-ttu-id="41fb0-121">Имя конечной точки маршрутки</span><span class="sxs-lookup"><span data-stu-id="41fb0-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="41fb0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41fb0-122">-InputObject</span></span>
<span data-ttu-id="41fb0-123">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="41fb0-123">IotHub Object</span></span>

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

### <span data-ttu-id="41fb0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="41fb0-124">-Name</span></span>
<span data-ttu-id="41fb0-125">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="41fb0-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="41fb0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41fb0-126">-ResourceGroupName</span></span>
<span data-ttu-id="41fb0-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="41fb0-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="41fb0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41fb0-128">-ResourceId</span></span>
<span data-ttu-id="41fb0-129">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="41fb0-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="41fb0-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="41fb0-130">-RouteName</span></span>
<span data-ttu-id="41fb0-131">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="41fb0-131">Name of the Route</span></span>

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

### <span data-ttu-id="41fb0-132">-Source</span><span class="sxs-lookup"><span data-stu-id="41fb0-132">-Source</span></span>
<span data-ttu-id="41fb0-133">Источник маршрута</span><span class="sxs-lookup"><span data-stu-id="41fb0-133">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41fb0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41fb0-134">-Confirm</span></span>
<span data-ttu-id="41fb0-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="41fb0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41fb0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41fb0-136">-WhatIf</span></span>
<span data-ttu-id="41fb0-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41fb0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41fb0-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="41fb0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41fb0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41fb0-139">CommonParameters</span></span>
<span data-ttu-id="41fb0-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41fb0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41fb0-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41fb0-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41fb0-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41fb0-142">INPUTS</span></span>

### <span data-ttu-id="41fb0-143">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="41fb0-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="41fb0-144">System.String</span><span class="sxs-lookup"><span data-stu-id="41fb0-144">System.String</span></span>

## <span data-ttu-id="41fb0-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="41fb0-145">OUTPUTS</span></span>

### <span data-ttu-id="41fb0-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="41fb0-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="41fb0-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="41fb0-147">NOTES</span></span>

## <span data-ttu-id="41fb0-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41fb0-148">RELATED LINKS</span></span>
