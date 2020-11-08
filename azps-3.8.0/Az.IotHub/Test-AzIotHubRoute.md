---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: eb9d6a7b847c360861fd13bb285bc6f09bb70fbc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066361"
---
# <span data-ttu-id="9fa84-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="9fa84-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="9fa84-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9fa84-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa84-103">Проверка маршрутов в центре Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="9fa84-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="9fa84-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9fa84-104">SYNTAX</span></span>

### <span data-ttu-id="9fa84-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9fa84-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fa84-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="9fa84-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fa84-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="9fa84-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fa84-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="9fa84-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fa84-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="9fa84-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fa84-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="9fa84-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fa84-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="9fa84-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fa84-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fa84-112">DESCRIPTION</span></span>
<span data-ttu-id="9fa84-113">Протестируйте конкретный маршрут.</span><span class="sxs-lookup"><span data-stu-id="9fa84-113">Test a specific route.</span></span>

## <span data-ttu-id="9fa84-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9fa84-114">EXAMPLES</span></span>

### <span data-ttu-id="9fa84-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9fa84-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="9fa84-116">Проверка всех маршрутов с источником "DeviceMessages".</span><span class="sxs-lookup"><span data-stu-id="9fa84-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="9fa84-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9fa84-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="9fa84-118">Протестируйте конкретный маршрут.</span><span class="sxs-lookup"><span data-stu-id="9fa84-118">Test a specific route.</span></span>

### <span data-ttu-id="9fa84-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9fa84-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="9fa84-120">Проверить конкретный маршрут и показать причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="9fa84-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="9fa84-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9fa84-121">PARAMETERS</span></span>

### <span data-ttu-id="9fa84-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="9fa84-122">-AppProperty</span></span>
<span data-ttu-id="9fa84-123">Свойства приложения для сообщения маршрута</span><span class="sxs-lookup"><span data-stu-id="9fa84-123">App properties of the route message</span></span>

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

### <span data-ttu-id="9fa84-124">-Body</span><span class="sxs-lookup"><span data-stu-id="9fa84-124">-Body</span></span>
<span data-ttu-id="9fa84-125">Текст сообщения маршрута</span><span class="sxs-lookup"><span data-stu-id="9fa84-125">Body of the route message</span></span>

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

### <span data-ttu-id="9fa84-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa84-126">-DefaultProfile</span></span>
<span data-ttu-id="9fa84-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa84-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fa84-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fa84-128">-InputObject</span></span>
<span data-ttu-id="9fa84-129">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="9fa84-129">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectTestRouteSet, InputObjectTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa84-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9fa84-130">-Name</span></span>
<span data-ttu-id="9fa84-131">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="9fa84-131">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa84-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fa84-132">-ResourceGroupName</span></span>
<span data-ttu-id="9fa84-133">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9fa84-133">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa84-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fa84-134">-ResourceId</span></span>
<span data-ttu-id="9fa84-135">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="9fa84-135">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdTestRouteSet, ResourceIdTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa84-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="9fa84-136">-RouteName</span></span>
<span data-ttu-id="9fa84-137">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="9fa84-137">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa84-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="9fa84-138">-ShowError</span></span>
<span data-ttu-id="9fa84-139">Показывать подробное сообщение об ошибке (если есть)</span><span class="sxs-lookup"><span data-stu-id="9fa84-139">Show detailed error, if exist</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa84-140">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="9fa84-140">-Source</span></span>
<span data-ttu-id="9fa84-141">Источник маршрута</span><span class="sxs-lookup"><span data-stu-id="9fa84-141">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: InputObjectTestAllRouteSet, TestAllRouteSet, ResourceIdTestAllRouteSet
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa84-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="9fa84-142">-SystemProperty</span></span>
<span data-ttu-id="9fa84-143">Свойства системы для сообщения маршрута</span><span class="sxs-lookup"><span data-stu-id="9fa84-143">System properties of the route message</span></span>

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

### <span data-ttu-id="9fa84-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa84-144">CommonParameters</span></span>
<span data-ttu-id="9fa84-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9fa84-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa84-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fa84-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa84-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9fa84-147">INPUTS</span></span>

### <span data-ttu-id="9fa84-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9fa84-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9fa84-149">System. String</span><span class="sxs-lookup"><span data-stu-id="9fa84-149">System.String</span></span>

## <span data-ttu-id="9fa84-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fa84-150">OUTPUTS</span></span>

### <span data-ttu-id="9fa84-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="9fa84-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="9fa84-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="9fa84-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="9fa84-153">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="9fa84-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="9fa84-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="9fa84-154">NOTES</span></span>

## <span data-ttu-id="9fa84-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9fa84-155">RELATED LINKS</span></span>
