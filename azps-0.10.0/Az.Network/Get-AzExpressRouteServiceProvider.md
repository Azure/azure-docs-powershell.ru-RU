---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: ce3d4e42c6644cd3181ec9389a7b571c7f6ca51a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909990"
---
# <span data-ttu-id="ce33b-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="ce33b-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="ce33b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce33b-102">SYNOPSIS</span></span>
<span data-ttu-id="ce33b-103">Получает список поставщиков услуг ExpressRoute и их атрибутов.</span><span class="sxs-lookup"><span data-stu-id="ce33b-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="ce33b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce33b-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce33b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce33b-105">DESCRIPTION</span></span>
<span data-ttu-id="ce33b-106">Командлет **Get-AzExpressRouteServiceProvider** извлекает список поставщиков служб ExpressRoute и их атрибуты.</span><span class="sxs-lookup"><span data-stu-id="ce33b-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="ce33b-107">Атрибут: расположение и параметры пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="ce33b-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="ce33b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce33b-108">EXAMPLES</span></span>

### <span data-ttu-id="ce33b-109">Пример 1: получение списка поставщика услуг с разположениями в «Silicon впадина»</span><span class="sxs-lookup"><span data-stu-id="ce33b-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="ce33b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce33b-110">PARAMETERS</span></span>

### <span data-ttu-id="ce33b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce33b-111">-DefaultProfile</span></span>
<span data-ttu-id="ce33b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce33b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce33b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce33b-113">CommonParameters</span></span>
<span data-ttu-id="ce33b-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce33b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce33b-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce33b-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce33b-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce33b-116">INPUTS</span></span>

## <span data-ttu-id="ce33b-117">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce33b-117">OUTPUTS</span></span>

### <span data-ttu-id="ce33b-118">Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="ce33b-118">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="ce33b-119">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce33b-119">NOTES</span></span>

## <span data-ttu-id="ce33b-120">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce33b-120">RELATED LINKS</span></span>

[<span data-ttu-id="ce33b-121">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ce33b-121">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="ce33b-122">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ce33b-122">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="ce33b-123">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ce33b-123">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="ce33b-124">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="ce33b-124">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
