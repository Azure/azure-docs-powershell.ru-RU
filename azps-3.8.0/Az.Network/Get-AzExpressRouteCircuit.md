---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: 7997949db725d50dd656479852b10d12094b8da7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065847"
---
# <span data-ttu-id="e7e7c-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e7e7c-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="e7e7c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="e7e7c-103">Возвращает цепь Azure ExpressRoute из Azure.</span><span class="sxs-lookup"><span data-stu-id="e7e7c-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="e7e7c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7e7c-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7e7c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7e7c-105">DESCRIPTION</span></span>
<span data-ttu-id="e7e7c-106">Командлет **Get-AzExpressRouteCircuit** используется для получения объекта цепи ExpressRoute из подписки.</span><span class="sxs-lookup"><span data-stu-id="e7e7c-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="e7e7c-107">Возвращаемый объект цепью можно использовать в качестве входных данных для других командлетов, которые работают с каналами ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e7e7c-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="e7e7c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7e7c-108">EXAMPLES</span></span>

### <span data-ttu-id="e7e7c-109">Пример 1: получение канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="e7e7c-109">Example 1: Get the ExpressRoute circuit</span></span>
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

<span data-ttu-id="e7e7c-110">Получить определенную цепь ExpressRoute с именем "testrg" и ResourceGroupName "Test"</span><span class="sxs-lookup"><span data-stu-id="e7e7c-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="e7e7c-111">Пример 2: перечисление каналов ExpressRoute с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="e7e7c-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
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

<span data-ttu-id="e7e7c-112">Получение всех каналов ExpressRoute с именем, начинающимся с "Test".</span><span class="sxs-lookup"><span data-stu-id="e7e7c-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="e7e7c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7e7c-113">PARAMETERS</span></span>

### <span data-ttu-id="e7e7c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7e7c-114">-DefaultProfile</span></span>
<span data-ttu-id="e7e7c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7e7c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7e7c-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e7e7c-116">-Name</span></span>
<span data-ttu-id="e7e7c-117">Имя канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e7e7c-117">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="e7e7c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7e7c-118">-ResourceGroupName</span></span>
<span data-ttu-id="e7e7c-119">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e7e7c-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="e7e7c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7e7c-120">CommonParameters</span></span>
<span data-ttu-id="e7e7c-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7e7c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7e7c-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7e7c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7e7c-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7e7c-123">INPUTS</span></span>

### <span data-ttu-id="e7e7c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e7e7c-124">System.String</span></span>

## <span data-ttu-id="e7e7c-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7e7c-125">OUTPUTS</span></span>

### <span data-ttu-id="e7e7c-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e7e7c-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e7e7c-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7e7c-127">NOTES</span></span>

## <span data-ttu-id="e7e7c-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7e7c-128">RELATED LINKS</span></span>

[<span data-ttu-id="e7e7c-129">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e7e7c-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="e7e7c-130">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e7e7c-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="e7e7c-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e7e7c-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="e7e7c-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e7e7c-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
