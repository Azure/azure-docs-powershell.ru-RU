---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: fd83b97a7b95760d0ee2ce88295ed14c98a43ab3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216756"
---
# <span data-ttu-id="69299-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="69299-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="69299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69299-102">SYNOPSIS</span></span>
<span data-ttu-id="69299-103">Восстановление пула средств аналитики Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="69299-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="69299-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="69299-104">SYNTAX</span></span>

### <span data-ttu-id="69299-105">RestoreFromBackupIdByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="69299-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69299-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69299-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69299-107">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="69299-107">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69299-108">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69299-108">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69299-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69299-109">DESCRIPTION</span></span>
<span data-ttu-id="69299-110">С  SQL Azure Synapse Analytics можно восстановить пул SQL Azure Synapse Analytics из резервной копии или SQL.</span><span class="sxs-lookup"><span data-stu-id="69299-110">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="69299-111">Восстановленный SQL будет создан как новый SQL пул.</span><span class="sxs-lookup"><span data-stu-id="69299-111">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="69299-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="69299-112">EXAMPLES</span></span>

### <span data-ttu-id="69299-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="69299-113">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="69299-114">Эта команда создает пул Azure Synapse Analytics SQL путем восстановления из последней резервной копии SQL пула в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="69299-114">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="69299-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="69299-115">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="69299-116">Эта команда создает пул аналитики Azure Synapse Analytics SQL используя точку восстановления из любого SQL пула в этой подписке для восстановления или копирования из предыдущего состояния.</span><span class="sxs-lookup"><span data-stu-id="69299-116">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="69299-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="69299-117">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="69299-118">Эта команда создает пул Azure Synapse Analytics SQL путем восстановления из последней резервной копии всех пулов SQL в этой подписке с помощью ИД ресурсов.</span><span class="sxs-lookup"><span data-stu-id="69299-118">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="69299-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="69299-119">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="69299-120">Эта команда создает пул аналитики Azure Synapse Analytics SQL используя точку восстановления из любого пула SQL в этой подписке для восстановления или копирования из предыдущего состояния с помощью ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="69299-120">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="69299-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69299-121">PARAMETERS</span></span>

### <span data-ttu-id="69299-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69299-122">-AsJob</span></span>
<span data-ttu-id="69299-123">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="69299-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69299-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69299-124">-DefaultProfile</span></span>
<span data-ttu-id="69299-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69299-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69299-126">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="69299-126">-FromBackup</span></span>
<span data-ttu-id="69299-127">Восстановление из последней резервной копии всех SQL в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="69299-127">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69299-128">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="69299-128">-FromRestorePoint</span></span>
<span data-ttu-id="69299-129">Указывает на использование точки восстановления из SQL пула в этой подписке для восстановления или копирования из предыдущего состояния.</span><span class="sxs-lookup"><span data-stu-id="69299-129">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69299-130">-Name</span><span class="sxs-lookup"><span data-stu-id="69299-130">-Name</span></span>
<span data-ttu-id="69299-131">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="69299-131">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetSqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69299-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="69299-132">-PerformanceLevel</span></span>
<span data-ttu-id="69299-133">Уровень SQL службы и уровень производительности, которые нужно назначить SQL пулу.</span><span class="sxs-lookup"><span data-stu-id="69299-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="69299-134">Например, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="69299-134">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69299-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69299-135">-ResourceGroupName</span></span>
<span data-ttu-id="69299-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="69299-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69299-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69299-137">-ResourceId</span></span>
<span data-ttu-id="69299-138">ИД ресурса базы данных, который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="69299-138">The resource ID of the database to restore.</span></span>

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

### <span data-ttu-id="69299-139">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="69299-139">-RestorePoint</span></span>
<span data-ttu-id="69299-140">Время для восстановления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="69299-140">Snapshot time to restore.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases: PointInTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69299-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="69299-141">-WorkspaceName</span></span>
<span data-ttu-id="69299-142">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="69299-142">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69299-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="69299-143">-WorkspaceObject</span></span>
<span data-ttu-id="69299-144">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="69299-144">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69299-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69299-145">-Confirm</span></span>
<span data-ttu-id="69299-146">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="69299-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69299-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69299-147">-WhatIf</span></span>
<span data-ttu-id="69299-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69299-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69299-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="69299-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69299-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69299-150">CommonParameters</span></span>
<span data-ttu-id="69299-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69299-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69299-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69299-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69299-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69299-153">INPUTS</span></span>

### <span data-ttu-id="69299-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="69299-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="69299-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="69299-155">OUTPUTS</span></span>

### <span data-ttu-id="69299-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="69299-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="69299-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="69299-157">NOTES</span></span>

## <span data-ttu-id="69299-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69299-158">RELATED LINKS</span></span>
