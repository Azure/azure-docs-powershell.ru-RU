---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: a54bfdb26b7013e490ca36e4ae5608da228d9d70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415236"
---
# <span data-ttu-id="cc660-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="cc660-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="cc660-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc660-102">SYNOPSIS</span></span>
<span data-ttu-id="cc660-103">Обновление маршрута в центре IoT</span><span class="sxs-lookup"><span data-stu-id="cc660-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="cc660-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cc660-104">SYNTAX</span></span>

### <span data-ttu-id="cc660-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cc660-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc660-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cc660-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc660-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cc660-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc660-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc660-108">DESCRIPTION</span></span>
<span data-ttu-id="cc660-109">Изменить маршрут.</span><span class="sxs-lookup"><span data-stu-id="cc660-109">Edit a route.</span></span> <span data-ttu-id="cc660-110">Вы можете обновить все поля в маршруте, включая источник данных, конечную точку, запрос маршрутинга, а также включить или отключить маршрут.</span><span class="sxs-lookup"><span data-stu-id="cc660-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="cc660-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cc660-111">EXAMPLES</span></span>

### <span data-ttu-id="cc660-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cc660-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="cc660-113">Обновление сведений о маршруте.</span><span class="sxs-lookup"><span data-stu-id="cc660-113">Updating the route information.</span></span>

### <span data-ttu-id="cc660-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cc660-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="cc660-115">Обновление сведений о маршруте.</span><span class="sxs-lookup"><span data-stu-id="cc660-115">Updating the route information.</span></span>

### <span data-ttu-id="cc660-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cc660-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="cc660-117">Обновление сведений о маршруте.</span><span class="sxs-lookup"><span data-stu-id="cc660-117">Updating the route information.</span></span>

## <span data-ttu-id="cc660-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc660-118">PARAMETERS</span></span>

### <span data-ttu-id="cc660-119">-Условие</span><span class="sxs-lookup"><span data-stu-id="cc660-119">-Condition</span></span>
<span data-ttu-id="cc660-120">Условие, оцениваемое для применения правила маршрутки</span><span class="sxs-lookup"><span data-stu-id="cc660-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="cc660-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc660-121">-DefaultProfile</span></span>
<span data-ttu-id="cc660-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc660-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc660-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="cc660-123">-Enabled</span></span>
<span data-ttu-id="cc660-124">Включить маршрут</span><span class="sxs-lookup"><span data-stu-id="cc660-124">Enable route</span></span>

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

### <span data-ttu-id="cc660-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cc660-125">-EndpointName</span></span>
<span data-ttu-id="cc660-126">Имя конечной точки маршрутки</span><span class="sxs-lookup"><span data-stu-id="cc660-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="cc660-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc660-127">-InputObject</span></span>
<span data-ttu-id="cc660-128">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="cc660-128">IotHub Object</span></span>

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

### <span data-ttu-id="cc660-129">-Name</span><span class="sxs-lookup"><span data-stu-id="cc660-129">-Name</span></span>
<span data-ttu-id="cc660-130">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="cc660-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cc660-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc660-131">-ResourceGroupName</span></span>
<span data-ttu-id="cc660-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cc660-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cc660-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc660-133">-ResourceId</span></span>
<span data-ttu-id="cc660-134">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="cc660-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cc660-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="cc660-135">-RouteName</span></span>
<span data-ttu-id="cc660-136">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="cc660-136">Name of the Route</span></span>

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

### <span data-ttu-id="cc660-137">-Source</span><span class="sxs-lookup"><span data-stu-id="cc660-137">-Source</span></span>
<span data-ttu-id="cc660-138">Источник маршрута</span><span class="sxs-lookup"><span data-stu-id="cc660-138">Source of the route</span></span>

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

### <span data-ttu-id="cc660-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc660-139">-Confirm</span></span>
<span data-ttu-id="cc660-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc660-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc660-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc660-141">-WhatIf</span></span>
<span data-ttu-id="cc660-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc660-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc660-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cc660-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc660-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc660-144">CommonParameters</span></span>
<span data-ttu-id="cc660-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc660-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc660-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc660-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc660-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc660-147">INPUTS</span></span>

### <span data-ttu-id="cc660-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cc660-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cc660-149">System.String</span><span class="sxs-lookup"><span data-stu-id="cc660-149">System.String</span></span>

## <span data-ttu-id="cc660-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc660-150">OUTPUTS</span></span>

### <span data-ttu-id="cc660-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="cc660-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="cc660-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cc660-152">NOTES</span></span>

## <span data-ttu-id="cc660-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc660-153">RELATED LINKS</span></span>
