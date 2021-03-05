---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 317614d67138b185dc58334d398bb368fc85911e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999891"
---
# <span data-ttu-id="cc206-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="cc206-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="cc206-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc206-102">SYNOPSIS</span></span>
<span data-ttu-id="cc206-103">Создает или обновляет коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="cc206-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="cc206-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cc206-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cc206-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc206-105">DESCRIPTION</span></span>
<span data-ttu-id="cc206-106">Создает или обновляет коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="cc206-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="cc206-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cc206-107">EXAMPLES</span></span>

### <span data-ttu-id="cc206-108">Пример 1. Создание коллекции "Перемещение".</span><span class="sxs-lookup"><span data-stu-id="cc206-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name "PS-centralus-westcentralus-demoRMS"  -ResourceGroupName "RG-MoveCollection-demoRMS" -SourceRegion "centralus" -TargetRegion "westcentralus" -Location "centraluseuap" -IdentityType "SystemAssigned"

Etag                                   Location      Name                               Type                             
----                                   --------      ----                               ----                             
"0200d92f-0000-3300-0000-6021e9ec0000" centraluseuap PS-centralus-westcentralus-demoRMs Microsoft.Migrate/moveCollections
```

<span data-ttu-id="cc206-109">Создайте новую коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="cc206-109">Create a new Move Collection.</span></span>

## <span data-ttu-id="cc206-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc206-110">PARAMETERS</span></span>

### <span data-ttu-id="cc206-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc206-111">-DefaultProfile</span></span>
<span data-ttu-id="cc206-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc206-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc206-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="cc206-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="cc206-114">Получает или задает основной id.</span><span class="sxs-lookup"><span data-stu-id="cc206-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="cc206-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="cc206-115">-IdentityTenantId</span></span>
<span data-ttu-id="cc206-116">Возвращает или задает ид клиента.</span><span class="sxs-lookup"><span data-stu-id="cc206-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="cc206-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="cc206-117">-IdentityType</span></span>
<span data-ttu-id="cc206-118">Тип удостоверения, используемого для службы mover ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc206-118">The type of identity used for the resource mover service.</span></span>

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

### <span data-ttu-id="cc206-119">-Location</span><span class="sxs-lookup"><span data-stu-id="cc206-119">-Location</span></span>
<span data-ttu-id="cc206-120">Географическое расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="cc206-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="cc206-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cc206-121">-Name</span></span>
<span data-ttu-id="cc206-122">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="cc206-122">The Move Collection Name.</span></span>

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

### <span data-ttu-id="cc206-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc206-123">-ResourceGroupName</span></span>
<span data-ttu-id="cc206-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc206-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="cc206-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="cc206-125">-SourceRegion</span></span>
<span data-ttu-id="cc206-126">Возвращает или задает исходный регион.</span><span class="sxs-lookup"><span data-stu-id="cc206-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="cc206-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc206-127">-SubscriptionId</span></span>
<span data-ttu-id="cc206-128">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="cc206-128">The Subscription ID.</span></span>

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

### <span data-ttu-id="cc206-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="cc206-129">-Tag</span></span>
<span data-ttu-id="cc206-130">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc206-130">Resource tags.</span></span>

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

### <span data-ttu-id="cc206-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="cc206-131">-TargetRegion</span></span>
<span data-ttu-id="cc206-132">Возвращает или задает целевой регион.</span><span class="sxs-lookup"><span data-stu-id="cc206-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="cc206-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc206-133">-Confirm</span></span>
<span data-ttu-id="cc206-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc206-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc206-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc206-135">-WhatIf</span></span>
<span data-ttu-id="cc206-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc206-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc206-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cc206-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc206-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc206-138">CommonParameters</span></span>
<span data-ttu-id="cc206-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc206-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc206-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc206-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc206-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc206-141">INPUTS</span></span>

## <span data-ttu-id="cc206-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc206-142">OUTPUTS</span></span>

### <span data-ttu-id="cc206-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="cc206-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span></span>

## <span data-ttu-id="cc206-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cc206-144">NOTES</span></span>

<span data-ttu-id="cc206-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cc206-145">ALIASES</span></span>

## <span data-ttu-id="cc206-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc206-146">RELATED LINKS</span></span>

