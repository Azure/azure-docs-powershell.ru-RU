---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
ms.openlocfilehash: 30addde4594c7b67fd5ba9c1358d64ac206a4531
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235566"
---
# <span data-ttu-id="7e1b5-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="7e1b5-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="7e1b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e1b5-102">SYNOPSIS</span></span>
<span data-ttu-id="7e1b5-103">Возвращает таблицу ARP из перекрестного соединения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7e1b5-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="7e1b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e1b5-104">SYNTAX</span></span>

### <span data-ttu-id="7e1b5-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="7e1b5-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e1b5-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="7e1b5-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e1b5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e1b5-107">DESCRIPTION</span></span>
<span data-ttu-id="7e1b5-108">Командлет **Get-AzExpressRouteCrossConnectionARPTable** ИЗВЛЕКАЕТ таблицу ARP из обоих интерфейсов перекрестного соединения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7e1b5-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="7e1b5-109">Таблица ARP обеспечивает сопоставление адреса IPv4 и MAC-адресу для определенного пиринга.</span><span class="sxs-lookup"><span data-stu-id="7e1b5-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="7e1b5-110">Вы можете использовать таблицу ARP для проверки конфигурации уровня 2 и подключения.</span><span class="sxs-lookup"><span data-stu-id="7e1b5-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="7e1b5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e1b5-111">EXAMPLES</span></span>

### <span data-ttu-id="7e1b5-112">Пример 1: отображение таблицы ARP для однорангового узла ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="7e1b5-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="7e1b5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e1b5-113">PARAMETERS</span></span>

### <span data-ttu-id="7e1b5-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="7e1b5-114">-CrossConnectionName</span></span>
<span data-ttu-id="7e1b5-115">Имя перекрестного соединения Express Route</span><span class="sxs-lookup"><span data-stu-id="7e1b5-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="7e1b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e1b5-116">-DefaultProfile</span></span>
<span data-ttu-id="7e1b5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e1b5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e1b5-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="7e1b5-118">-DevicePath</span></span>
<span data-ttu-id="7e1b5-119">Допустимые значения этого параметра: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="7e1b5-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="7e1b5-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7e1b5-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="7e1b5-121">Перекрестное соединение Express Route</span><span class="sxs-lookup"><span data-stu-id="7e1b5-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="7e1b5-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="7e1b5-122">-PeeringType</span></span>
<span data-ttu-id="7e1b5-123">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="7e1b5-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="7e1b5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e1b5-124">-ResourceGroupName</span></span>
<span data-ttu-id="7e1b5-125">Имя группы ресурсов, содержащей перекрестное соединение ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7e1b5-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="7e1b5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e1b5-126">CommonParameters</span></span>
<span data-ttu-id="7e1b5-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e1b5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e1b5-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e1b5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e1b5-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e1b5-129">INPUTS</span></span>

### <span data-ttu-id="7e1b5-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="7e1b5-130">None</span></span>
<span data-ttu-id="7e1b5-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7e1b5-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e1b5-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e1b5-132">OUTPUTS</span></span>

### <span data-ttu-id="7e1b5-133">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="7e1b5-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="7e1b5-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e1b5-134">NOTES</span></span>

## <span data-ttu-id="7e1b5-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e1b5-135">RELATED LINKS</span></span>

[<span data-ttu-id="7e1b5-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="7e1b5-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="7e1b5-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7e1b5-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)