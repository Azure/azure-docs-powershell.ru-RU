---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: d251d3159111437cd06880a49069aee7aca6d80f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563003"
---
# <span data-ttu-id="66655-101">Add-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="66655-101">Add-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="66655-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="66655-102">SYNOPSIS</span></span>
<span data-ttu-id="66655-103">Добавление конечной точки в центр Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="66655-103">Add an endpoint to your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66655-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="66655-104">SYNTAX</span></span>

### <span data-ttu-id="66655-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="66655-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66655-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="66655-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66655-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="66655-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66655-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66655-108">DESCRIPTION</span></span>
<span data-ttu-id="66655-109">Добавьте новую конечную точку в центр Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="66655-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="66655-110">Чтобы узнать, какие конечные точки поддерживаются, ознакомьтесь со статьей https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="66655-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="66655-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="66655-111">EXAMPLES</span></span>

### <span data-ttu-id="66655-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="66655-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="66655-113">Добавьте новую конечную точку E2 для типа EventHub в центр Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="66655-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="66655-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="66655-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : avro
```

<span data-ttu-id="66655-115">Добавьте новую конечную точку S1 для типа AzureStorageContainer в центр Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="66655-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="66655-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="66655-116">PARAMETERS</span></span>

### <span data-ttu-id="66655-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="66655-117">-ConnectionString</span></span>
<span data-ttu-id="66655-118">Строка подключения конечной точки маршрутизации</span><span class="sxs-lookup"><span data-stu-id="66655-118">Connection string of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66655-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66655-119">-DefaultProfile</span></span>
<span data-ttu-id="66655-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66655-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66655-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="66655-121">-EndpointName</span></span>
<span data-ttu-id="66655-122">Имя конечной точки маршрутизации</span><span class="sxs-lookup"><span data-stu-id="66655-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="66655-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66655-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="66655-124">Группа ресурсов для конечной точки изображение</span><span class="sxs-lookup"><span data-stu-id="66655-124">Resource group of the Endpoint resoure</span></span>

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

### <span data-ttu-id="66655-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="66655-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="66655-126">Идентификатор подписки ресурса конечной точки</span><span class="sxs-lookup"><span data-stu-id="66655-126">SubscriptionId of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66655-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="66655-127">-EndpointType</span></span>
<span data-ttu-id="66655-128">Тип конечной точки маршрутизации</span><span class="sxs-lookup"><span data-stu-id="66655-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66655-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66655-129">-InputObject</span></span>
<span data-ttu-id="66655-130">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="66655-130">IotHub Object</span></span>

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

### <span data-ttu-id="66655-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="66655-131">-Name</span></span>
<span data-ttu-id="66655-132">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="66655-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="66655-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66655-133">-ResourceGroupName</span></span>
<span data-ttu-id="66655-134">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="66655-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="66655-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66655-135">-ResourceId</span></span>
<span data-ttu-id="66655-136">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="66655-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="66655-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66655-137">-Confirm</span></span>
<span data-ttu-id="66655-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="66655-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66655-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66655-139">-WhatIf</span></span>
<span data-ttu-id="66655-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="66655-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66655-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="66655-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66655-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66655-142">CommonParameters</span></span>
<span data-ttu-id="66655-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="66655-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66655-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66655-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66655-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="66655-145">INPUTS</span></span>

### <span data-ttu-id="66655-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="66655-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="66655-147">System. String</span><span class="sxs-lookup"><span data-stu-id="66655-147">System.String</span></span>

## <span data-ttu-id="66655-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="66655-148">OUTPUTS</span></span>

### <span data-ttu-id="66655-149">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="66655-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="66655-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpoint Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="66655-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="66655-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="66655-151">NOTES</span></span>

## <span data-ttu-id="66655-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66655-152">RELATED LINKS</span></span>
