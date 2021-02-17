---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
ms.openlocfilehash: a07df2c6330757bf9e5b4f211429f6e2918fea39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220884"
---
# <span data-ttu-id="60c3c-101">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="60c3c-101">Update-AzVirtualHub</span></span>

## <span data-ttu-id="60c3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60c3c-102">SYNOPSIS</span></span>
<span data-ttu-id="60c3c-103">Обновляет виртуальный центр.</span><span class="sxs-lookup"><span data-stu-id="60c3c-103">Updates a virtual hub.</span></span>

## <span data-ttu-id="60c3c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="60c3c-104">SYNTAX</span></span>

### <span data-ttu-id="60c3c-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="60c3c-105">ByVirtualHubName (Default)</span></span>
```
Update-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60c3c-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="60c3c-106">ByVirtualHubResourceId</span></span>
```
Update-AzVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60c3c-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="60c3c-107">ByVirtualHubObject</span></span>
```
Update-AzVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60c3c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60c3c-108">DESCRIPTION</span></span>
<span data-ttu-id="60c3c-109">Для обновления виртуального концентратора обновляется **cmdlet Update-AzVirtualHub.**</span><span class="sxs-lookup"><span data-stu-id="60c3c-109">The **Update-AzVirtualHub** cmdlet updates a virtual hub.</span></span>

## <span data-ttu-id="60c3c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="60c3c-110">EXAMPLES</span></span>

### <span data-ttu-id="60c3c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="60c3c-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Update-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.2.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.2.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="60c3c-112">Выше будет создаваться группа ресурсов TestRG, виртуальная WAN и виртуальный концентратор в западной части США в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="60c3c-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="60c3c-113">В виртуальном центре будет адресная площадь 10.0.1.0/24.</span><span class="sxs-lookup"><span data-stu-id="60c3c-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="60c3c-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="60c3c-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> Update-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 192.168.2.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="60c3c-115">Выше будет создаваться группа ресурсов TestRG, виртуальная WAN и виртуальный концентратор в западной части США в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="60c3c-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="60c3c-116">В виртуальном центре будет адресная площадь 10.0.1.0/24.</span><span class="sxs-lookup"><span data-stu-id="60c3c-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="60c3c-117">Этот пример похож на пример 1, но прикрепит таблицу маршрутов к виртуальному центру.</span><span class="sxs-lookup"><span data-stu-id="60c3c-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="60c3c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60c3c-118">PARAMETERS</span></span>

### <span data-ttu-id="60c3c-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="60c3c-119">-AddressPrefix</span></span>
<span data-ttu-id="60c3c-120">Строка адресного пространства для этого виртуального центра.</span><span class="sxs-lookup"><span data-stu-id="60c3c-120">The address space string for this virtual hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c3c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60c3c-121">-AsJob</span></span>
<span data-ttu-id="60c3c-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="60c3c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60c3c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c3c-123">-DefaultProfile</span></span>
<span data-ttu-id="60c3c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60c3c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60c3c-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="60c3c-125">-HubVnetConnection</span></span>
<span data-ttu-id="60c3c-126">Виртуальные сетевые подключения концентратора, связанные с этим виртуальным центром.</span><span class="sxs-lookup"><span data-stu-id="60c3c-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c3c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60c3c-127">-InputObject</span></span>
<span data-ttu-id="60c3c-128">Объект виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="60c3c-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60c3c-129">-Name</span><span class="sxs-lookup"><span data-stu-id="60c3c-129">-Name</span></span>
<span data-ttu-id="60c3c-130">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="60c3c-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c3c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60c3c-131">-ResourceGroupName</span></span>
<span data-ttu-id="60c3c-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60c3c-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c3c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60c3c-133">-ResourceId</span></span>
<span data-ttu-id="60c3c-134">ИД ресурса виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="60c3c-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60c3c-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="60c3c-135">-RouteTable</span></span>
<span data-ttu-id="60c3c-136">Таблица маршрутов, связанная с этим виртуальным центром.</span><span class="sxs-lookup"><span data-stu-id="60c3c-136">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c3c-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="60c3c-137">-Sku</span></span>
<span data-ttu-id="60c3c-138">SKU виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="60c3c-138">The sku of the Virtual Hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c3c-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="60c3c-139">-Tag</span></span>
<span data-ttu-id="60c3c-140">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="60c3c-140">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c3c-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60c3c-141">-Confirm</span></span>
<span data-ttu-id="60c3c-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="60c3c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60c3c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60c3c-143">-WhatIf</span></span>
<span data-ttu-id="60c3c-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60c3c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60c3c-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="60c3c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60c3c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c3c-146">CommonParameters</span></span>
<span data-ttu-id="60c3c-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60c3c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c3c-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60c3c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c3c-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60c3c-149">INPUTS</span></span>

### <span data-ttu-id="60c3c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="60c3c-150">System.String</span></span>

### <span data-ttu-id="60c3c-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="60c3c-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="60c3c-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="60c3c-152">OUTPUTS</span></span>

### <span data-ttu-id="60c3c-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="60c3c-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="60c3c-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="60c3c-154">NOTES</span></span>

## <span data-ttu-id="60c3c-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60c3c-155">RELATED LINKS</span></span>

[<span data-ttu-id="60c3c-156">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="60c3c-156">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="60c3c-157">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="60c3c-157">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="60c3c-158">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="60c3c-158">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)
