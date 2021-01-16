---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 173e84e3587a6844896791ef38a185db522d4e4b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411775"
---
# <span data-ttu-id="ccecc-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="ccecc-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="ccecc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccecc-102">SYNOPSIS</span></span>
<span data-ttu-id="ccecc-103">Проверка маршрутов в центре IoT</span><span class="sxs-lookup"><span data-stu-id="ccecc-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="ccecc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ccecc-104">SYNTAX</span></span>

### <span data-ttu-id="ccecc-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ccecc-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccecc-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="ccecc-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccecc-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="ccecc-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ccecc-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="ccecc-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccecc-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="ccecc-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ccecc-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="ccecc-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccecc-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="ccecc-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccecc-112">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccecc-112">DESCRIPTION</span></span>
<span data-ttu-id="ccecc-113">Проверьте определенный маршрут.</span><span class="sxs-lookup"><span data-stu-id="ccecc-113">Test a specific route.</span></span>

## <span data-ttu-id="ccecc-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ccecc-114">EXAMPLES</span></span>

### <span data-ttu-id="ccecc-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ccecc-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="ccecc-116">Проверьте весь маршрут с исходным "DeviceMessages".</span><span class="sxs-lookup"><span data-stu-id="ccecc-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="ccecc-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ccecc-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="ccecc-118">Проверьте определенный маршрут.</span><span class="sxs-lookup"><span data-stu-id="ccecc-118">Test a specific route.</span></span>

### <span data-ttu-id="ccecc-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ccecc-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="ccecc-120">Протестировать определенный маршрут и показать причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="ccecc-120">Test a specific route and showing the reason of failure.</span></span>

### <span data-ttu-id="ccecc-121">Пример 4</span><span class="sxs-lookup"><span data-stu-id="ccecc-121">Example 4</span></span>
```
PS C:\> $ap = @{}
PS C:\> $ap.add("key0","value0")
PS C:\> $sp = @{}
PS C:\> $sp.add("key1", "value1")
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -AppProperty $ap -SystemProperty $sp

Result : true
```

<span data-ttu-id="ccecc-122">Проверьте определенный маршрут с помощью AppProperty и SystemProperty.</span><span class="sxs-lookup"><span data-stu-id="ccecc-122">Test a specific route with AppProperty and SystemProperty.</span></span>

## <span data-ttu-id="ccecc-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccecc-123">PARAMETERS</span></span>

### <span data-ttu-id="ccecc-124">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="ccecc-124">-AppProperty</span></span>
<span data-ttu-id="ccecc-125">Свойства приложения сообщения о маршруте</span><span class="sxs-lookup"><span data-stu-id="ccecc-125">App properties of the route message</span></span>

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

### <span data-ttu-id="ccecc-126">-Body</span><span class="sxs-lookup"><span data-stu-id="ccecc-126">-Body</span></span>
<span data-ttu-id="ccecc-127">Текст сообщения о маршруте</span><span class="sxs-lookup"><span data-stu-id="ccecc-127">Body of the route message</span></span>

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

### <span data-ttu-id="ccecc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccecc-128">-DefaultProfile</span></span>
<span data-ttu-id="ccecc-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ccecc-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccecc-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccecc-130">-InputObject</span></span>
<span data-ttu-id="ccecc-131">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="ccecc-131">IotHub Object</span></span>

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

### <span data-ttu-id="ccecc-132">-Name</span><span class="sxs-lookup"><span data-stu-id="ccecc-132">-Name</span></span>
<span data-ttu-id="ccecc-133">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="ccecc-133">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ccecc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccecc-134">-ResourceGroupName</span></span>
<span data-ttu-id="ccecc-135">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ccecc-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ccecc-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccecc-136">-ResourceId</span></span>
<span data-ttu-id="ccecc-137">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="ccecc-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ccecc-138">-RouteName</span><span class="sxs-lookup"><span data-stu-id="ccecc-138">-RouteName</span></span>
<span data-ttu-id="ccecc-139">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="ccecc-139">Name of the Route</span></span>

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

### <span data-ttu-id="ccecc-140">-ShowError</span><span class="sxs-lookup"><span data-stu-id="ccecc-140">-ShowError</span></span>
<span data-ttu-id="ccecc-141">Показывать подробные сведения об ошибке, если они существуют</span><span class="sxs-lookup"><span data-stu-id="ccecc-141">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="ccecc-142">-Source</span><span class="sxs-lookup"><span data-stu-id="ccecc-142">-Source</span></span>
<span data-ttu-id="ccecc-143">Источник маршрута</span><span class="sxs-lookup"><span data-stu-id="ccecc-143">Source of the route</span></span>

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

### <span data-ttu-id="ccecc-144">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="ccecc-144">-SystemProperty</span></span>
<span data-ttu-id="ccecc-145">Системные свойства сообщения о маршруте</span><span class="sxs-lookup"><span data-stu-id="ccecc-145">System properties of the route message</span></span>

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

### <span data-ttu-id="ccecc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccecc-146">CommonParameters</span></span>
<span data-ttu-id="ccecc-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccecc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccecc-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccecc-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccecc-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ccecc-149">INPUTS</span></span>

### <span data-ttu-id="ccecc-150">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ccecc-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ccecc-151">System.String</span><span class="sxs-lookup"><span data-stu-id="ccecc-151">System.String</span></span>

## <span data-ttu-id="ccecc-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ccecc-152">OUTPUTS</span></span>

### <span data-ttu-id="ccecc-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="ccecc-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="ccecc-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="ccecc-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="ccecc-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="ccecc-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="ccecc-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ccecc-156">NOTES</span></span>

## <span data-ttu-id="ccecc-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ccecc-157">RELATED LINKS</span></span>
