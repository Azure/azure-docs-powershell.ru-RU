---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: 980b84fd1b23cb7e4b034dee485b785b96893f11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730237"
---
# <span data-ttu-id="b2637-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b2637-101">New-AzVpnSite</span></span>

## <span data-ttu-id="b2637-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2637-102">SYNOPSIS</span></span>
<span data-ttu-id="b2637-103">Создание нового ресурса Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="b2637-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="b2637-104">Это представление RM для ветвей клиентов, которые отправляются в подключение к Azure для S2S с помощью виртуального концентратора Cortex.</span><span class="sxs-lookup"><span data-stu-id="b2637-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="b2637-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2637-105">SYNTAX</span></span>

### <span data-ttu-id="b2637-106">ByVirtualWanName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b2637-106">ByVirtualWanName (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2637-107">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="b2637-107">ByVirtualWanObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2637-108">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="b2637-108">ByVirtualWanResourceId</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2637-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2637-109">DESCRIPTION</span></span>
<span data-ttu-id="b2637-110">Создание нового ресурса Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="b2637-110">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="b2637-111">Это представление RM для ветвей клиентов, которые отправляются в подключение к Azure для S2S с помощью виртуального концентратора Cortex.</span><span class="sxs-lookup"><span data-stu-id="b2637-111">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="b2637-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2637-112">EXAMPLES</span></span>

### <span data-ttu-id="b2637-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b2637-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="b2637-114">В приведенном выше примере будет создана группа ресурсов, Виртуальная глобальная сеть в Запад США в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="b2637-114">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="b2637-115">Затем он создает VpnSite для представления ветви клиента и связывает ее с виртуальной глобальной сетью.</span><span class="sxs-lookup"><span data-stu-id="b2637-115">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="b2637-116">Подключение IPSec можно настроить с помощью этой ветви и VpnGateway, используя команду "New-AzVpnConnection".</span><span class="sxs-lookup"><span data-stu-id="b2637-116">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

## <span data-ttu-id="b2637-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2637-117">PARAMETERS</span></span>

### <span data-ttu-id="b2637-118">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="b2637-118">-AddressSpace</span></span>
<span data-ttu-id="b2637-119">Префиксы адреса виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b2637-119">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="b2637-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2637-120">-AsJob</span></span>
<span data-ttu-id="b2637-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b2637-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2637-122">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="b2637-122">-BgpAsn</span></span>
<span data-ttu-id="b2637-123">BGP ASN для этого VpnSite.</span><span class="sxs-lookup"><span data-stu-id="b2637-123">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="b2637-124">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="b2637-124">-BgpPeeringAddress</span></span>
<span data-ttu-id="b2637-125">Адрес пиринга BGP для этого VpnSite.</span><span class="sxs-lookup"><span data-stu-id="b2637-125">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="b2637-126">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="b2637-126">-BgpPeeringWeight</span></span>
<span data-ttu-id="b2637-127">Вес пиринга BGP для этого VpnSite.</span><span class="sxs-lookup"><span data-stu-id="b2637-127">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="b2637-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2637-128">-DefaultProfile</span></span>
<span data-ttu-id="b2637-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2637-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2637-130">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="b2637-130">-DeviceModel</span></span>
<span data-ttu-id="b2637-131">Модель устройства для удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="b2637-131">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="b2637-132">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="b2637-132">-DeviceVendor</span></span>
<span data-ttu-id="b2637-133">Поставщик устройства для удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="b2637-133">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="b2637-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="b2637-134">-IpAddress</span></span>
<span data-ttu-id="b2637-135">IP-адрес для этого VpnSite.</span><span class="sxs-lookup"><span data-stu-id="b2637-135">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="b2637-136">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="b2637-136">-LinkSpeedInMbps</span></span>
<span data-ttu-id="b2637-137">Модель устройства для удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="b2637-137">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="b2637-138">-Location</span><span class="sxs-lookup"><span data-stu-id="b2637-138">-Location</span></span>
<span data-ttu-id="b2637-139">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="b2637-139">The resource location.</span></span>

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

### <span data-ttu-id="b2637-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b2637-140">-Name</span></span>
<span data-ttu-id="b2637-141">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="b2637-141">The resource name.</span></span>

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

### <span data-ttu-id="b2637-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2637-142">-ResourceGroupName</span></span>
<span data-ttu-id="b2637-143">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="b2637-143">The resource name.</span></span>

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

### <span data-ttu-id="b2637-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="b2637-144">-Tag</span></span>
<span data-ttu-id="b2637-145">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2637-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b2637-146">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="b2637-146">-VirtualWan</span></span>
<span data-ttu-id="b2637-147">VirtualWan, к которому необходимо подключить этот VpnSite.</span><span class="sxs-lookup"><span data-stu-id="b2637-147">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2637-148">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="b2637-148">-VirtualWanId</span></span>
<span data-ttu-id="b2637-149">ResourceId VirtualWan, к которому необходимо подключить этот VpnSite.</span><span class="sxs-lookup"><span data-stu-id="b2637-149">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2637-150">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="b2637-150">-VirtualWanName</span></span>
<span data-ttu-id="b2637-151">Имя VirtualWan, к которому необходимо подключить этот VpnSite.</span><span class="sxs-lookup"><span data-stu-id="b2637-151">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2637-152">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2637-152">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="b2637-153">Имя группы ресурсов VirtualWan, к которой нужно подключить этот VpnSite.</span><span class="sxs-lookup"><span data-stu-id="b2637-153">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2637-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2637-154">-Confirm</span></span>
<span data-ttu-id="b2637-155">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b2637-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2637-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2637-156">-WhatIf</span></span>
<span data-ttu-id="b2637-157">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b2637-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2637-158">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b2637-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2637-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2637-159">CommonParameters</span></span>
<span data-ttu-id="b2637-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2637-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2637-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2637-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2637-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2637-162">INPUTS</span></span>

### <span data-ttu-id="b2637-163">Ничего</span><span class="sxs-lookup"><span data-stu-id="b2637-163">None</span></span>

## <span data-ttu-id="b2637-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2637-164">OUTPUTS</span></span>

### <span data-ttu-id="b2637-165">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="b2637-165">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="b2637-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2637-166">NOTES</span></span>

## <span data-ttu-id="b2637-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2637-167">RELATED LINKS</span></span>

[<span data-ttu-id="b2637-168">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b2637-168">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="b2637-169">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b2637-169">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="b2637-170">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b2637-170">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
