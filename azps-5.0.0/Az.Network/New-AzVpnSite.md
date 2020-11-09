---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: ac203d499674e97080edd645f9643b12291873d1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319208"
---
# <span data-ttu-id="5d520-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="5d520-101">New-AzVpnSite</span></span>

## <span data-ttu-id="5d520-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d520-102">SYNOPSIS</span></span>
<span data-ttu-id="5d520-103">Создание нового ресурса Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="5d520-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="5d520-104">Это представление RM для ветвей клиентов, которые отправляются в подключение к Azure для S2S с помощью виртуального концентратора Cortex.</span><span class="sxs-lookup"><span data-stu-id="5d520-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="5d520-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d520-105">SYNTAX</span></span>

### <span data-ttu-id="5d520-106">ByVirtualWanNameByVpnSiteIpAddress (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d520-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d520-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="5d520-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d520-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="5d520-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d520-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="5d520-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d520-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="5d520-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d520-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="5d520-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d520-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d520-112">DESCRIPTION</span></span>
<span data-ttu-id="5d520-113">Создание нового ресурса Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="5d520-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="5d520-114">Это представление RM для ветвей клиентов, которые отправляются в подключение к Azure для S2S с помощью виртуального концентратора Cortex.</span><span class="sxs-lookup"><span data-stu-id="5d520-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="5d520-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d520-115">EXAMPLES</span></span>

### <span data-ttu-id="5d520-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5d520-116">Example 1</span></span>

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

<span data-ttu-id="5d520-117">В примере выше будет создана группа ресурсов, Виртуальная глобальная сеть в Восточной США в группе ресурсов "nonlinkSite" в Azure.</span><span class="sxs-lookup"><span data-stu-id="5d520-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="5d520-118">Затем он создает VpnSite для представления ветви клиента и связывает ее с виртуальной глобальной сетью.</span><span class="sxs-lookup"><span data-stu-id="5d520-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="5d520-119">Подключение IPSec можно настроить с помощью этой ветви и VpnGateway, используя команду "New-AzVpnConnection".</span><span class="sxs-lookup"><span data-stu-id="5d520-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="5d520-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5d520-120">Example 2</span></span>
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

<span data-ttu-id="5d520-121">В описанном выше примере вы создадите группу ресурсов, виртуальную глобальную сеть и VpnSite с 1 VpnSiteLinks в группе ресурсов "многоканальная связь" в Azure.</span><span class="sxs-lookup"><span data-stu-id="5d520-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="5d520-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5d520-122">Example 3</span></span>

<span data-ttu-id="5d520-123">Создание нового ресурса Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="5d520-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="5d520-124">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="5d520-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="5d520-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d520-125">PARAMETERS</span></span>

### <span data-ttu-id="5d520-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="5d520-126">-AddressSpace</span></span>
<span data-ttu-id="5d520-127">Префиксы адреса виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5d520-127">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="5d520-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d520-128">-AsJob</span></span>
<span data-ttu-id="5d520-129">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5d520-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d520-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="5d520-130">-BgpAsn</span></span>
<span data-ttu-id="5d520-131">BGP ASN для этого VpnSite.</span><span class="sxs-lookup"><span data-stu-id="5d520-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="5d520-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="5d520-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="5d520-133">Адрес пиринга BGP для этого VpnSite.</span><span class="sxs-lookup"><span data-stu-id="5d520-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="5d520-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="5d520-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="5d520-135">Вес пиринга BGP для этого VpnSite.</span><span class="sxs-lookup"><span data-stu-id="5d520-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="5d520-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d520-136">-DefaultProfile</span></span>
<span data-ttu-id="5d520-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d520-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d520-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="5d520-138">-DeviceModel</span></span>
<span data-ttu-id="5d520-139">Модель устройства для удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="5d520-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="5d520-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="5d520-140">-DeviceVendor</span></span>
<span data-ttu-id="5d520-141">Поставщик устройства для удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="5d520-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="5d520-142">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="5d520-142">-IpAddress</span></span>
<span data-ttu-id="5d520-143">IP-адрес для этого VpnSite.</span><span class="sxs-lookup"><span data-stu-id="5d520-143">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="5d520-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="5d520-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="5d520-145">Модель устройства для удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="5d520-145">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="5d520-146">-Location</span><span class="sxs-lookup"><span data-stu-id="5d520-146">-Location</span></span>
<span data-ttu-id="5d520-147">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="5d520-147">The resource location.</span></span>

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

### <span data-ttu-id="5d520-148">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d520-148">-Name</span></span>
<span data-ttu-id="5d520-149">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="5d520-149">The resource name.</span></span>

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

### <span data-ttu-id="5d520-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="5d520-150">-O365Policy</span></span>
<span data-ttu-id="5d520-151">Политика трафика Office 365 для этого VpnSite.</span><span class="sxs-lookup"><span data-stu-id="5d520-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="5d520-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d520-152">-ResourceGroupName</span></span>
<span data-ttu-id="5d520-153">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="5d520-153">The resource name.</span></span>

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

### <span data-ttu-id="5d520-154">-Тег</span><span class="sxs-lookup"><span data-stu-id="5d520-154">-Tag</span></span>
<span data-ttu-id="5d520-155">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d520-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="5d520-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="5d520-156">-VirtualWan</span></span>
<span data-ttu-id="5d520-157">VirtualWan, к которому необходимо подключить этот VpnSite.</span><span class="sxs-lookup"><span data-stu-id="5d520-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="5d520-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="5d520-158">-VirtualWanId</span></span>
<span data-ttu-id="5d520-159">ResourceId VirtualWan, к которому необходимо подключить этот VpnSite.</span><span class="sxs-lookup"><span data-stu-id="5d520-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="5d520-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="5d520-160">-VirtualWanName</span></span>
<span data-ttu-id="5d520-161">Имя VirtualWan, к которому необходимо подключить этот VpnSite.</span><span class="sxs-lookup"><span data-stu-id="5d520-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="5d520-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d520-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="5d520-163">Имя группы ресурсов VirtualWan, к которой нужно подключить этот VpnSite.</span><span class="sxs-lookup"><span data-stu-id="5d520-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="5d520-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="5d520-164">-VpnSiteLink</span></span>
<span data-ttu-id="5d520-165">Список VpnSiteLinks, которые есть в этой VpnSite.</span><span class="sxs-lookup"><span data-stu-id="5d520-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="5d520-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d520-166">-Confirm</span></span>
<span data-ttu-id="5d520-167">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5d520-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d520-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d520-168">-WhatIf</span></span>
<span data-ttu-id="5d520-169">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5d520-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d520-170">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d520-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d520-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d520-171">CommonParameters</span></span>
<span data-ttu-id="5d520-172">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d520-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d520-173">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d520-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d520-174">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d520-174">INPUTS</span></span>

### <span data-ttu-id="5d520-175">Ничего</span><span class="sxs-lookup"><span data-stu-id="5d520-175">None</span></span>

## <span data-ttu-id="5d520-176">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d520-176">OUTPUTS</span></span>

### <span data-ttu-id="5d520-177">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="5d520-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="5d520-178">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d520-178">NOTES</span></span>

## <span data-ttu-id="5d520-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d520-179">RELATED LINKS</span></span>

[<span data-ttu-id="5d520-180">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="5d520-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="5d520-181">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="5d520-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="5d520-182">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="5d520-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
