---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWanVpnConfiguration.md
ms.openlocfilehash: be0fbc9b9fc6d91a5bf94344f432b67dfc38cab3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562936"
---
# <span data-ttu-id="ee9b6-101">Get-AzureRmVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee9b6-101">Get-AzureRmVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="ee9b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee9b6-102">SYNOPSIS</span></span>
<span data-ttu-id="ee9b6-103">Возвращает конфигурацию VPN для подмножества VpnSites, подключенного к этой глобальной сети через VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="ee9b6-104">Передает созданную конфигурацию VPN в большой двоичный объект хранилища, указанный клиентом.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee9b6-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee9b6-105">SYNTAX</span></span>

### <span data-ttu-id="ee9b6-106">ByVirtualWanNameByVpnSiteObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee9b6-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee9b6-107">ByVirtualWanNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="ee9b6-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee9b6-108">ByVirtualWanObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="ee9b6-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee9b6-109">ByVirtualWanObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="ee9b6-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee9b6-110">ByVirtualWanResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="ee9b6-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee9b6-111">ByVirtualWanResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="ee9b6-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee9b6-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee9b6-112">DESCRIPTION</span></span>
<span data-ttu-id="ee9b6-113">Возвращает конфигурацию VPN для подмножества VpnSites, подключенного к этой глобальной сети через VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="ee9b6-114">Передает созданную конфигурацию VPN в большой двоичный объект хранилища, указанный клиентом.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="ee9b6-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee9b6-115">EXAMPLES</span></span>

### <span data-ttu-id="ee9b6-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ee9b6-116">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite

PS C:\> $vpnSitesForConfig = New-Object Microsoft.Azure.Commands.Network.Models.PSVpnSite[] 1
PS C:\> $vpnSitesForConfig[0] = $vpnSite
PS C:\> Get-AzureRmVirtualWanVpnConfiguration -VirtualWan $virtualWan -StorageSasUrl "SignedSasUrl" -VpnSite $vpnSitesForConfig

SasUrl
------
SignedSasUrl
```

<span data-ttu-id="ee9b6-117">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую службу, виртуальный концентратор и VpnSite в области "Западная часть США" в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="ee9b6-118">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="ee9b6-119">После создания шлюза он подключается к VpnSite с помощью команды New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="ee9b6-120">Затем конфигурация загружается с помощью этого unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="ee9b6-121">Если unifiedgroup успешно, конфигурация загрузки будет записываться в большой двоичный объект, указываемый в SignedSasUrl.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="ee9b6-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee9b6-122">PARAMETERS</span></span>

### <span data-ttu-id="ee9b6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee9b6-123">-DefaultProfile</span></span>
<span data-ttu-id="ee9b6-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee9b6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee9b6-125">-InputObject</span></span>
<span data-ttu-id="ee9b6-126">Объект VPN-сайта, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-126">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="ee9b6-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ee9b6-127">-Name</span></span>
<span data-ttu-id="ee9b6-128">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-128">The resource name.</span></span>

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

### <span data-ttu-id="ee9b6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee9b6-129">-ResourceGroupName</span></span>
<span data-ttu-id="ee9b6-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-130">The resource group name.</span></span>

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

### <span data-ttu-id="ee9b6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee9b6-131">-ResourceId</span></span>
<span data-ttu-id="ee9b6-132">Идентификатор ресурса Azure для виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-132">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="ee9b6-133">-StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="ee9b6-133">-StorageSasUrl</span></span>
<span data-ttu-id="ee9b6-134">URL-адрес SAS для места хранения, в котором нужно создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

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

### <span data-ttu-id="ee9b6-135">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ee9b6-135">-VpnSite</span></span>
<span data-ttu-id="ee9b6-136">Список идентификаторов ресурсов VpnSite для создания конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-136">The list of VpnSite resource ids to generate configuration for.</span></span>

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

### <span data-ttu-id="ee9b6-137">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="ee9b6-137">-VpnSiteId</span></span>
<span data-ttu-id="ee9b6-138">Список идентификаторов ресурсов VpnSite для создания конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-138">The list of VpnSite resource ids to generate configuration for.</span></span>

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

### <span data-ttu-id="ee9b6-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee9b6-139">-Confirm</span></span>
<span data-ttu-id="ee9b6-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee9b6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee9b6-141">-WhatIf</span></span>
<span data-ttu-id="ee9b6-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee9b6-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee9b6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee9b6-144">CommonParameters</span></span>
<span data-ttu-id="ee9b6-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee9b6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee9b6-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee9b6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee9b6-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee9b6-147">INPUTS</span></span>

### <span data-ttu-id="ee9b6-148">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ee9b6-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="ee9b6-149">System. String</span><span class="sxs-lookup"><span data-stu-id="ee9b6-149">System.String</span></span>

## <span data-ttu-id="ee9b6-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee9b6-150">OUTPUTS</span></span>

### <span data-ttu-id="ee9b6-151">Microsoft. Azure. Commands. Network. Models. PSVirtualWanVpnSitesConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee9b6-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="ee9b6-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee9b6-152">NOTES</span></span>

## <span data-ttu-id="ee9b6-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee9b6-153">RELATED LINKS</span></span>
