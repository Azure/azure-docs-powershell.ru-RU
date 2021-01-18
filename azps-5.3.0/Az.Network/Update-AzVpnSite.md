---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: b7ed573ed8df8086cd5cef04204020498e1413c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517846"
---
# <span data-ttu-id="8f1ff-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="8f1ff-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="8f1ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f1ff-102">SYNOPSIS</span></span>
<span data-ttu-id="8f1ff-103">Обновляет сайт VPN.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-103">Updates a VPN site.</span></span>

## <span data-ttu-id="8f1ff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8f1ff-104">SYNTAX</span></span>

### <span data-ttu-id="8f1ff-105">ByVpnSiteNameNoVirtualWanUpdate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8f1ff-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f1ff-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="8f1ff-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f1ff-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="8f1ff-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f1ff-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="8f1ff-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f1ff-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="8f1ff-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f1ff-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="8f1ff-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f1ff-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="8f1ff-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f1ff-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="8f1ff-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f1ff-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="8f1ff-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f1ff-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="8f1ff-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f1ff-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="8f1ff-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f1ff-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="8f1ff-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f1ff-117">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f1ff-117">DESCRIPTION</span></span>
<span data-ttu-id="8f1ff-118">Для **обновления VPN-сайта обновляется cmdlet Update-AzVpnSite.**</span><span class="sxs-lookup"><span data-stu-id="8f1ff-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="8f1ff-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8f1ff-119">EXAMPLES</span></span>

### <span data-ttu-id="8f1ff-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8f1ff-120">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "2.3.5.5"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 2.3.4.5
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="8f1ff-121">Выше будет создаться группа ресурсов Virtual WAN в западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="8f1ff-122">Затем создается VPNSite, представляют ветвь клиента и связывает его с виртуальной сетью WAN.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="8f1ff-123">После создания сайта ipAddress сайта обновляется с помощью команды "Set-AzVpnSite".</span><span class="sxs-lookup"><span data-stu-id="8f1ff-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="8f1ff-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f1ff-124">PARAMETERS</span></span>

### <span data-ttu-id="8f1ff-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="8f1ff-125">-AddressSpace</span></span>
<span data-ttu-id="8f1ff-126">Префиксы адресов виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="8f1ff-127">Используйте этот или AddressSpaceObject, но не оба.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-127">Use this or AddressSpaceObject but not both.</span></span>

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

### <span data-ttu-id="8f1ff-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f1ff-128">-AsJob</span></span>
<span data-ttu-id="8f1ff-129">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8f1ff-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f1ff-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="8f1ff-130">-BgpAsn</span></span>
<span data-ttu-id="8f1ff-131">AsN BGP для этого VPNSite.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-131">The BGP ASN for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1ff-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="8f1ff-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="8f1ff-133">Адрес пиринга BGP для этого VPNSite.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="8f1ff-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="8f1ff-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="8f1ff-135">Вес пиринга BGP для этого VPNSite.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-135">The BGP Peering weight for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1ff-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f1ff-136">-DefaultProfile</span></span>
<span data-ttu-id="8f1ff-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f1ff-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="8f1ff-138">-DeviceModel</span></span>
<span data-ttu-id="8f1ff-139">Модель устройства удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="8f1ff-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="8f1ff-140">-DeviceVendor</span></span>
<span data-ttu-id="8f1ff-141">Поставщик устройства удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="8f1ff-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f1ff-142">-InputObject</span></span>
<span data-ttu-id="8f1ff-143">Объект VPN-сайта, который нужно изменить</span><span class="sxs-lookup"><span data-stu-id="8f1ff-143">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObjectByVirtualWanName, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteObjectNoVirtualWanUpdate
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f1ff-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="8f1ff-144">-IpAddress</span></span>
<span data-ttu-id="8f1ff-145">IP-адрес локального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="8f1ff-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="8f1ff-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="8f1ff-147">Модель устройства удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-147">The device model of the remote vpn device.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1ff-148">-Name</span><span class="sxs-lookup"><span data-stu-id="8f1ff-148">-Name</span></span>
<span data-ttu-id="8f1ff-149">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1ff-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="8f1ff-150">-O365Policy</span></span>
<span data-ttu-id="8f1ff-151">Политика разгона трафика Office 365 для этого VPNSite.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="8f1ff-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f1ff-152">-ResourceGroupName</span></span>
<span data-ttu-id="8f1ff-153">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-153">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1ff-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f1ff-154">-ResourceId</span></span>
<span data-ttu-id="8f1ff-155">ИД ресурса Azure для VPN-сайта.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-155">The Azure resource ID for the vpn site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceIdByVirtualWanName, ByVpnSiteResourceIdByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanObject, ByVpnSiteResourceIdNoVirtualWanUpdate
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f1ff-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="8f1ff-156">-Tag</span></span>
<span data-ttu-id="8f1ff-157">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-157">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8f1ff-158">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="8f1ff-158">-VirtualWan</span></span>
<span data-ttu-id="8f1ff-159">К этому VPNSite необходимо подключать virtualWan.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-159">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVpnSiteNameByVirtualWanObject, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteResourceIdByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1ff-160">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="8f1ff-160">-VirtualWanId</span></span>
<span data-ttu-id="8f1ff-161">К этому VPNSite должен быть подключен и виртуальный ресурс ResourceId.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-161">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1ff-162">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="8f1ff-162">-VirtualWanName</span></span>
<span data-ttu-id="8f1ff-163">Необходимо подключение к имени виртуальной аны этого VPNSite.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-163">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1ff-164">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f1ff-164">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="8f1ff-165">Имя группы ресурсов virtualWan, к сети VpnSite которого нужно быть подключено.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-165">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1ff-166">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="8f1ff-166">-VpnSiteLink</span></span>
<span data-ttu-id="8f1ff-167">Список VPNSiteLinks, которые есть у этого VPNSite.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-167">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1ff-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f1ff-168">-Confirm</span></span>
<span data-ttu-id="8f1ff-169">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f1ff-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f1ff-170">-WhatIf</span></span>
<span data-ttu-id="8f1ff-171">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f1ff-172">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f1ff-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f1ff-173">CommonParameters</span></span>
<span data-ttu-id="8f1ff-174">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f1ff-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f1ff-175">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f1ff-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f1ff-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f1ff-176">INPUTS</span></span>

### <span data-ttu-id="8f1ff-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="8f1ff-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="8f1ff-178">System.String</span><span class="sxs-lookup"><span data-stu-id="8f1ff-178">System.String</span></span>

## <span data-ttu-id="8f1ff-179">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8f1ff-179">OUTPUTS</span></span>

### <span data-ttu-id="8f1ff-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="8f1ff-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="8f1ff-181">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8f1ff-181">NOTES</span></span>

## <span data-ttu-id="8f1ff-182">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f1ff-182">RELATED LINKS</span></span>

[<span data-ttu-id="8f1ff-183">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="8f1ff-183">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="8f1ff-184">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="8f1ff-184">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="8f1ff-185">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="8f1ff-185">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)
