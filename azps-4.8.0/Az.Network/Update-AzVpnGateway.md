---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 419c7bc71def03bc2db004e378d80ea9c31f5183
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244049"
---
# <span data-ttu-id="7462e-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7462e-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="7462e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7462e-102">SYNOPSIS</span></span>
<span data-ttu-id="7462e-103">Обновляет масштабируемый шлюз VPN.</span><span class="sxs-lookup"><span data-stu-id="7462e-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="7462e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7462e-104">SYNTAX</span></span>

### <span data-ttu-id="7462e-105">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7462e-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7462e-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7462e-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7462e-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7462e-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7462e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7462e-108">DESCRIPTION</span></span>
<span data-ttu-id="7462e-109">Командлет **Update-AzVpnGateway** обновляет масштабируемый шлюз VPN.</span><span class="sxs-lookup"><span data-stu-id="7462e-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="7462e-110">Шлюз Azure VPN — это программное подключение для подключений между сайтами в VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="7462e-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="7462e-111">Этот шлюз изменяет размер и масштабируется в соответствии с единицей масштабирования, заданной пользователем.</span><span class="sxs-lookup"><span data-stu-id="7462e-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="7462e-112">Подключение можно настроить из ветви или сайта, известного как VPN-сайт, на масштабируемый шлюз.</span><span class="sxs-lookup"><span data-stu-id="7462e-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="7462e-113">Каждое соединение состоит из двух туннелей Active-Active</span><span class="sxs-lookup"><span data-stu-id="7462e-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="7462e-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7462e-114">EXAMPLES</span></span>

### <span data-ttu-id="7462e-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7462e-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="7462e-116">В приведенном выше примере создается группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор — Запад US в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="7462e-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7462e-117">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="7462e-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="7462e-118">После создания шлюза он использует Update-AzVpnGateway для обновления шлюза до 3 единиц масштаба.</span><span class="sxs-lookup"><span data-stu-id="7462e-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="7462e-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7462e-119">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\>$ipconfigurationId1 = 'Instance0'
PS C:\>$addresslist1 = @('169.254.21.5')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>$ipconfigurationId2 = 'Instance1'
PS C:\>$addresslist2 = @('169.254.21.10')
PS C:\>$gw1ipconfBgp2 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId2 -CustomAddress $addresslist2
PS C:\>$gw = Get-AzVpnGateway -ResourceGroupName testRg -Name testgw
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -BgpPeeringAddress @($gw1ipconfBgp1,$gw1ipconfBgp2)

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="7462e-120">В приведенном выше примере создается группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор — Запад US в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="7462e-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7462e-121">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="7462e-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="7462e-122">После создания шлюза он использует Set-AzVpnGateway для обновления BgpPeeringAddress.</span><span class="sxs-lookup"><span data-stu-id="7462e-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="7462e-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7462e-123">PARAMETERS</span></span>

### <span data-ttu-id="7462e-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7462e-124">-AsJob</span></span>
<span data-ttu-id="7462e-125">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7462e-125">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7462e-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="7462e-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="7462e-127">Адреса пиринга BGP для этого VpnGateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="7462e-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

```yaml
Type: PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7462e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7462e-128">-Confirm</span></span>
<span data-ttu-id="7462e-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7462e-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7462e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7462e-130">-DefaultProfile</span></span>
<span data-ttu-id="7462e-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7462e-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7462e-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7462e-132">-InputObject</span></span>
<span data-ttu-id="7462e-133">Объект VPN-шлюза, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="7462e-133">The vpn gateway object to be modified</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7462e-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7462e-134">-Name</span></span>
<span data-ttu-id="7462e-135">Имя шлюза VPN.</span><span class="sxs-lookup"><span data-stu-id="7462e-135">The vpn gateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7462e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7462e-136">-ResourceGroupName</span></span>
<span data-ttu-id="7462e-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7462e-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7462e-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7462e-138">-ResourceId</span></span>
<span data-ttu-id="7462e-139">Идентификатор ресурса Azure VpnGateway, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="7462e-139">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7462e-140">-Тег</span><span class="sxs-lookup"><span data-stu-id="7462e-140">-Tag</span></span>
<span data-ttu-id="7462e-141">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7462e-141">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7462e-142">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7462e-142">-VpnConnection</span></span>
<span data-ttu-id="7462e-143">Список VpnConnections, который должен иметь этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7462e-143">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7462e-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="7462e-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="7462e-145">Единица масштабирования для этого VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7462e-145">The scale unit for this VpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7462e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7462e-146">-WhatIf</span></span>
<span data-ttu-id="7462e-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7462e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7462e-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7462e-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7462e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7462e-149">CommonParameters</span></span>
<span data-ttu-id="7462e-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7462e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7462e-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7462e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7462e-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7462e-152">INPUTS</span></span>

### <span data-ttu-id="7462e-153">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7462e-153">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="7462e-154">System. String</span><span class="sxs-lookup"><span data-stu-id="7462e-154">System.String</span></span>

## <span data-ttu-id="7462e-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7462e-155">OUTPUTS</span></span>

### <span data-ttu-id="7462e-156">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7462e-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="7462e-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="7462e-157">NOTES</span></span>

## <span data-ttu-id="7462e-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7462e-158">RELATED LINKS</span></span>
[<span data-ttu-id="7462e-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7462e-159">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="7462e-160">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7462e-160">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="7462e-161">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7462e-161">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)