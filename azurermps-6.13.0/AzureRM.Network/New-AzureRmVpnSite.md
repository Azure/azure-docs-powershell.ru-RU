---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnSite.md
ms.openlocfilehash: b8594aab0b9475ed37a0a205010e92fdb2a4db7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732308"
---
# <span data-ttu-id="2cb55-101">New-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="2cb55-101">New-AzureRmVpnSite</span></span>

## <span data-ttu-id="2cb55-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2cb55-102">SYNOPSIS</span></span>
<span data-ttu-id="2cb55-103">Создание нового ресурса Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="2cb55-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="2cb55-104">Это представление RM для ветвей клиентов, которые отправляются в подключение к Azure для S2S с помощью виртуального концентратора Cortex.</span><span class="sxs-lookup"><span data-stu-id="2cb55-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cb55-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2cb55-105">SYNTAX</span></span>

### <span data-ttu-id="2cb55-106">ByVirtualWanName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2cb55-106">ByVirtualWanName (Default)</span></span>
```
New-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cb55-107">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="2cb55-107">ByVirtualWanObject</span></span>
```
New-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2cb55-108">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="2cb55-108">ByVirtualWanResourceId</span></span>
```
New-AzureRmVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2cb55-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cb55-109">DESCRIPTION</span></span>
<span data-ttu-id="2cb55-110">Создание нового ресурса Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="2cb55-110">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="2cb55-111">Это представление RM для ветвей клиентов, которые отправляются в подключение к Azure для S2S с помощью виртуального концентратора Cortex.</span><span class="sxs-lookup"><span data-stu-id="2cb55-111">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="2cb55-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2cb55-112">EXAMPLES</span></span>

### <span data-ttu-id="2cb55-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2cb55-113">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

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

<span data-ttu-id="2cb55-114">В приведенном выше примере будет создана группа ресурсов, Виртуальная глобальная сеть в Запад США в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="2cb55-114">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="2cb55-115">Затем он создает VpnSite для представления ветви клиента и связывает ее с виртуальной глобальной сетью.</span><span class="sxs-lookup"><span data-stu-id="2cb55-115">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="2cb55-116">Подключение IPSec можно настроить с помощью этой ветви и VpnGateway, используя команду "New-AzureRmVpnConnection".</span><span class="sxs-lookup"><span data-stu-id="2cb55-116">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzureRmVpnConnection command.</span></span>

## <span data-ttu-id="2cb55-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2cb55-117">PARAMETERS</span></span>

### <span data-ttu-id="2cb55-118">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="2cb55-118">-AddressSpace</span></span>
<span data-ttu-id="2cb55-119">Префиксы адреса виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2cb55-119">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="2cb55-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cb55-120">-AsJob</span></span>
<span data-ttu-id="2cb55-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2cb55-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2cb55-122">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="2cb55-122">-BgpAsn</span></span>
<span data-ttu-id="2cb55-123">BGP ASN для этого VpnSite.</span><span class="sxs-lookup"><span data-stu-id="2cb55-123">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="2cb55-124">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="2cb55-124">-BgpPeeringAddress</span></span>
<span data-ttu-id="2cb55-125">Адрес пиринга BGP для этого VpnSite.</span><span class="sxs-lookup"><span data-stu-id="2cb55-125">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="2cb55-126">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="2cb55-126">-BgpPeeringWeight</span></span>
<span data-ttu-id="2cb55-127">Вес пиринга BGP для этого VpnSite.</span><span class="sxs-lookup"><span data-stu-id="2cb55-127">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="2cb55-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cb55-128">-DefaultProfile</span></span>
<span data-ttu-id="2cb55-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2cb55-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb55-130">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="2cb55-130">-DeviceModel</span></span>
<span data-ttu-id="2cb55-131">Модель устройства для удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="2cb55-131">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="2cb55-132">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="2cb55-132">-DeviceVendor</span></span>
<span data-ttu-id="2cb55-133">Поставщик устройства для удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="2cb55-133">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="2cb55-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="2cb55-134">-IpAddress</span></span>
<span data-ttu-id="2cb55-135">IP-адрес для этого VpnSite.</span><span class="sxs-lookup"><span data-stu-id="2cb55-135">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="2cb55-136">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="2cb55-136">-LinkSpeedInMbps</span></span>
<span data-ttu-id="2cb55-137">Модель устройства для удаленного VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="2cb55-137">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="2cb55-138">-Location</span><span class="sxs-lookup"><span data-stu-id="2cb55-138">-Location</span></span>
<span data-ttu-id="2cb55-139">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="2cb55-139">The resource location.</span></span>

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

### <span data-ttu-id="2cb55-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2cb55-140">-Name</span></span>
<span data-ttu-id="2cb55-141">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2cb55-141">The resource name.</span></span>

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

### <span data-ttu-id="2cb55-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cb55-142">-ResourceGroupName</span></span>
<span data-ttu-id="2cb55-143">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2cb55-143">The resource name.</span></span>

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

### <span data-ttu-id="2cb55-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="2cb55-144">-Tag</span></span>
<span data-ttu-id="2cb55-145">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2cb55-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="2cb55-146">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="2cb55-146">-VirtualWan</span></span>
<span data-ttu-id="2cb55-147">VirtualWan, к которому необходимо подключить этот VpnSite.</span><span class="sxs-lookup"><span data-stu-id="2cb55-147">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="2cb55-148">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="2cb55-148">-VirtualWanId</span></span>
<span data-ttu-id="2cb55-149">ResourceId VirtualWan, к которому необходимо подключить этот VpnSite.</span><span class="sxs-lookup"><span data-stu-id="2cb55-149">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="2cb55-150">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="2cb55-150">-VirtualWanName</span></span>
<span data-ttu-id="2cb55-151">Имя VirtualWan, к которому необходимо подключить этот VpnSite.</span><span class="sxs-lookup"><span data-stu-id="2cb55-151">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="2cb55-152">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cb55-152">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="2cb55-153">Имя группы ресурсов VirtualWan, к которой нужно подключить этот VpnSite.</span><span class="sxs-lookup"><span data-stu-id="2cb55-153">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="2cb55-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cb55-154">-Confirm</span></span>
<span data-ttu-id="2cb55-155">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2cb55-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cb55-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cb55-156">-WhatIf</span></span>
<span data-ttu-id="2cb55-157">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2cb55-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cb55-158">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2cb55-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cb55-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cb55-159">CommonParameters</span></span>
<span data-ttu-id="2cb55-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2cb55-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cb55-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cb55-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cb55-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2cb55-162">INPUTS</span></span>

### <span data-ttu-id="2cb55-163">Ничего</span><span class="sxs-lookup"><span data-stu-id="2cb55-163">None</span></span>

## <span data-ttu-id="2cb55-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cb55-164">OUTPUTS</span></span>

### <span data-ttu-id="2cb55-165">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="2cb55-165">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="2cb55-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="2cb55-166">NOTES</span></span>

## <span data-ttu-id="2cb55-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2cb55-167">RELATED LINKS</span></span>
