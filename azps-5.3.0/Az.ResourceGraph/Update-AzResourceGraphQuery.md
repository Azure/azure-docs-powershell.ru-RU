---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/update-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
ms.openlocfilehash: 6ae44183a368babb43a93063518dfbf4f3d15e18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421004"
---
# <span data-ttu-id="93f80-101">Update-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="93f80-101">Update-AzResourceGraphQuery</span></span>

## <span data-ttu-id="93f80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93f80-102">SYNOPSIS</span></span>
<span data-ttu-id="93f80-103">Обновляет уже добавленный запрос на график.</span><span class="sxs-lookup"><span data-stu-id="93f80-103">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="93f80-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="93f80-104">SYNTAX</span></span>

### <span data-ttu-id="93f80-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="93f80-105">UpdateExpanded (Default)</span></span>
```
Update-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="93f80-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="93f80-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-Description <String>] [-File <String>]
 [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="93f80-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93f80-107">DESCRIPTION</span></span>
<span data-ttu-id="93f80-108">Обновляет уже добавленный запрос на график.</span><span class="sxs-lookup"><span data-stu-id="93f80-108">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="93f80-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="93f80-109">EXAMPLES</span></span>

### <span data-ttu-id="93f80-110">Пример 1. Обновление запроса с параметрами и тега по имени</span><span class="sxs-lookup"><span data-stu-id="93f80-110">Example 1: Update the parameter query and tag by name</span></span>
```powershell
PS C:\>  Update-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 -Query "project id, name, type, location, tags"  -Tag @{'key1'=1;'key2'=2}

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="93f80-111">Эта команда обновляет запрос с параметрами и тег по имени.</span><span class="sxs-lookup"><span data-stu-id="93f80-111">This command updates the parameter query and tag by name.</span></span>

### <span data-ttu-id="93f80-112">Пример 2. Обновление файла параметров по объектам</span><span class="sxs-lookup"><span data-stu-id="93f80-112">Example 2: Update the parameter file by object</span></span>
```powershell
PS C:\> $query =  Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 
PS C:\> Update-AzResourceGraphQuery -InputObject $query -File './Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="93f80-113">Эта команда обновляет запрос с параметрами и тег по объекту.</span><span class="sxs-lookup"><span data-stu-id="93f80-113">This command updates the parameter query and tag by object.</span></span>

## <span data-ttu-id="93f80-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93f80-114">PARAMETERS</span></span>

### <span data-ttu-id="93f80-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f80-115">-DefaultProfile</span></span>
<span data-ttu-id="93f80-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93f80-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93f80-117">-Description</span><span class="sxs-lookup"><span data-stu-id="93f80-117">-Description</span></span>
<span data-ttu-id="93f80-118">Описание запроса на диаграмму.</span><span class="sxs-lookup"><span data-stu-id="93f80-118">The description of a graph query.</span></span>

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

### <span data-ttu-id="93f80-119">-File</span><span class="sxs-lookup"><span data-stu-id="93f80-119">-File</span></span>
<span data-ttu-id="93f80-120">Содержимое файла будет передано параметру запроса.</span><span class="sxs-lookup"><span data-stu-id="93f80-120">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="93f80-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93f80-121">-InputObject</span></span>
<span data-ttu-id="93f80-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="93f80-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93f80-123">-Name</span><span class="sxs-lookup"><span data-stu-id="93f80-123">-Name</span></span>
<span data-ttu-id="93f80-124">Имя ресурса Graph Query.</span><span class="sxs-lookup"><span data-stu-id="93f80-124">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f80-125">-Query</span><span class="sxs-lookup"><span data-stu-id="93f80-125">-Query</span></span>
<span data-ttu-id="93f80-126">Запрос KQL, который будет графиком.</span><span class="sxs-lookup"><span data-stu-id="93f80-126">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="93f80-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93f80-127">-ResourceGroupName</span></span>
<span data-ttu-id="93f80-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93f80-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f80-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93f80-129">-SubscriptionId</span></span>
<span data-ttu-id="93f80-130">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="93f80-130">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f80-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="93f80-131">-Tag</span></span>
<span data-ttu-id="93f80-132">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="93f80-132">Resource tags</span></span>

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

### <span data-ttu-id="93f80-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93f80-133">-Confirm</span></span>
<span data-ttu-id="93f80-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="93f80-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93f80-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93f80-135">-WhatIf</span></span>
<span data-ttu-id="93f80-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93f80-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93f80-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="93f80-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93f80-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f80-138">CommonParameters</span></span>
<span data-ttu-id="93f80-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93f80-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f80-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93f80-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f80-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93f80-141">INPUTS</span></span>

### <span data-ttu-id="93f80-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="93f80-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="93f80-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="93f80-143">OUTPUTS</span></span>

### <span data-ttu-id="93f80-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="93f80-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="93f80-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="93f80-145">NOTES</span></span>

<span data-ttu-id="93f80-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="93f80-146">ALIASES</span></span>

<span data-ttu-id="93f80-147">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="93f80-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="93f80-148">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="93f80-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="93f80-149">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="93f80-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="93f80-150">INPUTOBJECT <IResourceGraphIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="93f80-150">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="93f80-151">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="93f80-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="93f80-152">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93f80-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="93f80-153">`[ResourceName <String>]`: имя ресурса Graph Query.</span><span class="sxs-lookup"><span data-stu-id="93f80-153">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="93f80-154">`[SubscriptionId <String>]`: ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="93f80-154">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="93f80-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93f80-155">RELATED LINKS</span></span>

