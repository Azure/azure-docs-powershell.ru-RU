---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: f162bf5f22ab435dd0d340bfd96db1ae616ccc96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219689"
---
# <span data-ttu-id="4f922-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f922-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="4f922-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f922-102">SYNOPSIS</span></span>
<span data-ttu-id="4f922-103">Удаление конечной точки для концентратора IoT</span><span class="sxs-lookup"><span data-stu-id="4f922-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="4f922-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4f922-104">SYNTAX</span></span>

### <span data-ttu-id="4f922-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4f922-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f922-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4f922-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f922-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4f922-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f922-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f922-108">DESCRIPTION</span></span>
<span data-ttu-id="4f922-109">Удаление конечной точки.</span><span class="sxs-lookup"><span data-stu-id="4f922-109">Delete an endpoint.</span></span> <span data-ttu-id="4f922-110">Не забудьте удалить все маршруты, которые используют эту конечную точку.</span><span class="sxs-lookup"><span data-stu-id="4f922-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="4f922-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4f922-111">EXAMPLES</span></span>

### <span data-ttu-id="4f922-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4f922-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="4f922-113">Удалите конечную точку E2 из концентратора IoT myiothub.</span><span class="sxs-lookup"><span data-stu-id="4f922-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="4f922-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f922-114">PARAMETERS</span></span>

### <span data-ttu-id="4f922-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f922-115">-DefaultProfile</span></span>
<span data-ttu-id="4f922-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4f922-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f922-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4f922-117">-EndpointName</span></span>
<span data-ttu-id="4f922-118">Имя конечной точки маршрутинга</span><span class="sxs-lookup"><span data-stu-id="4f922-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="4f922-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="4f922-119">-EndpointType</span></span>
<span data-ttu-id="4f922-120">Тип конечной точки маршрутинга</span><span class="sxs-lookup"><span data-stu-id="4f922-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="4f922-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f922-121">-InputObject</span></span>
<span data-ttu-id="4f922-122">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="4f922-122">IotHub Object</span></span>

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

### <span data-ttu-id="4f922-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4f922-123">-Name</span></span>
<span data-ttu-id="4f922-124">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="4f922-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4f922-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f922-125">-PassThru</span></span>
<span data-ttu-id="4f922-126">Возвращает объект boolean.</span><span class="sxs-lookup"><span data-stu-id="4f922-126">Allows to return the boolean object.</span></span> <span data-ttu-id="4f922-127">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4f922-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4f922-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f922-128">-ResourceGroupName</span></span>
<span data-ttu-id="4f922-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4f922-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4f922-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f922-130">-ResourceId</span></span>
<span data-ttu-id="4f922-131">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="4f922-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4f922-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f922-132">-Confirm</span></span>
<span data-ttu-id="4f922-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f922-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f922-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f922-134">-WhatIf</span></span>
<span data-ttu-id="4f922-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f922-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f922-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4f922-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f922-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f922-137">CommonParameters</span></span>
<span data-ttu-id="4f922-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f922-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f922-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f922-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f922-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f922-140">INPUTS</span></span>

### <span data-ttu-id="4f922-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4f922-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4f922-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4f922-142">System.String</span></span>

## <span data-ttu-id="4f922-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4f922-143">OUTPUTS</span></span>

### <span data-ttu-id="4f922-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4f922-144">System.Boolean</span></span>

## <span data-ttu-id="4f922-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4f922-145">NOTES</span></span>

## <span data-ttu-id="4f922-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f922-146">RELATED LINKS</span></span>
