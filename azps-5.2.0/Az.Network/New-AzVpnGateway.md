---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: fa7374264e46e65dcddacb9f35e5822f18294147
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401223"
---
# <span data-ttu-id="5ef80-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="5ef80-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="5ef80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ef80-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef80-103">Создает масштабируемый VPN-шлюз.</span><span class="sxs-lookup"><span data-stu-id="5ef80-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="5ef80-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5ef80-104">SYNTAX</span></span>

### <span data-ttu-id="5ef80-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ef80-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ef80-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="5ef80-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ef80-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="5ef80-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ef80-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ef80-108">DESCRIPTION</span></span>

<span data-ttu-id="5ef80-109">New-AzVpnGateway создает масштабируемый VPN-шлюз.</span><span class="sxs-lookup"><span data-stu-id="5ef80-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="5ef80-110">Это программное обеспечение, определяемое подключением сайта к подключениям к сайтам внутри VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="5ef80-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="5ef80-111">Размер и масштаб этого шлюза меняются в зависимости от единицы, указанной в этом или Set-AzVpnGateway блоке.</span><span class="sxs-lookup"><span data-stu-id="5ef80-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span> 

<span data-ttu-id="5ef80-112">Подключение устанавливается из ветви или сайта (VPNSite) к масштабируемого шлюзу.</span><span class="sxs-lookup"><span data-stu-id="5ef80-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="5ef80-113">Каждое подключение состоит из 2 Active-Active.</span><span class="sxs-lookup"><span data-stu-id="5ef80-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="5ef80-114">VpnGateway будет расположен в том же расположении, что и в VirtualHub, на который ссылается ссылка.</span><span class="sxs-lookup"><span data-stu-id="5ef80-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="5ef80-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5ef80-115">EXAMPLES</span></span>

### <span data-ttu-id="5ef80-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5ef80-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="5ef80-117">Выше будет создать группу ресурсов, виртуальную сеть, виртуальную сеть, виртуальный концентратор на западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="5ef80-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="5ef80-118">После этого в виртуальном центре будет создан VPN-шлюз с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="5ef80-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="5ef80-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ef80-119">PARAMETERS</span></span>

### <span data-ttu-id="5ef80-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ef80-120">-AsJob</span></span>
<span data-ttu-id="5ef80-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5ef80-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ef80-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ef80-122">-DefaultProfile</span></span>
<span data-ttu-id="5ef80-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ef80-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ef80-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5ef80-124">-Name</span></span>
<span data-ttu-id="5ef80-125">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="5ef80-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef80-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ef80-126">-ResourceGroupName</span></span>
<span data-ttu-id="5ef80-127">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="5ef80-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef80-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ef80-128">-Tag</span></span>
<span data-ttu-id="5ef80-129">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="5ef80-129">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef80-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="5ef80-130">-VirtualHub</span></span>
<span data-ttu-id="5ef80-131">С виртуальным ИТ-частью VpnGateway необходимо связано.</span><span class="sxs-lookup"><span data-stu-id="5ef80-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef80-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="5ef80-132">-VirtualHubId</span></span>
<span data-ttu-id="5ef80-133">С ИД VirtualHub этого VpnGateway нужно будет связан.</span><span class="sxs-lookup"><span data-stu-id="5ef80-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef80-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="5ef80-134">-VirtualHubName</span></span>
<span data-ttu-id="5ef80-135">С ИД VirtualHub этого VpnGateway необходимо связан.</span><span class="sxs-lookup"><span data-stu-id="5ef80-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef80-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="5ef80-136">-VpnConnection</span></span>
<span data-ttu-id="5ef80-137">Список VPNConnections, необходимых для этого VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="5ef80-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef80-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="5ef80-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="5ef80-139">Единица масштаба для этого VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="5ef80-139">The scale unit for this VpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef80-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ef80-140">-Confirm</span></span>
<span data-ttu-id="5ef80-141">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5ef80-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ef80-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ef80-142">-WhatIf</span></span>
<span data-ttu-id="5ef80-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ef80-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ef80-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5ef80-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ef80-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef80-145">CommonParameters</span></span>
<span data-ttu-id="5ef80-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ef80-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef80-147">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ef80-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef80-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ef80-148">INPUTS</span></span>

### <span data-ttu-id="5ef80-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5ef80-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="5ef80-150">System.String</span><span class="sxs-lookup"><span data-stu-id="5ef80-150">System.String</span></span>

## <span data-ttu-id="5ef80-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ef80-151">OUTPUTS</span></span>

### <span data-ttu-id="5ef80-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="5ef80-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="5ef80-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5ef80-153">NOTES</span></span>

## <span data-ttu-id="5ef80-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ef80-154">RELATED LINKS</span></span>

[<span data-ttu-id="5ef80-155">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="5ef80-155">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="5ef80-156">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="5ef80-156">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="5ef80-157">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="5ef80-157">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
