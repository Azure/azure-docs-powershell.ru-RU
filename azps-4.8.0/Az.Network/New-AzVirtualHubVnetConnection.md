---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e9156887f328242f8c4896dc707a1814f58f2869
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244361"
---
# <span data-ttu-id="0f183-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0f183-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="0f183-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f183-102">SYNOPSIS</span></span>
<span data-ttu-id="0f183-103">Командлет New-AzVirtualHubVnetConnection создает ресурс HubVirtualNetworkConnection, который является одноранговым узлом виртуальной сети для виртуального концентратора Azure.</span><span class="sxs-lookup"><span data-stu-id="0f183-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="0f183-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f183-104">SYNTAX</span></span>

### <span data-ttu-id="0f183-105">ByVirtualHubNameByRemoteVirtualNetworkObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f183-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f183-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="0f183-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f183-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="0f183-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f183-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="0f183-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f183-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="0f183-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f183-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="0f183-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f183-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f183-111">DESCRIPTION</span></span>
<span data-ttu-id="0f183-112">Командлет New-AzVirtualHubVnetConnection создает ресурс HubVirtualNetworkConnection, который является одноранговым узлом виртуальной сети для виртуального концентратора Azure.</span><span class="sxs-lookup"><span data-stu-id="0f183-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="0f183-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f183-113">EXAMPLES</span></span>

### <span data-ttu-id="0f183-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0f183-114">Example 1</span></span>

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
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="0f183-115">В этой группе ресурсов будет создана группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор в центре US в Azure.</span><span class="sxs-lookup"><span data-stu-id="0f183-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="0f183-116">После этого будет создано виртуальное сетевое подключение, которое будет использоваться для пиринга виртуальной сети с виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="0f183-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="0f183-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0f183-117">Example 2</span></span>

<span data-ttu-id="0f183-118">Командлет New-AzVirtualHubVnetConnection создает ресурс HubVirtualNetworkConnection, который является одноранговым узлом виртуальной сети для виртуального концентратора Azure.</span><span class="sxs-lookup"><span data-stu-id="0f183-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="0f183-119">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="0f183-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```

## <span data-ttu-id="0f183-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f183-120">PARAMETERS</span></span>

### <span data-ttu-id="0f183-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f183-121">-AsJob</span></span>
<span data-ttu-id="0f183-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0f183-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f183-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f183-123">-DefaultProfile</span></span>
<span data-ttu-id="0f183-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f183-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f183-125">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="0f183-125">-EnableInternetSecurity</span></span>
<span data-ttu-id="0f183-126">Включить Интернет-безопасность для этого подключения</span><span class="sxs-lookup"><span data-stu-id="0f183-126">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="0f183-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="0f183-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="0f183-128">Включить Интернет-безопасность для этого подключения</span><span class="sxs-lookup"><span data-stu-id="0f183-128">Enable internet security for this connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f183-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f183-129">-Name</span></span>
<span data-ttu-id="0f183-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="0f183-130">The resource name.</span></span>

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

### <span data-ttu-id="0f183-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0f183-131">-ParentObject</span></span>
<span data-ttu-id="0f183-132">Родительский ресурс.</span><span class="sxs-lookup"><span data-stu-id="0f183-132">The parent resource.</span></span>

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

### <span data-ttu-id="0f183-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0f183-133">-ParentResourceId</span></span>
<span data-ttu-id="0f183-134">Родительский ресурс.</span><span class="sxs-lookup"><span data-stu-id="0f183-134">The parent resource.</span></span>

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

### <span data-ttu-id="0f183-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="0f183-135">-ParentResourceName</span></span>
<span data-ttu-id="0f183-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f183-136">The resource group name.</span></span>

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

### <span data-ttu-id="0f183-137">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0f183-137">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="0f183-138">Удаленная виртуальная сеть, к которой подключено это подключение к виртуальному сетевому концентратору.</span><span class="sxs-lookup"><span data-stu-id="0f183-138">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="0f183-139">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="0f183-139">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="0f183-140">Удаленная виртуальная сеть, к которой подключено это подключение к виртуальному сетевому концентратору.</span><span class="sxs-lookup"><span data-stu-id="0f183-140">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="0f183-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f183-141">-ResourceGroupName</span></span>
<span data-ttu-id="0f183-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f183-142">The resource group name.</span></span>

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

### <span data-ttu-id="0f183-143">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f183-143">-RoutingConfiguration</span></span>
<span data-ttu-id="0f183-144">Настройка маршрутизации для этого подключения</span><span class="sxs-lookup"><span data-stu-id="0f183-144">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f183-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f183-145">-Confirm</span></span>
<span data-ttu-id="0f183-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0f183-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f183-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f183-147">-WhatIf</span></span>
<span data-ttu-id="0f183-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0f183-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f183-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0f183-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f183-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f183-150">CommonParameters</span></span>
<span data-ttu-id="0f183-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f183-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f183-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f183-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f183-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f183-153">INPUTS</span></span>

### <span data-ttu-id="0f183-154">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0f183-154">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="0f183-155">System. String</span><span class="sxs-lookup"><span data-stu-id="0f183-155">System.String</span></span>

## <span data-ttu-id="0f183-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f183-156">OUTPUTS</span></span>

### <span data-ttu-id="0f183-157">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="0f183-157">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="0f183-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f183-158">NOTES</span></span>

## <span data-ttu-id="0f183-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f183-159">RELATED LINKS</span></span>

[<span data-ttu-id="0f183-160">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0f183-160">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="0f183-161">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0f183-161">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="0f183-162">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f183-162">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
