---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitstats
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
ms.openlocfilehash: d9978c50186b520d8e956dc20581d1ceb615b673
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734625"
---
# <span data-ttu-id="dcacc-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="dcacc-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="dcacc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dcacc-102">SYNOPSIS</span></span>
<span data-ttu-id="dcacc-103">Возвращает статистику использования канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dcacc-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcacc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dcacc-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcacc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcacc-105">DESCRIPTION</span></span>
<span data-ttu-id="dcacc-106">Командлет **Get-AzureRmExpressRouteCircuitStats** извлекает статистику трафика для канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dcacc-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="dcacc-107">Статистика включает количество байтов, отправленных и полученных по основным и дополнительным маршрутам.</span><span class="sxs-lookup"><span data-stu-id="dcacc-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="dcacc-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dcacc-108">EXAMPLES</span></span>

### <span data-ttu-id="dcacc-109">Пример 1: отображение статистики трафика для однорангового узла ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="dcacc-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="dcacc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dcacc-110">PARAMETERS</span></span>

### <span data-ttu-id="dcacc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcacc-111">-DefaultProfile</span></span>
<span data-ttu-id="dcacc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dcacc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcacc-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="dcacc-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="dcacc-114">Имя проверяемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dcacc-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="dcacc-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="dcacc-115">-PeeringType</span></span>
<span data-ttu-id="dcacc-116">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="dcacc-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcacc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcacc-117">-ResourceGroupName</span></span>
<span data-ttu-id="dcacc-118">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dcacc-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="dcacc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcacc-119">CommonParameters</span></span>
<span data-ttu-id="dcacc-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dcacc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcacc-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcacc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcacc-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dcacc-122">INPUTS</span></span>

### <span data-ttu-id="dcacc-123">System. String</span><span class="sxs-lookup"><span data-stu-id="dcacc-123">System.String</span></span>

## <span data-ttu-id="dcacc-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcacc-124">OUTPUTS</span></span>

### <span data-ttu-id="dcacc-125">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="dcacc-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="dcacc-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="dcacc-126">NOTES</span></span>

## <span data-ttu-id="dcacc-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcacc-127">RELATED LINKS</span></span>

[<span data-ttu-id="dcacc-128">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="dcacc-128">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="dcacc-129">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="dcacc-129">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="dcacc-130">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="dcacc-130">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)
