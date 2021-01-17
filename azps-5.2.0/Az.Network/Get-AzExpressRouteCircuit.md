---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: 7997949db725d50dd656479852b10d12094b8da7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323794"
---
# <span data-ttu-id="fb591-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fb591-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="fb591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb591-102">SYNOPSIS</span></span>
<span data-ttu-id="fb591-103">Получает канал Azure ExpressRoute из Azure.</span><span class="sxs-lookup"><span data-stu-id="fb591-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="fb591-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fb591-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb591-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb591-105">DESCRIPTION</span></span>
<span data-ttu-id="fb591-106">Для извлечения объекта схемы ExpressRoute из вашей подписки используется **cmdlet Get-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="fb591-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="fb591-107">Возвращаемый объект схемы может использоваться в качестве входных данных для других cmdlets, которые работают по схемам ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fb591-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="fb591-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fb591-108">EXAMPLES</span></span>

### <span data-ttu-id="fb591-109">Пример 1. Получить канал ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="fb591-109">Example 1: Get the ExpressRoute circuit</span></span>
```
Get-AzExpressRouteCircuit -ResourceGroupName testrg -Name test

Name                             : test
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="fb591-110">Получить определенный канал ExpressRoute с name "testrg" и resourceGroupName "test"</span><span class="sxs-lookup"><span data-stu-id="fb591-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="fb591-111">Пример 2. Список каналов ExpressRoute с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="fb591-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
```
Get-AzExpressRouteCircuit -Name test*

Name                             : test1
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test1
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :

Name                             : test2
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test2
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="fb591-112">Получите все схемы ExpressRoute, имена которых начинаются с test.</span><span class="sxs-lookup"><span data-stu-id="fb591-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="fb591-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb591-113">PARAMETERS</span></span>

### <span data-ttu-id="fb591-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb591-114">-DefaultProfile</span></span>
<span data-ttu-id="fb591-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb591-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb591-116">-Name</span><span class="sxs-lookup"><span data-stu-id="fb591-116">-Name</span></span>
<span data-ttu-id="fb591-117">Имя схемы ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fb591-117">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="fb591-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb591-118">-ResourceGroupName</span></span>
<span data-ttu-id="fb591-119">Имя группы ресурсов, которая содержит канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fb591-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="fb591-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb591-120">CommonParameters</span></span>
<span data-ttu-id="fb591-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb591-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb591-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb591-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb591-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb591-123">INPUTS</span></span>

### <span data-ttu-id="fb591-124">System.String</span><span class="sxs-lookup"><span data-stu-id="fb591-124">System.String</span></span>

## <span data-ttu-id="fb591-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fb591-125">OUTPUTS</span></span>

### <span data-ttu-id="fb591-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fb591-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="fb591-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fb591-127">NOTES</span></span>

## <span data-ttu-id="fb591-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb591-128">RELATED LINKS</span></span>

[<span data-ttu-id="fb591-129">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fb591-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="fb591-130">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fb591-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="fb591-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fb591-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="fb591-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fb591-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
