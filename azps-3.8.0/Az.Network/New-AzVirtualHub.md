---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: d005ef841828dc1fe37915c4a7b0d28ad93e3b44
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073365"
---
# <span data-ttu-id="ae0b7-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ae0b7-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="ae0b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae0b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ae0b7-103">Создание ресурса Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="ae0b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae0b7-104">SYNTAX</span></span>

### <span data-ttu-id="ae0b7-105">ByVirtualWanObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ae0b7-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae0b7-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="ae0b7-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae0b7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae0b7-107">DESCRIPTION</span></span>
<span data-ttu-id="ae0b7-108">Создание ресурса Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="ae0b7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae0b7-109">EXAMPLES</span></span>

### <span data-ttu-id="ae0b7-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ae0b7-110">Example 1</span></span>

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

<span data-ttu-id="ae0b7-111">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="ae0b7-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="ae0b7-112">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="ae0b7-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="ae0b7-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ae0b7-113">Example 2</span></span>

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

<span data-ttu-id="ae0b7-114">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="ae0b7-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="ae0b7-115">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="ae0b7-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="ae0b7-116">Этот пример похож на пример 1, но использует идентификатор ресурса для ссылки на виртуальную глобальную сеть, необходимую для создания виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="ae0b7-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ae0b7-117">Example 3</span></span>

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

<span data-ttu-id="ae0b7-118">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="ae0b7-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="ae0b7-119">Для виртуального концентратора будет задано адресное пространство "10.0.1.0/24" и присоединенная таблица маршрутов.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="ae0b7-120">Этот пример похож на пример 2, но также прикрепляет таблицу маршрутов к виртуальному концентратору.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="ae0b7-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae0b7-121">PARAMETERS</span></span>

### <span data-ttu-id="ae0b7-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ae0b7-122">-AddressPrefix</span></span>
<span data-ttu-id="ae0b7-123">Строка адресного пространства для этого виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-123">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="ae0b7-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae0b7-124">-AsJob</span></span>
<span data-ttu-id="ae0b7-125">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ae0b7-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae0b7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae0b7-126">-DefaultProfile</span></span>
<span data-ttu-id="ae0b7-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae0b7-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="ae0b7-128">-HubVnetConnection</span></span>
<span data-ttu-id="ae0b7-129">Подключения к виртуальной сети Hub, связанные с этим виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="ae0b7-130">-Location</span><span class="sxs-lookup"><span data-stu-id="ae0b7-130">-Location</span></span>
<span data-ttu-id="ae0b7-131">поиска.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-131">location.</span></span>

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

### <span data-ttu-id="ae0b7-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ae0b7-132">-Name</span></span>
<span data-ttu-id="ae0b7-133">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-133">The resource name.</span></span>

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

### <span data-ttu-id="ae0b7-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae0b7-134">-ResourceGroupName</span></span>
<span data-ttu-id="ae0b7-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-135">The resource group name.</span></span>

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

### <span data-ttu-id="ae0b7-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="ae0b7-136">-RouteTable</span></span>
<span data-ttu-id="ae0b7-137">Таблица маршрутов, связанная с этим виртуальным центром.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-137">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="ae0b7-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="ae0b7-138">-Sku</span></span>
<span data-ttu-id="ae0b7-139">SKU виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-139">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="ae0b7-140">-Тег</span><span class="sxs-lookup"><span data-stu-id="ae0b7-140">-Tag</span></span>
<span data-ttu-id="ae0b7-141">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ae0b7-142">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae0b7-142">-VirtualWan</span></span>
<span data-ttu-id="ae0b7-143">Виртуальный объект глобальной сети, с которым связан этот концентратор.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-143">The virtual wan object this hub is linked to.</span></span>

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

### <span data-ttu-id="ae0b7-144">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="ae0b7-144">-VirtualWanId</span></span>
<span data-ttu-id="ae0b7-145">Идентификатор объекта виртуальной глобальной сети, с которым связан этот концентратор.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-145">The id of virtual wan object this hub is linked to.</span></span>

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

### <span data-ttu-id="ae0b7-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae0b7-146">-Confirm</span></span>
<span data-ttu-id="ae0b7-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae0b7-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae0b7-148">-WhatIf</span></span>
<span data-ttu-id="ae0b7-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae0b7-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae0b7-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae0b7-151">CommonParameters</span></span>
<span data-ttu-id="ae0b7-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae0b7-153">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae0b7-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae0b7-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae0b7-154">INPUTS</span></span>

### <span data-ttu-id="ae0b7-155">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae0b7-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="ae0b7-156">System. String</span><span class="sxs-lookup"><span data-stu-id="ae0b7-156">System.String</span></span>

## <span data-ttu-id="ae0b7-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae0b7-157">OUTPUTS</span></span>

### <span data-ttu-id="ae0b7-158">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ae0b7-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="ae0b7-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae0b7-159">NOTES</span></span>

## <span data-ttu-id="ae0b7-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae0b7-160">RELATED LINKS</span></span>

[<span data-ttu-id="ae0b7-161">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ae0b7-161">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="ae0b7-162">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ae0b7-162">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="ae0b7-163">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ae0b7-163">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
