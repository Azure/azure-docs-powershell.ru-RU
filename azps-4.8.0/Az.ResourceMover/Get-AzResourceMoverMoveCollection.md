---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 73bb67577a9160440c2e42e1e5b3259ad8435c5c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242898"
---
# <span data-ttu-id="1907b-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="1907b-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="1907b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1907b-102">SYNOPSIS</span></span>
<span data-ttu-id="1907b-103">Получает коллекцию Move.</span><span class="sxs-lookup"><span data-stu-id="1907b-103">Gets the move collection.</span></span>

## <span data-ttu-id="1907b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1907b-104">SYNTAX</span></span>

### <span data-ttu-id="1907b-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1907b-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1907b-106">Получить</span><span class="sxs-lookup"><span data-stu-id="1907b-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1907b-107">List1</span><span class="sxs-lookup"><span data-stu-id="1907b-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1907b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1907b-108">DESCRIPTION</span></span>
<span data-ttu-id="1907b-109">Получает коллекцию Move.</span><span class="sxs-lookup"><span data-stu-id="1907b-109">Gets the move collection.</span></span>

## <span data-ttu-id="1907b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1907b-110">EXAMPLES</span></span>

### <span data-ttu-id="1907b-111">Пример 1: получение сведений обо всех коллекциях перемещения в подписке</span><span class="sxs-lookup"><span data-stu-id="1907b-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId e80eb9fa-c996-4435-aa32-5af6f3d3077c

Location    Name                                            Type
--------    ----                                            ----
eastus2     mvcolle2e07001                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e34745                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e56720                                  Microsoft.Migrate/moveCollections


```

<span data-ttu-id="1907b-112">Получение сведений обо всех коллекциях перемещения в подписке.</span><span class="sxs-lookup"><span data-stu-id="1907b-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="1907b-113">Пример 2: получение сведений о коллекции Move с указанным именем коллекции для перемещения в подписке</span><span class="sxs-lookup"><span data-stu-id="1907b-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM -Name PS-centralus-westcentralus-demoRM

Location    Name                              Type
--------    ----                              ----
eastus2     PS-centralus-westcentralus-demoRM Microsoft.Migrate/moveCollections

```

<span data-ttu-id="1907b-114">Получение подробных сведений о коллекции перемещения с указанным именем перемещения коллекции в подписке.</span><span class="sxs-lookup"><span data-stu-id="1907b-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="1907b-115">Пример 3: получение сведений о коллекции Move с указанным именем группы ресурсов в подписке</span><span class="sxs-lookup"><span data-stu-id="1907b-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
eastus2euap PS-centralus-westcentralus-demoRM2 Microsoft.Migrate/moveCollections


```

<span data-ttu-id="1907b-116">Получение сведений о коллекции Move с указанным именем группы ресурсов в подписке.</span><span class="sxs-lookup"><span data-stu-id="1907b-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="1907b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1907b-117">PARAMETERS</span></span>

### <span data-ttu-id="1907b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1907b-118">-DefaultProfile</span></span>
<span data-ttu-id="1907b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1907b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1907b-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1907b-120">-Name</span></span>
<span data-ttu-id="1907b-121">Имя перемещения коллекции.</span><span class="sxs-lookup"><span data-stu-id="1907b-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="1907b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1907b-122">-ResourceGroupName</span></span>
<span data-ttu-id="1907b-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1907b-123">The Resource Group Name.</span></span>

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

### <span data-ttu-id="1907b-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1907b-124">-SubscriptionId</span></span>
<span data-ttu-id="1907b-125">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="1907b-125">The Subscription ID.</span></span>

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

### <span data-ttu-id="1907b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1907b-126">CommonParameters</span></span>
<span data-ttu-id="1907b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1907b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1907b-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1907b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1907b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1907b-129">INPUTS</span></span>

## <span data-ttu-id="1907b-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1907b-130">OUTPUTS</span></span>

### <span data-ttu-id="1907b-131">Microsoft. Azure. PowerShell. командлеты. ResourceMover. Models. Api20191001Preview. IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="1907b-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="1907b-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="1907b-132">NOTES</span></span>

<span data-ttu-id="1907b-133">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="1907b-133">ALIASES</span></span>

## <span data-ttu-id="1907b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1907b-134">RELATED LINKS</span></span>
