---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 1454e3ba3fc3a7e229e064a32146ebddddc19392
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951587"
---
# <span data-ttu-id="3af89-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3af89-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="3af89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3af89-102">SYNOPSIS</span></span>
<span data-ttu-id="3af89-103">Обновляет существующее подключение HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="3af89-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="3af89-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3af89-104">SYNTAX</span></span>

### <span data-ttu-id="3af89-105">ByHubVirtualNetworkConnectionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3af89-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3af89-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="3af89-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3af89-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="3af89-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3af89-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3af89-108">DESCRIPTION</span></span>
<span data-ttu-id="3af89-109">Обновляет существующее подключение HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="3af89-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="3af89-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3af89-110">EXAMPLES</span></span>

### <span data-ttu-id="3af89-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3af89-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Update-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -EnableInternetSecurity $true
Name                   : testvnetconnection
Id                     : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : True
ProvisioningState      : Succeeded
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

<span data-ttu-id="3af89-112">Выше будет создание группы ресурсов, виртуальной WAN, виртуальной сети, виртуального концентратора в центральной части США в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="3af89-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="3af89-113">Также создается виртуальное сетевое подключение, которое является одноранговой сетью с виртуальным центром.</span><span class="sxs-lookup"><span data-stu-id="3af89-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="3af89-114">Это виртуальное сетевое подключение будет обновлено для обеспечения безопасности в Интернете.</span><span class="sxs-lookup"><span data-stu-id="3af89-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="3af89-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3af89-115">PARAMETERS</span></span>

### <span data-ttu-id="3af89-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3af89-116">-AsJob</span></span>
<span data-ttu-id="3af89-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3af89-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3af89-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af89-118">-DefaultProfile</span></span>
<span data-ttu-id="3af89-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3af89-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af89-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="3af89-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="3af89-121">В этой связи можно включить безопасность Интернета.</span><span class="sxs-lookup"><span data-stu-id="3af89-121">Enable internet security for this connection.</span></span>

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

### <span data-ttu-id="3af89-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3af89-122">-InputObject</span></span>
<span data-ttu-id="3af89-123">Ресурс hubvirtualnetworkconnection, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="3af89-123">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3af89-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3af89-124">-Name</span></span>
<span data-ttu-id="3af89-125">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="3af89-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af89-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="3af89-126">-ParentResourceName</span></span>
<span data-ttu-id="3af89-127">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="3af89-127">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af89-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3af89-128">-ResourceGroupName</span></span>
<span data-ttu-id="3af89-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3af89-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af89-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3af89-130">-ResourceId</span></span>
<span data-ttu-id="3af89-131">Код ресурса hubvirtualnetworkconnection, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="3af89-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3af89-132">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="3af89-132">-RoutingConfiguration</span></span>
<span data-ttu-id="3af89-133">Настройка маршрутиации для этого подключения</span><span class="sxs-lookup"><span data-stu-id="3af89-133">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="3af89-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3af89-134">-Confirm</span></span>
<span data-ttu-id="3af89-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3af89-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3af89-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3af89-136">-WhatIf</span></span>
<span data-ttu-id="3af89-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3af89-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3af89-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3af89-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3af89-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af89-139">CommonParameters</span></span>
<span data-ttu-id="3af89-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3af89-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af89-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3af89-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af89-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3af89-142">INPUTS</span></span>

### <span data-ttu-id="3af89-143">System.String</span><span class="sxs-lookup"><span data-stu-id="3af89-143">System.String</span></span>

### <span data-ttu-id="3af89-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="3af89-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="3af89-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3af89-145">OUTPUTS</span></span>

### <span data-ttu-id="3af89-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="3af89-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="3af89-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3af89-147">NOTES</span></span>

## <span data-ttu-id="3af89-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3af89-148">RELATED LINKS</span></span>

[<span data-ttu-id="3af89-149">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="3af89-149">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
