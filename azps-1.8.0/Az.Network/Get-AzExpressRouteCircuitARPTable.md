---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: ce1e05106350adda37ffa5877585ff37337dad87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730603"
---
# <span data-ttu-id="24c6e-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="24c6e-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="24c6e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24c6e-102">SYNOPSIS</span></span>
<span data-ttu-id="24c6e-103">Возвращает таблицу ARP из канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="24c6e-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="24c6e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24c6e-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24c6e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24c6e-105">DESCRIPTION</span></span>
<span data-ttu-id="24c6e-106">Командлет **Get-AzExpressRouteCircuitARPTable** ИЗВЛЕКАЕТ таблицу ARP из обоих интерфейсов канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="24c6e-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="24c6e-107">Таблица ARP обеспечивает сопоставление адреса IPv4 и MAC-адресу для определенного пиринга.</span><span class="sxs-lookup"><span data-stu-id="24c6e-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="24c6e-108">Вы можете использовать таблицу ARP для проверки конфигурации уровня 2 и подключения.</span><span class="sxs-lookup"><span data-stu-id="24c6e-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="24c6e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24c6e-109">EXAMPLES</span></span>

### <span data-ttu-id="24c6e-110">Пример 1: отображение таблицы ARP для однорангового узла ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="24c6e-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="24c6e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24c6e-111">PARAMETERS</span></span>

### <span data-ttu-id="24c6e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c6e-112">-DefaultProfile</span></span>
<span data-ttu-id="24c6e-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24c6e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24c6e-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="24c6e-114">-DevicePath</span></span>
<span data-ttu-id="24c6e-115">Допустимые значения этого параметра: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="24c6e-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="24c6e-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="24c6e-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="24c6e-117">Имя проверяемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="24c6e-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="24c6e-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="24c6e-118">-PeeringType</span></span>
<span data-ttu-id="24c6e-119">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="24c6e-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="24c6e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24c6e-120">-ResourceGroupName</span></span>
<span data-ttu-id="24c6e-121">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="24c6e-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="24c6e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c6e-122">CommonParameters</span></span>
<span data-ttu-id="24c6e-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24c6e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c6e-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24c6e-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c6e-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24c6e-125">INPUTS</span></span>

### <span data-ttu-id="24c6e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="24c6e-126">System.String</span></span>

## <span data-ttu-id="24c6e-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24c6e-127">OUTPUTS</span></span>

### <span data-ttu-id="24c6e-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="24c6e-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="24c6e-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="24c6e-129">NOTES</span></span>

## <span data-ttu-id="24c6e-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24c6e-130">RELATED LINKS</span></span>

[<span data-ttu-id="24c6e-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="24c6e-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="24c6e-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="24c6e-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="24c6e-133">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="24c6e-133">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
