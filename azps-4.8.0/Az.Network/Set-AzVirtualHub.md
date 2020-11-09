---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: 12bf5d24421f79eecb3138a68425968b9b4fbe62
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244061"
---
# <span data-ttu-id="a11d5-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a11d5-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="a11d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a11d5-102">SYNOPSIS</span></span>
<span data-ttu-id="a11d5-103">Изменение виртуального концентратора для добавления в него таблицы виртуальных Ступицных маршрутов.</span><span class="sxs-lookup"><span data-stu-id="a11d5-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="a11d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a11d5-104">SYNTAX</span></span>

### <span data-ttu-id="a11d5-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a11d5-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a11d5-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="a11d5-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a11d5-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="a11d5-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a11d5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a11d5-108">DESCRIPTION</span></span>
<span data-ttu-id="a11d5-109">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="a11d5-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="a11d5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a11d5-110">EXAMPLES</span></span>

### <span data-ttu-id="a11d5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a11d5-111">Example 1</span></span>
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

<span data-ttu-id="a11d5-112">Сначала мы создаем объект маршрутизатора виртуального концентратора и используем его для создания ресурса таблицы виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="a11d5-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="a11d5-113">Затем мы устанавливаем этот ресурс таблицы маршрутов на виртуальный концентратор с помощью команды "Set-AzVirtualHub".</span><span class="sxs-lookup"><span data-stu-id="a11d5-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="a11d5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a11d5-114">PARAMETERS</span></span>

### <span data-ttu-id="a11d5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a11d5-115">-AsJob</span></span>
<span data-ttu-id="a11d5-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a11d5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a11d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a11d5-117">-DefaultProfile</span></span>
<span data-ttu-id="a11d5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a11d5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a11d5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a11d5-119">-InputObject</span></span>
<span data-ttu-id="a11d5-120">Объект виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="a11d5-120">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="a11d5-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a11d5-121">-Name</span></span>
<span data-ttu-id="a11d5-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="a11d5-122">The resource name.</span></span>

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

### <span data-ttu-id="a11d5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a11d5-123">-ResourceGroupName</span></span>
<span data-ttu-id="a11d5-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a11d5-124">The resource group name.</span></span>

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

### <span data-ttu-id="a11d5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a11d5-125">-ResourceId</span></span>
<span data-ttu-id="a11d5-126">Идентификатор ресурса виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="a11d5-126">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="a11d5-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="a11d5-127">-RouteTable</span></span>
<span data-ttu-id="a11d5-128">Таблицы маршрутов, связанные с этим виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="a11d5-128">The route tables associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="a11d5-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="a11d5-129">-Tag</span></span>
<span data-ttu-id="a11d5-130">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a11d5-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a11d5-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a11d5-131">-Confirm</span></span>
<span data-ttu-id="a11d5-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a11d5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a11d5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a11d5-133">-WhatIf</span></span>
<span data-ttu-id="a11d5-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a11d5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a11d5-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a11d5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a11d5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a11d5-136">CommonParameters</span></span>
<span data-ttu-id="a11d5-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a11d5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a11d5-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a11d5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a11d5-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a11d5-139">INPUTS</span></span>

### <span data-ttu-id="a11d5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a11d5-140">System.String</span></span>

### <span data-ttu-id="a11d5-141">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a11d5-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="a11d5-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a11d5-142">OUTPUTS</span></span>

### <span data-ttu-id="a11d5-143">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a11d5-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="a11d5-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="a11d5-144">NOTES</span></span>

## <span data-ttu-id="a11d5-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a11d5-145">RELATED LINKS</span></span>