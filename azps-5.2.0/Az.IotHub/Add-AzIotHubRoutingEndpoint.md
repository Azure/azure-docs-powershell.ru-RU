---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 2af7a4518d551509089585877f74468510746dcd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402292"
---
# <span data-ttu-id="981ee-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="981ee-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="981ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="981ee-102">SYNOPSIS</span></span>
<span data-ttu-id="981ee-103">Добавление конечной точки в концентратор IoT</span><span class="sxs-lookup"><span data-stu-id="981ee-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="981ee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="981ee-104">SYNTAX</span></span>

### <span data-ttu-id="981ee-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="981ee-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="981ee-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="981ee-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="981ee-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="981ee-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="981ee-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="981ee-108">DESCRIPTION</span></span>
<span data-ttu-id="981ee-109">Добавьте новую конечную точку в концентраторЕ IoT.</span><span class="sxs-lookup"><span data-stu-id="981ee-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="981ee-110">Чтобы узнать о поддерживаемых конечных точках, см. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="981ee-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="981ee-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="981ee-111">EXAMPLES</span></span>

### <span data-ttu-id="981ee-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="981ee-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="981ee-113">Добавьте новую конечную точку E2 типа EventHub в центр IoT myiothub.</span><span class="sxs-lookup"><span data-stu-id="981ee-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="981ee-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="981ee-114">Example 2</span></span>
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

<span data-ttu-id="981ee-115">Добавьте новую конечную точку "S1" типа AzureStorageContainer в концентратор IoT myiothub.</span><span class="sxs-lookup"><span data-stu-id="981ee-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="981ee-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="981ee-116">PARAMETERS</span></span>

### <span data-ttu-id="981ee-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="981ee-117">-ConnectionString</span></span>
<span data-ttu-id="981ee-118">Строка подключения конечной точки маршрутки</span><span class="sxs-lookup"><span data-stu-id="981ee-118">Connection string of the Routing Endpoint</span></span>

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

### <span data-ttu-id="981ee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="981ee-119">-DefaultProfile</span></span>
<span data-ttu-id="981ee-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="981ee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="981ee-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="981ee-121">-EndpointName</span></span>
<span data-ttu-id="981ee-122">Имя конечной точки маршрутинга</span><span class="sxs-lookup"><span data-stu-id="981ee-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="981ee-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="981ee-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="981ee-124">Группа ресурсов ресурса конечной точки</span><span class="sxs-lookup"><span data-stu-id="981ee-124">Resource group of the Endpoint resource</span></span>

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

### <span data-ttu-id="981ee-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="981ee-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="981ee-126">SubscriptionId ресурса конечной точки</span><span class="sxs-lookup"><span data-stu-id="981ee-126">SubscriptionId of the Endpoint resource</span></span>

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

### <span data-ttu-id="981ee-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="981ee-127">-EndpointType</span></span>
<span data-ttu-id="981ee-128">Тип конечной точки маршрутинга</span><span class="sxs-lookup"><span data-stu-id="981ee-128">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="981ee-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="981ee-129">-ContainerName</span></span>
<span data-ttu-id="981ee-130">Имя контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="981ee-130">Name of the storage container</span></span>

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

### <span data-ttu-id="981ee-131">-Кодировидная кодировидная</span><span class="sxs-lookup"><span data-stu-id="981ee-131">-Encoding</span></span>
<span data-ttu-id="981ee-132">Выберите формат, в котором вы хотите перена маршрутить данные.</span><span class="sxs-lookup"><span data-stu-id="981ee-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="981ee-133">Вы можете выбрать JSON или AVRO.</span><span class="sxs-lookup"><span data-stu-id="981ee-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="981ee-134">По умолчанию установлено значение AVRO.</span><span class="sxs-lookup"><span data-stu-id="981ee-134">The default is set to AVRO.</span></span>

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

### <span data-ttu-id="981ee-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="981ee-135">-InputObject</span></span>
<span data-ttu-id="981ee-136">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="981ee-136">IotHub Object</span></span>

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

### <span data-ttu-id="981ee-137">-Name</span><span class="sxs-lookup"><span data-stu-id="981ee-137">-Name</span></span>
<span data-ttu-id="981ee-138">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="981ee-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="981ee-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="981ee-139">-ResourceGroupName</span></span>
<span data-ttu-id="981ee-140">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="981ee-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="981ee-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="981ee-141">-ResourceId</span></span>
<span data-ttu-id="981ee-142">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="981ee-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="981ee-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="981ee-143">-Confirm</span></span>
<span data-ttu-id="981ee-144">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="981ee-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="981ee-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="981ee-145">-WhatIf</span></span>
<span data-ttu-id="981ee-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="981ee-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="981ee-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="981ee-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="981ee-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="981ee-148">CommonParameters</span></span>
<span data-ttu-id="981ee-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="981ee-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="981ee-150">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="981ee-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="981ee-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="981ee-151">INPUTS</span></span>

### <span data-ttu-id="981ee-152">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="981ee-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="981ee-153">System.String</span><span class="sxs-lookup"><span data-stu-id="981ee-153">System.String</span></span>

## <span data-ttu-id="981ee-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="981ee-154">OUTPUTS</span></span>

### <span data-ttu-id="981ee-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="981ee-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="981ee-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="981ee-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="981ee-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="981ee-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="981ee-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="981ee-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="981ee-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="981ee-159">NOTES</span></span>

## <span data-ttu-id="981ee-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="981ee-160">RELATED LINKS</span></span>
