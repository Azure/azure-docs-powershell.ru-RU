---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: ac203d499674e97080edd645f9643b12291873d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225881"
---
# <span data-ttu-id="e77d7-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="e77d7-101">New-AzVpnSite</span></span>

## <span data-ttu-id="e77d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e77d7-102">SYNOPSIS</span></span>
<span data-ttu-id="e77d7-103">Создает новый ресурс Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="e77d7-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="e77d7-104">Это представление RM для ветвей клиентов, которые загружаются в Azure для подключения к S2S с помощью виртуального концентратора Cortex.</span><span class="sxs-lookup"><span data-stu-id="e77d7-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="e77d7-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e77d7-105">SYNTAX</span></span>

### <span data-ttu-id="e77d7-106">ByVirtualWanNameByVpnSiteIpAddress (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e77d7-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e77d7-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="e77d7-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e77d7-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="e77d7-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e77d7-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="e77d7-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e77d7-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="e77d7-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e77d7-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="e77d7-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e77d7-112">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e77d7-112">DESCRIPTION</span></span>
<span data-ttu-id="e77d7-113">Создает новый ресурс Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="e77d7-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="e77d7-114">Это представление RM для ветвей клиентов, которые загружаются в Azure для подключения к S2S с помощью виртуального концентратора Cortex.</span><span class="sxs-lookup"><span data-stu-id="e77d7-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="e77d7-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e77d7-115">EXAMPLES</span></span>

