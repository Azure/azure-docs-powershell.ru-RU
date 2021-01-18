---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGateway.md
ms.openlocfilehash: 9118109de6262fd6214c80c41f2eafd415c440db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506546"
---
# <span data-ttu-id="6cd00-101">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6cd00-101">Get-AzApplicationGateway</span></span>

## <span data-ttu-id="6cd00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cd00-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd00-103">Получение шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="6cd00-103">Gets an application gateway.</span></span>

## <span data-ttu-id="6cd00-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6cd00-104">SYNTAX</span></span>

```
Get-AzApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cd00-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cd00-105">DESCRIPTION</span></span>
<span data-ttu-id="6cd00-106">Для **получения шлюза приложения возвращается cmdlet Get-AzApplicationGateway.**</span><span class="sxs-lookup"><span data-stu-id="6cd00-106">The **Get-AzApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="6cd00-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6cd00-107">EXAMPLES</span></span>

### <span data-ttu-id="6cd00-108">Пример 1. Получение указанного шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="6cd00-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"

Sku                                 : Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
SslPolicy                           :
GatewayIPConfigurations             : {appGatewayFrontendIP}
AuthenticationCertificates          : {}
SslCertificates                     : {}
TrustedRootCertificates             : {}
FrontendIPConfigurations            : {appGatewayFrontendIP}
FrontendPorts                       : {appGatewayFrontendPort}
Probes                              : {}
BackendAddressPools                 : {appGatewayBackendPool}
BackendHttpSettingsCollection       : {appGatewayBackendHttpSettings}
HttpListeners                       : {appGatewayHttpListener}
UrlPathMaps                         : {}
RequestRoutingRules                 : {rule1}
RewriteRuleSets                     : {}
RedirectConfigurations              : {}
WebApplicationFirewallConfiguration :
AutoscaleConfiguration              :
CustomErrorConfigurations           : {}
EnableHttp2                         :
EnableFips                          :
ForceFirewallPolicyAssociation      :
Zones                               : {}
OperationalState                    : Running
ProvisioningState                   : Succeeded
Identity                            :
GatewayIpConfigurationsText         : []
AuthenticationCertificatesText      : []
SslCertificatesText                 : []
FrontendIpConfigurationsText        : []
FrontendPortsText                   : []
BackendAddressPoolsText             : []
BackendHttpSettingsCollectionText   : []
HttpListenersText                   : []
RewriteRuleSetsText                 : []
RequestRoutingRulesText             : []
ProbesText                          : []
UrlPathMapsText                     : []
IdentityText                        : null
SslPolicyText                       : null
ResourceGroupName                   : tjp-rg
Location                            : westus
ResourceGuid                        : 00000000-0000-0000-0000-000000000000
Type                                : Microsoft.Network/applicationGateways
Tag                                 : {}
TagsTable                           :
Name                                : ApplicationGateway01
Etag                                : W/"00000000-0000-0000-0000-000000000000"
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/provide
                                      rs/Microsoft.Network/applicationGateways/ApplicationGateway01
```

<span data-ttu-id="6cd00-109">Эта команда получает шлюз приложения ApplicationGateway01, который принадлежит группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="6cd00-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="6cd00-110">Пример 2. Получение списка шлюзов приложений в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="6cd00-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway -ResourceGroupName "ResourceGroup01"

