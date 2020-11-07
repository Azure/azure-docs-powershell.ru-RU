---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHub.md
ms.openlocfilehash: 4058f9a2ba0de1e5610773ad4af21c8bb788d58c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733153"
---
# <span data-ttu-id="45968-101">New-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="45968-101">New-AzureRmVirtualHub</span></span>

## <span data-ttu-id="45968-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45968-102">SYNOPSIS</span></span>
<span data-ttu-id="45968-103">Создание ресурса Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="45968-103">Creates an Azure VirtualHub resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45968-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45968-104">SYNTAX</span></span>

### <span data-ttu-id="45968-105">ByVirtualWanObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45968-105">ByVirtualWanObject (Default)</span></span>
```
New-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan>
 -AddressPrefix <String> -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45968-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="45968-106">ByVirtualWanResourceId</span></span>
```
New-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45968-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45968-107">DESCRIPTION</span></span>
<span data-ttu-id="45968-108">Создание ресурса Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="45968-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="45968-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45968-109">EXAMPLES</span></span>

### <span data-ttu-id="45968-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="45968-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

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

<span data-ttu-id="45968-111">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="45968-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="45968-112">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="45968-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="45968-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="45968-113">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

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

<span data-ttu-id="45968-114">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="45968-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="45968-115">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="45968-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="45968-116">Этот пример похож на пример 1, но использует идентификатор ресурса для ссылки на виртуальную глобальную сеть, необходимую для создания виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="45968-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="45968-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="45968-117">Example 3</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzureRmVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzureRmVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzureRmVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzureRmVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

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

<span data-ttu-id="45968-118">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="45968-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="45968-119">Для виртуального концентратора будет задано адресное пространство "10.0.1.0/24" и присоединенная таблица маршрутов.</span><span class="sxs-lookup"><span data-stu-id="45968-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="45968-120">Этот пример похож на пример 2, но также прикрепляет таблицу маршрутов к виртуальному концентратору.</span><span class="sxs-lookup"><span data-stu-id="45968-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="45968-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45968-121">PARAMETERS</span></span>

### <span data-ttu-id="45968-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="45968-122">-AddressPrefix</span></span>
<span data-ttu-id="45968-123">Строка адресного пространства для этого виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="45968-123">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="45968-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45968-124">-AsJob</span></span>
<span data-ttu-id="45968-125">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="45968-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45968-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45968-126">-DefaultProfile</span></span>
<span data-ttu-id="45968-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45968-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45968-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="45968-128">-HubVnetConnection</span></span>
<span data-ttu-id="45968-129">Подключения к виртуальной сети Hub, связанные с этим виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="45968-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="45968-130">-Location</span><span class="sxs-lookup"><span data-stu-id="45968-130">-Location</span></span>
<span data-ttu-id="45968-131">поиска.</span><span class="sxs-lookup"><span data-stu-id="45968-131">location.</span></span>

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

### <span data-ttu-id="45968-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="45968-132">-Name</span></span>
<span data-ttu-id="45968-133">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="45968-133">The resource name.</span></span>

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

### <span data-ttu-id="45968-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45968-134">-ResourceGroupName</span></span>
<span data-ttu-id="45968-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45968-135">The resource group name.</span></span>

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

### <span data-ttu-id="45968-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="45968-136">-RouteTable</span></span>
<span data-ttu-id="45968-137">Таблица маршрутов, связанная с этим виртуальным центром.</span><span class="sxs-lookup"><span data-stu-id="45968-137">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="45968-138">-Тег</span><span class="sxs-lookup"><span data-stu-id="45968-138">-Tag</span></span>
<span data-ttu-id="45968-139">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45968-139">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="45968-140">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="45968-140">-VirtualWan</span></span>
<span data-ttu-id="45968-141">Виртуальный объект глобальной сети, с которым связан этот концентратор.</span><span class="sxs-lookup"><span data-stu-id="45968-141">The virtual wan object this hub is linked to.</span></span>

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

### <span data-ttu-id="45968-142">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="45968-142">-VirtualWanId</span></span>
<span data-ttu-id="45968-143">Идентификатор объекта виртуальной глобальной сети, с которым связан этот концентратор.</span><span class="sxs-lookup"><span data-stu-id="45968-143">The id of virtual wan object this hub is linked to.</span></span>

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

### <span data-ttu-id="45968-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45968-144">-Confirm</span></span>
<span data-ttu-id="45968-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="45968-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45968-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45968-146">-WhatIf</span></span>
<span data-ttu-id="45968-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="45968-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45968-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="45968-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45968-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45968-149">CommonParameters</span></span>
<span data-ttu-id="45968-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45968-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45968-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45968-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45968-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45968-152">INPUTS</span></span>

### <span data-ttu-id="45968-153">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="45968-153">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="45968-154">System. String</span><span class="sxs-lookup"><span data-stu-id="45968-154">System.String</span></span>

## <span data-ttu-id="45968-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45968-155">OUTPUTS</span></span>

### <span data-ttu-id="45968-156">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="45968-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="45968-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="45968-157">NOTES</span></span>

## <span data-ttu-id="45968-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45968-158">RELATED LINKS</span></span>
