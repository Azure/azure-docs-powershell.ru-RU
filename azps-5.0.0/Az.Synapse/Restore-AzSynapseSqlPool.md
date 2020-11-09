---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 2dae942470dba8a36258ffb8c813e08c664f2e26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316865"
---
# <span data-ttu-id="a63fc-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a63fc-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="a63fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a63fc-102">SYNOPSIS</span></span>
<span data-ttu-id="a63fc-103">Восстановление пула SQL Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="a63fc-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a63fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a63fc-104">SYNTAX</span></span>

### <span data-ttu-id="a63fc-105">RestoreFromBackupIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a63fc-105">RestoreFromBackupIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a63fc-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a63fc-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a63fc-107">RestoreFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a63fc-107">RestoreFromBackupNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a63fc-108">RestoreFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a63fc-108">RestoreFromBackupNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-BackupResourceGroupName <String>] -BackupWorkspaceName <String> -BackupSqlPoolName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a63fc-109">RestoreFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a63fc-109">RestoreFromBackupInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a63fc-110">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a63fc-110">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a63fc-111">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a63fc-111">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String> [-RestorePoint <DateTime>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a63fc-112">RestoreFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a63fc-112">RestoreFromRestorePointNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a63fc-113">RestoreFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a63fc-113">RestoreFromRestorePointNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a63fc-114">RestoreFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a63fc-114">RestoreFromRestorePointInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a63fc-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a63fc-115">DESCRIPTION</span></span>
<span data-ttu-id="a63fc-116">Командлет **RESTORE-AzSynapseSqlPool** восстанавливает пул SQL Azure Synapse Analytics из резервной копии или точки восстановления любого пула SQL.</span><span class="sxs-lookup"><span data-stu-id="a63fc-116">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="a63fc-117">Восстановленный пул SQL создается в качестве нового пула SQL.</span><span class="sxs-lookup"><span data-stu-id="a63fc-117">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="a63fc-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a63fc-118">EXAMPLES</span></span>

### <span data-ttu-id="a63fc-119">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a63fc-119">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="a63fc-120">Эта команда создает пул SQL Azure Synapse Analytics, восстанавливая из последней резервной копии любого пула SQL в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="a63fc-120">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="a63fc-121">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a63fc-121">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="a63fc-122">Эта команда создает пул SQL Azure Synapse Analytics, используя точку восстановления из любого пула SQL в этой подписке для восстановления или копирования из предыдущего состояния.</span><span class="sxs-lookup"><span data-stu-id="a63fc-122">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="a63fc-123">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a63fc-123">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="a63fc-124">Эта команда создает пул SQL Azure Synapse Analytics, восстановив данные из последней резервной копии любого пула SQL в этой подписке с ИДЕНТИФИКАТОРом ресурса.</span><span class="sxs-lookup"><span data-stu-id="a63fc-124">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="a63fc-125">Пример 4</span><span class="sxs-lookup"><span data-stu-id="a63fc-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="a63fc-126">Эта команда создает пул SQL Azure Synapse Analytics, используя точку восстановления из любого пула SQL в этой подписке, чтобы восстановить или скопировать предыдущее состояние с ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="a63fc-126">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="a63fc-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a63fc-127">PARAMETERS</span></span>

