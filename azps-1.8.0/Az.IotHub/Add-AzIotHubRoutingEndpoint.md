---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 1c1c865f37a6cb98fec0cc6b1403f9d9257a6d85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900374"
---
# <span data-ttu-id="dda4d-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="dda4d-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="dda4d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dda4d-102">SYNOPSIS</span></span>
<span data-ttu-id="dda4d-103">Добавление конечной точки в центр Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="dda4d-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="dda4d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dda4d-104">SYNTAX</span></span>

### <span data-ttu-id="dda4d-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dda4d-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dda4d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dda4d-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dda4d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dda4d-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dda4d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dda4d-108">DESCRIPTION</span></span>
<span data-ttu-id="dda4d-109">Добавьте новую конечную точку в центр Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="dda4d-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="dda4d-110">Чтобы узнать, какие конечные точки поддерживаются, ознакомьтесь со статьей https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="dda4d-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="dda4d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dda4d-111">EXAMPLES</span></span>

### <span data-ttu-id="dda4d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dda4d-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="dda4d-113">Добавьте новую конечную точку E2 для типа EventHub в центр Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="dda4d-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="dda4d-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dda4d-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container -Encoding json

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : json
```

<span data-ttu-id="dda4d-115">Добавьте новую конечную точку S1 для типа AzureStorageContainer в центр Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="dda4d-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="dda4d-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dda4d-116">PARAMETERS</span></span>

### <span data-ttu-id="dda4d-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="dda4d-117">-ConnectionString</span></span>
<span data-ttu-id="dda4d-118">Строка подключения конечной точки маршрутизации</span><span class="sxs-lookup"><span data-stu-id="dda4d-118">Connection string of the Routing Endpoint</span></span>

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

### <span data-ttu-id="dda4d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda4d-119">-DefaultProfile</span></span>
<span data-ttu-id="dda4d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dda4d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dda4d-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="dda4d-121">-EndpointName</span></span>
<span data-ttu-id="dda4d-122">Имя конечной точки маршрутизации</span><span class="sxs-lookup"><span data-stu-id="dda4d-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="dda4d-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dda4d-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="dda4d-124">Группа ресурсов для конечной точки изображение</span><span class="sxs-lookup"><span data-stu-id="dda4d-124">Resource group of the Endpoint resoure</span></span>

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

### <span data-ttu-id="dda4d-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dda4d-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="dda4d-126">Идентификатор подписки ресурса конечной точки</span><span class="sxs-lookup"><span data-stu-id="dda4d-126">SubscriptionId of the Endpoint resource</span></span>

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

### <span data-ttu-id="dda4d-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="dda4d-127">-EndpointType</span></span>
<span data-ttu-id="dda4d-128">Тип конечной точки маршрутизации</span><span class="sxs-lookup"><span data-stu-id="dda4d-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda4d-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="dda4d-129">-ContainerName</span></span>
<span data-ttu-id="dda4d-130">Имя контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="dda4d-130">Name of the storage container</span></span>

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

### <span data-ttu-id="dda4d-131">-Encoding</span><span class="sxs-lookup"><span data-stu-id="dda4d-131">-Encoding</span></span>
<span data-ttu-id="dda4d-132">Выберите формат, в котором вы хотите перенаправлять данные.</span><span class="sxs-lookup"><span data-stu-id="dda4d-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="dda4d-133">Вы можете выбрать JSON или AVRO.</span><span class="sxs-lookup"><span data-stu-id="dda4d-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="dda4d-134">По умолчанию выбрано значение AVRO.</span><span class="sxs-lookup"><span data-stu-id="dda4d-134">The default is set to AVRO.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:
Accepted values: JSON, AVRO

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda4d-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dda4d-135">-InputObject</span></span>
<span data-ttu-id="dda4d-136">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="dda4d-136">IotHub Object</span></span>

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

### <span data-ttu-id="dda4d-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dda4d-137">-Name</span></span>
<span data-ttu-id="dda4d-138">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="dda4d-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="dda4d-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda4d-139">-ResourceGroupName</span></span>
<span data-ttu-id="dda4d-140">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="dda4d-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dda4d-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dda4d-141">-ResourceId</span></span>
<span data-ttu-id="dda4d-142">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="dda4d-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="dda4d-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dda4d-143">-Confirm</span></span>
<span data-ttu-id="dda4d-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dda4d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dda4d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dda4d-145">-WhatIf</span></span>
<span data-ttu-id="dda4d-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dda4d-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dda4d-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dda4d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dda4d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda4d-148">CommonParameters</span></span>
<span data-ttu-id="dda4d-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dda4d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda4d-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dda4d-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda4d-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dda4d-151">INPUTS</span></span>

### <span data-ttu-id="dda4d-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dda4d-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="dda4d-153">System. String</span><span class="sxs-lookup"><span data-stu-id="dda4d-153">System.String</span></span>

## <span data-ttu-id="dda4d-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dda4d-154">OUTPUTS</span></span>

### <span data-ttu-id="dda4d-155">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="dda4d-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="dda4d-156">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="dda4d-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="dda4d-157">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="dda4d-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="dda4d-158">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dda4d-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="dda4d-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="dda4d-159">NOTES</span></span>

## <span data-ttu-id="dda4d-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dda4d-160">RELATED LINKS</span></span>
