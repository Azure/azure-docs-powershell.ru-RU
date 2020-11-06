---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoute.md
ms.openlocfilehash: 1b248225e86f4294603d3a07f1d8a1c7068e2851
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564424"
---
# <span data-ttu-id="e2848-101">Add-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="e2848-101">Add-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="e2848-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2848-102">SYNOPSIS</span></span>
<span data-ttu-id="e2848-103">Создание маршрута в центре Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="e2848-103">Create a route in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2848-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2848-104">SYNTAX</span></span>

### <span data-ttu-id="e2848-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2848-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source] <PSRoutingSource> [-EndpointName] <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2848-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e2848-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source] <PSRoutingSource>
 [-EndpointName] <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2848-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e2848-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source] <PSRoutingSource>
 [-EndpointName] <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2848-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2848-108">DESCRIPTION</span></span>
<span data-ttu-id="e2848-109">Создание маршрута для отправки определенного источника данных и условия на нужную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="e2848-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="e2848-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2848-110">EXAMPLES</span></span>

### <span data-ttu-id="e2848-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e2848-111">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="e2848-112">Создать новый маршрут R1.</span><span class="sxs-lookup"><span data-stu-id="e2848-112">Create a new route "R1".</span></span>

## <span data-ttu-id="e2848-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2848-113">PARAMETERS</span></span>

### <span data-ttu-id="e2848-114">-Условие</span><span class="sxs-lookup"><span data-stu-id="e2848-114">-Condition</span></span>
<span data-ttu-id="e2848-115">Условие, которое оценивается для применения правила маршрутизации</span><span class="sxs-lookup"><span data-stu-id="e2848-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="e2848-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2848-116">-DefaultProfile</span></span>
<span data-ttu-id="e2848-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2848-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2848-118">-Включено</span><span class="sxs-lookup"><span data-stu-id="e2848-118">-Enabled</span></span>
<span data-ttu-id="e2848-119">Включить маршрут</span><span class="sxs-lookup"><span data-stu-id="e2848-119">Enable route</span></span>

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

### <span data-ttu-id="e2848-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e2848-120">-EndpointName</span></span>
<span data-ttu-id="e2848-121">Имя конечной точки маршрутизации</span><span class="sxs-lookup"><span data-stu-id="e2848-121">Name of the routing endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2848-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2848-122">-InputObject</span></span>
<span data-ttu-id="e2848-123">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="e2848-123">IotHub Object</span></span>

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

### <span data-ttu-id="e2848-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2848-124">-Name</span></span>
<span data-ttu-id="e2848-125">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="e2848-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e2848-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2848-126">-ResourceGroupName</span></span>
<span data-ttu-id="e2848-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e2848-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e2848-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2848-128">-ResourceId</span></span>
<span data-ttu-id="e2848-129">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="e2848-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e2848-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="e2848-130">-RouteName</span></span>
<span data-ttu-id="e2848-131">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="e2848-131">Name of the Route</span></span>

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

### <span data-ttu-id="e2848-132">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="e2848-132">-Source</span></span>
<span data-ttu-id="e2848-133">Источник маршрута</span><span class="sxs-lookup"><span data-stu-id="e2848-133">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2848-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2848-134">-Confirm</span></span>
<span data-ttu-id="e2848-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2848-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2848-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2848-136">-WhatIf</span></span>
<span data-ttu-id="e2848-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2848-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2848-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2848-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2848-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2848-139">CommonParameters</span></span>
<span data-ttu-id="e2848-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2848-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2848-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2848-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2848-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2848-142">INPUTS</span></span>

### <span data-ttu-id="e2848-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e2848-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="e2848-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e2848-144">System.String</span></span>

## <span data-ttu-id="e2848-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2848-145">OUTPUTS</span></span>

### <span data-ttu-id="e2848-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="e2848-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="e2848-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2848-147">NOTES</span></span>

## <span data-ttu-id="e2848-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2848-148">RELATED LINKS</span></span>
