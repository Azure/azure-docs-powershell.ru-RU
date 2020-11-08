---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: f162bf5f22ab435dd0d340bfd96db1ae616ccc96
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065886"
---
# <span data-ttu-id="a98af-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="a98af-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="a98af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a98af-102">SYNOPSIS</span></span>
<span data-ttu-id="a98af-103">Удаление конечной точки для центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="a98af-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="a98af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a98af-104">SYNTAX</span></span>

### <span data-ttu-id="a98af-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a98af-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a98af-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a98af-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a98af-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a98af-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a98af-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a98af-108">DESCRIPTION</span></span>
<span data-ttu-id="a98af-109">Удалите конечную точку.</span><span class="sxs-lookup"><span data-stu-id="a98af-109">Delete an endpoint.</span></span> <span data-ttu-id="a98af-110">Не забудьте удалить все маршруты, которые используют эту конечную точку.</span><span class="sxs-lookup"><span data-stu-id="a98af-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="a98af-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a98af-111">EXAMPLES</span></span>

### <span data-ttu-id="a98af-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a98af-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="a98af-113">Удаление конечной точки "E2" из центра Интернета вещей "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a98af-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="a98af-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a98af-114">PARAMETERS</span></span>

### <span data-ttu-id="a98af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a98af-115">-DefaultProfile</span></span>
<span data-ttu-id="a98af-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a98af-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a98af-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a98af-117">-EndpointName</span></span>
<span data-ttu-id="a98af-118">Имя конечной точки маршрутизации</span><span class="sxs-lookup"><span data-stu-id="a98af-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="a98af-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="a98af-119">-EndpointType</span></span>
<span data-ttu-id="a98af-120">Тип конечной точки маршрутизации</span><span class="sxs-lookup"><span data-stu-id="a98af-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="a98af-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a98af-121">-InputObject</span></span>
<span data-ttu-id="a98af-122">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="a98af-122">IotHub Object</span></span>

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

### <span data-ttu-id="a98af-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a98af-123">-Name</span></span>
<span data-ttu-id="a98af-124">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="a98af-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a98af-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a98af-125">-PassThru</span></span>
<span data-ttu-id="a98af-126">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="a98af-126">Allows to return the boolean object.</span></span> <span data-ttu-id="a98af-127">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a98af-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a98af-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a98af-128">-ResourceGroupName</span></span>
<span data-ttu-id="a98af-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a98af-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a98af-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a98af-130">-ResourceId</span></span>
<span data-ttu-id="a98af-131">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="a98af-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a98af-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a98af-132">-Confirm</span></span>
<span data-ttu-id="a98af-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a98af-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a98af-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a98af-134">-WhatIf</span></span>
<span data-ttu-id="a98af-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a98af-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a98af-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a98af-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a98af-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a98af-137">CommonParameters</span></span>
<span data-ttu-id="a98af-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a98af-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a98af-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a98af-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a98af-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a98af-140">INPUTS</span></span>

### <span data-ttu-id="a98af-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a98af-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a98af-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a98af-142">System.String</span></span>

## <span data-ttu-id="a98af-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a98af-143">OUTPUTS</span></span>

### <span data-ttu-id="a98af-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a98af-144">System.Boolean</span></span>

## <span data-ttu-id="a98af-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="a98af-145">NOTES</span></span>

## <span data-ttu-id="a98af-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a98af-146">RELATED LINKS</span></span>
