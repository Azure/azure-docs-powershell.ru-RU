---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
ms.openlocfilehash: a07df2c6330757bf9e5b4f211429f6e2918fea39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911831"
---
# <span data-ttu-id="a3c89-101">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a3c89-101">Update-AzVirtualHub</span></span>

## <span data-ttu-id="a3c89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a3c89-102">SYNOPSIS</span></span>
<span data-ttu-id="a3c89-103">Обновляет виртуальный концентратор.</span><span class="sxs-lookup"><span data-stu-id="a3c89-103">Updates a virtual hub.</span></span>

## <span data-ttu-id="a3c89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a3c89-104">SYNTAX</span></span>

### <span data-ttu-id="a3c89-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a3c89-105">ByVirtualHubName (Default)</span></span>
```
Update-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3c89-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="a3c89-106">ByVirtualHubResourceId</span></span>
```
Update-AzVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3c89-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="a3c89-107">ByVirtualHubObject</span></span>
```
Update-AzVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3c89-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3c89-108">DESCRIPTION</span></span>
<span data-ttu-id="a3c89-109">Командлет **Update-AzVirtualHub** обновляет виртуальный концентратор.</span><span class="sxs-lookup"><span data-stu-id="a3c89-109">The **Update-AzVirtualHub** cmdlet updates a virtual hub.</span></span>

## <span data-ttu-id="a3c89-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a3c89-110">EXAMPLES</span></span>

### <span data-ttu-id="a3c89-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a3c89-111">Example 1</span></span>

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

<span data-ttu-id="a3c89-112">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="a3c89-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="a3c89-113">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="a3c89-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="a3c89-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a3c89-114">Example 2</span></span>

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

<span data-ttu-id="a3c89-115">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="a3c89-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="a3c89-116">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="a3c89-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="a3c89-117">Этот пример похож на пример 1, но также прикрепляет таблицу маршрутов к виртуальному концентратору.</span><span class="sxs-lookup"><span data-stu-id="a3c89-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="a3c89-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a3c89-118">PARAMETERS</span></span>

### <span data-ttu-id="a3c89-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a3c89-119">-AddressPrefix</span></span>
<span data-ttu-id="a3c89-120">Строка адресного пространства для этого виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="a3c89-120">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="a3c89-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3c89-121">-AsJob</span></span>
<span data-ttu-id="a3c89-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a3c89-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3c89-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3c89-123">-DefaultProfile</span></span>
<span data-ttu-id="a3c89-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3c89-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3c89-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a3c89-125">-HubVnetConnection</span></span>
<span data-ttu-id="a3c89-126">Подключения к виртуальной сети Hub, связанные с этим виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="a3c89-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="a3c89-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3c89-127">-InputObject</span></span>
<span data-ttu-id="a3c89-128">Объект виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="a3c89-128">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="a3c89-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a3c89-129">-Name</span></span>
<span data-ttu-id="a3c89-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="a3c89-130">The resource name.</span></span>

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

### <span data-ttu-id="a3c89-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3c89-131">-ResourceGroupName</span></span>
<span data-ttu-id="a3c89-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a3c89-132">The resource group name.</span></span>

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

### <span data-ttu-id="a3c89-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3c89-133">-ResourceId</span></span>
<span data-ttu-id="a3c89-134">Идентификатор ресурса виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="a3c89-134">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="a3c89-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="a3c89-135">-RouteTable</span></span>
<span data-ttu-id="a3c89-136">Таблица маршрутов, связанная с этим виртуальным центром.</span><span class="sxs-lookup"><span data-stu-id="a3c89-136">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="a3c89-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="a3c89-137">-Sku</span></span>
<span data-ttu-id="a3c89-138">SKU виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="a3c89-138">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="a3c89-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="a3c89-139">-Tag</span></span>
<span data-ttu-id="a3c89-140">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a3c89-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a3c89-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3c89-141">-Confirm</span></span>
<span data-ttu-id="a3c89-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a3c89-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3c89-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3c89-143">-WhatIf</span></span>
<span data-ttu-id="a3c89-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a3c89-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3c89-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a3c89-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3c89-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3c89-146">CommonParameters</span></span>
<span data-ttu-id="a3c89-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a3c89-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3c89-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3c89-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3c89-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a3c89-149">INPUTS</span></span>

### <span data-ttu-id="a3c89-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a3c89-150">System.String</span></span>

### <span data-ttu-id="a3c89-151">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a3c89-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="a3c89-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3c89-152">OUTPUTS</span></span>

### <span data-ttu-id="a3c89-153">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a3c89-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="a3c89-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="a3c89-154">NOTES</span></span>

## <span data-ttu-id="a3c89-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3c89-155">RELATED LINKS</span></span>

[<span data-ttu-id="a3c89-156">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a3c89-156">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="a3c89-157">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a3c89-157">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="a3c89-158">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a3c89-158">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)
