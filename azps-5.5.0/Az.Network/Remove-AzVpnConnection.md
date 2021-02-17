---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 825090358ea94223d483fe418d06896f1f741045
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225761"
---
# <span data-ttu-id="32c23-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="32c23-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="32c23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32c23-102">SYNOPSIS</span></span>
<span data-ttu-id="32c23-103">Удаляет VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="32c23-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="32c23-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="32c23-104">SYNTAX</span></span>

### <span data-ttu-id="32c23-105">ByVpnConnectionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32c23-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32c23-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="32c23-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32c23-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="32c23-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32c23-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32c23-108">DESCRIPTION</span></span>
<span data-ttu-id="32c23-109">Удаляет VPNConnection.</span><span class="sxs-lookup"><span data-stu-id="32c23-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="32c23-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="32c23-110">EXAMPLES</span></span>

### <span data-ttu-id="32c23-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32c23-111">Example 1</span></span>
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
PS C:\> Remove-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="32c23-112">Выше будет создать группу ресурсов, виртуальную сеть, виртуальную сеть, виртуальный концентратор и VPNSite в западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="32c23-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="32c23-113">После этого в виртуальном центре будет создан VPN-шлюз с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="32c23-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="32c23-114">Созданный шлюз подключается к VPNSite с помощью команды New-AzVpnConnection входа.</span><span class="sxs-lookup"><span data-stu-id="32c23-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="32c23-115">Затем соединение удаляется с использованием имени подключения.</span><span class="sxs-lookup"><span data-stu-id="32c23-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="32c23-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="32c23-116">Example 2</span></span>

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
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzVpnConnection
```

<span data-ttu-id="32c23-117">То же, что и в примере 1, но теперь соединение с помощью канала Get-AzVpnConnection удаляется.</span><span class="sxs-lookup"><span data-stu-id="32c23-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="32c23-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32c23-118">PARAMETERS</span></span>

### <span data-ttu-id="32c23-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32c23-119">-DefaultProfile</span></span>
<span data-ttu-id="32c23-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32c23-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32c23-121">-Force</span><span class="sxs-lookup"><span data-stu-id="32c23-121">-Force</span></span>
<span data-ttu-id="32c23-122">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="32c23-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="32c23-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32c23-123">-InputObject</span></span>
<span data-ttu-id="32c23-124">Объект VpnConnection, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="32c23-124">The VpnConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32c23-125">-Name</span><span class="sxs-lookup"><span data-stu-id="32c23-125">-Name</span></span>
<span data-ttu-id="32c23-126">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="32c23-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32c23-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="32c23-127">-ParentResourceName</span></span>
<span data-ttu-id="32c23-128">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="32c23-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32c23-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32c23-129">-PassThru</span></span>
<span data-ttu-id="32c23-130">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="32c23-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="32c23-131">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="32c23-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="32c23-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32c23-132">-ResourceGroupName</span></span>
<span data-ttu-id="32c23-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32c23-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32c23-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32c23-134">-ResourceId</span></span>
<span data-ttu-id="32c23-135">ИД ресурса объекта VpnConnection, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="32c23-135">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32c23-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32c23-136">-Confirm</span></span>
<span data-ttu-id="32c23-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="32c23-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32c23-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32c23-138">-WhatIf</span></span>
<span data-ttu-id="32c23-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32c23-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32c23-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="32c23-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32c23-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32c23-141">CommonParameters</span></span>
<span data-ttu-id="32c23-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32c23-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32c23-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32c23-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32c23-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32c23-144">INPUTS</span></span>

### <span data-ttu-id="32c23-145">System.String</span><span class="sxs-lookup"><span data-stu-id="32c23-145">System.String</span></span>

### <span data-ttu-id="32c23-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="32c23-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="32c23-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="32c23-147">OUTPUTS</span></span>

### <span data-ttu-id="32c23-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="32c23-148">System.Boolean</span></span>

## <span data-ttu-id="32c23-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="32c23-149">NOTES</span></span>

## <span data-ttu-id="32c23-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32c23-150">RELATED LINKS</span></span>

[<span data-ttu-id="32c23-151">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="32c23-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="32c23-152">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="32c23-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="32c23-153">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="32c23-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
