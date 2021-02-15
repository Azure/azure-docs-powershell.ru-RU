---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 01fa891933c8c3e3c0b4681a84d17b95ea06a6b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217780"
---
# <span data-ttu-id="50aff-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="50aff-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="50aff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50aff-102">SYNOPSIS</span></span>
<span data-ttu-id="50aff-103">Создает или обновляет коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="50aff-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="50aff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="50aff-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="50aff-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50aff-105">DESCRIPTION</span></span>
<span data-ttu-id="50aff-106">Создает или обновляет коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="50aff-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="50aff-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="50aff-107">EXAMPLES</span></span>

### <span data-ttu-id="50aff-108">Пример 1. Создание коллекции "Перемещение".</span><span class="sxs-lookup"><span data-stu-id="50aff-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name PS-centralus-westcentralus-demoRM  -ResourceGroupName RG-MoveCollection-demoRM -SourceRegion centralus -TargetRegion westcentralus -Location eastus2

Location Name                               Type
-------- ----                               ----
eastus2  PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
```

<span data-ttu-id="50aff-109">Создайте новую коллекцию перемещения в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="50aff-109">Create a new Move collection within a subscription.</span></span>

## <span data-ttu-id="50aff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50aff-110">PARAMETERS</span></span>

### <span data-ttu-id="50aff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50aff-111">-DefaultProfile</span></span>
<span data-ttu-id="50aff-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50aff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50aff-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="50aff-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="50aff-114">Получает или задает основной id.</span><span class="sxs-lookup"><span data-stu-id="50aff-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="50aff-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="50aff-115">-IdentityTenantId</span></span>
<span data-ttu-id="50aff-116">Возвращает или задает ид клиента.</span><span class="sxs-lookup"><span data-stu-id="50aff-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="50aff-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="50aff-117">-IdentityType</span></span>
<span data-ttu-id="50aff-118">Тип удостоверения, используемого для службы перемещения региона.</span><span class="sxs-lookup"><span data-stu-id="50aff-118">The type of identity used for the region move service.</span></span>

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

### <span data-ttu-id="50aff-119">-Location</span><span class="sxs-lookup"><span data-stu-id="50aff-119">-Location</span></span>
<span data-ttu-id="50aff-120">Географическое расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="50aff-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="50aff-121">-Name</span><span class="sxs-lookup"><span data-stu-id="50aff-121">-Name</span></span>
<span data-ttu-id="50aff-122">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="50aff-122">The Move Collection Name.</span></span>

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

### <span data-ttu-id="50aff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50aff-123">-ResourceGroupName</span></span>
<span data-ttu-id="50aff-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="50aff-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="50aff-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="50aff-125">-SourceRegion</span></span>
<span data-ttu-id="50aff-126">Возвращает или задает исходный регион.</span><span class="sxs-lookup"><span data-stu-id="50aff-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="50aff-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50aff-127">-SubscriptionId</span></span>
<span data-ttu-id="50aff-128">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="50aff-128">The Subscription ID.</span></span>

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

### <span data-ttu-id="50aff-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="50aff-129">-Tag</span></span>
<span data-ttu-id="50aff-130">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="50aff-130">Resource tags.</span></span>

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

### <span data-ttu-id="50aff-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="50aff-131">-TargetRegion</span></span>
<span data-ttu-id="50aff-132">Возвращает или задает целевой регион.</span><span class="sxs-lookup"><span data-stu-id="50aff-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="50aff-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50aff-133">-Confirm</span></span>
<span data-ttu-id="50aff-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50aff-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50aff-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50aff-135">-WhatIf</span></span>
<span data-ttu-id="50aff-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50aff-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50aff-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="50aff-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50aff-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50aff-138">CommonParameters</span></span>
<span data-ttu-id="50aff-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50aff-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50aff-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50aff-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50aff-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50aff-141">INPUTS</span></span>

## <span data-ttu-id="50aff-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50aff-142">OUTPUTS</span></span>

### <span data-ttu-id="50aff-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="50aff-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="50aff-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="50aff-144">NOTES</span></span>

<span data-ttu-id="50aff-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="50aff-145">ALIASES</span></span>

## <span data-ttu-id="50aff-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50aff-146">RELATED LINKS</span></span>

