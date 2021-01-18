---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 73bb67577a9160440c2e42e1e5b3259ad8435c5c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505970"
---
# <span data-ttu-id="bf669-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="bf669-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="bf669-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf669-102">SYNOPSIS</span></span>
<span data-ttu-id="bf669-103">Возвращает коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="bf669-103">Gets the move collection.</span></span>

## <span data-ttu-id="bf669-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bf669-104">SYNTAX</span></span>

### <span data-ttu-id="bf669-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bf669-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf669-106">Получить</span><span class="sxs-lookup"><span data-stu-id="bf669-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bf669-107">Список1</span><span class="sxs-lookup"><span data-stu-id="bf669-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="bf669-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf669-108">DESCRIPTION</span></span>
<span data-ttu-id="bf669-109">Возвращает коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="bf669-109">Gets the move collection.</span></span>

## <span data-ttu-id="bf669-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bf669-110">EXAMPLES</span></span>

### <span data-ttu-id="bf669-111">Пример 1. Подробные сведения о всех коллекциях перемещения в подписке</span><span class="sxs-lookup"><span data-stu-id="bf669-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId e80eb9fa-c996-4435-aa32-5af6f3d3077c

Location    Name                                            Type
--------    ----                                            ----
eastus2     mvcolle2e07001                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e34745                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e56720                                  Microsoft.Migrate/moveCollections


```

<span data-ttu-id="bf669-112">Получите сведения о всех коллекциях перемещения в подписке.</span><span class="sxs-lookup"><span data-stu-id="bf669-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="bf669-113">Пример 2. Получите сведения о коллекции "Переместить" с указанным именем коллекции перемещения в подписке</span><span class="sxs-lookup"><span data-stu-id="bf669-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM -Name PS-centralus-westcentralus-demoRM

Location    Name                              Type
--------    ----                              ----
eastus2     PS-centralus-westcentralus-demoRM Microsoft.Migrate/moveCollections

```

<span data-ttu-id="bf669-114">Получите сведения о коллекции перемещения с указанным именем коллекции перемещения в подписке.</span><span class="sxs-lookup"><span data-stu-id="bf669-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="bf669-115">Пример 3. Подробные сведения о коллекции "Перемещение" с указанным именем группы ресурсов в подписке</span><span class="sxs-lookup"><span data-stu-id="bf669-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
eastus2euap PS-centralus-westcentralus-demoRM2 Microsoft.Migrate/moveCollections


```

<span data-ttu-id="bf669-116">Получите сведения о move Collection с указанным именем группы ресурсов в подписке.</span><span class="sxs-lookup"><span data-stu-id="bf669-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="bf669-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf669-117">PARAMETERS</span></span>

### <span data-ttu-id="bf669-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf669-118">-DefaultProfile</span></span>
<span data-ttu-id="bf669-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf669-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf669-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bf669-120">-Name</span></span>
<span data-ttu-id="bf669-121">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="bf669-121">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf669-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf669-122">-ResourceGroupName</span></span>
<span data-ttu-id="bf669-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bf669-123">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf669-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bf669-124">-SubscriptionId</span></span>
<span data-ttu-id="bf669-125">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="bf669-125">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf669-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf669-126">CommonParameters</span></span>
<span data-ttu-id="bf669-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf669-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf669-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf669-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf669-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf669-129">INPUTS</span></span>

## <span data-ttu-id="bf669-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bf669-130">OUTPUTS</span></span>

### <span data-ttu-id="bf669-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="bf669-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="bf669-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bf669-132">NOTES</span></span>

<span data-ttu-id="bf669-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bf669-133">ALIASES</span></span>

## <span data-ttu-id="bf669-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf669-134">RELATED LINKS</span></span>

