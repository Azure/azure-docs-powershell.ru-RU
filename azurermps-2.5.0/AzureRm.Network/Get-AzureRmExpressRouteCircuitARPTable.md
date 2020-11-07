---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitarptable
schema: 2.0.0
ms.openlocfilehash: bdfb86eb53221466beca2566d8ea446072ea33d6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913632"
---
# <span data-ttu-id="b473d-101">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b473d-101">Get-AzureRmExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="b473d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b473d-102">SYNOPSIS</span></span>
<span data-ttu-id="b473d-103">Возвращает таблицу ARP из канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b473d-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b473d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b473d-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b473d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b473d-105">DESCRIPTION</span></span>
<span data-ttu-id="b473d-106">Командлет **Get-AzureRmExpressRouteCircuitARPTable** ИЗВЛЕКАЕТ таблицу ARP из обоих интерфейсов канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b473d-106">The **Get-AzureRmExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="b473d-107">Таблица ARP обеспечивает сопоставление адреса IPv4 и MAC-адресу для определенного пиринга.</span><span class="sxs-lookup"><span data-stu-id="b473d-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="b473d-108">Вы можете использовать таблицу ARP для проверки конфигурации уровня 2 и подключения.</span><span class="sxs-lookup"><span data-stu-id="b473d-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="b473d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b473d-109">EXAMPLES</span></span>

### <span data-ttu-id="b473d-110">Пример 1: отображение таблицы ARP для однорангового узла ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="b473d-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="b473d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b473d-111">PARAMETERS</span></span>

### <span data-ttu-id="b473d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b473d-112">-DefaultProfile</span></span>
<span data-ttu-id="b473d-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b473d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b473d-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="b473d-114">-DevicePath</span></span>
<span data-ttu-id="b473d-115">Допустимые значения этого параметра: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="b473d-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: DevicePathEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b473d-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="b473d-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="b473d-117">Имя проверяемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b473d-117">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b473d-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="b473d-118">-PeeringType</span></span>
<span data-ttu-id="b473d-119">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="b473d-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b473d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b473d-120">-ResourceGroupName</span></span>
<span data-ttu-id="b473d-121">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b473d-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b473d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b473d-122">CommonParameters</span></span>
<span data-ttu-id="b473d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b473d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b473d-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b473d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b473d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b473d-125">INPUTS</span></span>

## <span data-ttu-id="b473d-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b473d-126">OUTPUTS</span></span>

### <span data-ttu-id="b473d-127">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="b473d-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="b473d-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b473d-128">NOTES</span></span>

## <span data-ttu-id="b473d-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b473d-129">RELATED LINKS</span></span>

[<span data-ttu-id="b473d-130">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b473d-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="b473d-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b473d-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="b473d-132">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="b473d-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
