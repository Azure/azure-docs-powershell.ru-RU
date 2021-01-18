---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
ms.openlocfilehash: d330b7e25cc1184a3efaea2c3deb569bf44171b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505473"
---
# <span data-ttu-id="bddea-101">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bddea-101">Update-AzVHubRouteTable</span></span>

## <span data-ttu-id="bddea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bddea-102">SYNOPSIS</span></span>
<span data-ttu-id="bddea-103">Удаление ресурса таблицы маршрутов концентратора, связанного с VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="bddea-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="bddea-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bddea-104">SYNTAX</span></span>

### <span data-ttu-id="bddea-105">ByVHubRouteTableName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bddea-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Update-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String>[-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bddea-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="bddea-106">ByVirtualHubObject</span></span>
```powershell
Update-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bddea-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="bddea-107">ByVHubRouteTableObject</span></span>
```powershell
Update-AzVHubRouteTable -InputObject <PSVHubRouteTable> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bddea-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="bddea-108">ByVHubRouteTableResourceId</span></span>
```powershell
Update-AzVHubRouteTable -ResourceId <String> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bddea-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bddea-109">DESCRIPTION</span></span>
<span data-ttu-id="bddea-110">Обновляет указанную таблицу маршрутов, связанную с указанным виртуальным центром, с предоставленными маршрутами или метами.</span><span class="sxs-lookup"><span data-stu-id="bddea-110">Updates the specified route table that is associated with the specified virtual hub with the provided routes or the labels.</span></span>

## <span data-ttu-id="bddea-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bddea-111">EXAMPLES</span></span>

### <span data-ttu-id="bddea-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bddea-112">Example 1</span></span>
```powershell
PS C:\> New-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan" -Location "westcentralus" -VirtualWANType "Standard" -AllowVnetToVnetTraffic -AllowBranchToBranchTraffic
PS C:\> $virtualWan = Get-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan"

PS C:\> New-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub" -Location "westcentralus" -AddressPrefix "10.0.0.0/16" -VirtualWan $virtualWan
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub"

PS C:\> $fwIp = New-AzFirewallHubPublicIpAddress -Count 1
PS C:\> $hubIpAddresses = New-AzFirewallHubIpAddress -PublicIP $fwIp
PS C:\> New-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg" -Location "westcentralus" -Sku AZFW_Hub -VirtualHubId $virtualHub.Id -HubIPAddress $hubIpAddresses
PS C:\> $firewall = Get-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg"

PS C:\> $route1 = New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> New-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route1) -Label @("testLabel")
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

PS C:\> $route2 = New-AzVHubRoute -Name "internet-traffic" -Destination @("0.0.0.0/0") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> Update-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route2)
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "internet-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "0.0.0.0/0"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="bddea-113">Эта команда удаляет таблицу маршрутов концентратора виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="bddea-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="bddea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bddea-114">PARAMETERS</span></span>

### <span data-ttu-id="bddea-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bddea-115">-AsJob</span></span>
<span data-ttu-id="bddea-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bddea-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bddea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bddea-117">-DefaultProfile</span></span>
<span data-ttu-id="bddea-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bddea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bddea-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bddea-119">-InputObject</span></span>
<span data-ttu-id="bddea-120">Ресурс, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="bddea-120">The vhubroutetable resource to Update.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bddea-121">-Label</span><span class="sxs-lookup"><span data-stu-id="bddea-121">-Label</span></span>
<span data-ttu-id="bddea-122">Список наклеев.</span><span class="sxs-lookup"><span data-stu-id="bddea-122">The list of labels.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bddea-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bddea-123">-Name</span></span>
<span data-ttu-id="bddea-124">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="bddea-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bddea-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bddea-125">-ParentObject</span></span>
<span data-ttu-id="bddea-126">Родительский виртуальный центр этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="bddea-126">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bddea-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="bddea-127">-ParentResourceName</span></span>
<span data-ttu-id="bddea-128">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="bddea-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bddea-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bddea-129">-ResourceGroupName</span></span>
<span data-ttu-id="bddea-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bddea-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bddea-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bddea-131">-ResourceId</span></span>
<span data-ttu-id="bddea-132">ИД ресурса, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="bddea-132">The resource id of the vhubroutetable resource to Update.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bddea-133">-Route</span><span class="sxs-lookup"><span data-stu-id="bddea-133">-Route</span></span>
<span data-ttu-id="bddea-134">Список маршрутов для этой таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="bddea-134">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bddea-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bddea-135">-Confirm</span></span>
<span data-ttu-id="bddea-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bddea-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bddea-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bddea-137">-WhatIf</span></span>
<span data-ttu-id="bddea-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bddea-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bddea-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bddea-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bddea-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bddea-140">CommonParameters</span></span>
<span data-ttu-id="bddea-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bddea-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bddea-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bddea-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bddea-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bddea-143">INPUTS</span></span>

### <span data-ttu-id="bddea-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="bddea-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="bddea-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bddea-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="bddea-146">System.String</span><span class="sxs-lookup"><span data-stu-id="bddea-146">System.String</span></span>

## <span data-ttu-id="bddea-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bddea-147">OUTPUTS</span></span>

### <span data-ttu-id="bddea-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bddea-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="bddea-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bddea-149">NOTES</span></span>

## <span data-ttu-id="bddea-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bddea-150">RELATED LINKS</span></span>

[<span data-ttu-id="bddea-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bddea-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="bddea-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="bddea-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="bddea-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bddea-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="bddea-154">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bddea-154">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)