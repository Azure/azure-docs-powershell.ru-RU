---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: 271d86db8cd67f75d27e94a5a5dea851cfc9e3b7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074508"
---
# <span data-ttu-id="bd14e-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="bd14e-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="bd14e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd14e-102">SYNOPSIS</span></span>
<span data-ttu-id="bd14e-103">Обновляет сайт VPN.</span><span class="sxs-lookup"><span data-stu-id="bd14e-103">Updates a VPN site.</span></span>

## <span data-ttu-id="bd14e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd14e-104">SYNTAX</span></span>

### <span data-ttu-id="bd14e-105">ByVpnSiteNameNoVirtualWanUpdate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd14e-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd14e-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="bd14e-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd14e-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="bd14e-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd14e-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="bd14e-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd14e-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="bd14e-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd14e-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="bd14e-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd14e-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="bd14e-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd14e-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="bd14e-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd14e-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="bd14e-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd14e-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="bd14e-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd14e-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="bd14e-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd14e-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="bd14e-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd14e-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd14e-117">DESCRIPTION</span></span>
<span data-ttu-id="bd14e-118">Командлет **Update-AzVpnSite** ОБНОВЛЯЕТ сайт VPN.</span><span class="sxs-lookup"><span data-stu-id="bd14e-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="bd14e-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd14e-119">EXAMPLES</span></span>

### <span data-ttu-id="bd14e-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd14e-120">Example 1</span></span>

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

<span data-ttu-id="bd14e-121">В приведенном выше примере будет создана группа ресурсов, Виртуальная глобальная сеть в Запад США в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="bd14e-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="bd14e-122">Затем он создает VpnSite для представления ветви клиента и связывает ее с виртуальной глобальной сетью.</span><span class="sxs-lookup"><span data-stu-id="bd14e-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="bd14e-123">После создания сайта он обновляет IP-адрес сайта с помощью команды Set-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="bd14e-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="bd14e-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd14e-124">PARAMETERS</span></span>

### <span data-ttu-id="bd14e-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="bd14e-125">-AddressSpace</span></span>
<span data-ttu-id="bd14e-126">Префиксы адреса виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="bd14e-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="bd14e-127">Используйте этот или AddressSpaceObject, но не оба.</span><span class="sxs-lookup"><span data-stu-id="bd14e-127">Use this or AddressSpaceObject but not both.</span></span>

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

### <span data-ttu-id="bd14e-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd14e-128">-AsJob</span></span>
<span data-ttu-id="bd14e-129">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bd14e-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd14e-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="bd14e-130">-BgpAsn</span></span>
<span data-ttu-id="bd14e-131">BGP ASN для этого VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bd14e-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="bd14e-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="bd14e-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="bd14e-133">Адрес пиринга BGP для этого VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bd14e-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="bd14e-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="bd14e-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="bd14e-135">Вес пиринга BGP для этого VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bd14e-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="bd14e-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd14e-136">-DefaultProfile</span></span>
<span data-ttu-id="bd14e-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd14e-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd14e-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="bd14e-138">-DeviceModel</span></span>
<span data-ttu-id="bd14e-139">Модель устройства для удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="bd14e-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="bd14e-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="bd14e-140">-DeviceVendor</span></span>
<span data-ttu-id="bd14e-141">Поставщик устройства для удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="bd14e-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="bd14e-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd14e-142">-InputObject</span></span>
<span data-ttu-id="bd14e-143">Объект VPN-сайта, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="bd14e-143">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="bd14e-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="bd14e-144">-IpAddress</span></span>
<span data-ttu-id="bd14e-145">IP-адрес шлюза локальной сети.</span><span class="sxs-lookup"><span data-stu-id="bd14e-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="bd14e-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="bd14e-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="bd14e-147">Модель устройства для удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="bd14e-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="bd14e-148">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bd14e-148">-Name</span></span>
<span data-ttu-id="bd14e-149">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="bd14e-149">The resource name.</span></span>

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

### <span data-ttu-id="bd14e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd14e-150">-ResourceGroupName</span></span>
<span data-ttu-id="bd14e-151">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd14e-151">The resource group name.</span></span>

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

### <span data-ttu-id="bd14e-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd14e-152">-ResourceId</span></span>
<span data-ttu-id="bd14e-153">Идентификатор ресурса Azure для VPN-сайта.</span><span class="sxs-lookup"><span data-stu-id="bd14e-153">The Azure resource ID for the vpn site.</span></span>

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

### <span data-ttu-id="bd14e-154">-Тег</span><span class="sxs-lookup"><span data-stu-id="bd14e-154">-Tag</span></span>
<span data-ttu-id="bd14e-155">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd14e-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="bd14e-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="bd14e-156">-VirtualWan</span></span>
<span data-ttu-id="bd14e-157">VirtualWan, к которому необходимо подключить этот VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bd14e-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="bd14e-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="bd14e-158">-VirtualWanId</span></span>
<span data-ttu-id="bd14e-159">ResourceId VirtualWan, к которому необходимо подключить этот VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bd14e-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="bd14e-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="bd14e-160">-VirtualWanName</span></span>
<span data-ttu-id="bd14e-161">Имя VirtualWan, к которому необходимо подключить этот VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bd14e-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="bd14e-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd14e-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="bd14e-163">Имя группы ресурсов VirtualWan, к которой нужно подключить этот VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bd14e-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="bd14e-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="bd14e-164">-VpnSiteLink</span></span>
<span data-ttu-id="bd14e-165">Список VpnSiteLinks, которые есть в этой VpnSite.</span><span class="sxs-lookup"><span data-stu-id="bd14e-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="bd14e-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd14e-166">-Confirm</span></span>
<span data-ttu-id="bd14e-167">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bd14e-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd14e-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd14e-168">-WhatIf</span></span>
<span data-ttu-id="bd14e-169">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bd14e-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd14e-170">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bd14e-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd14e-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd14e-171">CommonParameters</span></span>
<span data-ttu-id="bd14e-172">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd14e-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd14e-173">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd14e-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd14e-174">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd14e-174">INPUTS</span></span>

### <span data-ttu-id="bd14e-175">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="bd14e-175">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="bd14e-176">System. String</span><span class="sxs-lookup"><span data-stu-id="bd14e-176">System.String</span></span>

## <span data-ttu-id="bd14e-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd14e-177">OUTPUTS</span></span>

### <span data-ttu-id="bd14e-178">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="bd14e-178">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="bd14e-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd14e-179">NOTES</span></span>

## <span data-ttu-id="bd14e-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd14e-180">RELATED LINKS</span></span>

[<span data-ttu-id="bd14e-181">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="bd14e-181">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="bd14e-182">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="bd14e-182">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="bd14e-183">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="bd14e-183">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)
