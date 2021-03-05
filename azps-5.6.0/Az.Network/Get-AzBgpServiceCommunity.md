---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azbgpservicecommunity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBgpServiceCommunity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBgpServiceCommunity.md
ms.openlocfilehash: 649fb6734caf2df11a65c43c59d123db425e90bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997772"
---
# <span data-ttu-id="acbf0-101">Get-AzBgpServiceCommunity</span><span class="sxs-lookup"><span data-stu-id="acbf0-101">Get-AzBgpServiceCommunity</span></span>

## <span data-ttu-id="acbf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acbf0-102">SYNOPSIS</span></span>
<span data-ttu-id="acbf0-103">Содержит список всех служб и регионов, сообществ BGP и связанных префиксов.</span><span class="sxs-lookup"><span data-stu-id="acbf0-103">Provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="acbf0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="acbf0-104">SYNTAX</span></span>

```
Get-AzBgpServiceCommunity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acbf0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="acbf0-105">DESCRIPTION</span></span>
<span data-ttu-id="acbf0-106">Этот cmdlet содержит список всех служб и регионов, сообществ BGP и связанных префиксов.</span><span class="sxs-lookup"><span data-stu-id="acbf0-106">This cmdlet provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="acbf0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="acbf0-107">EXAMPLES</span></span>

### <span data-ttu-id="acbf0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="acbf0-108">Example 1</span></span>
```
Get-AzBgpServiceCommunity

...

Name           : AzureCentralIndia
Id             : /subscriptions//resourceGroups//providers/Microsoft.Network/bgpServiceCommunities/AzureCentralIndia
Type           : Microsoft.Network/bgpServiceCommunities
BgpCommunities : [
                   {
                     "ServiceSupportedRegion": "Global",
                     "CommunityName": "Azure Central India",
                     "CommunityValue": "12076:51017",
                     "CommunityPrefixes": [
                       "13.71.0.0/18",
                       "20.190.146.0/25",
                       "40.79.214.0/24",
                       "40.81.224.0/19",
                       "40.87.224.0/22",
                       "40.112.39.0/25",
                       "40.112.39.128/26",
                       "40.126.18.0/25",
                       "52.136.24.0/24",
                       "52.140.64.0/18",
                       "52.159.64.0/19",
                       "52.172.128.0/17",
                       "52.239.135.64/26",
                       "52.239.202.0/24",
                       "52.245.96.0/22",
                       "52.253.168.0/22",
                       "104.47.210.0/23",
                       "104.211.64.0/20",
                       "104.211.81.0/24",
                       "104.211.82.0/23",
                       "104.211.84.0/22",
                       "104.211.88.0/21",
                       "104.211.96.0/19"
                     ],
                     "IsAuthorizedToUse": true,
                     "ServiceGroup": "Azure"
                   }
                 ]
...
```

<span data-ttu-id="acbf0-109">Этот cmdlet содержит список всех служб и регионов, сообществ BGP и связанных префиксов.</span><span class="sxs-lookup"><span data-stu-id="acbf0-109">This cmdlet provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="acbf0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acbf0-110">PARAMETERS</span></span>

### <span data-ttu-id="acbf0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acbf0-111">-DefaultProfile</span></span>
<span data-ttu-id="acbf0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="acbf0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acbf0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acbf0-113">CommonParameters</span></span>
<span data-ttu-id="acbf0-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acbf0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acbf0-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acbf0-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acbf0-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="acbf0-116">INPUTS</span></span>

### <span data-ttu-id="acbf0-117">Нет</span><span class="sxs-lookup"><span data-stu-id="acbf0-117">None</span></span>

## <span data-ttu-id="acbf0-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="acbf0-118">OUTPUTS</span></span>

### <span data-ttu-id="acbf0-119">Microsoft.Azure.Commands.Network.Models.PSBgpServiceCommunity</span><span class="sxs-lookup"><span data-stu-id="acbf0-119">Microsoft.Azure.Commands.Network.Models.PSBgpServiceCommunity</span></span>

## <span data-ttu-id="acbf0-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="acbf0-120">NOTES</span></span>

## <span data-ttu-id="acbf0-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="acbf0-121">RELATED LINKS</span></span>

[<span data-ttu-id="acbf0-122">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="acbf0-122">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="acbf0-123">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="acbf0-123">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="acbf0-124">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="acbf0-124">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="acbf0-125">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="acbf0-125">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="acbf0-126">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="acbf0-126">Get-AzRouteFilter</span></span>](Get-AzRouteFilter.md)

[<span data-ttu-id="acbf0-127">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="acbf0-127">Get-AzRouteFilterRuleConfig</span></span>](Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="acbf0-128">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="acbf0-128">Remove-AzRouteFilter</span></span>](Remove-AzRouteFilter.md)

[<span data-ttu-id="acbf0-129">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="acbf0-129">Remove-AzRouteFilterRuleConfig</span></span>](Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="acbf0-130">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="acbf0-130">Set-AzRouteFilter</span></span>](Set-AzRouteFilter.md)

[<span data-ttu-id="acbf0-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="acbf0-131">Set-AzRouteFilterRuleConfig</span></span>](Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="acbf0-132">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="acbf0-132">New-AzRouteFilter</span></span>](New-AzRouteFilter.md)

[<span data-ttu-id="acbf0-133">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="acbf0-133">New-AzRouteFilterRuleConfig</span></span>](New-AzRouteFilterRuleConfig.md)
