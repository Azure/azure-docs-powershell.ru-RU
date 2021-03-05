---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
ms.openlocfilehash: 83758842fe91ef6cf8fca24f360750f813a31311
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016232"
---
# <span data-ttu-id="60b33-101">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="60b33-101">Get-AzVHubRouteTable</span></span>

## <span data-ttu-id="60b33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60b33-102">SYNOPSIS</span></span>
<span data-ttu-id="60b33-103">Извлекает ресурс таблицы маршрутов концентратора, связанный с VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="60b33-103">Retrieves  a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="60b33-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="60b33-104">SYNTAX</span></span>

### <span data-ttu-id="60b33-105">ByVHubRouteTableName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="60b33-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Get-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60b33-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="60b33-106">ByVirtualHubObject</span></span>
```powershell
Get-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60b33-107">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="60b33-107">ByVHubRouteTableResourceId</span></span>
```powershell
Get-AzVHubRouteTable -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60b33-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60b33-108">DESCRIPTION</span></span>
<span data-ttu-id="60b33-109">Возвращает указанную таблицу маршрутов концентратора, связанную с указанным виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="60b33-109">Gets the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="60b33-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="60b33-110">EXAMPLES</span></span>

### <span data-ttu-id="60b33-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="60b33-111">Example 1</span></span>

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

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "private-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "10.30.0.0/16",
                               "10.40.0.0/16"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="60b33-112">Эта команда получает таблицу маршрутов концентратора виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="60b33-112">This command gets the hub route table of the virtual hub.</span></span>

### <span data-ttu-id="60b33-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="60b33-113">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName


Name                   : defaultRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []


Name                   : noneRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="60b33-114">Эта команда содержит все таблицы маршрутов концентратора в указанной службе VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="60b33-114">This command lists all the hub route tables in the specified VirtualHub.</span></span>

## <span data-ttu-id="60b33-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60b33-115">PARAMETERS</span></span>

### <span data-ttu-id="60b33-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60b33-116">-AsJob</span></span>
<span data-ttu-id="60b33-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="60b33-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60b33-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60b33-118">-DefaultProfile</span></span>
<span data-ttu-id="60b33-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60b33-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60b33-120">-Name</span><span class="sxs-lookup"><span data-stu-id="60b33-120">-Name</span></span>
<span data-ttu-id="60b33-121">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="60b33-121">The resource name.</span></span>

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

### <span data-ttu-id="60b33-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="60b33-122">-ParentObject</span></span>
<span data-ttu-id="60b33-123">Родительский виртуальный центр этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="60b33-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="60b33-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="60b33-124">-ParentResourceName</span></span>
<span data-ttu-id="60b33-125">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="60b33-125">The parent resource name.</span></span>

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

### <span data-ttu-id="60b33-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60b33-126">-ResourceGroupName</span></span>
<span data-ttu-id="60b33-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60b33-127">The resource group name.</span></span>

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

### <span data-ttu-id="60b33-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60b33-128">-ResourceId</span></span>
<span data-ttu-id="60b33-129">ИД ресурса, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="60b33-129">The resource id of the vhubroutetable resource to Get.</span></span>

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

### <span data-ttu-id="60b33-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60b33-130">-Confirm</span></span>
<span data-ttu-id="60b33-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60b33-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60b33-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60b33-132">-WhatIf</span></span>
<span data-ttu-id="60b33-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60b33-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60b33-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="60b33-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60b33-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b33-135">CommonParameters</span></span>
<span data-ttu-id="60b33-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60b33-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b33-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60b33-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b33-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60b33-138">INPUTS</span></span>

### <span data-ttu-id="60b33-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="60b33-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="60b33-140">System.String</span><span class="sxs-lookup"><span data-stu-id="60b33-140">System.String</span></span>

## <span data-ttu-id="60b33-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="60b33-141">OUTPUTS</span></span>

### <span data-ttu-id="60b33-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="60b33-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="60b33-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="60b33-143">NOTES</span></span>

## <span data-ttu-id="60b33-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60b33-144">RELATED LINKS</span></span>

[<span data-ttu-id="60b33-145">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="60b33-145">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="60b33-146">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="60b33-146">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="60b33-147">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="60b33-147">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)

[<span data-ttu-id="60b33-148">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="60b33-148">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)