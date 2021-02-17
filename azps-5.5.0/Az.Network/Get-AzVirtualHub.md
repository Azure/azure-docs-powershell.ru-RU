---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: 5f65ec635c71e64fb0e16d6a7391f188c6e2582c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236956"
---
# <span data-ttu-id="a0258-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a0258-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="a0258-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0258-102">SYNOPSIS</span></span>
<span data-ttu-id="a0258-103">Получает Azure VirtualHub по имени и resourceGroupName или перечисляет все виртуальные концентраторы по ResourceGroupName/Subscription.</span><span class="sxs-lookup"><span data-stu-id="a0258-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="a0258-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a0258-104">SYNTAX</span></span>

### <span data-ttu-id="a0258-105">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a0258-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0258-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0258-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0258-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0258-107">DESCRIPTION</span></span>
<span data-ttu-id="a0258-108">Получает Azure VirtualHub по имени и resourceGroupName или перечисляет все виртуальные концентраторы по ResourceGroupName/Subscription.</span><span class="sxs-lookup"><span data-stu-id="a0258-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="a0258-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a0258-109">EXAMPLES</span></span>

### <span data-ttu-id="a0258-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a0258-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"

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

<span data-ttu-id="a0258-111">Выше будет создаваться группа ресурсов TestRG, виртуальная WAN и виртуальный концентратор в западной части США в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="a0258-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="a0258-112">В виртуальном центре будет адресная площадь 10.0.1.0/24.</span><span class="sxs-lookup"><span data-stu-id="a0258-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="a0258-113">Затем он получает виртуальный концентратор, используя его ResourceGroupName и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="a0258-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="a0258-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a0258-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualHub -Name westushub*

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub1
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub1
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub2
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub2
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="a0258-115">Этот cmdlet получает виртуальный концентратор с помощью фильтрации.</span><span class="sxs-lookup"><span data-stu-id="a0258-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="a0258-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0258-116">PARAMETERS</span></span>

### <span data-ttu-id="a0258-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0258-117">-DefaultProfile</span></span>
<span data-ttu-id="a0258-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0258-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0258-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a0258-119">-Name</span></span>
<span data-ttu-id="a0258-120">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="a0258-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="a0258-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0258-121">-ResourceGroupName</span></span>
<span data-ttu-id="a0258-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a0258-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="a0258-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0258-123">CommonParameters</span></span>
<span data-ttu-id="a0258-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0258-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0258-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0258-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0258-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0258-126">INPUTS</span></span>

### <span data-ttu-id="a0258-127">Нет</span><span class="sxs-lookup"><span data-stu-id="a0258-127">None</span></span>

## <span data-ttu-id="a0258-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a0258-128">OUTPUTS</span></span>

### <span data-ttu-id="a0258-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a0258-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="a0258-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a0258-130">NOTES</span></span>

## <span data-ttu-id="a0258-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0258-131">RELATED LINKS</span></span>

[<span data-ttu-id="a0258-132">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a0258-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="a0258-133">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a0258-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="a0258-134">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a0258-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
