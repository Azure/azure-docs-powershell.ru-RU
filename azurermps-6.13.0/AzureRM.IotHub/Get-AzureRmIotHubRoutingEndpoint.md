---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: 2aa49f01b16547987604a7ee978018596c7d9647
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734391"
---
# <span data-ttu-id="a6d61-101">Get-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6d61-101">Get-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="a6d61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6d61-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d61-103">Получение сведений обо всех конечных точках центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="a6d61-103">Get information on all the endpoints for your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6d61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6d61-104">SYNTAX</span></span>

### <span data-ttu-id="a6d61-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6d61-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String>
 [-EndpointType <PSEndpointType>] [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6d61-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a6d61-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6d61-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a6d61-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6d61-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6d61-108">DESCRIPTION</span></span>
<span data-ttu-id="a6d61-109">Получение сведений о конечной точке.</span><span class="sxs-lookup"><span data-stu-id="a6d61-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="a6d61-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6d61-110">EXAMPLES</span></span>

### <span data-ttu-id="a6d61-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a6d61-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="a6d61-112">Получение всех конечных точек из центра Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a6d61-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="a6d61-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a6d61-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="a6d61-114">Получение всех конечных точек типа EventHub из центра Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a6d61-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="a6d61-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a6d61-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="a6d61-116">Получение всех конечных точек типа EventHub из центра Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a6d61-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="a6d61-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="a6d61-117">Example 4</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="a6d61-118">Получение сведений о конечной точке из центра Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a6d61-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="a6d61-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6d61-119">PARAMETERS</span></span>

### <span data-ttu-id="a6d61-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6d61-120">-DefaultProfile</span></span>
<span data-ttu-id="a6d61-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6d61-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6d61-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a6d61-122">-EndpointName</span></span>
<span data-ttu-id="a6d61-123">Имя конечной точки маршрутизации</span><span class="sxs-lookup"><span data-stu-id="a6d61-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="a6d61-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="a6d61-124">-EndpointType</span></span>
<span data-ttu-id="a6d61-125">Тип конечной точки маршрутизации</span><span class="sxs-lookup"><span data-stu-id="a6d61-125">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="a6d61-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6d61-126">-InputObject</span></span>
<span data-ttu-id="a6d61-127">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="a6d61-127">IotHub Object</span></span>

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

### <span data-ttu-id="a6d61-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a6d61-128">-Name</span></span>
<span data-ttu-id="a6d61-129">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="a6d61-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a6d61-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6d61-130">-ResourceGroupName</span></span>
<span data-ttu-id="a6d61-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a6d61-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a6d61-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6d61-132">-ResourceId</span></span>
<span data-ttu-id="a6d61-133">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="a6d61-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a6d61-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d61-134">CommonParameters</span></span>
<span data-ttu-id="a6d61-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6d61-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d61-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6d61-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d61-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6d61-137">INPUTS</span></span>

### <span data-ttu-id="a6d61-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a6d61-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="a6d61-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a6d61-139">System.String</span></span>

## <span data-ttu-id="a6d61-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6d61-140">OUTPUTS</span></span>

### <span data-ttu-id="a6d61-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6d61-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="a6d61-142">System. Collections. Generic. List `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. System. Management. IotHub. Models. PSRoutingServiceBusQueueEndpointProperties, Microsoft. Azure., PublicKeyToken = NULL]] Microsoft. Azure. Commands. Management. IotHub. Models. IotHub System. коллекций. Generic. List `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = Neutral, PublicKeyToken = NULL]] System. Collections. Generic. List "1 [[Microsoft. Azure. System. Management. IotHub... Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="a6d61-142">System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a6d61-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6d61-143">NOTES</span></span>

## <span data-ttu-id="a6d61-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6d61-144">RELATED LINKS</span></span>
