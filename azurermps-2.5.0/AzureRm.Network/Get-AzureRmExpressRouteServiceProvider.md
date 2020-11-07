---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
ms.openlocfilehash: 7e4febe620b8a440d1f9a5eb0c9432da9ff47c74
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913834"
---
# <span data-ttu-id="90384-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="90384-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="90384-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90384-102">SYNOPSIS</span></span>
<span data-ttu-id="90384-103">Получает список поставщиков услуг ExpressRoute и их атрибутов.</span><span class="sxs-lookup"><span data-stu-id="90384-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90384-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90384-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90384-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90384-105">DESCRIPTION</span></span>
<span data-ttu-id="90384-106">Командлет **Get-AzureRmExpressRouteServiceProvider** извлекает список поставщиков служб ExpressRoute и их атрибуты.</span><span class="sxs-lookup"><span data-stu-id="90384-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="90384-107">Атрибут: расположение и параметры пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="90384-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="90384-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90384-108">EXAMPLES</span></span>

### <span data-ttu-id="90384-109">Пример 1: получение списка поставщика услуг с разположениями в «Silicon впадина»</span><span class="sxs-lookup"><span data-stu-id="90384-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="90384-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90384-110">PARAMETERS</span></span>

### <span data-ttu-id="90384-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90384-111">-DefaultProfile</span></span>
<span data-ttu-id="90384-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90384-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90384-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90384-113">CommonParameters</span></span>
<span data-ttu-id="90384-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90384-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90384-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90384-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90384-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90384-116">INPUTS</span></span>

## <span data-ttu-id="90384-117">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90384-117">OUTPUTS</span></span>

### <span data-ttu-id="90384-118">Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="90384-118">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="90384-119">Пуск</span><span class="sxs-lookup"><span data-stu-id="90384-119">NOTES</span></span>

## <span data-ttu-id="90384-120">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90384-120">RELATED LINKS</span></span>

[<span data-ttu-id="90384-121">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="90384-121">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="90384-122">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="90384-122">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="90384-123">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="90384-123">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="90384-124">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="90384-124">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
