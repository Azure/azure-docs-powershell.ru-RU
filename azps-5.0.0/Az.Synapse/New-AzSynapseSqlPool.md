---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 997132e201864653307af3d072920d36b19d5af3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249294"
---
# <span data-ttu-id="46353-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="46353-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="46353-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46353-102">SYNOPSIS</span></span>
<span data-ttu-id="46353-103">Создание пула SQL Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="46353-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="46353-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46353-104">SYNTAX</span></span>

### <span data-ttu-id="46353-105">CreateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="46353-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46353-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46353-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46353-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46353-107">DESCRIPTION</span></span>
<span data-ttu-id="46353-108">Командлет **New-AzSynapseSqlPool** создает пул SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="46353-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="46353-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46353-109">EXAMPLES</span></span>

### <span data-ttu-id="46353-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46353-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="46353-111">Эта команда создает пул SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="46353-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="46353-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46353-112">PARAMETERS</span></span>

### <span data-ttu-id="46353-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46353-113">-AsJob</span></span>
<span data-ttu-id="46353-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="46353-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46353-115">-Параметры сортировки</span><span class="sxs-lookup"><span data-stu-id="46353-115">-Collation</span></span>
<span data-ttu-id="46353-116">Параметры сортировки определяют правила, которые сортируют и сравнивают данные, и их нельзя изменить после создания пула SQL.</span><span class="sxs-lookup"><span data-stu-id="46353-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="46353-117">Параметры сортировки по умолчанию SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="46353-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="46353-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46353-118">-DefaultProfile</span></span>
<span data-ttu-id="46353-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46353-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46353-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="46353-120">-Name</span></span>
<span data-ttu-id="46353-121">Имя пула SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="46353-121">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="46353-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="46353-122">-PerformanceLevel</span></span>
<span data-ttu-id="46353-123">Уровень производительности служб SQL, который нужно назначить пулу SQL.</span><span class="sxs-lookup"><span data-stu-id="46353-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="46353-124">Например, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="46353-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="46353-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46353-125">-ResourceGroupName</span></span>
<span data-ttu-id="46353-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46353-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46353-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="46353-127">-Tag</span></span>
<span data-ttu-id="46353-128">Строковый словарь тегов, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="46353-128">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="46353-129">-Version</span><span class="sxs-lookup"><span data-stu-id="46353-129">-Version</span></span>
<span data-ttu-id="46353-130">Версия пула Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="46353-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="46353-131">Например, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="46353-131">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46353-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="46353-132">-WorkspaceName</span></span>
<span data-ttu-id="46353-133">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="46353-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46353-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="46353-134">-WorkspaceObject</span></span>
<span data-ttu-id="46353-135">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="46353-135">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46353-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46353-136">-Confirm</span></span>
<span data-ttu-id="46353-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="46353-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46353-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46353-138">-WhatIf</span></span>
<span data-ttu-id="46353-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="46353-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46353-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="46353-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46353-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46353-141">CommonParameters</span></span>
<span data-ttu-id="46353-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46353-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46353-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46353-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46353-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46353-144">INPUTS</span></span>

### <span data-ttu-id="46353-145">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="46353-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="46353-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46353-146">OUTPUTS</span></span>

### <span data-ttu-id="46353-147">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="46353-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="46353-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="46353-148">NOTES</span></span>

## <span data-ttu-id="46353-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46353-149">RELATED LINKS</span></span>
