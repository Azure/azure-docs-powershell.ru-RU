---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 574c41fe8b0f3266a6fff80c020b60c9832cb431
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216804"
---
# <span data-ttu-id="cc622-101">New-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="cc622-101">New-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="cc622-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc622-102">SYNOPSIS</span></span>
<span data-ttu-id="cc622-103">Создает новую точку восстановления в пуле аналитики Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="cc622-103">Creates a new restore point in an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="cc622-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cc622-104">SYNTAX</span></span>

### <span data-ttu-id="cc622-105">CreateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cc622-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc622-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc622-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc622-107">CreateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc622-107">CreateByInputObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc622-108">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc622-108">CreateByResourceIdParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -ResourceId <String> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc622-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc622-109">DESCRIPTION</span></span>
<span data-ttu-id="cc622-110">Для создания новой точки восстановления, из SQL Azure Synapse Analytics, создается новый SQL **AzSynapseSqlPoolRestorePoint.**</span><span class="sxs-lookup"><span data-stu-id="cc622-110">The **New-AzSynapseSqlPoolRestorePoint** cmdlet creates a new restore point that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="cc622-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cc622-111">EXAMPLES</span></span>

### <span data-ttu-id="cc622-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cc622-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -RestorePointLabel ContosoRestorePoint
```

<span data-ttu-id="cc622-113">Эта команда создает точку восстановления для SQL contosoSqlPool в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cc622-113">This command creates a restore point for SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="cc622-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc622-114">PARAMETERS</span></span>

### <span data-ttu-id="cc622-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc622-115">-AsJob</span></span>
<span data-ttu-id="cc622-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cc622-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc622-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc622-117">-DefaultProfile</span></span>
<span data-ttu-id="cc622-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc622-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc622-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc622-119">-InputObject</span></span>
<span data-ttu-id="cc622-120">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="cc622-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cc622-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cc622-121">-Name</span></span>
<span data-ttu-id="cc622-122">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="cc622-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="cc622-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc622-123">-ResourceGroupName</span></span>
<span data-ttu-id="cc622-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc622-124">Resource group name.</span></span>

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

### <span data-ttu-id="cc622-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc622-125">-ResourceId</span></span>
<span data-ttu-id="cc622-126">Идентификатор ресурса в SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="cc622-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="cc622-127">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="cc622-127">-RestorePointLabel</span></span>
<span data-ttu-id="cc622-128">Метка, с которая связывается с точкой восстановления, может быть не уникальной.</span><span class="sxs-lookup"><span data-stu-id="cc622-128">The label we associate a restore point with, may not be unique.</span></span>

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

### <span data-ttu-id="cc622-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cc622-129">-WorkspaceName</span></span>
<span data-ttu-id="cc622-130">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="cc622-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cc622-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cc622-131">-WorkspaceObject</span></span>
<span data-ttu-id="cc622-132">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="cc622-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cc622-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc622-133">-Confirm</span></span>
<span data-ttu-id="cc622-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc622-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc622-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc622-135">-WhatIf</span></span>
<span data-ttu-id="cc622-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc622-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc622-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cc622-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc622-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc622-138">CommonParameters</span></span>
<span data-ttu-id="cc622-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc622-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc622-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc622-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc622-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc622-141">INPUTS</span></span>

### <span data-ttu-id="cc622-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cc622-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="cc622-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="cc622-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="cc622-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc622-144">OUTPUTS</span></span>

### <span data-ttu-id="cc622-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="cc622-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

## <span data-ttu-id="cc622-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cc622-146">NOTES</span></span>

## <span data-ttu-id="cc622-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc622-147">RELATED LINKS</span></span>
