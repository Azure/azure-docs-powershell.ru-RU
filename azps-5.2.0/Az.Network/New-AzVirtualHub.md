---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: d005ef841828dc1fe37915c4a7b0d28ad93e3b44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391511"
---
# <span data-ttu-id="71bcf-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="71bcf-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="71bcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="71bcf-103">Создает ресурс Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="71bcf-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="71bcf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="71bcf-104">SYNTAX</span></span>

### <span data-ttu-id="71bcf-105">ByVirtualWanObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="71bcf-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71bcf-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="71bcf-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71bcf-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71bcf-107">DESCRIPTION</span></span>
<span data-ttu-id="71bcf-108">Создает ресурс Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="71bcf-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="71bcf-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="71bcf-109">EXAMPLES</span></span>

### <span data-ttu-id="71bcf-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="71bcf-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="71bcf-111">Выше будет создаваться группа ресурсов TestRG, виртуальная WAN и виртуальный концентратор в западной части США в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="71bcf-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="71bcf-112">В виртуальном центре будет адресная площадь 10.0.1.0/24.</span><span class="sxs-lookup"><span data-stu-id="71bcf-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="71bcf-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="71bcf-113">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="71bcf-114">Выше будет создаваться группа ресурсов TestRG, виртуальная WAN и виртуальный концентратор в западной части США в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="71bcf-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="71bcf-115">В виртуальном центре будет адресная площадь 10.0.1.0/24.</span><span class="sxs-lookup"><span data-stu-id="71bcf-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="71bcf-116">Этот пример похож на пример 1, но использует ИД ресурса для ссылки на виртуальную WAN, необходимую для создания виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="71bcf-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="71bcf-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="71bcf-117">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="71bcf-118">Выше будет создаваться группа ресурсов TestRG, виртуальная WAN и виртуальный концентратор в западной части США в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="71bcf-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="71bcf-119">Виртуальный концентратор будет иметь адресную площадь "10.0.1.0/24" и подключенную таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="71bcf-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="71bcf-120">Этот пример похож на пример 2, но прикрепит таблицу маршрутов к виртуальному центру.</span><span class="sxs-lookup"><span data-stu-id="71bcf-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="71bcf-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71bcf-121">PARAMETERS</span></span>

### <span data-ttu-id="71bcf-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="71bcf-122">-AddressPrefix</span></span>
<span data-ttu-id="71bcf-123">Строка адресного пространства для этого виртуального центра.</span><span class="sxs-lookup"><span data-stu-id="71bcf-123">The address space string for this virtual hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71bcf-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71bcf-124">-AsJob</span></span>
<span data-ttu-id="71bcf-125">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="71bcf-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71bcf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71bcf-126">-DefaultProfile</span></span>
<span data-ttu-id="71bcf-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71bcf-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71bcf-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="71bcf-128">-HubVnetConnection</span></span>
<span data-ttu-id="71bcf-129">Виртуальные сетевые подключения концентратора, связанные с этим виртуальным центром.</span><span class="sxs-lookup"><span data-stu-id="71bcf-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="71bcf-130">-Location</span><span class="sxs-lookup"><span data-stu-id="71bcf-130">-Location</span></span>
<span data-ttu-id="71bcf-131">расположение.</span><span class="sxs-lookup"><span data-stu-id="71bcf-131">location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71bcf-132">-Name</span><span class="sxs-lookup"><span data-stu-id="71bcf-132">-Name</span></span>
<span data-ttu-id="71bcf-133">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="71bcf-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71bcf-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71bcf-134">-ResourceGroupName</span></span>
<span data-ttu-id="71bcf-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71bcf-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71bcf-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="71bcf-136">-RouteTable</span></span>
<span data-ttu-id="71bcf-137">Таблица маршрутов, связанная с этим виртуальным центром.</span><span class="sxs-lookup"><span data-stu-id="71bcf-137">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="71bcf-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="71bcf-138">-Sku</span></span>
<span data-ttu-id="71bcf-139">SKU виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="71bcf-139">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="71bcf-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="71bcf-140">-Tag</span></span>
<span data-ttu-id="71bcf-141">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="71bcf-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="71bcf-142">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="71bcf-142">-VirtualWan</span></span>
<span data-ttu-id="71bcf-143">Объект виртуальной wan, с который связан этот центр.</span><span class="sxs-lookup"><span data-stu-id="71bcf-143">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71bcf-144">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="71bcf-144">-VirtualWanId</span></span>
<span data-ttu-id="71bcf-145">Id объекта виртуальной wan, с который связан этот центр.</span><span class="sxs-lookup"><span data-stu-id="71bcf-145">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71bcf-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71bcf-146">-Confirm</span></span>
<span data-ttu-id="71bcf-147">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71bcf-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71bcf-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71bcf-148">-WhatIf</span></span>
<span data-ttu-id="71bcf-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71bcf-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71bcf-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="71bcf-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71bcf-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71bcf-151">CommonParameters</span></span>
<span data-ttu-id="71bcf-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71bcf-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71bcf-153">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71bcf-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71bcf-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71bcf-154">INPUTS</span></span>

### <span data-ttu-id="71bcf-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="71bcf-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="71bcf-156">System.String</span><span class="sxs-lookup"><span data-stu-id="71bcf-156">System.String</span></span>

## <span data-ttu-id="71bcf-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="71bcf-157">OUTPUTS</span></span>

### <span data-ttu-id="71bcf-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="71bcf-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="71bcf-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="71bcf-159">NOTES</span></span>

## <span data-ttu-id="71bcf-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71bcf-160">RELATED LINKS</span></span>

[<span data-ttu-id="71bcf-161">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="71bcf-161">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="71bcf-162">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="71bcf-162">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="71bcf-163">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="71bcf-163">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
