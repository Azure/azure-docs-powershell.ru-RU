---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: 6caad4faec3dd292f902689757b82b90091afcde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568530"
---
# <span data-ttu-id="b5a5e-101">Remove-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5a5e-101">Remove-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="b5a5e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a5e-103">Удаление конечной точки для центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="b5a5e-103">Delete an endpoint for your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5a5e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5a5e-104">SYNTAX</span></span>

### <span data-ttu-id="b5a5e-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b5a5e-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5a5e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b5a5e-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5a5e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b5a5e-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5a5e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5a5e-108">DESCRIPTION</span></span>
<span data-ttu-id="b5a5e-109">Удалите конечную точку.</span><span class="sxs-lookup"><span data-stu-id="b5a5e-109">Delete an endpoint.</span></span> <span data-ttu-id="b5a5e-110">Не забудьте удалить все маршруты, которые используют эту конечную точку.</span><span class="sxs-lookup"><span data-stu-id="b5a5e-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="b5a5e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5a5e-111">EXAMPLES</span></span>

### <span data-ttu-id="b5a5e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b5a5e-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="b5a5e-113">Удаление конечной точки "E2" из центра Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="b5a5e-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="b5a5e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5a5e-114">PARAMETERS</span></span>

### <span data-ttu-id="b5a5e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a5e-115">-DefaultProfile</span></span>
<span data-ttu-id="b5a5e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5a5e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5a5e-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b5a5e-117">-EndpointName</span></span>
<span data-ttu-id="b5a5e-118">Имя конечной точки маршрутизации</span><span class="sxs-lookup"><span data-stu-id="b5a5e-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="b5a5e-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="b5a5e-119">-EndpointType</span></span>
<span data-ttu-id="b5a5e-120">Тип конечной точки маршрутизации</span><span class="sxs-lookup"><span data-stu-id="b5a5e-120">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a5e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5a5e-121">-InputObject</span></span>
<span data-ttu-id="b5a5e-122">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="b5a5e-122">IotHub Object</span></span>

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

### <span data-ttu-id="b5a5e-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b5a5e-123">-Name</span></span>
<span data-ttu-id="b5a5e-124">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="b5a5e-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b5a5e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5a5e-125">-PassThru</span></span>
<span data-ttu-id="b5a5e-126">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="b5a5e-126">Allows to return the boolean object.</span></span> <span data-ttu-id="b5a5e-127">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b5a5e-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b5a5e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5a5e-128">-ResourceGroupName</span></span>
<span data-ttu-id="b5a5e-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b5a5e-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b5a5e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5a5e-130">-ResourceId</span></span>
<span data-ttu-id="b5a5e-131">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="b5a5e-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b5a5e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5a5e-132">-Confirm</span></span>
<span data-ttu-id="b5a5e-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b5a5e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5a5e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5a5e-134">-WhatIf</span></span>
<span data-ttu-id="b5a5e-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b5a5e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5a5e-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b5a5e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5a5e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a5e-137">CommonParameters</span></span>
<span data-ttu-id="b5a5e-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5a5e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a5e-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5a5e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a5e-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5a5e-140">INPUTS</span></span>

### <span data-ttu-id="b5a5e-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b5a5e-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="b5a5e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b5a5e-142">System.String</span></span>

## <span data-ttu-id="b5a5e-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5a5e-143">OUTPUTS</span></span>

### <span data-ttu-id="b5a5e-144">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5a5e-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="b5a5e-145">System. Collections. Generic. List `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. System. Management. IotHub. Models. PSRoutingServiceBusQueueEndpointProperties, Microsoft. Azure., PublicKeyToken = NULL]] Microsoft. Azure. Commands. Management. IotHub. Models. IotHub System. коллекций. Generic. List `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = Neutral, PublicKeyToken = NULL]] System. Collections. Generic. List "1 [[Microsoft. Azure. System. Management. IotHub... Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="b5a5e-145">System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b5a5e-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5a5e-146">NOTES</span></span>

## <span data-ttu-id="b5a5e-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5a5e-147">RELATED LINKS</span></span>
