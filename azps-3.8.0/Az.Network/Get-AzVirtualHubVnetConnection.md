---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 1f04b47889f334f095c8c3163bc601a3b1950c82
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073280"
---
# <span data-ttu-id="e56a1-101">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e56a1-101">Get-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="e56a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e56a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e56a1-103">Возвращает виртуальную сетевое подключение в виртуальном концентраторе или список всех виртуальных сетевых подключений в виртуальном концентраторе.</span><span class="sxs-lookup"><span data-stu-id="e56a1-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="e56a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e56a1-104">SYNTAX</span></span>

### <span data-ttu-id="e56a1-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e56a1-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e56a1-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="e56a1-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e56a1-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="e56a1-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e56a1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e56a1-108">DESCRIPTION</span></span>
<span data-ttu-id="e56a1-109">Возвращает виртуальную сетевое подключение в виртуальном концентраторе или список всех виртуальных сетевых подключений в виртуальном концентраторе.</span><span class="sxs-lookup"><span data-stu-id="e56a1-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="e56a1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e56a1-110">EXAMPLES</span></span>

### <span data-ttu-id="e56a1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e56a1-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="e56a1-112">В этой группе ресурсов будет создана группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор в центре US в Azure.</span><span class="sxs-lookup"><span data-stu-id="e56a1-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="e56a1-113">После этого будет создано виртуальное сетевое подключение, которое будет использоваться для пиринга виртуальной сети с виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="e56a1-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="e56a1-114">После создания подключения к виртуальной сети Hub оно получает виртуальную сетевую подключение Hub, используя имя группы ресурсов, имя концентратора и имя подключения.</span><span class="sxs-lookup"><span data-stu-id="e56a1-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="e56a1-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e56a1-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="e56a1-116">В этой группе ресурсов будет создана группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор в центре US в Azure.</span><span class="sxs-lookup"><span data-stu-id="e56a1-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="e56a1-117">После этого будет создано виртуальное сетевое подключение, которое будет использоваться для пиринга виртуальной сети с виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="e56a1-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="e56a1-118">После создания подключения к виртуальной сети Hub на нем выводятся все подключения к виртуальной сети Hub с использованием имени группы ресурсов и имени концентратора.</span><span class="sxs-lookup"><span data-stu-id="e56a1-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

### <span data-ttu-id="e56a1-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e56a1-119">Example 3</span></span>

```powershell
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name test*

Name                 : testvnetconnection1
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection1
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded

Name                 : testvnetconnection2
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection2
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="e56a1-120">Этот командлет выводит список всех подключений к виртуальным сетевым центрам, начиная с "Test", с помощью имени группы ресурсов и имени концентратора.</span><span class="sxs-lookup"><span data-stu-id="e56a1-120">This cmdlet lists all the hub virtual network connections starting with "test" using its resource group name and the hub name.</span></span>

## <span data-ttu-id="e56a1-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e56a1-121">PARAMETERS</span></span>

### <span data-ttu-id="e56a1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e56a1-122">-DefaultProfile</span></span>
<span data-ttu-id="e56a1-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e56a1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e56a1-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e56a1-124">-Name</span></span>
<span data-ttu-id="e56a1-125">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e56a1-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="e56a1-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e56a1-126">-ParentObject</span></span>
<span data-ttu-id="e56a1-127">Родительский ресурс.</span><span class="sxs-lookup"><span data-stu-id="e56a1-127">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e56a1-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e56a1-128">-ParentResourceId</span></span>
<span data-ttu-id="e56a1-129">Родительский идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="e56a1-129">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e56a1-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="e56a1-130">-ParentResourceName</span></span>
<span data-ttu-id="e56a1-131">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="e56a1-131">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e56a1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e56a1-132">-ResourceGroupName</span></span>
<span data-ttu-id="e56a1-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e56a1-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e56a1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e56a1-134">CommonParameters</span></span>
<span data-ttu-id="e56a1-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e56a1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e56a1-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e56a1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e56a1-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e56a1-137">INPUTS</span></span>

### <span data-ttu-id="e56a1-138">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e56a1-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="e56a1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e56a1-139">System.String</span></span>

## <span data-ttu-id="e56a1-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e56a1-140">OUTPUTS</span></span>

### <span data-ttu-id="e56a1-141">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="e56a1-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="e56a1-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="e56a1-142">NOTES</span></span>

## <span data-ttu-id="e56a1-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e56a1-143">RELATED LINKS</span></span>

[<span data-ttu-id="e56a1-144">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e56a1-144">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="e56a1-145">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e56a1-145">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