### <span data-ttu-id="e77d7-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e77d7-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "nonlinkSite"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "nonlinkSite" -Name myVirtualWAN -Location "East US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "nonlinkSite" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : nonlinkSite
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="e77d7-117">Выше будет создаваться группа ресурсов Virtual WAN на востоке США в группе ресурсов nonlinkSite в Azure.</span><span class="sxs-lookup"><span data-stu-id="e77d7-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="e77d7-118">Затем создается VPNSite, представляют ветвь клиента и связывает его с виртуальной сетью WAN.</span><span class="sxs-lookup"><span data-stu-id="e77d7-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="e77d7-119">Затем можно настроить подключение IPSec с этой ветвью и VpnGateway с помощью команды New-AzVpnConnection настройки.</span><span class="sxs-lookup"><span data-stu-id="e77d7-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="e77d7-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e77d7-120">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "multilink"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName multilink -Name myVirtualWAN -Location "East US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "multilink" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)
```

<span data-ttu-id="e77d7-121">Выше будет создаваться группа ресурсов Virtual WAN и VPNSite с 1 VpnSiteLinks в восточной части США в группе ресурсов multilink в Azure.</span><span class="sxs-lookup"><span data-stu-id="e77d7-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="e77d7-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e77d7-122">Example 3</span></span>

<span data-ttu-id="e77d7-123">Создает новый ресурс Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="e77d7-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="e77d7-124">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="e77d7-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="e77d7-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e77d7-125">PARAMETERS</span></span>

### <span data-ttu-id="e77d7-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="e77d7-126">-AddressSpace</span></span>
<span data-ttu-id="e77d7-127">Префиксы адресов виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e77d7-127">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="e77d7-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e77d7-128">-AsJob</span></span>
<span data-ttu-id="e77d7-129">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e77d7-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e77d7-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="e77d7-130">-BgpAsn</span></span>
<span data-ttu-id="e77d7-131">AsN BGP для этого VPNSite.</span><span class="sxs-lookup"><span data-stu-id="e77d7-131">The BGP ASN for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77d7-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="e77d7-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="e77d7-133">Адрес пиринга BGP для этого VPNSite.</span><span class="sxs-lookup"><span data-stu-id="e77d7-133">The BGP Peering Address for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77d7-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="e77d7-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="e77d7-135">Вес пиринга BGP для этого VPNSite.</span><span class="sxs-lookup"><span data-stu-id="e77d7-135">The BGP Peering weight for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77d7-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e77d7-136">-DefaultProfile</span></span>
<span data-ttu-id="e77d7-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e77d7-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e77d7-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="e77d7-138">-DeviceModel</span></span>
<span data-ttu-id="e77d7-139">Модель устройства удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="e77d7-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="e77d7-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="e77d7-140">-DeviceVendor</span></span>
<span data-ttu-id="e77d7-141">Поставщик устройства удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="e77d7-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="e77d7-142">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="e77d7-142">-IpAddress</span></span>
<span data-ttu-id="e77d7-143">IPAddress этого VPNSite.</span><span class="sxs-lookup"><span data-stu-id="e77d7-143">The IPAddress for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77d7-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="e77d7-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="e77d7-145">Модель устройства удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="e77d7-145">The device model of the remote vpn device.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77d7-146">-Location</span><span class="sxs-lookup"><span data-stu-id="e77d7-146">-Location</span></span>
<span data-ttu-id="e77d7-147">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="e77d7-147">The resource location.</span></span>

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

### <span data-ttu-id="e77d7-148">-Name</span><span class="sxs-lookup"><span data-stu-id="e77d7-148">-Name</span></span>
<span data-ttu-id="e77d7-149">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="e77d7-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77d7-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="e77d7-150">-O365Policy</span></span>
<span data-ttu-id="e77d7-151">Политика разгона трафика Office 365 для этого VPNSite.</span><span class="sxs-lookup"><span data-stu-id="e77d7-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77d7-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e77d7-152">-ResourceGroupName</span></span>
<span data-ttu-id="e77d7-153">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="e77d7-153">The resource name.</span></span>

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

### <span data-ttu-id="e77d7-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="e77d7-154">-Tag</span></span>
<span data-ttu-id="e77d7-155">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="e77d7-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e77d7-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="e77d7-156">-VirtualWan</span></span>
<span data-ttu-id="e77d7-157">К этому VPNSite необходимо подключать virtualWan.</span><span class="sxs-lookup"><span data-stu-id="e77d7-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77d7-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="e77d7-158">-VirtualWanId</span></span>
<span data-ttu-id="e77d7-159">К этому VPNSite должен быть подключен и виртуальный ресурс ResourceId.</span><span class="sxs-lookup"><span data-stu-id="e77d7-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77d7-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="e77d7-160">-VirtualWanName</span></span>
<span data-ttu-id="e77d7-161">Необходимо подключение к имени виртуальной аны этого VPNSite.</span><span class="sxs-lookup"><span data-stu-id="e77d7-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77d7-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e77d7-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="e77d7-163">Имя группы ресурсов virtualWan, к сети VpnSite которого нужно быть подключено.</span><span class="sxs-lookup"><span data-stu-id="e77d7-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77d7-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="e77d7-164">-VpnSiteLink</span></span>
<span data-ttu-id="e77d7-165">Список VPNSiteLinks, которые есть у этого VPNSite.</span><span class="sxs-lookup"><span data-stu-id="e77d7-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: ByVirtualWanNameByVpnSiteLinkObject, ByVirtualWanObjectByVpnSiteLinkObject, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77d7-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e77d7-166">-Confirm</span></span>
<span data-ttu-id="e77d7-167">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e77d7-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e77d7-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e77d7-168">-WhatIf</span></span>
<span data-ttu-id="e77d7-169">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e77d7-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e77d7-170">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e77d7-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e77d7-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e77d7-171">CommonParameters</span></span>
<span data-ttu-id="e77d7-172">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e77d7-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e77d7-173">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e77d7-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e77d7-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e77d7-174">INPUTS</span></span>

### <span data-ttu-id="e77d7-175">Нет</span><span class="sxs-lookup"><span data-stu-id="e77d7-175">None</span></span>

## <span data-ttu-id="e77d7-176">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e77d7-176">OUTPUTS</span></span>

### <span data-ttu-id="e77d7-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="e77d7-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="e77d7-178">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e77d7-178">NOTES</span></span>

## <span data-ttu-id="e77d7-179">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e77d7-179">RELATED LINKS</span></span>

[<span data-ttu-id="e77d7-180">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="e77d7-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="e77d7-181">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="e77d7-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="e77d7-182">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="e77d7-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
