---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 5e0464a4266a68905da26859f20faca918a9caab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507067"
---
# <span data-ttu-id="6c213-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="6c213-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="6c213-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c213-102">SYNOPSIS</span></span>
<span data-ttu-id="6c213-103">Список поставщиков услуг ExpressRoute и их атрибутов.</span><span class="sxs-lookup"><span data-stu-id="6c213-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="6c213-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6c213-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c213-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c213-105">DESCRIPTION</span></span>
<span data-ttu-id="6c213-106">Для получения списка поставщиков услуг ExpressRoute и их атрибутов извлекается **cmdlet Get-AzExpressRouteServiceProvider.**</span><span class="sxs-lookup"><span data-stu-id="6c213-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="6c213-107">Атрибут включает параметры расположения и пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="6c213-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="6c213-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6c213-108">EXAMPLES</span></span>

### <span data-ttu-id="6c213-109">Пример 1. Получить список поставщиков услуг с расположениями в "Кремниевой долине"</span><span class="sxs-lookup"><span data-stu-id="6c213-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="6c213-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c213-110">PARAMETERS</span></span>

### <span data-ttu-id="6c213-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c213-111">-DefaultProfile</span></span>
<span data-ttu-id="6c213-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c213-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c213-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c213-113">CommonParameters</span></span>
<span data-ttu-id="6c213-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c213-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c213-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c213-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c213-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c213-116">INPUTS</span></span>

### <span data-ttu-id="6c213-117">Нет</span><span class="sxs-lookup"><span data-stu-id="6c213-117">None</span></span>

## <span data-ttu-id="6c213-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6c213-118">OUTPUTS</span></span>

### <span data-ttu-id="6c213-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="6c213-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="6c213-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6c213-120">NOTES</span></span>

## <span data-ttu-id="6c213-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c213-121">RELATED LINKS</span></span>

[<span data-ttu-id="6c213-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6c213-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="6c213-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6c213-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="6c213-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6c213-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="6c213-125">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="6c213-125">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
