---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: 12bf5d24421f79eecb3138a68425968b9b4fbe62
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220889"
---
# <span data-ttu-id="47955-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="47955-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="47955-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47955-102">SYNOPSIS</span></span>
<span data-ttu-id="47955-103">Изменяет виртуальный концентратор, чтобы добавить в него виртуальную таблицу маршрутов HUb.</span><span class="sxs-lookup"><span data-stu-id="47955-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="47955-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="47955-104">SYNTAX</span></span>

### <span data-ttu-id="47955-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="47955-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47955-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="47955-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47955-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="47955-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47955-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47955-108">DESCRIPTION</span></span>
<span data-ttu-id="47955-109">{{ Заполнить в описании }}</span><span class="sxs-lookup"><span data-stu-id="47955-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="47955-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="47955-110">EXAMPLES</span></span>

### <span data-ttu-id="47955-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="47955-111">Example 1</span></span>
```powershell
PS C:\> $existingHub�=�Get-AzVirtualHub�-ResourceGroupName�"testRg"�-Name�"westushub"
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> $routeTable1�=�Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"
PS C:\> Set-AzVirtualHub�-VirtualHub�$existingHub�-RouteTable�@($routeTable1)

VirtualWan                            : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/testWan
ResourceGroupName                     : testRg
Name                                  : westushub
Id                                    : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubswestushub
AddressPrefix                         : 10.40.0.0/16
RouteTable                            : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkExpressRouteConnections :
RouteTables                           : {routeTable1}
Location                              : westus
Sku                                   : Standard
Type                                  : Microsoft.Network/virtualHubs
ProvisioningState                     : Succeeded
```

<span data-ttu-id="47955-112">Сначала мы создадим объект Virtual Hub Route и используем его для создания ресурса виртуальной таблицы маршрутов концентратора.</span><span class="sxs-lookup"><span data-stu-id="47955-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="47955-113">Затем мы перенастроим этот ресурс таблицы маршрутов на виртуальный концентратор с помощью Set-AzVirtualHub управления.</span><span class="sxs-lookup"><span data-stu-id="47955-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="47955-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47955-114">PARAMETERS</span></span>

### <span data-ttu-id="47955-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47955-115">-AsJob</span></span>
<span data-ttu-id="47955-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="47955-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47955-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47955-117">-DefaultProfile</span></span>
<span data-ttu-id="47955-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47955-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47955-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47955-119">-InputObject</span></span>
<span data-ttu-id="47955-120">Объект виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="47955-120">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="47955-121">-Name</span><span class="sxs-lookup"><span data-stu-id="47955-121">-Name</span></span>
<span data-ttu-id="47955-122">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="47955-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47955-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47955-123">-ResourceGroupName</span></span>
<span data-ttu-id="47955-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47955-124">The resource group name.</span></span>

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

### <span data-ttu-id="47955-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47955-125">-ResourceId</span></span>
<span data-ttu-id="47955-126">ИД ресурса виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="47955-126">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="47955-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="47955-127">-RouteTable</span></span>
<span data-ttu-id="47955-128">Таблицы маршрутов, связанные с этим виртуальным центром.</span><span class="sxs-lookup"><span data-stu-id="47955-128">The route tables associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47955-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="47955-129">-Tag</span></span>
<span data-ttu-id="47955-130">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="47955-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="47955-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47955-131">-Confirm</span></span>
<span data-ttu-id="47955-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="47955-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47955-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47955-133">-WhatIf</span></span>
<span data-ttu-id="47955-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47955-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47955-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="47955-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47955-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47955-136">CommonParameters</span></span>
<span data-ttu-id="47955-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47955-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47955-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47955-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47955-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47955-139">INPUTS</span></span>

### <span data-ttu-id="47955-140">System.String</span><span class="sxs-lookup"><span data-stu-id="47955-140">System.String</span></span>

### <span data-ttu-id="47955-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="47955-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="47955-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47955-142">OUTPUTS</span></span>

### <span data-ttu-id="47955-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="47955-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="47955-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="47955-144">NOTES</span></span>

## <span data-ttu-id="47955-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47955-145">RELATED LINKS</span></span>
