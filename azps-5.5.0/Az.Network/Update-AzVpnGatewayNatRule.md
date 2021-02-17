---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
ms.openlocfilehash: 60f68795e79e751dda75ae4d549d2b25a43392e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220865"
---
# <span data-ttu-id="057dc-101">Update-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="057dc-101">Update-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="057dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="057dc-102">SYNOPSIS</span></span>
<span data-ttu-id="057dc-103">Обновляет правило NAT, связанное с VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="057dc-103">Updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="057dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="057dc-104">SYNTAX</span></span>

### <span data-ttu-id="057dc-105">ByVpnGatewayNatRuleName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="057dc-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Update-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>] [-ExternalMapping <String[]>]
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="057dc-106">ByVpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="057dc-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Update-AzVpnGatewayNatRule -ResourceId <String> [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>]
 [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="057dc-107">ByVpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="057dc-107">ByVpnGatewayNatRuleObject</span></span>
```
Update-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Type <String>] [-Mode <String>]
 [-InternalMapping <String[]>] [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="057dc-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="057dc-108">DESCRIPTION</span></span>
<span data-ttu-id="057dc-109">Для **обновления AzVpnGatewayNatRule** обновляется правило NAT, связанное с VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="057dc-109">The **Update-AzVpnGatewayNatRule** cmdlet updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="057dc-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="057dc-110">EXAMPLES</span></span>

### <span data-ttu-id="057dc-111">Пример</span><span class="sxs-lookup"><span data-stu-id="057dc-111">Example</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> $natRule = Update-AzVpnGatewayNatRule -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy
PS C:\> Update-AzVpnGatewayNatRule -InputObject $natRule -Type Dynamic -Mode IngressSnat

Type                      : Dynamic
Mode                      : IngressSnat
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

<span data-ttu-id="057dc-112">Выше будет создаваться группа ресурсов, виртуальная сеть, виртуальная сеть и виртуальный концентратор.</span><span class="sxs-lookup"><span data-stu-id="057dc-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="057dc-113">Затем мы создадим VpnGateway в этом виртуальном центре.</span><span class="sxs-lookup"><span data-stu-id="057dc-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="057dc-114">Затем создайте новое правило NAT, связанное с созданным VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="057dc-114">Then, create new NAT rule associated with created VpnGateway.</span></span>
<span data-ttu-id="057dc-115">Команда Update-AzVpnGatewayNatRule, обновление правила NAT.</span><span class="sxs-lookup"><span data-stu-id="057dc-115">Using this command: Update-AzVpnGatewayNatRule, update NAT rule.</span></span>

## <span data-ttu-id="057dc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="057dc-116">PARAMETERS</span></span>

### <span data-ttu-id="057dc-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="057dc-117">-AsJob</span></span>
<span data-ttu-id="057dc-118">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="057dc-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="057dc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="057dc-119">-DefaultProfile</span></span>
<span data-ttu-id="057dc-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="057dc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="057dc-121">-ExternalMapping</span><span class="sxs-lookup"><span data-stu-id="057dc-121">-ExternalMapping</span></span>
<span data-ttu-id="057dc-122">Список внешних сопоставлений частных IP-адресов подсети для NAT</span><span class="sxs-lookup"><span data-stu-id="057dc-122">The list of private IP address subnet external mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="057dc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="057dc-123">-InputObject</span></span>
<span data-ttu-id="057dc-124">Объект VpnGatewayNatRule, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="057dc-124">The VpnGatewayNatRule object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule
Parameter Sets: ByVpnGatewayNatRuleObject
Aliases: VpnGatewayNatRule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="057dc-125">-InternalMapping</span><span class="sxs-lookup"><span data-stu-id="057dc-125">-InternalMapping</span></span>
<span data-ttu-id="057dc-126">Список внутренних сопоставлений частных IP-адресов подсети для NAT</span><span class="sxs-lookup"><span data-stu-id="057dc-126">The list of private IP address subnet internal mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="057dc-127">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="057dc-127">-IpConfigurationId</span></span>
<span data-ttu-id="057dc-128">ID конфигурации IP,применяемая к этому правилу NAT</span><span class="sxs-lookup"><span data-stu-id="057dc-128">The IP Configuration ID this NAT rule applies to</span></span>

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

### <span data-ttu-id="057dc-129">-Mode</span><span class="sxs-lookup"><span data-stu-id="057dc-129">-Mode</span></span>
<span data-ttu-id="057dc-130">Направление NAT источника для NAT VPN</span><span class="sxs-lookup"><span data-stu-id="057dc-130">The Source NAT direction of a VPN NAT</span></span>

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

### <span data-ttu-id="057dc-131">-Name</span><span class="sxs-lookup"><span data-stu-id="057dc-131">-Name</span></span>
<span data-ttu-id="057dc-132">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="057dc-132">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="057dc-133">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="057dc-133">-ParentResourceName</span></span>
<span data-ttu-id="057dc-134">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="057dc-134">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="057dc-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="057dc-135">-ResourceGroupName</span></span>
<span data-ttu-id="057dc-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="057dc-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="057dc-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="057dc-137">-ResourceId</span></span>
<span data-ttu-id="057dc-138">ИД ресурса объекта VpnGatewayNatRule, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="057dc-138">The resource id of the VpnGatewayNatRule object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleResourceId
Aliases: VpnGatewayNatRuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="057dc-139">-Type</span><span class="sxs-lookup"><span data-stu-id="057dc-139">-Type</span></span>
<span data-ttu-id="057dc-140">Тип правила NAT для NAT VPN</span><span class="sxs-lookup"><span data-stu-id="057dc-140">The type of NAT rule for VPN NAT</span></span>

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

### <span data-ttu-id="057dc-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="057dc-141">-Confirm</span></span>
<span data-ttu-id="057dc-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="057dc-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="057dc-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="057dc-143">-WhatIf</span></span>
<span data-ttu-id="057dc-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="057dc-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="057dc-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="057dc-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="057dc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="057dc-146">CommonParameters</span></span>
<span data-ttu-id="057dc-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="057dc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="057dc-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="057dc-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="057dc-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="057dc-149">INPUTS</span></span>

### <span data-ttu-id="057dc-150">System.String</span><span class="sxs-lookup"><span data-stu-id="057dc-150">System.String</span></span>

### <span data-ttu-id="057dc-151">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="057dc-151">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="057dc-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="057dc-152">OUTPUTS</span></span>

### <span data-ttu-id="057dc-153">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="057dc-153">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="057dc-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="057dc-154">NOTES</span></span>

## <span data-ttu-id="057dc-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="057dc-155">RELATED LINKS</span></span>
