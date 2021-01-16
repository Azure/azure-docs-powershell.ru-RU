---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 7fbc6cedf039cca33d0a30b39a21f9cdcb350b61
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507957"
---
# <span data-ttu-id="47c43-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="47c43-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="47c43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47c43-102">SYNOPSIS</span></span>
<span data-ttu-id="47c43-103">Восстановление пула средств аналитики Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="47c43-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="47c43-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="47c43-104">SYNTAX</span></span>

### <span data-ttu-id="47c43-105">RestoreFromBackupIdByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="47c43-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47c43-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47c43-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47c43-107">RestoreFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47c43-107">RestoreFromBackupNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47c43-108">RestoreFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47c43-108">RestoreFromBackupNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-BackupResourceGroupName <String>] -BackupWorkspaceName <String> -BackupSqlPoolName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47c43-109">RestoreFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47c43-109">RestoreFromBackupInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47c43-110">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47c43-110">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47c43-111">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47c43-111">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String> [-RestorePoint <DateTime>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47c43-112">RestoreFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47c43-112">RestoreFromRestorePointNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47c43-113">RestoreFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47c43-113">RestoreFromRestorePointNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47c43-114">RestoreFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47c43-114">RestoreFromRestorePointInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47c43-115">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47c43-115">DESCRIPTION</span></span>
<span data-ttu-id="47c43-116">С  SQL Analytics Azure Synapse Analytics можно восстановить пул SQL Azure Synapse Analytics из резервной копии или SQL.</span><span class="sxs-lookup"><span data-stu-id="47c43-116">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="47c43-117">Восстановленный SQL будет создан как новый SQL пул.</span><span class="sxs-lookup"><span data-stu-id="47c43-117">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="47c43-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="47c43-118">EXAMPLES</span></span>

### <span data-ttu-id="47c43-119">Пример 1</span><span class="sxs-lookup"><span data-stu-id="47c43-119">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="47c43-120">Эта команда создает пул Azure Synapse Analytics SQL путем восстановления из последней резервной копии SQL пула в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="47c43-120">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="47c43-121">Пример 2</span><span class="sxs-lookup"><span data-stu-id="47c43-121">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="47c43-122">Эта команда создает пул аналитики Azure Synapse Analytics SQL используя точку восстановления из любого SQL пула в этой подписке для восстановления или копирования из предыдущего состояния.</span><span class="sxs-lookup"><span data-stu-id="47c43-122">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="47c43-123">Пример 3</span><span class="sxs-lookup"><span data-stu-id="47c43-123">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="47c43-124">Эта команда создает пул Azure Synapse Analytics SQL путем восстановления из последней резервной копии всех пулов SQL в этой подписке с помощью ИД ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47c43-124">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="47c43-125">Пример 4</span><span class="sxs-lookup"><span data-stu-id="47c43-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="47c43-126">Эта команда создает пул аналитики Azure Synapse Analytics SQL используя точку восстановления из любого пула SQL в этой подписке для восстановления или копирования из предыдущего состояния с помощью ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="47c43-126">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="47c43-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47c43-127">PARAMETERS</span></span>

### <span data-ttu-id="47c43-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47c43-128">-AsJob</span></span>
<span data-ttu-id="47c43-129">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="47c43-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47c43-130">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47c43-130">-BackupResourceGroupName</span></span>
<span data-ttu-id="47c43-131">Имя группы ресурсов: bakcup SQL, из которого создается объект пула.</span><span class="sxs-lookup"><span data-stu-id="47c43-131">The resource group name of bakcup SQL pool object to create from.</span></span>

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

### <span data-ttu-id="47c43-132">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="47c43-132">-BackupResourceId</span></span>
<span data-ttu-id="47c43-133">Идентификатор ресурса резервной копии SQL объекта пула, из который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="47c43-133">The resource identifier of backup SQL pool object to restore from.</span></span>

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

### <span data-ttu-id="47c43-134">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="47c43-134">-BackupSqlPoolName</span></span>
<span data-ttu-id="47c43-135">Имя bakcup SQL пула, из которого создается объект.</span><span class="sxs-lookup"><span data-stu-id="47c43-135">The name of bakcup SQL pool object to create from.</span></span>

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

