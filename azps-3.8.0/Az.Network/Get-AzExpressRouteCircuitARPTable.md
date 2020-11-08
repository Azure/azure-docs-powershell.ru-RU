---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 12c920d0bacc6bd214e6ebe8d374a80d2b50a072
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065851"
---
# <span data-ttu-id="f769c-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f769c-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="f769c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f769c-102">SYNOPSIS</span></span>
<span data-ttu-id="f769c-103">Возвращает таблицу ARP из канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f769c-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f769c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f769c-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f769c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f769c-105">DESCRIPTION</span></span>
<span data-ttu-id="f769c-106">Командлет **Get-AzExpressRouteCircuitARPTable** ИЗВЛЕКАЕТ таблицу ARP из обоих интерфейсов канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f769c-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="f769c-107">Таблица ARP обеспечивает сопоставление адреса IPv4 и MAC-адресу для определенного пиринга.</span><span class="sxs-lookup"><span data-stu-id="f769c-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="f769c-108">Вы можете использовать таблицу ARP для проверки конфигурации уровня 2 и подключения.</span><span class="sxs-lookup"><span data-stu-id="f769c-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="f769c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f769c-109">EXAMPLES</span></span>

### <span data-ttu-id="f769c-110">Пример 1: отображение таблицы ARP для однорангового узла ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f769c-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="f769c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f769c-111">PARAMETERS</span></span>

### <span data-ttu-id="f769c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f769c-112">-DefaultProfile</span></span>
<span data-ttu-id="f769c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f769c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f769c-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="f769c-114">-DevicePath</span></span>
<span data-ttu-id="f769c-115">Допустимые значения этого параметра: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="f769c-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="f769c-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="f769c-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="f769c-117">Имя проверяемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f769c-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="f769c-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="f769c-118">-PeeringType</span></span>
<span data-ttu-id="f769c-119">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="f769c-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="f769c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f769c-120">-ResourceGroupName</span></span>
<span data-ttu-id="f769c-121">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f769c-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="f769c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f769c-122">CommonParameters</span></span>
<span data-ttu-id="f769c-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f769c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f769c-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f769c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f769c-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f769c-125">INPUTS</span></span>

### <span data-ttu-id="f769c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f769c-126">System.String</span></span>

## <span data-ttu-id="f769c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f769c-127">OUTPUTS</span></span>

### <span data-ttu-id="f769c-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="f769c-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="f769c-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="f769c-129">NOTES</span></span>

## <span data-ttu-id="f769c-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f769c-130">RELATED LINKS</span></span>

[<span data-ttu-id="f769c-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f769c-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="f769c-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f769c-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="f769c-133">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="f769c-133">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
