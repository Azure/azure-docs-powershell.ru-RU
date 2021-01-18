---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/new-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
ms.openlocfilehash: 853c06c6179f25065efba71b2d148c36e2d74ef4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505974"
---
# <span data-ttu-id="35db2-101">New-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="35db2-101">New-AzResourceGraphQuery</span></span>

## <span data-ttu-id="35db2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35db2-102">SYNOPSIS</span></span>
<span data-ttu-id="35db2-103">Создание запроса на создание графика.</span><span class="sxs-lookup"><span data-stu-id="35db2-103">Create a new graph query.</span></span>

## <span data-ttu-id="35db2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35db2-104">SYNTAX</span></span>

```
New-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Location <String>] [-Query <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35db2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35db2-105">DESCRIPTION</span></span>
<span data-ttu-id="35db2-106">Создание запроса на создание графика.</span><span class="sxs-lookup"><span data-stu-id="35db2-106">Create a new graph query.</span></span>

## <span data-ttu-id="35db2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35db2-107">EXAMPLES</span></span>

### <span data-ttu-id="35db2-108">Пример 1. Создание запроса на график ресурсов с помощью параметра запроса</span><span class="sxs-lookup"><span data-stu-id="35db2-108">Example 1: Create a resource graph query by the query parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t03 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -Query "project id, name, type, location, tags" 


Location Name      Type
-------- ----      ----
     global   query-t03 microsoft.resourcegraph/queries
```

<span data-ttu-id="35db2-109">Эта команда создает запрос на график ресурсов с помощью параметра запроса.</span><span class="sxs-lookup"><span data-stu-id="35db2-109">This command creates a resource graph query by the query parameter.</span></span>

### <span data-ttu-id="35db2-110">Пример 2. Создание запроса на график ресурсов с помощью параметра файла</span><span class="sxs-lookup"><span data-stu-id="35db2-110">Example 2: Create a resource graph query by the file parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t04 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -File 'D:\azure-service\ResourceGraph.Autorest\azure-powershell\src\ResourceGraph\ResourceGraph.Autorest\test\Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t04 microsoft.resourcegraph/queries
```

<span data-ttu-id="35db2-111">Эта команда создает запрос на график ресурсов с помощью параметра файла.</span><span class="sxs-lookup"><span data-stu-id="35db2-111">This command creates a resource graph query by the file parameter.</span></span>

## <span data-ttu-id="35db2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35db2-112">PARAMETERS</span></span>

### <span data-ttu-id="35db2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35db2-113">-DefaultProfile</span></span>
<span data-ttu-id="35db2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35db2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35db2-115">-Description</span><span class="sxs-lookup"><span data-stu-id="35db2-115">-Description</span></span>
<span data-ttu-id="35db2-116">Описание запроса на диаграмму.</span><span class="sxs-lookup"><span data-stu-id="35db2-116">The description of a graph query.</span></span>

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

### <span data-ttu-id="35db2-117">-File</span><span class="sxs-lookup"><span data-stu-id="35db2-117">-File</span></span>
<span data-ttu-id="35db2-118">Содержимое файла будет передано параметру запроса.</span><span class="sxs-lookup"><span data-stu-id="35db2-118">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="35db2-119">-Location</span><span class="sxs-lookup"><span data-stu-id="35db2-119">-Location</span></span>
<span data-ttu-id="35db2-120">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="35db2-120">The location of the resource</span></span>

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

### <span data-ttu-id="35db2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="35db2-121">-Name</span></span>
<span data-ttu-id="35db2-122">Имя ресурса Graph Query.</span><span class="sxs-lookup"><span data-stu-id="35db2-122">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="35db2-123">-Query</span><span class="sxs-lookup"><span data-stu-id="35db2-123">-Query</span></span>
<span data-ttu-id="35db2-124">Запрос KQL, который будет графиком.</span><span class="sxs-lookup"><span data-stu-id="35db2-124">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="35db2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35db2-125">-ResourceGroupName</span></span>
<span data-ttu-id="35db2-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35db2-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="35db2-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35db2-127">-SubscriptionId</span></span>
<span data-ttu-id="35db2-128">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="35db2-128">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="35db2-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="35db2-129">-Tag</span></span>
<span data-ttu-id="35db2-130">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="35db2-130">Resource tags</span></span>

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

### <span data-ttu-id="35db2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35db2-131">-Confirm</span></span>
<span data-ttu-id="35db2-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35db2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35db2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35db2-133">-WhatIf</span></span>
<span data-ttu-id="35db2-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35db2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35db2-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="35db2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35db2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35db2-136">CommonParameters</span></span>
<span data-ttu-id="35db2-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35db2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35db2-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35db2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35db2-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35db2-139">INPUTS</span></span>

### <span data-ttu-id="35db2-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="35db2-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

### <span data-ttu-id="35db2-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="35db2-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="35db2-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35db2-142">OUTPUTS</span></span>

### <span data-ttu-id="35db2-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="35db2-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="35db2-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35db2-144">NOTES</span></span>

<span data-ttu-id="35db2-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="35db2-145">ALIASES</span></span>

## <span data-ttu-id="35db2-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35db2-146">RELATED LINKS</span></span>

