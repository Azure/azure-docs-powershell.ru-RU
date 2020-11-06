---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 8aeb992b08e2749168ef3da2db6c264158c6a9ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560899"
---
# <span data-ttu-id="3bf08-101">Get-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3bf08-101">Get-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="3bf08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3bf08-102">SYNOPSIS</span></span>
<span data-ttu-id="3bf08-103">Возвращает виртуальную сетевое подключение в виртуальном концентраторе или список всех виртуальных сетевых подключений в виртуальном концентраторе.</span><span class="sxs-lookup"><span data-stu-id="3bf08-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bf08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3bf08-104">SYNTAX</span></span>

### <span data-ttu-id="3bf08-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3bf08-105">ByVirtualHubName (Default)</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bf08-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="3bf08-106">ByVirtualHubObject</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bf08-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="3bf08-107">ByVirtualHubResourceId</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bf08-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bf08-108">DESCRIPTION</span></span>
<span data-ttu-id="3bf08-109">Возвращает виртуальную сетевое подключение в виртуальном концентраторе или список всех виртуальных сетевых подключений в виртуальном концентраторе.</span><span class="sxs-lookup"><span data-stu-id="3bf08-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="3bf08-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3bf08-110">EXAMPLES</span></span>

### <span data-ttu-id="3bf08-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3bf08-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="3bf08-112">В этой группе ресурсов будет создана группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор в центре US в Azure.</span><span class="sxs-lookup"><span data-stu-id="3bf08-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="3bf08-113">После этого будет создано виртуальное сетевое подключение, которое будет использоваться для пиринга виртуальной сети с виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="3bf08-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="3bf08-114">После создания подключения к виртуальной сети Hub оно получает виртуальную сетевую подключение Hub, используя имя группы ресурсов, имя концентратора и имя подключения.</span><span class="sxs-lookup"><span data-stu-id="3bf08-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="3bf08-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3bf08-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="3bf08-116">В этой группе ресурсов будет создана группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор в центре US в Azure.</span><span class="sxs-lookup"><span data-stu-id="3bf08-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="3bf08-117">После этого будет создано виртуальное сетевое подключение, которое будет использоваться для пиринга виртуальной сети с виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="3bf08-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="3bf08-118">После создания подключения к виртуальной сети Hub на нем выводятся все подключения к виртуальной сети Hub с использованием имени группы ресурсов и имени концентратора.</span><span class="sxs-lookup"><span data-stu-id="3bf08-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

## <span data-ttu-id="3bf08-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3bf08-119">PARAMETERS</span></span>

### <span data-ttu-id="3bf08-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bf08-120">-DefaultProfile</span></span>
<span data-ttu-id="3bf08-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3bf08-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bf08-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3bf08-122">-Name</span></span>
<span data-ttu-id="3bf08-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="3bf08-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bf08-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3bf08-124">-ParentObject</span></span>
<span data-ttu-id="3bf08-125">Родительский ресурс.</span><span class="sxs-lookup"><span data-stu-id="3bf08-125">The parent resource.</span></span>

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

### <span data-ttu-id="3bf08-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3bf08-126">-ParentResourceId</span></span>
<span data-ttu-id="3bf08-127">Родительский идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="3bf08-127">The parent resource id.</span></span>

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

### <span data-ttu-id="3bf08-128">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="3bf08-128">-ParentResourceName</span></span>
<span data-ttu-id="3bf08-129">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="3bf08-129">The parent resource name.</span></span>

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

### <span data-ttu-id="3bf08-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bf08-130">-ResourceGroupName</span></span>
<span data-ttu-id="3bf08-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3bf08-131">The resource group name.</span></span>

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

### <span data-ttu-id="3bf08-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bf08-132">CommonParameters</span></span>
<span data-ttu-id="3bf08-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3bf08-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bf08-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bf08-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bf08-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3bf08-135">INPUTS</span></span>

### <span data-ttu-id="3bf08-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="3bf08-136">None</span></span>

## <span data-ttu-id="3bf08-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bf08-137">OUTPUTS</span></span>

### <span data-ttu-id="3bf08-138">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="3bf08-138">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="3bf08-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="3bf08-139">NOTES</span></span>

## <span data-ttu-id="3bf08-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3bf08-140">RELATED LINKS</span></span>
