---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
ms.openlocfilehash: e007f220b827db144a4c10b1adb5732e110ddf0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565488"
---
# <span data-ttu-id="2be18-101">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="2be18-101">Get-AzureRmExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="2be18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2be18-102">SYNOPSIS</span></span>
<span data-ttu-id="2be18-103">Возвращает таблицу ARP из канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2be18-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2be18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2be18-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2be18-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2be18-105">DESCRIPTION</span></span>
<span data-ttu-id="2be18-106">Командлет **Get-AzureRmExpressRouteCircuitARPTable** ИЗВЛЕКАЕТ таблицу ARP из обоих интерфейсов канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2be18-106">The **Get-AzureRmExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="2be18-107">Таблица ARP обеспечивает сопоставление адреса IPv4 и MAC-адресу для определенного пиринга.</span><span class="sxs-lookup"><span data-stu-id="2be18-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="2be18-108">Вы можете использовать таблицу ARP для проверки конфигурации уровня 2 и подключения.</span><span class="sxs-lookup"><span data-stu-id="2be18-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="2be18-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2be18-109">EXAMPLES</span></span>

### <span data-ttu-id="2be18-110">Пример 1: отображение таблицы ARP для однорангового узла ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="2be18-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="2be18-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2be18-111">PARAMETERS</span></span>

### <span data-ttu-id="2be18-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be18-112">-DefaultProfile</span></span>
<span data-ttu-id="2be18-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2be18-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2be18-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="2be18-114">-DevicePath</span></span>
<span data-ttu-id="2be18-115">Допустимые значения этого параметра: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="2be18-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="2be18-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="2be18-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="2be18-117">Имя проверяемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2be18-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="2be18-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="2be18-118">-PeeringType</span></span>
<span data-ttu-id="2be18-119">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="2be18-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="2be18-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2be18-120">-ResourceGroupName</span></span>
<span data-ttu-id="2be18-121">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2be18-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="2be18-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be18-122">CommonParameters</span></span>
<span data-ttu-id="2be18-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2be18-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2be18-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2be18-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be18-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2be18-125">INPUTS</span></span>

### <span data-ttu-id="2be18-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="2be18-126">None</span></span>
<span data-ttu-id="2be18-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2be18-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2be18-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2be18-128">OUTPUTS</span></span>

### <span data-ttu-id="2be18-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="2be18-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="2be18-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2be18-130">NOTES</span></span>

## <span data-ttu-id="2be18-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2be18-131">RELATED LINKS</span></span>

[<span data-ttu-id="2be18-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="2be18-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="2be18-133">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2be18-133">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="2be18-134">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="2be18-134">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
