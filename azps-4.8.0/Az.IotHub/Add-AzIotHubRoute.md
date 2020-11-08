---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: a84d432e5771b5f04a7d9f478cd8ef446e08620a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236674"
---
# <span data-ttu-id="1fd8f-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="1fd8f-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="1fd8f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fd8f-102">SYNOPSIS</span></span>
<span data-ttu-id="1fd8f-103">Создание маршрута в центре Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="1fd8f-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="1fd8f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fd8f-104">SYNTAX</span></span>

### <span data-ttu-id="1fd8f-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1fd8f-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fd8f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1fd8f-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fd8f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1fd8f-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1fd8f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fd8f-108">DESCRIPTION</span></span>
<span data-ttu-id="1fd8f-109">Создание маршрута для отправки определенного источника данных и условия на нужную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="1fd8f-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="1fd8f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fd8f-110">EXAMPLES</span></span>

### <span data-ttu-id="1fd8f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1fd8f-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="1fd8f-112">Создать новый маршрут R1.</span><span class="sxs-lookup"><span data-stu-id="1fd8f-112">Create a new route "R1".</span></span>

## <span data-ttu-id="1fd8f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fd8f-113">PARAMETERS</span></span>

### <span data-ttu-id="1fd8f-114">-Условие</span><span class="sxs-lookup"><span data-stu-id="1fd8f-114">-Condition</span></span>
<span data-ttu-id="1fd8f-115">Условие, которое оценивается для применения правила маршрутизации</span><span class="sxs-lookup"><span data-stu-id="1fd8f-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="1fd8f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fd8f-116">-DefaultProfile</span></span>
<span data-ttu-id="1fd8f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fd8f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fd8f-118">-Включено</span><span class="sxs-lookup"><span data-stu-id="1fd8f-118">-Enabled</span></span>
<span data-ttu-id="1fd8f-119">Включить маршрут</span><span class="sxs-lookup"><span data-stu-id="1fd8f-119">Enable route</span></span>

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

### <span data-ttu-id="1fd8f-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1fd8f-120">-EndpointName</span></span>
<span data-ttu-id="1fd8f-121">Имя конечной точки маршрутизации</span><span class="sxs-lookup"><span data-stu-id="1fd8f-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="1fd8f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fd8f-122">-InputObject</span></span>
<span data-ttu-id="1fd8f-123">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="1fd8f-123">IotHub Object</span></span>

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

### <span data-ttu-id="1fd8f-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1fd8f-124">-Name</span></span>
<span data-ttu-id="1fd8f-125">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="1fd8f-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1fd8f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fd8f-126">-ResourceGroupName</span></span>
<span data-ttu-id="1fd8f-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1fd8f-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1fd8f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fd8f-128">-ResourceId</span></span>
<span data-ttu-id="1fd8f-129">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="1fd8f-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1fd8f-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="1fd8f-130">-RouteName</span></span>
<span data-ttu-id="1fd8f-131">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="1fd8f-131">Name of the Route</span></span>

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

### <span data-ttu-id="1fd8f-132">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="1fd8f-132">-Source</span></span>
<span data-ttu-id="1fd8f-133">Источник маршрута</span><span class="sxs-lookup"><span data-stu-id="1fd8f-133">Source of the route</span></span>

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

### <span data-ttu-id="1fd8f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fd8f-134">-Confirm</span></span>
<span data-ttu-id="1fd8f-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1fd8f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fd8f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fd8f-136">-WhatIf</span></span>
<span data-ttu-id="1fd8f-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1fd8f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fd8f-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1fd8f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fd8f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fd8f-139">CommonParameters</span></span>
<span data-ttu-id="1fd8f-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fd8f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fd8f-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fd8f-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fd8f-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fd8f-142">INPUTS</span></span>

### <span data-ttu-id="1fd8f-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1fd8f-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1fd8f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1fd8f-144">System.String</span></span>

## <span data-ttu-id="1fd8f-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fd8f-145">OUTPUTS</span></span>

### <span data-ttu-id="1fd8f-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="1fd8f-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="1fd8f-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fd8f-147">NOTES</span></span>

## <span data-ttu-id="1fd8f-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fd8f-148">RELATED LINKS</span></span>
