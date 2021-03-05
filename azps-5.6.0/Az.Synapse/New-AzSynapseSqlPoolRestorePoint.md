---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 1f30dd8d0757e857934c1f8337e879cf1de8384e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963475"
---
# <span data-ttu-id="49243-101">New-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="49243-101">New-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="49243-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49243-102">SYNOPSIS</span></span>
<span data-ttu-id="49243-103">Создает новую точку восстановления в пуле аналитики Synapse Analytics SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="49243-103">Creates a new restore point in an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="49243-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="49243-104">SYNTAX</span></span>

### <span data-ttu-id="49243-105">CreateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49243-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49243-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49243-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49243-107">CreateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49243-107">CreateByInputObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49243-108">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49243-108">CreateByResourceIdParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -ResourceId <String> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49243-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49243-109">DESCRIPTION</span></span>
<span data-ttu-id="49243-110">Для создания новой точки восстановления, из SQL Azure Synapse Analytics, создается новый SQL **AzSynapseSqlPoolRestorePoint.**</span><span class="sxs-lookup"><span data-stu-id="49243-110">The **New-AzSynapseSqlPoolRestorePoint** cmdlet creates a new restore point that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="49243-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="49243-111">EXAMPLES</span></span>

### <span data-ttu-id="49243-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="49243-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -RestorePointLabel ContosoRestorePoint
```

<span data-ttu-id="49243-113">Эта команда создает точку восстановления для SQL contosoSqlPool в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="49243-113">This command creates a restore point for SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="49243-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49243-114">PARAMETERS</span></span>

### <span data-ttu-id="49243-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49243-115">-AsJob</span></span>
<span data-ttu-id="49243-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="49243-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49243-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49243-117">-DefaultProfile</span></span>
<span data-ttu-id="49243-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49243-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49243-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49243-119">-InputObject</span></span>
<span data-ttu-id="49243-120">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="49243-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49243-121">-Name</span><span class="sxs-lookup"><span data-stu-id="49243-121">-Name</span></span>
<span data-ttu-id="49243-122">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="49243-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49243-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49243-123">-ResourceGroupName</span></span>
<span data-ttu-id="49243-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49243-124">Resource group name.</span></span>

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

### <span data-ttu-id="49243-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49243-125">-ResourceId</span></span>
<span data-ttu-id="49243-126">Идентификатор ресурса в SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="49243-126">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49243-127">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="49243-127">-RestorePointLabel</span></span>
<span data-ttu-id="49243-128">Метка, с которая связывается с точкой восстановления, может быть не уникальной.</span><span class="sxs-lookup"><span data-stu-id="49243-128">The label we associate a restore point with, may not be unique.</span></span>

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

### <span data-ttu-id="49243-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="49243-129">-WorkspaceName</span></span>
<span data-ttu-id="49243-130">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="49243-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="49243-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="49243-131">-WorkspaceObject</span></span>
<span data-ttu-id="49243-132">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="49243-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="49243-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49243-133">-Confirm</span></span>
<span data-ttu-id="49243-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49243-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49243-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49243-135">-WhatIf</span></span>
<span data-ttu-id="49243-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49243-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49243-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="49243-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49243-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49243-138">CommonParameters</span></span>
<span data-ttu-id="49243-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49243-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49243-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49243-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49243-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49243-141">INPUTS</span></span>

### <span data-ttu-id="49243-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="49243-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="49243-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="49243-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="49243-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49243-144">OUTPUTS</span></span>

### <span data-ttu-id="49243-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="49243-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

## <span data-ttu-id="49243-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="49243-146">NOTES</span></span>

## <span data-ttu-id="49243-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49243-147">RELATED LINKS</span></span>
