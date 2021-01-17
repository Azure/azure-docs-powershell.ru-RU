---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
ms.openlocfilehash: 6e67f192cab1d1183d8c8cfd1a38f6c398311bf9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403695"
---
# <span data-ttu-id="5cb03-101">Get-AzVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="5cb03-101">Get-AzVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="5cb03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cb03-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb03-103">Получает конфигурацию Vpn для подмножества VPNSites, подключенных к этой WAN через VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="5cb03-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="5cb03-104">Загружает созданную конфигурацию Vpn в большой объем хранилища, указанный клиентом.</span><span class="sxs-lookup"><span data-stu-id="5cb03-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="5cb03-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5cb03-105">SYNTAX</span></span>

### <span data-ttu-id="5cb03-106">ByVirtualWanNameByVpnSiteObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5cb03-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cb03-107">ByVirtualWanNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="5cb03-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cb03-108">ByVirtualWanObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="5cb03-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cb03-109">ByVirtualWanObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="5cb03-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cb03-110">ByVirtualWanResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="5cb03-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cb03-111">ByVirtualWanResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="5cb03-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cb03-112">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cb03-112">DESCRIPTION</span></span>
<span data-ttu-id="5cb03-113">Получает конфигурацию Vpn для подмножества VPNSites, подключенных к этой WAN через VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="5cb03-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="5cb03-114">Загружает созданную конфигурацию Vpn в большой объем хранилища, указанный клиентом.</span><span class="sxs-lookup"><span data-stu-id="5cb03-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="5cb03-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5cb03-115">EXAMPLES</span></span>

### <span data-ttu-id="5cb03-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5cb03-116">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite

PS C:\> $vpnSitesForConfig = New-Object Microsoft.Azure.Commands.Network.Models.PSVpnSite[] 1
PS C:\> $vpnSitesForConfig[0] = $vpnSite
PS C:\> Get-AzVirtualWanVpnConfiguration -VirtualWan $virtualWan -StorageSasUrl "SignedSasUrl" -VpnSite $vpnSitesForConfig

SasUrl
------
SignedSasUrl
```

<span data-ttu-id="5cb03-117">Выше будет создать группу ресурсов, виртуальную сеть, виртуальную сеть, виртуальный концентратор и VPNSite в западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="5cb03-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="5cb03-118">После этого в виртуальном центре будет создан VPN-шлюз с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="5cb03-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="5cb03-119">Созданный шлюз подключается к VPNSite с помощью команды New-AzVpnConnection входа.</span><span class="sxs-lookup"><span data-stu-id="5cb03-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="5cb03-120">Затем конфигурация загружается с помощью этого командлета.</span><span class="sxs-lookup"><span data-stu-id="5cb03-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="5cb03-121">В случае успешного написания командлета конфигурация скачивания будет записана в BLOB-файл, указанный командлетом SignedSasUrl.</span><span class="sxs-lookup"><span data-stu-id="5cb03-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="5cb03-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cb03-122">PARAMETERS</span></span>

### <span data-ttu-id="5cb03-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cb03-123">-DefaultProfile</span></span>
<span data-ttu-id="5cb03-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5cb03-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cb03-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cb03-125">-InputObject</span></span>
<span data-ttu-id="5cb03-126">Объект VPN-сайта, который нужно изменить</span><span class="sxs-lookup"><span data-stu-id="5cb03-126">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteObject, ByVirtualWanObjectByVpnSiteResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb03-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5cb03-127">-Name</span></span>
<span data-ttu-id="5cb03-128">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="5cb03-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cb03-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cb03-129">-ResourceGroupName</span></span>
<span data-ttu-id="5cb03-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5cb03-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cb03-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cb03-131">-ResourceId</span></span>
<span data-ttu-id="5cb03-132">ИД ресурсов Azure для виртуальной wan.</span><span class="sxs-lookup"><span data-stu-id="5cb03-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb03-133">-StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="5cb03-133">-StorageSasUrl</span></span>
<span data-ttu-id="5cb03-134">URL-адрес SAS для хранилища, в котором будет сгенерирована конфигурация.</span><span class="sxs-lookup"><span data-stu-id="5cb03-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

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

### <span data-ttu-id="5cb03-135">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="5cb03-135">-VpnSite</span></span>
<span data-ttu-id="5cb03-136">Список ИД ресурсов VpnSite, для которые нужно создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="5cb03-136">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite[]
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanObjectByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cb03-137">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="5cb03-137">-VpnSiteId</span></span>
<span data-ttu-id="5cb03-138">Список ИД ресурсов VpnSite, для которые нужно создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="5cb03-138">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVirtualWanNameByVpnSiteResourceId, ByVirtualWanObjectByVpnSiteResourceId, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cb03-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cb03-139">-Confirm</span></span>
<span data-ttu-id="5cb03-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cb03-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cb03-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cb03-141">-WhatIf</span></span>
<span data-ttu-id="5cb03-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cb03-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cb03-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5cb03-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cb03-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb03-144">CommonParameters</span></span>
<span data-ttu-id="5cb03-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cb03-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb03-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cb03-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb03-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5cb03-147">INPUTS</span></span>

### <span data-ttu-id="5cb03-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="5cb03-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="5cb03-149">System.String</span><span class="sxs-lookup"><span data-stu-id="5cb03-149">System.String</span></span>

## <span data-ttu-id="5cb03-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5cb03-150">OUTPUTS</span></span>

### <span data-ttu-id="5cb03-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span><span class="sxs-lookup"><span data-stu-id="5cb03-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="5cb03-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5cb03-152">NOTES</span></span>

## <span data-ttu-id="5cb03-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5cb03-153">RELATED LINKS</span></span>
