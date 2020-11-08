---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 1c59ef12964ddd022add01ae296b8ecac9ad0acd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249869"
---
# <span data-ttu-id="a4ca3-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a4ca3-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="a4ca3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ca3-103">Возвращает таблицу ARP из канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a4ca3-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a4ca3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4ca3-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4ca3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4ca3-105">DESCRIPTION</span></span>
<span data-ttu-id="a4ca3-106">Командлет **Get-AzExpressRouteCircuitARPTable** ИЗВЛЕКАЕТ таблицу ARP из обоих интерфейсов канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a4ca3-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="a4ca3-107">Таблица ARP обеспечивает сопоставление адреса IPv4 и MAC-адресу для определенного пиринга.</span><span class="sxs-lookup"><span data-stu-id="a4ca3-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="a4ca3-108">Вы можете использовать таблицу ARP для проверки конфигурации уровня 2 и подключения.</span><span class="sxs-lookup"><span data-stu-id="a4ca3-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="a4ca3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4ca3-109">EXAMPLES</span></span>

### <span data-ttu-id="a4ca3-110">Пример 1: отображение таблицы ARP для однорангового узла ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="a4ca3-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="a4ca3-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4ca3-111">PARAMETERS</span></span>

### <span data-ttu-id="a4ca3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ca3-112">-DefaultProfile</span></span>
<span data-ttu-id="a4ca3-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4ca3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4ca3-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="a4ca3-114">-DevicePath</span></span>
<span data-ttu-id="a4ca3-115">Допустимые значения этого параметра: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="a4ca3-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="a4ca3-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="a4ca3-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="a4ca3-117">Имя проверяемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a4ca3-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="a4ca3-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a4ca3-118">-PeeringType</span></span>
<span data-ttu-id="a4ca3-119">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a4ca3-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="a4ca3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ca3-120">-ResourceGroupName</span></span>
<span data-ttu-id="a4ca3-121">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a4ca3-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="a4ca3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ca3-122">CommonParameters</span></span>
<span data-ttu-id="a4ca3-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4ca3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ca3-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4ca3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ca3-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4ca3-125">INPUTS</span></span>

### <span data-ttu-id="a4ca3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a4ca3-126">System.String</span></span>

## <span data-ttu-id="a4ca3-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4ca3-127">OUTPUTS</span></span>

### <span data-ttu-id="a4ca3-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="a4ca3-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="a4ca3-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4ca3-129">NOTES</span></span>

## <span data-ttu-id="a4ca3-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4ca3-130">RELATED LINKS</span></span>

[<span data-ttu-id="a4ca3-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a4ca3-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="a4ca3-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a4ca3-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="a4ca3-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="a4ca3-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
