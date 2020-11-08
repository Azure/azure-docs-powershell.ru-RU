---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 694b9811bf11454e232f1514b59b1b537e4720a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244674"
---
# <span data-ttu-id="6fbdd-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6fbdd-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="6fbdd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6fbdd-102">SYNOPSIS</span></span>
<span data-ttu-id="6fbdd-103">Создание пула SQL Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6fbdd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6fbdd-104">SYNTAX</span></span>

### <span data-ttu-id="6fbdd-105">CreateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6fbdd-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fbdd-106">CreateFromBackupIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbdd-106">CreateFromBackupIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fbdd-107">CreateFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbdd-107">CreateFromBackupIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fbdd-108">CreateFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbdd-108">CreateFromBackupNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fbdd-109">CreateFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbdd-109">CreateFromBackupNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fbdd-110">CreateFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbdd-110">CreateFromBackupInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fbdd-111">CreateFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbdd-111">CreateFromRestorePointIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fbdd-112">CreateFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbdd-112">CreateFromRestorePointIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fbdd-113">CreateFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbdd-113">CreateFromRestorePointNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fbdd-114">CreateFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbdd-114">CreateFromRestorePointNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fbdd-115">CreateFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbdd-115">CreateFromRestorePointInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fbdd-116">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbdd-116">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fbdd-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fbdd-117">DESCRIPTION</span></span>
<span data-ttu-id="6fbdd-118">Командлет **New-AzSynapseSqlPool** создает пул SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-118">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6fbdd-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6fbdd-119">EXAMPLES</span></span>

### <span data-ttu-id="6fbdd-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6fbdd-120">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="6fbdd-121">Эта команда создает пул SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-121">This command creates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="6fbdd-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6fbdd-122">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="6fbdd-123">Эта команда создает пул SQL Azure Synapse Analytics, восстанавливая из последней резервной копии любого пула SQL в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-123">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="6fbdd-124">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6fbdd-124">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="6fbdd-125">Эта команда создает пул SQL Azure Synapse Analytics, используя точку восстановления из любого пула SQL в этой подписке для восстановления или копирования из предыдущего состояния.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-125">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="6fbdd-126">Пример 4</span><span class="sxs-lookup"><span data-stu-id="6fbdd-126">Example 4</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="6fbdd-127">Эта команда создает пул SQL Azure Synapse Analytics, восстановив данные из последней резервной копии любого пула SQL в этой подписке с ИДЕНТИФИКАТОРом ресурса.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-127">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="6fbdd-128">Пример 5</span><span class="sxs-lookup"><span data-stu-id="6fbdd-128">Example 5</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws |  New-AzSynapseSqlPool -FromRestorePoint -Name dwsql0554 -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/mandywtest/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="6fbdd-129">Эта команда создает пул SQL Azure Synapse Analytics, используя точку восстановления из любого пула SQL в этой подписке, чтобы восстановить или скопировать предыдущее состояние с ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-129">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="6fbdd-130">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6fbdd-130">PARAMETERS</span></span>

