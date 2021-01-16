---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 997132e201864653307af3d072920d36b19d5af3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414876"
---
# <span data-ttu-id="7e83c-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7e83c-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="7e83c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e83c-102">SYNOPSIS</span></span>
<span data-ttu-id="7e83c-103">Создает пул средств аналитики Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="7e83c-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="7e83c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7e83c-104">SYNTAX</span></span>

### <span data-ttu-id="7e83c-105">CreateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7e83c-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e83c-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e83c-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e83c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e83c-107">DESCRIPTION</span></span>
<span data-ttu-id="7e83c-108">Для создания пула аналитики Azure Synapse Analytics создается SQL **AzSynapseSqlPool.**</span><span class="sxs-lookup"><span data-stu-id="7e83c-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="7e83c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7e83c-109">EXAMPLES</span></span>

### <span data-ttu-id="7e83c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7e83c-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="7e83c-111">Эта команда создает пул azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="7e83c-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="7e83c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e83c-112">PARAMETERS</span></span>

### <span data-ttu-id="7e83c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e83c-113">-AsJob</span></span>
<span data-ttu-id="7e83c-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7e83c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e83c-115">-Collation</span><span class="sxs-lookup"><span data-stu-id="7e83c-115">-Collation</span></span>
<span data-ttu-id="7e83c-116">Сортировка определяет правила сортировки и сравнения данных, и их невозможно изменить SQL создания пула.</span><span class="sxs-lookup"><span data-stu-id="7e83c-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="7e83c-117">По умолчанию для этого SQL_latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="7e83c-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="7e83c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e83c-118">-DefaultProfile</span></span>
<span data-ttu-id="7e83c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e83c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e83c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7e83c-120">-Name</span></span>
<span data-ttu-id="7e83c-121">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="7e83c-121">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="7e83c-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="7e83c-122">-PerformanceLevel</span></span>
<span data-ttu-id="7e83c-123">Уровень SQL службы и уровень производительности, которые нужно назначить SQL пулу.</span><span class="sxs-lookup"><span data-stu-id="7e83c-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="7e83c-124">Например, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="7e83c-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="7e83c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e83c-125">-ResourceGroupName</span></span>
<span data-ttu-id="7e83c-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e83c-126">Resource group name.</span></span>

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

### <span data-ttu-id="7e83c-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e83c-127">-Tag</span></span>
<span data-ttu-id="7e83c-128">Строковый строковый словарь тегов, связанный с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="7e83c-128">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="7e83c-129">-Версия</span><span class="sxs-lookup"><span data-stu-id="7e83c-129">-Version</span></span>
<span data-ttu-id="7e83c-130">Версия SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="7e83c-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="7e83c-131">Например, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="7e83c-131">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="7e83c-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7e83c-132">-WorkspaceName</span></span>
<span data-ttu-id="7e83c-133">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="7e83c-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7e83c-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7e83c-134">-WorkspaceObject</span></span>
<span data-ttu-id="7e83c-135">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="7e83c-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7e83c-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e83c-136">-Confirm</span></span>
<span data-ttu-id="7e83c-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e83c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e83c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e83c-138">-WhatIf</span></span>
<span data-ttu-id="7e83c-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e83c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e83c-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7e83c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e83c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e83c-141">CommonParameters</span></span>
<span data-ttu-id="7e83c-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e83c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e83c-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e83c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e83c-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e83c-144">INPUTS</span></span>

### <span data-ttu-id="7e83c-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7e83c-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7e83c-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7e83c-146">OUTPUTS</span></span>

### <span data-ttu-id="7e83c-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7e83c-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="7e83c-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7e83c-148">NOTES</span></span>

## <span data-ttu-id="7e83c-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e83c-149">RELATED LINKS</span></span>
