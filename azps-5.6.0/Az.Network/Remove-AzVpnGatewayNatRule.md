---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
ms.openlocfilehash: 5c91ba0dbca881e7e6a6909ef1b7200adf2ba1ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990013"
---
# <span data-ttu-id="e62a9-101">Remove-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="e62a9-101">Remove-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="e62a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e62a9-102">SYNOPSIS</span></span>
<span data-ttu-id="e62a9-103">Удаляет правило NAT, связанное с VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e62a9-103">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="e62a9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e62a9-104">SYNTAX</span></span>

### <span data-ttu-id="e62a9-105">ByVpnGatewayNatRuleName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e62a9-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e62a9-106">ByVpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="e62a9-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e62a9-107">ByVpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="e62a9-107">ByVpnGatewayNatRuleObject</span></span>
```
Remove-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e62a9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e62a9-108">DESCRIPTION</span></span>
<span data-ttu-id="e62a9-109">Удаляет правило NAT, связанное с VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e62a9-109">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="e62a9-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e62a9-110">EXAMPLES</span></span>

### <span data-ttu-id="e62a9-111">Пример1</span><span class="sxs-lookup"><span data-stu-id="e62a9-111">Example1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> Remove-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule"
```

<span data-ttu-id="e62a9-112">Выше будет создание группы ресурсов, виртуальной WAN, виртуальной сети, виртуального концентратора, VPNGateway и правила NAT, связанных с этим VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e62a9-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub,VpnGateway and NAT rule associated with that VpnGateway.</span></span>
<span data-ttu-id="e62a9-113">Затем правило NAT удаляется с использованием имени правила NAT.</span><span class="sxs-lookup"><span data-stu-id="e62a9-113">Then it removes the NAT rule using the NAT rule name.</span></span>


## <span data-ttu-id="e62a9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e62a9-114">PARAMETERS</span></span>

### <span data-ttu-id="e62a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e62a9-115">-DefaultProfile</span></span>
<span data-ttu-id="e62a9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e62a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e62a9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e62a9-117">-Force</span></span>
<span data-ttu-id="e62a9-118">Не спрашивайте подтверждения при удалении ресурса</span><span class="sxs-lookup"><span data-stu-id="e62a9-118">Do not ask for confirmation if you want to delete a resource</span></span>

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

### <span data-ttu-id="e62a9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e62a9-119">-InputObject</span></span>
<span data-ttu-id="e62a9-120">Объект VpnGatewayNatRule, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="e62a9-120">The VpnGatewayNatRule object to update.</span></span>

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

### <span data-ttu-id="e62a9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e62a9-121">-Name</span></span>
<span data-ttu-id="e62a9-122">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="e62a9-122">The resource name.</span></span>

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

### <span data-ttu-id="e62a9-123">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="e62a9-123">-ParentResourceName</span></span>
<span data-ttu-id="e62a9-124">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="e62a9-124">The parent resource name.</span></span>

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

### <span data-ttu-id="e62a9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e62a9-125">-PassThru</span></span>
<span data-ttu-id="e62a9-126">Возвращает объект, представляющий элемент, с которым выполняется данной операция.</span><span class="sxs-lookup"><span data-stu-id="e62a9-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="e62a9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e62a9-127">-ResourceGroupName</span></span>
<span data-ttu-id="e62a9-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e62a9-128">The resource group name.</span></span>

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

### <span data-ttu-id="e62a9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e62a9-129">-ResourceId</span></span>
<span data-ttu-id="e62a9-130">ИД ресурса объекта VpnGatewayNatRule, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e62a9-130">The resource id of the VpnGatewayNatRule object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleResourceId
Aliases: VpnGatewayNatRuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e62a9-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e62a9-131">-Confirm</span></span>
<span data-ttu-id="e62a9-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e62a9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e62a9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e62a9-133">-WhatIf</span></span>
<span data-ttu-id="e62a9-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e62a9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e62a9-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e62a9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e62a9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62a9-136">CommonParameters</span></span>
<span data-ttu-id="e62a9-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e62a9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62a9-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e62a9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62a9-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e62a9-139">INPUTS</span></span>

### <span data-ttu-id="e62a9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e62a9-140">System.String</span></span>

### <span data-ttu-id="e62a9-141">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="e62a9-141">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="e62a9-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e62a9-142">OUTPUTS</span></span>

### <span data-ttu-id="e62a9-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e62a9-143">System.Boolean</span></span>

## <span data-ttu-id="e62a9-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e62a9-144">NOTES</span></span>

## <span data-ttu-id="e62a9-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e62a9-145">RELATED LINKS</span></span>
