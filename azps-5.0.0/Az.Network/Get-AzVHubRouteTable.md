---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
ms.openlocfilehash: 3461d629eac47a1bbf2842d2cb0a913c2734f94e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317174"
---
# <span data-ttu-id="635a2-101">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="635a2-101">Get-AzVHubRouteTable</span></span>

## <span data-ttu-id="635a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="635a2-102">SYNOPSIS</span></span>
<span data-ttu-id="635a2-103">Извлекает ресурс таблицы маршрута Hub, связанный с VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="635a2-103">Retrieves  a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="635a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="635a2-104">SYNTAX</span></span>

### <span data-ttu-id="635a2-105">ByVHubRouteTableName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="635a2-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Get-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="635a2-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="635a2-106">ByVirtualHubObject</span></span>
```powershell
Get-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="635a2-107">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="635a2-107">ByVHubRouteTableResourceId</span></span>
```powershell
Get-AzVHubRouteTable -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="635a2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="635a2-108">DESCRIPTION</span></span>
<span data-ttu-id="635a2-109">Получает указанную таблицу маршрутов Hub, связанную с указанным виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="635a2-109">Gets the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="635a2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="635a2-110">EXAMPLES</span></span>

### <span data-ttu-id="635a2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="635a2-111">Example 1</span></span>

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

<span data-ttu-id="635a2-112">Эта команда получает таблицу маршрута Hub виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="635a2-112">This command gets the hub route table of the virtual hub.</span></span>

### <span data-ttu-id="635a2-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="635a2-113">Example 2</span></span>

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

<span data-ttu-id="635a2-114">Эта команда выводит список всех таблиц маршрутизатора Hub в указанном VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="635a2-114">This command lists all the hub route tables in the specified VirtualHub.</span></span>

## <span data-ttu-id="635a2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="635a2-115">PARAMETERS</span></span>

### <span data-ttu-id="635a2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="635a2-116">-AsJob</span></span>
<span data-ttu-id="635a2-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="635a2-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="635a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="635a2-118">-DefaultProfile</span></span>
<span data-ttu-id="635a2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="635a2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="635a2-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="635a2-120">-Name</span></span>
<span data-ttu-id="635a2-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="635a2-121">The resource name.</span></span>

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

### <span data-ttu-id="635a2-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="635a2-122">-ParentObject</span></span>
<span data-ttu-id="635a2-123">Родительский объект виртуального концентратора для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="635a2-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="635a2-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="635a2-124">-ParentResourceName</span></span>
<span data-ttu-id="635a2-125">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="635a2-125">The parent resource name.</span></span>

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

### <span data-ttu-id="635a2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="635a2-126">-ResourceGroupName</span></span>
<span data-ttu-id="635a2-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="635a2-127">The resource group name.</span></span>

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

### <span data-ttu-id="635a2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="635a2-128">-ResourceId</span></span>
<span data-ttu-id="635a2-129">Идентификатор ресурса vhubroutetable ресурса, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="635a2-129">The resource id of the vhubroutetable resource to Get.</span></span>

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

### <span data-ttu-id="635a2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="635a2-130">-Confirm</span></span>
<span data-ttu-id="635a2-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="635a2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="635a2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="635a2-132">-WhatIf</span></span>
<span data-ttu-id="635a2-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="635a2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="635a2-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="635a2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="635a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="635a2-135">CommonParameters</span></span>
<span data-ttu-id="635a2-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="635a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="635a2-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="635a2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="635a2-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="635a2-138">INPUTS</span></span>

### <span data-ttu-id="635a2-139">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="635a2-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="635a2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="635a2-140">System.String</span></span>

## <span data-ttu-id="635a2-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="635a2-141">OUTPUTS</span></span>

### <span data-ttu-id="635a2-142">Microsoft. Azure. Commands. Network. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="635a2-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="635a2-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="635a2-143">NOTES</span></span>

## <span data-ttu-id="635a2-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="635a2-144">RELATED LINKS</span></span>

[<span data-ttu-id="635a2-145">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="635a2-145">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="635a2-146">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="635a2-146">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="635a2-147">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="635a2-147">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)

[<span data-ttu-id="635a2-148">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="635a2-148">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)