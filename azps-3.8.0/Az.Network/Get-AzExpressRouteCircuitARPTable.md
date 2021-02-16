---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 4b3f7e455d11696ca92ae8a2e8b530dc8d875123
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408276"
---
# <span data-ttu-id="d26d8-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d26d8-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="d26d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d26d8-102">SYNOPSIS</span></span>
<span data-ttu-id="d26d8-103">Возвращает таблицу ARP из каналов ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d26d8-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="d26d8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d26d8-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d26d8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d26d8-105">DESCRIPTION</span></span>
<span data-ttu-id="d26d8-106">Cmdlet **Get-AzExpressRouteCircuitARPTable** извлекает таблицу ARP из обоих интерфейсов каналов ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d26d8-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="d26d8-107">Таблица "ARP" содержит сопоставление IPv4-адреса с MAC-адресом для определенного пиринга.</span><span class="sxs-lookup"><span data-stu-id="d26d8-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="d26d8-108">Таблицу ARP можно использовать для проверки конфигурации и подключения уровня 2.</span><span class="sxs-lookup"><span data-stu-id="d26d8-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="d26d8-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d26d8-109">EXAMPLES</span></span>

### <span data-ttu-id="d26d8-110">Пример 1. Отображение таблицы ARP для одноранговой сети ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="d26d8-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="d26d8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d26d8-111">PARAMETERS</span></span>

### <span data-ttu-id="d26d8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d26d8-112">-DefaultProfile</span></span>
<span data-ttu-id="d26d8-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d26d8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d26d8-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="d26d8-114">-DevicePath</span></span>
<span data-ttu-id="d26d8-115">Допустимыми значениями для этого параметра являются: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="d26d8-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="d26d8-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="d26d8-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="d26d8-117">Имя проверяемого контура ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d26d8-117">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d26d8-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="d26d8-118">-PeeringType</span></span>
<span data-ttu-id="d26d8-119">Допустимыми значениями для этого параметра являются: `AzurePrivatePeering` `AzurePublicPeering` , и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="d26d8-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="d26d8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d26d8-120">-ResourceGroupName</span></span>
<span data-ttu-id="d26d8-121">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d26d8-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d26d8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d26d8-122">CommonParameters</span></span>
<span data-ttu-id="d26d8-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d26d8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d26d8-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d26d8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d26d8-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d26d8-125">INPUTS</span></span>

### <span data-ttu-id="d26d8-126">System.String</span><span class="sxs-lookup"><span data-stu-id="d26d8-126">System.String</span></span>

## <span data-ttu-id="d26d8-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d26d8-127">OUTPUTS</span></span>

### <span data-ttu-id="d26d8-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="d26d8-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="d26d8-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d26d8-129">NOTES</span></span>

## <span data-ttu-id="d26d8-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d26d8-130">RELATED LINKS</span></span>

[<span data-ttu-id="d26d8-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d26d8-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="d26d8-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d26d8-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="d26d8-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="d26d8-133">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
