---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: d4945c93fdfb402e56e1822229a1bb9592951d20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902846"
---
# <span data-ttu-id="6a558-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6a558-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="6a558-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6a558-102">SYNOPSIS</span></span>
<span data-ttu-id="6a558-103">Получает Azure VirtualHub по имени и ResourceGroupName или отображает список всех виртуальных концентраторов по ResourceGroupName и подписке.</span><span class="sxs-lookup"><span data-stu-id="6a558-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="6a558-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6a558-104">SYNTAX</span></span>

### <span data-ttu-id="6a558-105">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6a558-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a558-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a558-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a558-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a558-107">DESCRIPTION</span></span>
<span data-ttu-id="6a558-108">Получает Azure VirtualHub по имени и ResourceGroupName или отображает список всех виртуальных концентраторов по ResourceGroupName и подписке.</span><span class="sxs-lookup"><span data-stu-id="6a558-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="6a558-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6a558-109">EXAMPLES</span></span>

### <span data-ttu-id="6a558-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6a558-110">Example 1</span></span>

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

<span data-ttu-id="6a558-111">В описанном выше примере создается группа ресурсов "testRG", Виртуальная глобальная сеть и виртуальный концентратор (Запад США в этой группе ресурсов в Azure).</span><span class="sxs-lookup"><span data-stu-id="6a558-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="6a558-112">Виртуальный концентратор будет иметь адресное пространство "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="6a558-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="6a558-113">Затем он получает виртуальный концентратор, используя его ResourceGroupName и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="6a558-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="6a558-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6a558-114">Example 2</span></span>

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

<span data-ttu-id="6a558-115">Этот командлет получает виртуальный концентратор с помощью фильтрации.</span><span class="sxs-lookup"><span data-stu-id="6a558-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="6a558-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6a558-116">PARAMETERS</span></span>

### <span data-ttu-id="6a558-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a558-117">-DefaultProfile</span></span>
<span data-ttu-id="6a558-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a558-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a558-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6a558-119">-Name</span></span>
<span data-ttu-id="6a558-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="6a558-120">The resource name.</span></span>

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

### <span data-ttu-id="6a558-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a558-121">-ResourceGroupName</span></span>
<span data-ttu-id="6a558-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6a558-122">The resource group name.</span></span>

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

### <span data-ttu-id="6a558-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a558-123">CommonParameters</span></span>
<span data-ttu-id="6a558-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6a558-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a558-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a558-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a558-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6a558-126">INPUTS</span></span>

### <span data-ttu-id="6a558-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="6a558-127">None</span></span>

## <span data-ttu-id="6a558-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a558-128">OUTPUTS</span></span>

### <span data-ttu-id="6a558-129">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6a558-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="6a558-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="6a558-130">NOTES</span></span>

## <span data-ttu-id="6a558-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a558-131">RELATED LINKS</span></span>

[<span data-ttu-id="6a558-132">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6a558-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="6a558-133">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6a558-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="6a558-134">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6a558-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
