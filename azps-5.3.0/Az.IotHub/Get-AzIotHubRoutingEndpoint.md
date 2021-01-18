---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 8b3d139d822452231451a1f07907ac20cdf3589c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518418"
---
# <span data-ttu-id="f48aa-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="f48aa-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="f48aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f48aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f48aa-103">Сведения о всех конечных точках для концентратора IoT</span><span class="sxs-lookup"><span data-stu-id="f48aa-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="f48aa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f48aa-104">SYNTAX</span></span>

### <span data-ttu-id="f48aa-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f48aa-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f48aa-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f48aa-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f48aa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f48aa-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f48aa-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f48aa-108">DESCRIPTION</span></span>
<span data-ttu-id="f48aa-109">Получите сведения о конечной точке.</span><span class="sxs-lookup"><span data-stu-id="f48aa-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="f48aa-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f48aa-110">EXAMPLES</span></span>

### <span data-ttu-id="f48aa-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f48aa-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="f48aa-112">Получите все конечные точки из IoT-концентратора Myiothub.</span><span class="sxs-lookup"><span data-stu-id="f48aa-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="f48aa-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f48aa-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="f48aa-114">Получите все конечные точки типа EventHub из IoT-концентратора Myiothub.</span><span class="sxs-lookup"><span data-stu-id="f48aa-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="f48aa-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f48aa-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="f48aa-116">Получите все конечные точки типа EventHub из IoT-концентратора Myiothub.</span><span class="sxs-lookup"><span data-stu-id="f48aa-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="f48aa-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="f48aa-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="f48aa-118">Получите сведения о конечной точке из IoT Hub myiothub.</span><span class="sxs-lookup"><span data-stu-id="f48aa-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="f48aa-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f48aa-119">PARAMETERS</span></span>

### <span data-ttu-id="f48aa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f48aa-120">-DefaultProfile</span></span>
<span data-ttu-id="f48aa-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f48aa-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f48aa-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f48aa-122">-EndpointName</span></span>
<span data-ttu-id="f48aa-123">Имя конечной точки маршрутинга</span><span class="sxs-lookup"><span data-stu-id="f48aa-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="f48aa-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="f48aa-124">-EndpointType</span></span>
<span data-ttu-id="f48aa-125">Тип конечной точки маршрутинга</span><span class="sxs-lookup"><span data-stu-id="f48aa-125">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f48aa-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f48aa-126">-InputObject</span></span>
<span data-ttu-id="f48aa-127">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="f48aa-127">IotHub Object</span></span>

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

### <span data-ttu-id="f48aa-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f48aa-128">-Name</span></span>
<span data-ttu-id="f48aa-129">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="f48aa-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f48aa-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f48aa-130">-ResourceGroupName</span></span>
<span data-ttu-id="f48aa-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f48aa-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f48aa-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f48aa-132">-ResourceId</span></span>
<span data-ttu-id="f48aa-133">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="f48aa-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f48aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f48aa-134">CommonParameters</span></span>
<span data-ttu-id="f48aa-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f48aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f48aa-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f48aa-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f48aa-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f48aa-137">INPUTS</span></span>

### <span data-ttu-id="f48aa-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f48aa-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f48aa-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f48aa-139">System.String</span></span>

## <span data-ttu-id="f48aa-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f48aa-140">OUTPUTS</span></span>

### <span data-ttu-id="f48aa-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="f48aa-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="f48aa-142">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f48aa-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f48aa-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="f48aa-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="f48aa-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span><span class="sxs-lookup"><span data-stu-id="f48aa-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="f48aa-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="f48aa-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="f48aa-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span><span class="sxs-lookup"><span data-stu-id="f48aa-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="f48aa-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f48aa-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="f48aa-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span><span class="sxs-lookup"><span data-stu-id="f48aa-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="f48aa-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span><span class="sxs-lookup"><span data-stu-id="f48aa-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="f48aa-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f48aa-150">NOTES</span></span>

## <span data-ttu-id="f48aa-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f48aa-151">RELATED LINKS</span></span>
