---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azp2svpngatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2sVpnGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2sVpnGatewayVpnConnection.md
ms.openlocfilehash: ee14842a636ff451e100a75db427934f9f0a1043
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407239"
---
# <span data-ttu-id="e416c-101">Disconnect-AzP2sVpnGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="e416c-101">Disconnect-AzP2sVpnGatewayVpnConnection</span></span>

## <span data-ttu-id="e416c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e416c-102">SYNOPSIS</span></span>
<span data-ttu-id="e416c-103">Отключение подключенных подключенных vpn-клиентских подключений с помощью заданного VPN-шлюза p2s</span><span class="sxs-lookup"><span data-stu-id="e416c-103">Disconnect given connected vpn client connections with a given p2s vpn gateway</span></span>

## <span data-ttu-id="e416c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e416c-104">SYNTAX</span></span>

### <span data-ttu-id="e416c-105">ByP2SVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e416c-105">ByP2SVpnGatewayName (Default)</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -Name <String> -ResourceGroupName <String>
 -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="e416c-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="e416c-106">ByP2SVpnGatewayObject</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="e416c-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="e416c-107">ByP2SVpnGatewayResourceId</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="e416c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e416c-108">DESCRIPTION</span></span>
<span data-ttu-id="e416c-109">С помощью cmdlet **Disconnect-AzP2sVpnGatewayVpnConnection** вы можете отключить текущую точку подключения к сайту от P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e416c-109">The **Disconnect-AzP2sVpnGatewayVpnConnection** cmdlet enables you to disconnect given current point to site connection from P2SVpnGateway.</span></span>

## <span data-ttu-id="e416c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e416c-110">EXAMPLES</span></span>

### <span data-ttu-id="e416c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e416c-111">Example 1</span></span>
```powershell
PS C:\> Disconnect-AzP2sVpnGatewayVpnConnection -ResourceName 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

## <span data-ttu-id="e416c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e416c-112">PARAMETERS</span></span>

### <span data-ttu-id="e416c-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e416c-113">-InputObject</span></span>
<span data-ttu-id="e416c-114">Объект VPN-шлюза p2s, который нужно изменить</span><span class="sxs-lookup"><span data-stu-id="e416c-114">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e416c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e416c-115">-Name</span></span>
<span data-ttu-id="e416c-116">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="e416c-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e416c-117">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="e416c-117">-VpnConnectionId</span></span>
<span data-ttu-id="e416c-118">Vpn Connection Ida</span><span class="sxs-lookup"><span data-stu-id="e416c-118">Vpn Connection Ida</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e416c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e416c-119">-ResourceGroupName</span></span>
<span data-ttu-id="e416c-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e416c-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e416c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e416c-121">-ResourceId</span></span>
<span data-ttu-id="e416c-122">ИД ресурса виртуального сетевого шлюза P2s</span><span class="sxs-lookup"><span data-stu-id="e416c-122">P2s Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e416c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e416c-123">CommonParameters</span></span>
<span data-ttu-id="e416c-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e416c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e416c-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e416c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e416c-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e416c-126">INPUTS</span></span>

### <span data-ttu-id="e416c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e416c-127">System.String</span></span>

## <span data-ttu-id="e416c-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e416c-128">OUTPUTS</span></span>

### <span data-ttu-id="e416c-129">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e416c-129">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="e416c-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e416c-130">NOTES</span></span>

## <span data-ttu-id="e416c-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e416c-131">RELATED LINKS</span></span>
