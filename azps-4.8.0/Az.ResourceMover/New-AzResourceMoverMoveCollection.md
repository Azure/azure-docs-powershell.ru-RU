---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 01fa891933c8c3e3c0b4681a84d17b95ea06a6b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235907"
---
# <span data-ttu-id="70924-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="70924-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="70924-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="70924-102">SYNOPSIS</span></span>
<span data-ttu-id="70924-103">Создание или обновление коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="70924-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="70924-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="70924-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="70924-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70924-105">DESCRIPTION</span></span>
<span data-ttu-id="70924-106">Создание или обновление коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="70924-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="70924-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="70924-107">EXAMPLES</span></span>

### <span data-ttu-id="70924-108">Пример 1: создание новой коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="70924-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name PS-centralus-westcentralus-demoRM  -ResourceGroupName RG-MoveCollection-demoRM -SourceRegion centralus -TargetRegion westcentralus -Location eastus2

Location Name                               Type
-------- ----                               ----
eastus2  PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
```

<span data-ttu-id="70924-109">Создание новой коллекции перемещения в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="70924-109">Create a new Move collection within a subscription.</span></span>

## <span data-ttu-id="70924-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="70924-110">PARAMETERS</span></span>

### <span data-ttu-id="70924-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70924-111">-DefaultProfile</span></span>
<span data-ttu-id="70924-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="70924-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70924-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="70924-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="70924-114">Возвращает или задает идентификатор участника.</span><span class="sxs-lookup"><span data-stu-id="70924-114">Gets or sets the principal id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70924-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="70924-115">-IdentityTenantId</span></span>
<span data-ttu-id="70924-116">Возвращает или задает идентификатор клиента.</span><span class="sxs-lookup"><span data-stu-id="70924-116">Gets or sets the tenant id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70924-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="70924-117">-IdentityType</span></span>
<span data-ttu-id="70924-118">Тип удостоверения, используемого для службы перемещения региона.</span><span class="sxs-lookup"><span data-stu-id="70924-118">The type of identity used for the region move service.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.ResourceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70924-119">-Location</span><span class="sxs-lookup"><span data-stu-id="70924-119">-Location</span></span>
<span data-ttu-id="70924-120">Географическое расположение, в котором находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="70924-120">The geo-location where the resource lives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70924-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="70924-121">-Name</span></span>
<span data-ttu-id="70924-122">Имя перемещения коллекции.</span><span class="sxs-lookup"><span data-stu-id="70924-122">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70924-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70924-123">-ResourceGroupName</span></span>
<span data-ttu-id="70924-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="70924-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="70924-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="70924-125">-SourceRegion</span></span>
<span data-ttu-id="70924-126">Возвращает или задает исходную область.</span><span class="sxs-lookup"><span data-stu-id="70924-126">Gets or sets the source region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70924-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70924-127">-SubscriptionId</span></span>
<span data-ttu-id="70924-128">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="70924-128">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70924-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="70924-129">-Tag</span></span>
<span data-ttu-id="70924-130">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="70924-130">Resource tags.</span></span>

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

### <span data-ttu-id="70924-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="70924-131">-TargetRegion</span></span>
<span data-ttu-id="70924-132">Возвращает или задает целевую область.</span><span class="sxs-lookup"><span data-stu-id="70924-132">Gets or sets the target region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70924-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70924-133">-Confirm</span></span>
<span data-ttu-id="70924-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="70924-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70924-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70924-135">-WhatIf</span></span>
<span data-ttu-id="70924-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="70924-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70924-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="70924-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70924-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70924-138">CommonParameters</span></span>
<span data-ttu-id="70924-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="70924-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70924-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70924-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70924-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="70924-141">INPUTS</span></span>

## <span data-ttu-id="70924-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="70924-142">OUTPUTS</span></span>

### <span data-ttu-id="70924-143">Microsoft. Azure. PowerShell. командлеты. ResourceMover. Models. Api20191001Preview. IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="70924-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="70924-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="70924-144">NOTES</span></span>

<span data-ttu-id="70924-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="70924-145">ALIASES</span></span>

## <span data-ttu-id="70924-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70924-146">RELATED LINKS</span></span>