### <span data-ttu-id="6fbdd-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fbdd-131">-AsJob</span></span>
<span data-ttu-id="6fbdd-132">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6fbdd-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6fbdd-133">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fbdd-133">-BackupResourceGroupName</span></span>
<span data-ttu-id="6fbdd-134">Имя группы ресурсов, из которой bakcup объект пула SQL для создания.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-134">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-135">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="6fbdd-135">-BackupResourceId</span></span>
<span data-ttu-id="6fbdd-136">Идентификатор ресурса резервного объекта пула SQL, из которого нужно выполнить восстановление.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-136">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-137">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="6fbdd-137">-BackupSqlPoolName</span></span>
<span data-ttu-id="6fbdd-138">Имя объекта пула SQL bakcup, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-138">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-139">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="6fbdd-139">-BackupSqlPoolObject</span></span>
<span data-ttu-id="6fbdd-140">Входной объект пула SQL, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-140">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-141">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6fbdd-141">-BackupWorkspaceName</span></span>
<span data-ttu-id="6fbdd-142">Имя рабочей области Synapse объекта пула bakcup SQL для создания.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-142">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-143">-Параметры сортировки</span><span class="sxs-lookup"><span data-stu-id="6fbdd-143">-Collation</span></span>
<span data-ttu-id="6fbdd-144">Параметры сортировки определяют правила, которые сортируют и сравнивают данные, и их нельзя изменить после создания пула SQL.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-144">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="6fbdd-145">Параметры сортировки по умолчанию SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-145">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fbdd-146">-DefaultProfile</span></span>
<span data-ttu-id="6fbdd-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fbdd-148">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="6fbdd-148">-FromBackup</span></span>
<span data-ttu-id="6fbdd-149">Указывает, что нужно восстановить из последней резервной копии любого пула SQL в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-149">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-150">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="6fbdd-150">-FromRestorePoint</span></span>
<span data-ttu-id="6fbdd-151">Указывает, что вы можете использовать точку восстановления из любого пула SQL в этой подписке, чтобы восстановить или скопировать предыдущее состояние.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-151">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-152">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6fbdd-152">-Name</span></span>
<span data-ttu-id="6fbdd-153">Имя пула SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-153">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="6fbdd-154">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="6fbdd-154">-PerformanceLevel</span></span>
<span data-ttu-id="6fbdd-155">Уровень производительности служб SQL, который нужно назначить пулу SQL.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-155">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="6fbdd-156">Например, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-156">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fbdd-157">-ResourceGroupName</span></span>
<span data-ttu-id="6fbdd-158">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-159">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="6fbdd-159">-RestorePoint</span></span>
<span data-ttu-id="6fbdd-160">Время восстановления снимка.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-160">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-161">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fbdd-161">-SourceResourceGroupName</span></span>
<span data-ttu-id="6fbdd-162">Имя группы ресурсов исходного объекта пула SQL для создания.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-162">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-163">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="6fbdd-163">-SourceResourceId</span></span>
<span data-ttu-id="6fbdd-164">Идентификатор ресурса исходного объекта пула SQL для создания.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-164">The resource identifier of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-165">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="6fbdd-165">-SourceSqlPoolName</span></span>
<span data-ttu-id="6fbdd-166">Имя исходного объекта пула SQL для создания.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-166">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-167">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="6fbdd-167">-SourceSqlPoolObject</span></span>
<span data-ttu-id="6fbdd-168">Входной объект пула SQL, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-168">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-169">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6fbdd-169">-SourceWorkspaceName</span></span>
<span data-ttu-id="6fbdd-170">Имя рабочей области Synapse исходного объекта пула SQL для создания.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-170">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-171">-Тег</span><span class="sxs-lookup"><span data-stu-id="6fbdd-171">-Tag</span></span>
<span data-ttu-id="6fbdd-172">Строковый словарь тегов, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-172">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="6fbdd-173">-Version</span><span class="sxs-lookup"><span data-stu-id="6fbdd-173">-Version</span></span>
<span data-ttu-id="6fbdd-174">Версия пула Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-174">Version of Synapse SQL pool.</span></span> <span data-ttu-id="6fbdd-175">Например, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-175">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="6fbdd-176">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6fbdd-176">-WorkspaceName</span></span>
<span data-ttu-id="6fbdd-177">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-177">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-178">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6fbdd-178">-WorkspaceObject</span></span>
<span data-ttu-id="6fbdd-179">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-179">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fbdd-180">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6fbdd-180">-Confirm</span></span>
<span data-ttu-id="6fbdd-181">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fbdd-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fbdd-182">-WhatIf</span></span>
<span data-ttu-id="6fbdd-183">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fbdd-184">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fbdd-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fbdd-185">CommonParameters</span></span>
<span data-ttu-id="6fbdd-186">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fbdd-187">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fbdd-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fbdd-188">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6fbdd-188">INPUTS</span></span>

### <span data-ttu-id="6fbdd-189">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6fbdd-189">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6fbdd-190">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fbdd-190">OUTPUTS</span></span>

### <span data-ttu-id="6fbdd-191">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6fbdd-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="6fbdd-192">Пуск</span><span class="sxs-lookup"><span data-stu-id="6fbdd-192">NOTES</span></span>

## <span data-ttu-id="6fbdd-193">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6fbdd-193">RELATED LINKS</span></span>
