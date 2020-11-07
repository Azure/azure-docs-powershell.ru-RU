---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: 8527b383dd5469d1a9bc34b7916a1e28b3f673f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902070"
---
# <span data-ttu-id="09623-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="09623-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="09623-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09623-102">SYNOPSIS</span></span>
<span data-ttu-id="09623-103">Создание ресурса Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="09623-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="09623-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09623-104">SYNTAX</span></span>

### <span data-ttu-id="09623-105">ByVirtualWanObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="09623-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09623-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="09623-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09623-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09623-107">DESCRIPTION</span></span>
<span data-ttu-id="09623-108">Создание ресурса Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="09623-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="09623-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09623-109">EXAMPLES</span></span>

### <span data-ttu-id="09623-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="09623-110">Example 1</span></span>

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
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="09623-111">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="09623-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="09623-112">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="09623-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="09623-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="09623-113">Example 2</span></span>

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
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="09623-114">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="09623-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="09623-115">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="09623-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="09623-116">Этот пример похож на пример 1, но использует идентификатор ресурса для ссылки на виртуальную глобальную сеть, необходимую для создания виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="09623-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="09623-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="09623-117">Example 3</span></span>

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
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="09623-118">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="09623-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="09623-119">Для виртуального концентратора будет задано адресное пространство "10.0.1.0/24" и присоединенная таблица маршрутов.</span><span class="sxs-lookup"><span data-stu-id="09623-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="09623-120">Этот пример похож на пример 2, но также прикрепляет таблицу маршрутов к виртуальному концентратору.</span><span class="sxs-lookup"><span data-stu-id="09623-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="09623-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09623-121">PARAMETERS</span></span>

### <span data-ttu-id="09623-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="09623-122">-AddressPrefix</span></span>
<span data-ttu-id="09623-123">Строка адресного пространства для этого виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="09623-123">The address space string for this virtual hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09623-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09623-124">-AsJob</span></span>
<span data-ttu-id="09623-125">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="09623-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09623-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09623-126">-DefaultProfile</span></span>
<span data-ttu-id="09623-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="09623-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09623-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="09623-128">-HubVnetConnection</span></span>
<span data-ttu-id="09623-129">Подключения к виртуальной сети Hub, связанные с этим виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="09623-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09623-130">-Location</span><span class="sxs-lookup"><span data-stu-id="09623-130">-Location</span></span>
<span data-ttu-id="09623-131">поиска.</span><span class="sxs-lookup"><span data-stu-id="09623-131">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09623-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="09623-132">-Name</span></span>
<span data-ttu-id="09623-133">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="09623-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09623-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09623-134">-ResourceGroupName</span></span>
<span data-ttu-id="09623-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="09623-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09623-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="09623-136">-RouteTable</span></span>
<span data-ttu-id="09623-137">Таблица маршрутов, связанная с этим виртуальным центром.</span><span class="sxs-lookup"><span data-stu-id="09623-137">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09623-138">-Тег</span><span class="sxs-lookup"><span data-stu-id="09623-138">-Tag</span></span>
<span data-ttu-id="09623-139">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="09623-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09623-140">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="09623-140">-VirtualWan</span></span>
<span data-ttu-id="09623-141">Виртуальный объект глобальной сети, с которым связан этот концентратор.</span><span class="sxs-lookup"><span data-stu-id="09623-141">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09623-142">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="09623-142">-VirtualWanId</span></span>
<span data-ttu-id="09623-143">Идентификатор объекта виртуальной глобальной сети, с которым связан этот концентратор.</span><span class="sxs-lookup"><span data-stu-id="09623-143">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09623-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09623-144">-Confirm</span></span>
<span data-ttu-id="09623-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="09623-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09623-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09623-146">-WhatIf</span></span>
<span data-ttu-id="09623-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="09623-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09623-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="09623-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09623-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09623-149">CommonParameters</span></span>
<span data-ttu-id="09623-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09623-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09623-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09623-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09623-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09623-152">INPUTS</span></span>

### <span data-ttu-id="09623-153">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="09623-153">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="09623-154">System. String</span><span class="sxs-lookup"><span data-stu-id="09623-154">System.String</span></span>

## <span data-ttu-id="09623-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09623-155">OUTPUTS</span></span>

### <span data-ttu-id="09623-156">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="09623-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="09623-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="09623-157">NOTES</span></span>

## <span data-ttu-id="09623-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09623-158">RELATED LINKS</span></span>

[<span data-ttu-id="09623-159">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="09623-159">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="09623-160">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="09623-160">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="09623-161">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="09623-161">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