### <span data-ttu-id="47c43-136">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="47c43-136">-BackupSqlPoolObject</span></span>
<span data-ttu-id="47c43-137">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="47c43-137">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="47c43-138">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="47c43-138">-BackupWorkspaceName</span></span>
<span data-ttu-id="47c43-139">Имя рабочей области Synapse: bakcup SQL пула, из которого создается объект.</span><span class="sxs-lookup"><span data-stu-id="47c43-139">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

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

### <span data-ttu-id="47c43-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47c43-140">-DefaultProfile</span></span>
<span data-ttu-id="47c43-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47c43-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47c43-142">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="47c43-142">-FromBackup</span></span>
<span data-ttu-id="47c43-143">Восстановление из последней резервной копии всех SQL в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="47c43-143">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

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

### <span data-ttu-id="47c43-144">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="47c43-144">-FromRestorePoint</span></span>
<span data-ttu-id="47c43-145">Указывает на использование точки восстановления из SQL пула в этой подписке для восстановления или копирования из предыдущего состояния.</span><span class="sxs-lookup"><span data-stu-id="47c43-145">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

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

### <span data-ttu-id="47c43-146">-Name</span><span class="sxs-lookup"><span data-stu-id="47c43-146">-Name</span></span>
<span data-ttu-id="47c43-147">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="47c43-147">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="47c43-148">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="47c43-148">-PerformanceLevel</span></span>
<span data-ttu-id="47c43-149">Уровень SQL и уровень производительности службы, которые нужно назначить SQL пулу.</span><span class="sxs-lookup"><span data-stu-id="47c43-149">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="47c43-150">Например, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="47c43-150">For example, DW2000c.</span></span>

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

### <span data-ttu-id="47c43-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47c43-151">-ResourceGroupName</span></span>
<span data-ttu-id="47c43-152">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47c43-152">Resource group name.</span></span>

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

### <span data-ttu-id="47c43-153">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="47c43-153">-RestorePoint</span></span>
<span data-ttu-id="47c43-154">Время для восстановления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="47c43-154">Snapshot time to restore.</span></span>

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

### <span data-ttu-id="47c43-155">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47c43-155">-SourceResourceGroupName</span></span>
<span data-ttu-id="47c43-156">Имя группы ресурсов для объекта SQL пула.</span><span class="sxs-lookup"><span data-stu-id="47c43-156">The resource group name of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="47c43-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="47c43-157">-SourceResourceId</span></span>
<span data-ttu-id="47c43-158">Идентификатор ресурса объекта пула SQL из него.</span><span class="sxs-lookup"><span data-stu-id="47c43-158">The resource identifier of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="47c43-159">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="47c43-159">-SourceSqlPoolName</span></span>
<span data-ttu-id="47c43-160">Имя объекта пула SQL, из которого нужно создать объект.</span><span class="sxs-lookup"><span data-stu-id="47c43-160">The name of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="47c43-161">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="47c43-161">-SourceSqlPoolObject</span></span>
<span data-ttu-id="47c43-162">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="47c43-162">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="47c43-163">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="47c43-163">-SourceWorkspaceName</span></span>
<span data-ttu-id="47c43-164">Имя рабочей области Synapse для источника SQL пула, из которого создается объект.</span><span class="sxs-lookup"><span data-stu-id="47c43-164">The Synapse workspace name of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="47c43-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="47c43-165">-Tag</span></span>
<span data-ttu-id="47c43-166">Строковый строковый словарь тегов, связанный с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="47c43-166">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="47c43-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="47c43-167">-WorkspaceName</span></span>
<span data-ttu-id="47c43-168">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="47c43-168">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="47c43-169">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="47c43-169">-WorkspaceObject</span></span>
<span data-ttu-id="47c43-170">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="47c43-170">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="47c43-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47c43-171">-Confirm</span></span>
<span data-ttu-id="47c43-172">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="47c43-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47c43-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47c43-173">-WhatIf</span></span>
<span data-ttu-id="47c43-174">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47c43-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47c43-175">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="47c43-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47c43-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47c43-176">CommonParameters</span></span>
<span data-ttu-id="47c43-177">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47c43-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47c43-178">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47c43-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47c43-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47c43-179">INPUTS</span></span>

### <span data-ttu-id="47c43-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="47c43-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="47c43-181">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47c43-181">OUTPUTS</span></span>

### <span data-ttu-id="47c43-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="47c43-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="47c43-183">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="47c43-183">NOTES</span></span>

## <span data-ttu-id="47c43-184">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47c43-184">RELATED LINKS</span></span>