### <span data-ttu-id="a63fc-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a63fc-128">-AsJob</span></span>
<span data-ttu-id="a63fc-129">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a63fc-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a63fc-130">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a63fc-130">-BackupResourceGroupName</span></span>
<span data-ttu-id="a63fc-131">Имя группы ресурсов, из которой bakcup объект пула SQL для создания.</span><span class="sxs-lookup"><span data-stu-id="a63fc-131">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63fc-132">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="a63fc-132">-BackupResourceId</span></span>
<span data-ttu-id="a63fc-133">Идентификатор ресурса резервного объекта пула SQL, из которого нужно выполнить восстановление.</span><span class="sxs-lookup"><span data-stu-id="a63fc-133">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63fc-134">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="a63fc-134">-BackupSqlPoolName</span></span>
<span data-ttu-id="a63fc-135">Имя объекта пула SQL bakcup, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="a63fc-135">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63fc-136">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="a63fc-136">-BackupSqlPoolObject</span></span>
<span data-ttu-id="a63fc-137">Входной объект пула SQL, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="a63fc-137">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63fc-138">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a63fc-138">-BackupWorkspaceName</span></span>
<span data-ttu-id="a63fc-139">Имя рабочей области Synapse объекта пула bakcup SQL для создания.</span><span class="sxs-lookup"><span data-stu-id="a63fc-139">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63fc-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a63fc-140">-DefaultProfile</span></span>
<span data-ttu-id="a63fc-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a63fc-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a63fc-142">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="a63fc-142">-FromBackup</span></span>
<span data-ttu-id="a63fc-143">Указывает, что нужно восстановить из последней резервной копии любого пула SQL в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="a63fc-143">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63fc-144">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="a63fc-144">-FromRestorePoint</span></span>
<span data-ttu-id="a63fc-145">Указывает, что вы можете использовать точку восстановления из любого пула SQL в этой подписке, чтобы восстановить или скопировать предыдущее состояние.</span><span class="sxs-lookup"><span data-stu-id="a63fc-145">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63fc-146">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a63fc-146">-Name</span></span>
<span data-ttu-id="a63fc-147">Имя пула SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="a63fc-147">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="a63fc-148">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="a63fc-148">-PerformanceLevel</span></span>
<span data-ttu-id="a63fc-149">Уровень производительности служб SQL, который нужно назначить пулу SQL.</span><span class="sxs-lookup"><span data-stu-id="a63fc-149">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="a63fc-150">Например, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="a63fc-150">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63fc-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a63fc-151">-ResourceGroupName</span></span>
<span data-ttu-id="a63fc-152">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a63fc-152">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63fc-153">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="a63fc-153">-RestorePoint</span></span>
<span data-ttu-id="a63fc-154">Время восстановления снимка.</span><span class="sxs-lookup"><span data-stu-id="a63fc-154">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63fc-155">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a63fc-155">-SourceResourceGroupName</span></span>
<span data-ttu-id="a63fc-156">Имя группы ресурсов исходного объекта пула SQL для создания.</span><span class="sxs-lookup"><span data-stu-id="a63fc-156">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63fc-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="a63fc-157">-SourceResourceId</span></span>
<span data-ttu-id="a63fc-158">Идентификатор ресурса исходного объекта пула SQL для создания.</span><span class="sxs-lookup"><span data-stu-id="a63fc-158">The resource identifier of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="a63fc-159">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="a63fc-159">-SourceSqlPoolName</span></span>
<span data-ttu-id="a63fc-160">Имя исходного объекта пула SQL для создания.</span><span class="sxs-lookup"><span data-stu-id="a63fc-160">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63fc-161">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="a63fc-161">-SourceSqlPoolObject</span></span>
<span data-ttu-id="a63fc-162">Входной объект пула SQL, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="a63fc-162">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63fc-163">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a63fc-163">-SourceWorkspaceName</span></span>
<span data-ttu-id="a63fc-164">Имя рабочей области Synapse исходного объекта пула SQL для создания.</span><span class="sxs-lookup"><span data-stu-id="a63fc-164">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63fc-165">-Тег</span><span class="sxs-lookup"><span data-stu-id="a63fc-165">-Tag</span></span>
<span data-ttu-id="a63fc-166">Строковый словарь тегов, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="a63fc-166">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="a63fc-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a63fc-167">-WorkspaceName</span></span>
<span data-ttu-id="a63fc-168">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a63fc-168">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a63fc-169">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a63fc-169">-WorkspaceObject</span></span>
<span data-ttu-id="a63fc-170">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="a63fc-170">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a63fc-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a63fc-171">-Confirm</span></span>
<span data-ttu-id="a63fc-172">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a63fc-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a63fc-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a63fc-173">-WhatIf</span></span>
<span data-ttu-id="a63fc-174">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a63fc-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a63fc-175">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a63fc-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a63fc-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a63fc-176">CommonParameters</span></span>
<span data-ttu-id="a63fc-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a63fc-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a63fc-178">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a63fc-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a63fc-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a63fc-179">INPUTS</span></span>

### <span data-ttu-id="a63fc-180">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a63fc-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a63fc-181">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a63fc-181">OUTPUTS</span></span>

### <span data-ttu-id="a63fc-182">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a63fc-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a63fc-183">Пуск</span><span class="sxs-lookup"><span data-stu-id="a63fc-183">NOTES</span></span>

## <span data-ttu-id="a63fc-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a63fc-184">RELATED LINKS</span></span>
