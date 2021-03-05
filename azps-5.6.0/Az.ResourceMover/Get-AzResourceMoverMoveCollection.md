---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: a10ac77515b225c5e5ef06335f9cee1e99ecd3b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000040"
---
# <span data-ttu-id="e461d-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="e461d-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="e461d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e461d-102">SYNOPSIS</span></span>
<span data-ttu-id="e461d-103">Возвращает коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="e461d-103">Gets the move collection.</span></span>

## <span data-ttu-id="e461d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e461d-104">SYNTAX</span></span>

### <span data-ttu-id="e461d-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e461d-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e461d-106">Получить</span><span class="sxs-lookup"><span data-stu-id="e461d-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e461d-107">Список1</span><span class="sxs-lookup"><span data-stu-id="e461d-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e461d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e461d-108">DESCRIPTION</span></span>
<span data-ttu-id="e461d-109">Возвращает коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="e461d-109">Gets the move collection.</span></span>

## <span data-ttu-id="e461d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e461d-110">EXAMPLES</span></span>

### <span data-ttu-id="e461d-111">Пример 1. Подробные сведения о всех коллекциях перемещения в подписке</span><span class="sxs-lookup"><span data-stu-id="e461d-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"270119e0-0000-0c00-0000-5f5c94940000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"39015ed4-0000-0c00-0000-5f5ce2760000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections
"1000b505-0000-0c00-0000-5f69db6e0000" centraluseuap MoveCollection-cus-eus-ccy         Microsoft.Migrate/moveCollections


```

<span data-ttu-id="e461d-112">Получите сведения о всех коллекциях перемещения в подписке.</span><span class="sxs-lookup"><span data-stu-id="e461d-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="e461d-113">Пример 2. Получите сведения о коллекции "Переместить" с указанным именем коллекции перемещения в подписке</span><span class="sxs-lookup"><span data-stu-id="e461d-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -Name "PS-centralus-westcentralus-demoRMS"

Etag                                   Location      Name                               Type                             
----                                   --------      ----                               ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS Microsoft.Migrate/moveCollections

```

<span data-ttu-id="e461d-114">Получите сведения о коллекции перемещения с указанным именем коллекции перемещения в подписке.</span><span class="sxs-lookup"><span data-stu-id="e461d-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="e461d-115">Пример 3. Подробные сведения о коллекции "Перемещение" с указанным именем группы ресурсов в подписке</span><span class="sxs-lookup"><span data-stu-id="e461d-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"4e02b0a9-0000-0c00-0000-5fd101cc0000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections

```

<span data-ttu-id="e461d-116">Получите сведения о move Collection с указанным именем группы ресурсов в подписке.</span><span class="sxs-lookup"><span data-stu-id="e461d-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="e461d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e461d-117">PARAMETERS</span></span>

### <span data-ttu-id="e461d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e461d-118">-DefaultProfile</span></span>
<span data-ttu-id="e461d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e461d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e461d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e461d-120">-Name</span></span>
<span data-ttu-id="e461d-121">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="e461d-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="e461d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e461d-122">-ResourceGroupName</span></span>
<span data-ttu-id="e461d-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e461d-123">The Resource Group Name.</span></span>

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

### <span data-ttu-id="e461d-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e461d-124">-SubscriptionId</span></span>
<span data-ttu-id="e461d-125">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="e461d-125">The Subscription ID.</span></span>

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

### <span data-ttu-id="e461d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e461d-126">CommonParameters</span></span>
<span data-ttu-id="e461d-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e461d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e461d-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e461d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e461d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e461d-129">INPUTS</span></span>

## <span data-ttu-id="e461d-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e461d-130">OUTPUTS</span></span>

### <span data-ttu-id="e461d-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="e461d-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span></span>

## <span data-ttu-id="e461d-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e461d-132">NOTES</span></span>

<span data-ttu-id="e461d-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e461d-133">ALIASES</span></span>

## <span data-ttu-id="e461d-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e461d-134">RELATED LINKS</span></span>