Sku                                 : Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
SslPolicy                           :
GatewayIPConfigurations             : {appGatewayFrontendIP}
AuthenticationCertificates          : {}
SslCertificates                     : {}
TrustedRootCertificates             : {}
FrontendIPConfigurations            : {appGatewayFrontendIP}
FrontendPorts                       : {appGatewayFrontendPort}
Probes                              : {}
BackendAddressPools                 : {appGatewayBackendPool}
BackendHttpSettingsCollection       : {appGatewayBackendHttpSettings}
HttpListeners                       : {appGatewayHttpListener}
UrlPathMaps                         : {}
RequestRoutingRules                 : {rule1}
RewriteRuleSets                     : {}
RedirectConfigurations              : {}
WebApplicationFirewallConfiguration :
AutoscaleConfiguration              :
CustomErrorConfigurations           : {}
EnableHttp2                         :
EnableFips                          :
ForceFirewallPolicyAssociation      :
Zones                               : {}
OperationalState                    : Running
ProvisioningState                   : Succeeded
Identity                            :
GatewayIpConfigurationsText         : []
AuthenticationCertificatesText      : []
SslCertificatesText                 : []
FrontendIpConfigurationsText        : []
FrontendPortsText                   : []
BackendAddressPoolsText             : []
BackendHttpSettingsCollectionText   : []
HttpListenersText                   : []
RewriteRuleSetsText                 : []
RequestRoutingRulesText             : []
ProbesText                          : []
UrlPathMapsText                     : []
IdentityText                        : null
SslPolicyText                       : null
ResourceGroupName                   : tjp-rg
Location                            : westus
ResourceGuid                        : 00000000-0000-0000-0000-000000000000
Type                                : Microsoft.Network/applicationGateways
Tag                                 : {}
TagsTable                           :
Name                                : ApplicationGateway01
Etag                                : W/"00000000-0000-0000-0000-000000000000"
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/provide
                                      rs/Microsoft.Network/applicationGateways/ApplicationGateway01
```

<span data-ttu-id="6cd00-111">Эта команда получает список всех шлюзов приложений в группе ресурсов ResourceGroup01 и сохраняет ее в переменной $AppGwList ресурса.</span><span class="sxs-lookup"><span data-stu-id="6cd00-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="6cd00-112">Пример 3. Получение списка шлюзов приложений в подписке</span><span class="sxs-lookup"><span data-stu-id="6cd00-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway

Sku                                 : Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
SslPolicy                           :
GatewayIPConfigurations             : {appGatewayFrontendIP}
AuthenticationCertificates          : {}
SslCertificates                     : {}
TrustedRootCertificates             : {}
FrontendIPConfigurations            : {appGatewayFrontendIP}
FrontendPorts                       : {appGatewayFrontendPort}
Probes                              : {}
BackendAddressPools                 : {appGatewayBackendPool}
BackendHttpSettingsCollection       : {appGatewayBackendHttpSettings}
HttpListeners                       : {appGatewayHttpListener}
UrlPathMaps                         : {}
RequestRoutingRules                 : {rule1}
RewriteRuleSets                     : {}
RedirectConfigurations              : {}
WebApplicationFirewallConfiguration :
AutoscaleConfiguration              :
CustomErrorConfigurations           : {}
EnableHttp2                         :
EnableFips                          :
ForceFirewallPolicyAssociation      :
Zones                               : {}
OperationalState                    : Running
ProvisioningState                   : Succeeded
Identity                            :
GatewayIpConfigurationsText         : []
AuthenticationCertificatesText      : []
SslCertificatesText                 : []
FrontendIpConfigurationsText        : []
FrontendPortsText                   : []
BackendAddressPoolsText             : []
BackendHttpSettingsCollectionText   : []
HttpListenersText                   : []
RewriteRuleSetsText                 : []
RequestRoutingRulesText             : []
ProbesText                          : []
UrlPathMapsText                     : []
IdentityText                        : null
SslPolicyText                       : null
ResourceGroupName                   : tjp-rg
Location                            : westus
ResourceGuid                        : 00000000-0000-0000-0000-000000000000
Type                                : Microsoft.Network/applicationGateways
Tag                                 : {}
TagsTable                           :
Name                                : ApplicationGateway01
Etag                                : W/"00000000-0000-0000-0000-000000000000"
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/provide
                                      rs/Microsoft.Network/applicationGateways/ApplicationGateway01
```

