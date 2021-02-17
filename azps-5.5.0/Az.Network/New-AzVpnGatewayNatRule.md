---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGatewayNatRule.md
ms.openlocfilehash: 45ec34bf437c64b96c3c46afa142d5e5b12f6010
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227604"
---
# <span data-ttu-id="2a923-101">New-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="2a923-101">New-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="2a923-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a923-102">SYNOPSIS</span></span>
<span data-ttu-id="2a923-103">Создает правило NAT в VpnGateway, которое может быть связано с VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="2a923-103">Creates a NAT rule on a VpnGateway which can be associated with VpnSiteLinkConnection.</span></span>

## <span data-ttu-id="2a923-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a923-104">SYNTAX</span></span>

### <span data-ttu-id="2a923-105">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a923-105">ByVpnGatewayName (Default)</span></span>
```
New-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] -InternalMapping <String[]> -ExternalMapping <String[]>
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a923-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="2a923-106">ByVpnGatewayObject</span></span>
```
New-AzVpnGatewayNatRule -ParentObject <PSVpnGateway> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a923-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="2a923-107">ByVpnGatewayResourceId</span></span>
```
New-AzVpnGatewayNatRule -ParentResourceId <String> -Name <String> [-Type <String>] [-Mode <String>]
 -InternalMapping <String[]> -ExternalMapping <String[]> [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a923-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a923-108">DESCRIPTION</span></span>
<span data-ttu-id="2a923-109">Создает правило NAT для VpnGateway, которое может быть связано с VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="2a923-109">Creates a NAT rule on a VpnGateway which can be associated with VpnGateway.</span></span>

## <span data-ttu-id="2a923-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a923-110">EXAMPLES</span></span>

### <span data-ttu-id="2a923-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2a923-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"

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

<span data-ttu-id="2a923-112">Выше будет создаваться группа ресурсов, виртуальная сеть, виртуальная сеть и виртуальный концентратор.</span><span class="sxs-lookup"><span data-stu-id="2a923-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="2a923-113">Затем мы создадим VpnGateway в этом виртуальном центре.</span><span class="sxs-lookup"><span data-stu-id="2a923-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="2a923-114">Затем, используя эту команду: New-AzVpnGatewayNatRule, можно создать правило NAT и связанное с созданным VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="2a923-114">Then, using this command: New-AzVpnGatewayNatRule, NAT rule can be createdand associated with created VpnGateway.</span></span>

## <span data-ttu-id="2a923-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a923-115">PARAMETERS</span></span>

### <span data-ttu-id="2a923-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a923-116">-AsJob</span></span>
<span data-ttu-id="2a923-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2a923-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a923-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a923-118">-DefaultProfile</span></span>
<span data-ttu-id="2a923-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a923-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a923-120">-ExternalMapping</span><span class="sxs-lookup"><span data-stu-id="2a923-120">-ExternalMapping</span></span>
<span data-ttu-id="2a923-121">Список внешних сопоставлений частных IP-адресов подсети для NAT</span><span class="sxs-lookup"><span data-stu-id="2a923-121">The list of private IP address subnet external mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a923-122">-InternalMapping</span><span class="sxs-lookup"><span data-stu-id="2a923-122">-InternalMapping</span></span>
<span data-ttu-id="2a923-123">Список внутренних сопоставлений частных IP-адресов подсети для NAT</span><span class="sxs-lookup"><span data-stu-id="2a923-123">The list of private IP address subnet internal mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a923-124">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2a923-124">-IpConfigurationId</span></span>
<span data-ttu-id="2a923-125">ID конфигурации IP для правила NAT</span><span class="sxs-lookup"><span data-stu-id="2a923-125">The IP Configuration ID this NAT rule applies to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a923-126">-Mode</span><span class="sxs-lookup"><span data-stu-id="2a923-126">-Mode</span></span>
<span data-ttu-id="2a923-127">Направление NAT источника для NAT VPN</span><span class="sxs-lookup"><span data-stu-id="2a923-127">The Source NAT direction of a VPN NAT</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EgressSnat, IngressSnat

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a923-128">-Name</span><span class="sxs-lookup"><span data-stu-id="2a923-128">-Name</span></span>
<span data-ttu-id="2a923-129">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2a923-129">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a923-130">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2a923-130">-ParentObject</span></span>
<span data-ttu-id="2a923-131">Родительское правило VPNGateway для этого правила NAT.</span><span class="sxs-lookup"><span data-stu-id="2a923-131">The parent VpnGateway for this NAT Rule.</span></span>

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

### <span data-ttu-id="2a923-132">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2a923-132">-ParentResourceId</span></span>
<span data-ttu-id="2a923-133">ИД ресурса родительского VPNGateway для этого правила NAT.</span><span class="sxs-lookup"><span data-stu-id="2a923-133">The resource id of the parent VpnGateway for this NAT Rule.</span></span>

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

### <span data-ttu-id="2a923-134">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="2a923-134">-ParentResourceName</span></span>
<span data-ttu-id="2a923-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a923-135">The resource group name.</span></span>

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

### <span data-ttu-id="2a923-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a923-136">-ResourceGroupName</span></span>
<span data-ttu-id="2a923-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a923-137">The resource group name.</span></span>

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

### <span data-ttu-id="2a923-138">-Type</span><span class="sxs-lookup"><span data-stu-id="2a923-138">-Type</span></span>
<span data-ttu-id="2a923-139">Тип правила NAT для NAT VPN</span><span class="sxs-lookup"><span data-stu-id="2a923-139">The type of NAT rule for VPN NAT</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a923-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a923-140">-Confirm</span></span>
<span data-ttu-id="2a923-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a923-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a923-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a923-142">-WhatIf</span></span>
<span data-ttu-id="2a923-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a923-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a923-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2a923-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a923-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a923-145">CommonParameters</span></span>
<span data-ttu-id="2a923-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a923-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a923-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a923-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a923-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a923-148">INPUTS</span></span>

### <span data-ttu-id="2a923-149">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2a923-149">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="2a923-150">System.String</span><span class="sxs-lookup"><span data-stu-id="2a923-150">System.String</span></span>

## <span data-ttu-id="2a923-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a923-151">OUTPUTS</span></span>

### <span data-ttu-id="2a923-152">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="2a923-152">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="2a923-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a923-153">NOTES</span></span>

## <span data-ttu-id="2a923-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a923-154">RELATED LINKS</span></span>
