---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 43bf5a0a551840d03ac19e9ea78b26135dde5493
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910022"
---
# <span data-ttu-id="443d2-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="443d2-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="443d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="443d2-102">SYNOPSIS</span></span>
<span data-ttu-id="443d2-103">Возвращает таблицу ARP из канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="443d2-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="443d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="443d2-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="443d2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="443d2-105">DESCRIPTION</span></span>
<span data-ttu-id="443d2-106">Командлет **Get-AzExpressRouteCircuitARPTable** ИЗВЛЕКАЕТ таблицу ARP из обоих интерфейсов канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="443d2-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="443d2-107">Таблица ARP обеспечивает сопоставление адреса IPv4 и MAC-адресу для определенного пиринга.</span><span class="sxs-lookup"><span data-stu-id="443d2-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="443d2-108">Вы можете использовать таблицу ARP для проверки конфигурации уровня 2 и подключения.</span><span class="sxs-lookup"><span data-stu-id="443d2-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="443d2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="443d2-109">EXAMPLES</span></span>

### <span data-ttu-id="443d2-110">Пример 1: отображение таблицы ARP для однорангового узла ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="443d2-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="443d2-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="443d2-111">PARAMETERS</span></span>

### <span data-ttu-id="443d2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="443d2-112">-DefaultProfile</span></span>
<span data-ttu-id="443d2-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="443d2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="443d2-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="443d2-114">-DevicePath</span></span>
<span data-ttu-id="443d2-115">Допустимые значения этого параметра: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="443d2-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="443d2-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="443d2-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="443d2-117">Имя проверяемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="443d2-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="443d2-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="443d2-118">-PeeringType</span></span>
<span data-ttu-id="443d2-119">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="443d2-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="443d2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="443d2-120">-ResourceGroupName</span></span>
<span data-ttu-id="443d2-121">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="443d2-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="443d2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="443d2-122">CommonParameters</span></span>
<span data-ttu-id="443d2-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="443d2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="443d2-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="443d2-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="443d2-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="443d2-125">INPUTS</span></span>

## <span data-ttu-id="443d2-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="443d2-126">OUTPUTS</span></span>

### <span data-ttu-id="443d2-127">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="443d2-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="443d2-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="443d2-128">NOTES</span></span>

## <span data-ttu-id="443d2-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="443d2-129">RELATED LINKS</span></span>

[<span data-ttu-id="443d2-130">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="443d2-130">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="443d2-131">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="443d2-131">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="443d2-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="443d2-132">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
