---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/remove-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
ms.openlocfilehash: 0253a5fa7cf5ff13c678eb0a6d86c31335239fdb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000115"
---
# <span data-ttu-id="67528-101">Remove-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="67528-101">Remove-AzResourceGraphQuery</span></span>

## <span data-ttu-id="67528-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67528-102">SYNOPSIS</span></span>
<span data-ttu-id="67528-103">Удаление запроса graph.</span><span class="sxs-lookup"><span data-stu-id="67528-103">Delete a graph query.</span></span>

## <span data-ttu-id="67528-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67528-104">SYNTAX</span></span>

### <span data-ttu-id="67528-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="67528-105">Delete (Default)</span></span>
```
Remove-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="67528-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="67528-106">DeleteViaIdentity</span></span>
```
Remove-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="67528-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67528-107">DESCRIPTION</span></span>
<span data-ttu-id="67528-108">Удаление запроса graph.</span><span class="sxs-lookup"><span data-stu-id="67528-108">Delete a graph query.</span></span>

## <span data-ttu-id="67528-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67528-109">EXAMPLES</span></span>

### <span data-ttu-id="67528-110">Пример 1. Удаление запроса на график ресурсов по имени</span><span class="sxs-lookup"><span data-stu-id="67528-110">Example 1: Remove a resource graph query by name</span></span>
```powershell
PS C:\> Remove-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03

```

<span data-ttu-id="67528-111">Эта команда удаляет запрос на график ресурсов по имени.</span><span class="sxs-lookup"><span data-stu-id="67528-111">This command removes a resource graph query by name.</span></span>

### <span data-ttu-id="67528-112">Пример 2. Удаление запроса на график ресурсов для объекта</span><span class="sxs-lookup"><span data-stu-id="67528-112">Example 2: Remove a resource graph query by object</span></span>
```powershell
PS C:\> $query = Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t02
PS C:\> Remove-AzResourceGraphQuery -InputObject $query 

```

<span data-ttu-id="67528-113">Эта команда удаляет запрос на график ресурсов для объекта.</span><span class="sxs-lookup"><span data-stu-id="67528-113">This command removes a resource graph query by object.</span></span>

## <span data-ttu-id="67528-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67528-114">PARAMETERS</span></span>

### <span data-ttu-id="67528-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67528-115">-DefaultProfile</span></span>
<span data-ttu-id="67528-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67528-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67528-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67528-117">-InputObject</span></span>
<span data-ttu-id="67528-118">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="67528-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67528-119">-Name</span><span class="sxs-lookup"><span data-stu-id="67528-119">-Name</span></span>
<span data-ttu-id="67528-120">Имя ресурса Graph Query.</span><span class="sxs-lookup"><span data-stu-id="67528-120">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67528-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67528-121">-PassThru</span></span>
<span data-ttu-id="67528-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="67528-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67528-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67528-123">-ResourceGroupName</span></span>
<span data-ttu-id="67528-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67528-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67528-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67528-125">-SubscriptionId</span></span>
<span data-ttu-id="67528-126">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="67528-126">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67528-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67528-127">-Confirm</span></span>
<span data-ttu-id="67528-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="67528-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67528-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67528-129">-WhatIf</span></span>
<span data-ttu-id="67528-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67528-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67528-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="67528-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67528-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67528-132">CommonParameters</span></span>
<span data-ttu-id="67528-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67528-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67528-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67528-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67528-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67528-135">INPUTS</span></span>

### <span data-ttu-id="67528-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="67528-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="67528-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67528-137">OUTPUTS</span></span>

### <span data-ttu-id="67528-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="67528-138">System.Boolean</span></span>

## <span data-ttu-id="67528-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67528-139">NOTES</span></span>

<span data-ttu-id="67528-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="67528-140">ALIASES</span></span>

<span data-ttu-id="67528-141">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="67528-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="67528-142">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="67528-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="67528-143">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="67528-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="67528-144">INPUTOBJECT <IResourceGraphIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="67528-144">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="67528-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="67528-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="67528-146">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67528-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="67528-147">`[ResourceName <String>]`: имя ресурса Graph Query.</span><span class="sxs-lookup"><span data-stu-id="67528-147">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="67528-148">`[SubscriptionId <String>]`: ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="67528-148">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="67528-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67528-149">RELATED LINKS</span></span>

