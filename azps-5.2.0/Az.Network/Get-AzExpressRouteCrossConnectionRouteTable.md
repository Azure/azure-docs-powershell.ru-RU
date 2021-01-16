---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: 4c93528c8cf89d64dd99640ce9eca4668d4093c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390951"
---
# <span data-ttu-id="bc6b3-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="bc6b3-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="bc6b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="bc6b3-103">Получает таблицу маршрутов из перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bc6b3-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="bc6b3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bc6b3-104">SYNTAX</span></span>

### <span data-ttu-id="bc6b3-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="bc6b3-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc6b3-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="bc6b3-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc6b3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc6b3-107">DESCRIPTION</span></span>
<span data-ttu-id="bc6b3-108">Для получения подробной таблицы маршрутов из схемы ExpressRoute извлекается из таблицы маршрутов **Get-AzExpressRouteCrossConnectionRouteTable.**</span><span class="sxs-lookup"><span data-stu-id="bc6b3-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="bc6b3-109">В таблице маршрутов будут отфильтроваться все маршруты или отфильтровать маршруты для определенного типа пиринга.</span><span class="sxs-lookup"><span data-stu-id="bc6b3-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="bc6b3-110">Таблицу маршрутов можно использовать для проверки конфигурации пиринга и подключения.</span><span class="sxs-lookup"><span data-stu-id="bc6b3-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="bc6b3-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bc6b3-111">EXAMPLES</span></span>

### <span data-ttu-id="bc6b3-112">Пример 1. Отображение таблицы маршрутов для основного пути</span><span class="sxs-lookup"><span data-stu-id="bc6b3-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="bc6b3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc6b3-113">PARAMETERS</span></span>

### <span data-ttu-id="bc6b3-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="bc6b3-114">-CrossConnectionName</span></span>
<span data-ttu-id="bc6b3-115">Имя перекрестного подключения Express Route</span><span class="sxs-lookup"><span data-stu-id="bc6b3-115">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc6b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc6b3-116">-DefaultProfile</span></span>
<span data-ttu-id="bc6b3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc6b3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc6b3-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="bc6b3-118">-DevicePath</span></span>
<span data-ttu-id="bc6b3-119">Допустимыми значениями для этого параметра являются: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="bc6b3-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc6b3-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="bc6b3-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="bc6b3-121">Перекрестное подключение Express Route</span><span class="sxs-lookup"><span data-stu-id="bc6b3-121">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc6b3-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="bc6b3-122">-PeeringType</span></span>
<span data-ttu-id="bc6b3-123">Допустимыми значениями для этого параметра являются: `AzurePrivatePeering` `AzurePublicPeering` , и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="bc6b3-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc6b3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc6b3-124">-ResourceGroupName</span></span>
<span data-ttu-id="bc6b3-125">Имя группы ресурсов, содержащей перекрестное подключение ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bc6b3-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc6b3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc6b3-126">CommonParameters</span></span>
<span data-ttu-id="bc6b3-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc6b3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc6b3-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc6b3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc6b3-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc6b3-129">INPUTS</span></span>

### <span data-ttu-id="bc6b3-130">Нет</span><span class="sxs-lookup"><span data-stu-id="bc6b3-130">None</span></span>
<span data-ttu-id="bc6b3-131">Этот cmdlet не принимает входные данные.</span><span class="sxs-lookup"><span data-stu-id="bc6b3-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bc6b3-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bc6b3-132">OUTPUTS</span></span>

### <span data-ttu-id="bc6b3-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="bc6b3-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="bc6b3-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bc6b3-134">NOTES</span></span>

## <span data-ttu-id="bc6b3-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc6b3-135">RELATED LINKS</span></span>

[<span data-ttu-id="bc6b3-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="bc6b3-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="bc6b3-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="bc6b3-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
