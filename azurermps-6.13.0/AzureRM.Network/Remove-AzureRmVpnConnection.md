---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnConnection.md
ms.openlocfilehash: da023b7c0b060e9e263b6b0677065746568524b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562792"
---
# <span data-ttu-id="b45e8-101">Remove-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b45e8-101">Remove-AzureRmVpnConnection</span></span>

## <span data-ttu-id="b45e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b45e8-102">SYNOPSIS</span></span>
<span data-ttu-id="b45e8-103">Удаление VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="b45e8-103">Removes a VpnConnection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b45e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b45e8-104">SYNTAX</span></span>

### <span data-ttu-id="b45e8-105">ByVpnConnectionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b45e8-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b45e8-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="b45e8-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzureRmVpnConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b45e8-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="b45e8-107">ByVpnConnectionObject</span></span>
```
Remove-AzureRmVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b45e8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b45e8-108">DESCRIPTION</span></span>
<span data-ttu-id="b45e8-109">Удаление VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="b45e8-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="b45e8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b45e8-110">EXAMPLES</span></span>

### <span data-ttu-id="b45e8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b45e8-111">Example 1</span></span>
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
PS C:\> Remove-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="b45e8-112">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую службу, виртуальный концентратор и VpnSite в области "Западная часть США" в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="b45e8-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="b45e8-113">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="b45e8-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="b45e8-114">После создания шлюза он подключается к VpnSite с помощью команды New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="b45e8-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="b45e8-115">После этого соединение будет удалено с помощью имени соединения.</span><span class="sxs-lookup"><span data-stu-id="b45e8-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="b45e8-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b45e8-116">Example 2</span></span>

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
PS C:\> Get-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzureRmVpnConnection
```

<span data-ttu-id="b45e8-117">То же, что и в примере 1, но теперь он удаляет подключение, используя объект, переданный из командлета Get-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="b45e8-117">Same as example 1, but it now removes the connection using the piped object from Get-AzureRmVpnConnection.</span></span>

## <span data-ttu-id="b45e8-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b45e8-118">PARAMETERS</span></span>

### <span data-ttu-id="b45e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b45e8-119">-DefaultProfile</span></span>
<span data-ttu-id="b45e8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b45e8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b45e8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b45e8-121">-Force</span></span>
<span data-ttu-id="b45e8-122">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="b45e8-122">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="b45e8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b45e8-123">-InputObject</span></span>
<span data-ttu-id="b45e8-124">Объект VpnConenction, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="b45e8-124">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="b45e8-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b45e8-125">-Name</span></span>
<span data-ttu-id="b45e8-126">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="b45e8-126">The resource name.</span></span>

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

### <span data-ttu-id="b45e8-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="b45e8-127">-ParentResourceName</span></span>
<span data-ttu-id="b45e8-128">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="b45e8-128">The parent resource name.</span></span>

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

### <span data-ttu-id="b45e8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b45e8-129">-PassThru</span></span>
<span data-ttu-id="b45e8-130">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b45e8-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b45e8-131">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b45e8-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b45e8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b45e8-132">-ResourceGroupName</span></span>
<span data-ttu-id="b45e8-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b45e8-133">The resource group name.</span></span>

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

### <span data-ttu-id="b45e8-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b45e8-134">-ResourceId</span></span>
<span data-ttu-id="b45e8-135">Идентификатор ресурса объекта VpnConenction, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b45e8-135">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="b45e8-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b45e8-136">-Confirm</span></span>
<span data-ttu-id="b45e8-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b45e8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b45e8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b45e8-138">-WhatIf</span></span>
<span data-ttu-id="b45e8-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b45e8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b45e8-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b45e8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b45e8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b45e8-141">CommonParameters</span></span>
<span data-ttu-id="b45e8-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b45e8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b45e8-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b45e8-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b45e8-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b45e8-144">INPUTS</span></span>

### <span data-ttu-id="b45e8-145">System. String</span><span class="sxs-lookup"><span data-stu-id="b45e8-145">System.String</span></span>

### <span data-ttu-id="b45e8-146">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b45e8-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="b45e8-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b45e8-147">OUTPUTS</span></span>

### <span data-ttu-id="b45e8-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b45e8-148">System.Boolean</span></span>

## <span data-ttu-id="b45e8-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="b45e8-149">NOTES</span></span>

## <span data-ttu-id="b45e8-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b45e8-150">RELATED LINKS</span></span>