<span data-ttu-id="6cd00-113">Эта команда получает список всех шлюзов приложения в подписке и сохраняет его в переменной $AppGwList параметрами.</span><span class="sxs-lookup"><span data-stu-id="6cd00-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="6cd00-114">Пример 4. Получение списка шлюзов приложений в подписке с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="6cd00-114">Example 4: Get a list of application gateways in a subscription using filtering</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway -Name ApplicationGateway*

Sku                                 : Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
SslPolicy                           :
GatewayIPConfigurations             : {appGatewayFrontendIP}
AuthenticationCertificates          : {}
SslCertificates                     : {}
TrustedRootCertificates             : {}
FrontendIPConfigurations            : {appGatewayFrontendIP}
FrontendPorts                       : {appGatewayFrontendPort}
Probes                              : {}
BackendAddressPools                 : {appGatewayBackendPool}
BackendHttpSettingsCollection       : {appGatewayBackendHttpSettings}
HttpListeners                       : {appGatewayHttpListener}
UrlPathMaps                         : {}
RequestRoutingRules                 : {rule1}
RewriteRuleSets                     : {}
RedirectConfigurations              : {}
WebApplicationFirewallConfiguration :
AutoscaleConfiguration              :
CustomErrorConfigurations           : {}
EnableHttp2                         :
EnableFips                          :
ForceFirewallPolicyAssociation      :
Zones                               : {}
OperationalState                    : Running
ProvisioningState                   : Succeeded
Identity                            :
GatewayIpConfigurationsText         : []
AuthenticationCertificatesText      : []
SslCertificatesText                 : []
FrontendIpConfigurationsText        : []
FrontendPortsText                   : []
BackendAddressPoolsText             : []
BackendHttpSettingsCollectionText   : []
HttpListenersText                   : []
RewriteRuleSetsText                 : []
RequestRoutingRulesText             : []
ProbesText                          : []
UrlPathMapsText                     : []
IdentityText                        : null
SslPolicyText                       : null
ResourceGroupName                   : tjp-rg
Location                            : westus
ResourceGuid                        : 00000000-0000-0000-0000-000000000000
Type                                : Microsoft.Network/applicationGateways
Tag                                 : {}
TagsTable                           :
Name                                : ApplicationGateway01
Etag                                : W/"00000000-0000-0000-0000-000000000000"
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/provide
                                      rs/Microsoft.Network/applicationGateways/ApplicationGateway01
```

<span data-ttu-id="6cd00-115">Эта команда получает список всех шлюзов приложений в подписке, которые начинаются с ApplicationGateway01, и сохраняет их в переменной $AppGwList.</span><span class="sxs-lookup"><span data-stu-id="6cd00-115">This command gets a list of all the application gateways in the subscription that start with "ApplicationGateway01" and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="6cd00-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cd00-116">PARAMETERS</span></span>

### <span data-ttu-id="6cd00-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cd00-117">-DefaultProfile</span></span>
<span data-ttu-id="6cd00-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6cd00-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cd00-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6cd00-119">-Name</span></span>
<span data-ttu-id="6cd00-120">Указывает имя шлюза приложения, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cd00-120">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6cd00-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cd00-121">-ResourceGroupName</span></span>
<span data-ttu-id="6cd00-122">Имя группы ресурсов, которая содержит шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="6cd00-122">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="6cd00-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd00-123">CommonParameters</span></span>
<span data-ttu-id="6cd00-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cd00-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd00-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cd00-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd00-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cd00-126">INPUTS</span></span>

### <span data-ttu-id="6cd00-127">System.String</span><span class="sxs-lookup"><span data-stu-id="6cd00-127">System.String</span></span>

## <span data-ttu-id="6cd00-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6cd00-128">OUTPUTS</span></span>

### <span data-ttu-id="6cd00-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6cd00-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6cd00-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6cd00-130">NOTES</span></span>

## <span data-ttu-id="6cd00-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cd00-131">RELATED LINKS</span></span>

[<span data-ttu-id="6cd00-132">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6cd00-132">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


