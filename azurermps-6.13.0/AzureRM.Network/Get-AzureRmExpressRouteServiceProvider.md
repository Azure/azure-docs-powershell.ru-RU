---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
ms.openlocfilehash: 0c7beb4bc53635a8bf4293abf50441b0f15b66b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734620"
---
# <span data-ttu-id="bb0a2-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="bb0a2-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="bb0a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb0a2-102">SYNOPSIS</span></span>
<span data-ttu-id="bb0a2-103">Получает список поставщиков услуг ExpressRoute и их атрибутов.</span><span class="sxs-lookup"><span data-stu-id="bb0a2-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb0a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb0a2-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb0a2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb0a2-105">DESCRIPTION</span></span>
<span data-ttu-id="bb0a2-106">Командлет **Get-AzureRmExpressRouteServiceProvider** извлекает список поставщиков служб ExpressRoute и их атрибуты.</span><span class="sxs-lookup"><span data-stu-id="bb0a2-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="bb0a2-107">Атрибут: расположение и параметры пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="bb0a2-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="bb0a2-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb0a2-108">EXAMPLES</span></span>

### <span data-ttu-id="bb0a2-109">Пример 1: получение списка поставщика услуг с разположениями в «Silicon впадина»</span><span class="sxs-lookup"><span data-stu-id="bb0a2-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="bb0a2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb0a2-110">PARAMETERS</span></span>

### <span data-ttu-id="bb0a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb0a2-111">-DefaultProfile</span></span>
<span data-ttu-id="bb0a2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb0a2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb0a2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb0a2-113">CommonParameters</span></span>
<span data-ttu-id="bb0a2-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb0a2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb0a2-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb0a2-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb0a2-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb0a2-116">INPUTS</span></span>

### <span data-ttu-id="bb0a2-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="bb0a2-117">None</span></span>

## <span data-ttu-id="bb0a2-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb0a2-118">OUTPUTS</span></span>

### <span data-ttu-id="bb0a2-119">Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="bb0a2-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="bb0a2-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb0a2-120">NOTES</span></span>

## <span data-ttu-id="bb0a2-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb0a2-121">RELATED LINKS</span></span>

[<span data-ttu-id="bb0a2-122">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="bb0a2-122">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="bb0a2-123">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="bb0a2-123">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="bb0a2-124">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="bb0a2-124">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="bb0a2-125">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="bb0a2-125">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
