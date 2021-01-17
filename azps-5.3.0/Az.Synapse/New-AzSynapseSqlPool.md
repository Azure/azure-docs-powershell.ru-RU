---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: bb653669ff15dad78ce3cec10f406aa099808e55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424252"
---
# <span data-ttu-id="30f6f-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="30f6f-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="30f6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="30f6f-103">Создает пул средств аналитики Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="30f6f-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="30f6f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="30f6f-104">SYNTAX</span></span>

### <span data-ttu-id="30f6f-105">CreateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="30f6f-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30f6f-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30f6f-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30f6f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30f6f-107">DESCRIPTION</span></span>
<span data-ttu-id="30f6f-108">Для создания пула аналитики Azure Synapse Analytics создается SQL **AzSynapseSqlPool.**</span><span class="sxs-lookup"><span data-stu-id="30f6f-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="30f6f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="30f6f-109">EXAMPLES</span></span>

### <span data-ttu-id="30f6f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="30f6f-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="30f6f-111">Эта команда создает пул azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="30f6f-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="30f6f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30f6f-112">PARAMETERS</span></span>

### <span data-ttu-id="30f6f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30f6f-113">-AsJob</span></span>
<span data-ttu-id="30f6f-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="30f6f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30f6f-115">-Collation</span><span class="sxs-lookup"><span data-stu-id="30f6f-115">-Collation</span></span>
<span data-ttu-id="30f6f-116">Сортировка определяет правила сортировки и сравнения данных, и их невозможно изменить SQL создания пула.</span><span class="sxs-lookup"><span data-stu-id="30f6f-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="30f6f-117">По умолчанию для этого SQL_latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="30f6f-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="30f6f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f6f-118">-DefaultProfile</span></span>
<span data-ttu-id="30f6f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30f6f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30f6f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="30f6f-120">-Name</span></span>
<span data-ttu-id="30f6f-121">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="30f6f-121">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f6f-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="30f6f-122">-PerformanceLevel</span></span>
<span data-ttu-id="30f6f-123">Уровень SQL и уровень производительности службы, которые нужно назначить SQL пулу.</span><span class="sxs-lookup"><span data-stu-id="30f6f-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="30f6f-124">Например, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="30f6f-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="30f6f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30f6f-125">-ResourceGroupName</span></span>
<span data-ttu-id="30f6f-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30f6f-126">Resource group name.</span></span>

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

### <span data-ttu-id="30f6f-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="30f6f-127">-Tag</span></span>
<span data-ttu-id="30f6f-128">Строковый строковый словарь тегов, связанный с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="30f6f-128">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="30f6f-129">-Версия</span><span class="sxs-lookup"><span data-stu-id="30f6f-129">-Version</span></span>
<span data-ttu-id="30f6f-130">Версия SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="30f6f-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="30f6f-131">Например, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="30f6f-131">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="30f6f-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="30f6f-132">-WorkspaceName</span></span>
<span data-ttu-id="30f6f-133">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="30f6f-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="30f6f-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="30f6f-134">-WorkspaceObject</span></span>
<span data-ttu-id="30f6f-135">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="30f6f-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="30f6f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30f6f-136">-Confirm</span></span>
<span data-ttu-id="30f6f-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="30f6f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30f6f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30f6f-138">-WhatIf</span></span>
<span data-ttu-id="30f6f-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30f6f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30f6f-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="30f6f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30f6f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f6f-141">CommonParameters</span></span>
<span data-ttu-id="30f6f-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30f6f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f6f-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30f6f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f6f-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30f6f-144">INPUTS</span></span>

### <span data-ttu-id="30f6f-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="30f6f-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="30f6f-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="30f6f-146">OUTPUTS</span></span>

### <span data-ttu-id="30f6f-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="30f6f-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="30f6f-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="30f6f-148">NOTES</span></span>

## <span data-ttu-id="30f6f-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30f6f-149">RELATED LINKS</span></span>
