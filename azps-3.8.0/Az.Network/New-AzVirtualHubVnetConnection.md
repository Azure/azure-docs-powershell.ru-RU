---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 3be41be3c62b0676ea10e9fe7c9d89927c4de757
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073237"
---
# <span data-ttu-id="f4420-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f4420-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="f4420-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4420-102">SYNOPSIS</span></span>
<span data-ttu-id="f4420-103">Командлет New-AzVirtualHubVnetConnection создает ресурс HubVirtualNetworkConnection, который является одноранговым узлом виртуальной сети для виртуального концентратора Azure.</span><span class="sxs-lookup"><span data-stu-id="f4420-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="f4420-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4420-104">SYNTAX</span></span>

### <span data-ttu-id="f4420-105">ByVirtualHubNameByRemoteVirtualNetworkObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4420-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4420-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="f4420-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4420-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="f4420-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4420-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="f4420-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4420-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="f4420-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4420-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="f4420-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4420-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4420-111">DESCRIPTION</span></span>
<span data-ttu-id="f4420-112">Командлет New-AzVirtualHubVnetConnection создает ресурс HubVirtualNetworkConnection, который является одноранговым узлом виртуальной сети для виртуального концентратора Azure.</span><span class="sxs-lookup"><span data-stu-id="f4420-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="f4420-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4420-113">EXAMPLES</span></span>

### <span data-ttu-id="f4420-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f4420-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : False
ProvisioningState    : Succeeded
```

<span data-ttu-id="f4420-115">В этой группе ресурсов будет создана группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор в центре US в Azure.</span><span class="sxs-lookup"><span data-stu-id="f4420-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="f4420-116">После этого будет создано виртуальное сетевое подключение, которое будет использоваться для пиринга виртуальной сети с виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="f4420-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

## <span data-ttu-id="f4420-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4420-117">PARAMETERS</span></span>

### <span data-ttu-id="f4420-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4420-118">-AsJob</span></span>
<span data-ttu-id="f4420-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f4420-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4420-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4420-120">-DefaultProfile</span></span>
<span data-ttu-id="f4420-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4420-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4420-122">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="f4420-122">-EnableInternetSecurity</span></span>
<span data-ttu-id="f4420-123">Включить Интернет-безопасность для этого подключения</span><span class="sxs-lookup"><span data-stu-id="f4420-123">Enable internet security for this connection</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4420-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f4420-124">-Name</span></span>
<span data-ttu-id="f4420-125">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="f4420-125">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4420-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f4420-126">-ParentObject</span></span>
<span data-ttu-id="f4420-127">Родительский ресурс.</span><span class="sxs-lookup"><span data-stu-id="f4420-127">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4420-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f4420-128">-ParentResourceId</span></span>
<span data-ttu-id="f4420-129">Родительский ресурс.</span><span class="sxs-lookup"><span data-stu-id="f4420-129">The parent resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4420-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f4420-130">-ParentResourceName</span></span>
<span data-ttu-id="f4420-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4420-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4420-132">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f4420-132">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="f4420-133">Удаленная виртуальная сеть, к которой подключено это подключение к виртуальному сетевому концентратору.</span><span class="sxs-lookup"><span data-stu-id="f4420-133">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4420-134">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="f4420-134">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="f4420-135">Удаленная виртуальная сеть, к которой подключено это подключение к виртуальному сетевому концентратору.</span><span class="sxs-lookup"><span data-stu-id="f4420-135">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4420-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4420-136">-ResourceGroupName</span></span>
<span data-ttu-id="f4420-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4420-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4420-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4420-138">-Confirm</span></span>
<span data-ttu-id="f4420-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4420-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4420-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4420-140">-WhatIf</span></span>
<span data-ttu-id="f4420-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4420-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4420-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4420-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4420-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4420-143">CommonParameters</span></span>
<span data-ttu-id="f4420-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4420-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4420-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4420-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4420-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4420-146">INPUTS</span></span>

### <span data-ttu-id="f4420-147">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f4420-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="f4420-148">System. String</span><span class="sxs-lookup"><span data-stu-id="f4420-148">System.String</span></span>

## <span data-ttu-id="f4420-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4420-149">OUTPUTS</span></span>

### <span data-ttu-id="f4420-150">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="f4420-150">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="f4420-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4420-151">NOTES</span></span>

## <span data-ttu-id="f4420-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4420-152">RELATED LINKS</span></span>

[<span data-ttu-id="f4420-153">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f4420-153">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="f4420-154">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f4420-154">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
