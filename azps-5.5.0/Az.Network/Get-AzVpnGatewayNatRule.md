---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGatewayNatRule.md
ms.openlocfilehash: 61dbb86c7eaa574abfcb3fad4bd37d6dbb242260
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223777"
---
# <span data-ttu-id="7b5fd-101">Get-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="7b5fd-101">Get-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="7b5fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b5fd-102">SYNOPSIS</span></span>
<span data-ttu-id="7b5fd-103">Возвращает правило NAT, связанное с VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-103">Gets a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="7b5fd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7b5fd-104">SYNTAX</span></span>

### <span data-ttu-id="7b5fd-105">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7b5fd-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b5fd-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7b5fd-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnGatewayNatRule -ParentObject <PSVpnGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b5fd-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7b5fd-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnGatewayNatRule -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b5fd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b5fd-108">DESCRIPTION</span></span>
<span data-ttu-id="7b5fd-109">Возвращает правило NAT, связанное с VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-109">Gets a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="7b5fd-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7b5fd-110">EXAMPLES</span></span>

### <span data-ttu-id="7b5fd-111">Пример</span><span class="sxs-lookup"><span data-stu-id="7b5fd-111">Example</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> Get-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule"

Type                      : Static
Mode                      : EgressSnat
VpnConnectionProtocolType : IKEv2
InternalMappings          : 10.0.0.1/26
ExternalMappings          : 192.168.0.0/26
IpConfigurationId         :
IngressVpnSiteLinkConnections : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
EgressVpnSiteLinkConnections  : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
ProvisioningState         : Provisioned
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/natRules/testNatRule

```

<span data-ttu-id="7b5fd-112">Выше будет создание группы ресурсов, виртуальной WAN, виртуальной сети, виртуального концентратора и VpnGateway & правила NAT, связанного с Vpngateway.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and VpnGateway & a NAT rule associated with Vpngateway.</span></span>
<span data-ttu-id="7b5fd-113">Затем правило NAT получает с использованием имени правила NAT.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-113">Then it gets the NAT rule using the NAT rule name.</span></span>

## <span data-ttu-id="7b5fd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b5fd-114">PARAMETERS</span></span>

### <span data-ttu-id="7b5fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b5fd-115">-DefaultProfile</span></span>
<span data-ttu-id="7b5fd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b5fd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7b5fd-117">-Name</span></span>
<span data-ttu-id="7b5fd-118">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayNatRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b5fd-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7b5fd-119">-ParentObject</span></span>
<span data-ttu-id="7b5fd-120">Родительская vpnGateway для этого VPNGatewayNatRule.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-120">The parent VpnGateway for this VpnGatewayNatRule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5fd-121">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7b5fd-121">-ParentResourceId</span></span>
<span data-ttu-id="7b5fd-122">ИД ресурса родительского VPNGateway для этого VPNGatewayNatRule.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-122">The resource id of the parent VpnGateway for this VpnGatewayNatRule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5fd-123">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="7b5fd-123">-ParentResourceName</span></span>
<span data-ttu-id="7b5fd-124">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-124">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b5fd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b5fd-125">-ResourceGroupName</span></span>
<span data-ttu-id="7b5fd-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b5fd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b5fd-127">CommonParameters</span></span>
<span data-ttu-id="7b5fd-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b5fd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b5fd-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b5fd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b5fd-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b5fd-130">INPUTS</span></span>

### <span data-ttu-id="7b5fd-131">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7b5fd-131">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="7b5fd-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7b5fd-132">System.String</span></span>

## <span data-ttu-id="7b5fd-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7b5fd-133">OUTPUTS</span></span>

### <span data-ttu-id="7b5fd-134">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="7b5fd-134">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="7b5fd-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7b5fd-135">NOTES</span></span>

## <span data-ttu-id="7b5fd-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b5fd-136">RELATED LINKS</span></span>
