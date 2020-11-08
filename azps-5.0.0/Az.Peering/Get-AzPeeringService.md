---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 016701a762a87ec03912cda62dd5f436f1a45950
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246377"
---
# <span data-ttu-id="43bc8-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="43bc8-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="43bc8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="43bc8-103">Получение списка объектов службы пиринга для одного объекта.</span><span class="sxs-lookup"><span data-stu-id="43bc8-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="43bc8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43bc8-104">SYNTAX</span></span>

### <span data-ttu-id="43bc8-105">ByResourceGroupName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="43bc8-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43bc8-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="43bc8-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43bc8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="43bc8-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43bc8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43bc8-108">DESCRIPTION</span></span>
<span data-ttu-id="43bc8-109">Получение служб пиринга для подписки</span><span class="sxs-lookup"><span data-stu-id="43bc8-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="43bc8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43bc8-110">EXAMPLES</span></span>

### <span data-ttu-id="43bc8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="43bc8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="43bc8-112">Возвращает службу пиринга для группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="43bc8-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="43bc8-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="43bc8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="43bc8-114">Возвращает службу пиринга для группы ресурсов и имени.</span><span class="sxs-lookup"><span data-stu-id="43bc8-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="43bc8-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="43bc8-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceId $rid

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="43bc8-116">Возвращает службу пиринга по идентификатору ресурса.</span><span class="sxs-lookup"><span data-stu-id="43bc8-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="43bc8-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43bc8-117">PARAMETERS</span></span>

### <span data-ttu-id="43bc8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43bc8-118">-DefaultProfile</span></span>
<span data-ttu-id="43bc8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43bc8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43bc8-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="43bc8-120">-Name</span></span>
<span data-ttu-id="43bc8-121">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="43bc8-121">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43bc8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43bc8-122">-ResourceGroupName</span></span>
<span data-ttu-id="43bc8-123">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="43bc8-123">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43bc8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43bc8-124">-ResourceId</span></span>
<span data-ttu-id="43bc8-125">Имя строки идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="43bc8-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43bc8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43bc8-126">CommonParameters</span></span>
<span data-ttu-id="43bc8-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43bc8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43bc8-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43bc8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43bc8-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43bc8-129">INPUTS</span></span>

### <span data-ttu-id="43bc8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="43bc8-130">System.String</span></span>

## <span data-ttu-id="43bc8-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43bc8-131">OUTPUTS</span></span>

### <span data-ttu-id="43bc8-132">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringService)</span><span class="sxs-lookup"><span data-stu-id="43bc8-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="43bc8-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="43bc8-133">NOTES</span></span>

## <span data-ttu-id="43bc8-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43bc8-134">RELATED LINKS</span></span>
