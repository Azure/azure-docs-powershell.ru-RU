---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/test-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Test-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Test-AzureRmIotHubRoute.md
ms.openlocfilehash: f51ba85215d252959b974a39ea864b1c98fce460
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734381"
---
# <span data-ttu-id="e5c74-101">Test-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="e5c74-101">Test-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="e5c74-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5c74-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c74-103">Проверка маршрутов в центре Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="e5c74-103">Test routes in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5c74-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5c74-104">SYNTAX</span></span>

### <span data-ttu-id="e5c74-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5c74-105">ResourceSet (Default)</span></span>
```
Test-AzureRmIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c74-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="e5c74-106">InputObjectTestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c74-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="e5c74-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5c74-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="e5c74-108">TestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c74-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="e5c74-109">TestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource>
 [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c74-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="e5c74-110">ResourceIdTestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c74-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="e5c74-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5c74-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5c74-112">DESCRIPTION</span></span>
<span data-ttu-id="e5c74-113">Протестируйте конкретный маршрут.</span><span class="sxs-lookup"><span data-stu-id="e5c74-113">Test a specific route.</span></span>

## <span data-ttu-id="e5c74-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5c74-114">EXAMPLES</span></span>

### <span data-ttu-id="e5c74-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5c74-115">Example 1</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="e5c74-116">Проверка всех маршрутов с источником "DeviceMessges".</span><span class="sxs-lookup"><span data-stu-id="e5c74-116">Test all route with source "DeviceMessges".</span></span>

### <span data-ttu-id="e5c74-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e5c74-117">Example 2</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="e5c74-118">Протестируйте конкретный маршрут.</span><span class="sxs-lookup"><span data-stu-id="e5c74-118">Test a specific route.</span></span>

### <span data-ttu-id="e5c74-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e5c74-119">Example 3</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="e5c74-120">Проверить конкретный маршрут и показать причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="e5c74-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="e5c74-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5c74-121">PARAMETERS</span></span>

### <span data-ttu-id="e5c74-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="e5c74-122">-AppProperty</span></span>
<span data-ttu-id="e5c74-123">Свойства приложения для сообщения маршрута</span><span class="sxs-lookup"><span data-stu-id="e5c74-123">App properties of the route message</span></span>

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

### <span data-ttu-id="e5c74-124">-Body</span><span class="sxs-lookup"><span data-stu-id="e5c74-124">-Body</span></span>
<span data-ttu-id="e5c74-125">Текст сообщения маршрута</span><span class="sxs-lookup"><span data-stu-id="e5c74-125">Body of the route message</span></span>

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

### <span data-ttu-id="e5c74-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c74-126">-DefaultProfile</span></span>
<span data-ttu-id="e5c74-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c74-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5c74-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5c74-128">-InputObject</span></span>
<span data-ttu-id="e5c74-129">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c74-129">IotHub Object</span></span>

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

### <span data-ttu-id="e5c74-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e5c74-130">-Name</span></span>
<span data-ttu-id="e5c74-131">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="e5c74-131">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e5c74-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c74-132">-ResourceGroupName</span></span>
<span data-ttu-id="e5c74-133">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e5c74-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e5c74-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5c74-134">-ResourceId</span></span>
<span data-ttu-id="e5c74-135">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="e5c74-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e5c74-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="e5c74-136">-RouteName</span></span>
<span data-ttu-id="e5c74-137">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="e5c74-137">Name of the Route</span></span>

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

### <span data-ttu-id="e5c74-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="e5c74-138">-ShowError</span></span>
<span data-ttu-id="e5c74-139">Показывать подробное сообщение об ошибке (если есть)</span><span class="sxs-lookup"><span data-stu-id="e5c74-139">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="e5c74-140">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="e5c74-140">-Source</span></span>
<span data-ttu-id="e5c74-141">Источник маршрута</span><span class="sxs-lookup"><span data-stu-id="e5c74-141">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: InputObjectTestAllRouteSet, TestAllRouteSet, ResourceIdTestAllRouteSet
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c74-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="e5c74-142">-SystemProperty</span></span>
<span data-ttu-id="e5c74-143">Свойства системы для сообщения маршрута</span><span class="sxs-lookup"><span data-stu-id="e5c74-143">System properties of the route message</span></span>

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

### <span data-ttu-id="e5c74-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c74-144">CommonParameters</span></span>
<span data-ttu-id="e5c74-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5c74-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c74-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5c74-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c74-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5c74-147">INPUTS</span></span>

### <span data-ttu-id="e5c74-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e5c74-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="e5c74-149">System. String</span><span class="sxs-lookup"><span data-stu-id="e5c74-149">System.String</span></span>

## <span data-ttu-id="e5c74-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5c74-150">OUTPUTS</span></span>

### <span data-ttu-id="e5c74-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="e5c74-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>
<span data-ttu-id="e5c74-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteCompilationError System. Collections. Generic. List "1 [[Microsoft. Azure. System. Management. IotHub. Models. PSRouteProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="e5c74-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e5c74-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5c74-153">NOTES</span></span>

## <span data-ttu-id="e5c74-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5c74-154">RELATED LINKS</span></span>
