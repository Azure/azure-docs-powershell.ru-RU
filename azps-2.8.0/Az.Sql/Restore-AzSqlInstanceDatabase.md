---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: d513c186f621329510582c9cd69a64461f9e068f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906481"
---
# <span data-ttu-id="e2faa-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e2faa-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="e2faa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2faa-102">SYNOPSIS</span></span>
<span data-ttu-id="e2faa-103">Восстанавливает базу данных экземпляра, управляемой службой Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e2faa-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="e2faa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2faa-104">SYNTAX</span></span>

### <span data-ttu-id="e2faa-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2faa-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2faa-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e2faa-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2faa-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="e2faa-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2faa-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="e2faa-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2faa-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e2faa-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2faa-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="e2faa-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2faa-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e2faa-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2faa-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e2faa-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2faa-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="e2faa-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2faa-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2faa-114">DESCRIPTION</span></span>
<span data-ttu-id="e2faa-115">Командлет **RESTORE-AzSqlInstanceDatabase** восстанавливает базу данных экземпляра из резервной копии с геоизбыточной учетной записью или на момент времени в действующей базе данных.</span><span class="sxs-lookup"><span data-stu-id="e2faa-115">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup or a point in time in a live database.</span></span>
<span data-ttu-id="e2faa-116">Восстановленная база данных создается как новая база данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e2faa-116">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="e2faa-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2faa-117">EXAMPLES</span></span>

### <span data-ttu-id="e2faa-118">Пример 1: восстановление базы данных экземпляра на момент времени</span><span class="sxs-lookup"><span data-stu-id="e2faa-118">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="e2faa-119">Команда восстанавливает базу данных экземпляра Database01 из указанного резервного копирования на момент времени в базу данных экземпляра с именем Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="e2faa-119">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="e2faa-120">Пример 2: восстановление базы данных экземпляра с момента времени до другого экземпляра в другой группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="e2faa-120">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="e2faa-121">Команда восстанавливает базу данных экземпляра Database01 на экземпляре managedInstance1 в группе ресурсов ResourceGroup01 с указанной на момент времени резервной копии в базу данных экземпляра с именем Database01_restored на экземпляре managedInstance2 в группе ресурсов ResourceGroup02.</span><span class="sxs-lookup"><span data-stu-id="e2faa-121">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="e2faa-122">Пример 3: Geo-Restore базы данных экземпляра</span><span class="sxs-lookup"><span data-stu-id="e2faa-122">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="e2faa-123">Первая команда получает геоизбыточное резервное копирование базы данных с именем Database01 и сохраняет его в переменной $GeoBackup.</span><span class="sxs-lookup"><span data-stu-id="e2faa-123">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="e2faa-124">Вторая команда восстанавливает резервную копию в $GeoBackup на базу данных экземпляра с именем Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="e2faa-124">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

## <span data-ttu-id="e2faa-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2faa-125">PARAMETERS</span></span>

### <span data-ttu-id="e2faa-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2faa-126">-AsJob</span></span>
<span data-ttu-id="e2faa-127">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e2faa-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2faa-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2faa-128">-DefaultProfile</span></span>
<span data-ttu-id="e2faa-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e2faa-129">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="e2faa-130">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="e2faa-130">-FromGeoBackup</span></span>
<span data-ttu-id="e2faa-131">Восстановите из географической резервной копии.</span><span class="sxs-lookup"><span data-stu-id="e2faa-131">Restore from a geo backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2faa-132">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="e2faa-132">-FromPointInTimeBackup</span></span>
<span data-ttu-id="e2faa-133">Восстановление из резервной копии на момент времени.</span><span class="sxs-lookup"><span data-stu-id="e2faa-133">Restore from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2faa-134">-GeoBackupObject</span><span class="sxs-lookup"><span data-stu-id="e2faa-134">-GeoBackupObject</span></span>
<span data-ttu-id="e2faa-135">Восстанавливаемый объект базы данных экземпляра для восстановления</span><span class="sxs-lookup"><span data-stu-id="e2faa-135">The recoverable instance database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter
Aliases: RecoverableInstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2faa-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2faa-136">-InputObject</span></span>
<span data-ttu-id="e2faa-137">Объект базы данных экземпляра для восстановления</span><span class="sxs-lookup"><span data-stu-id="e2faa-137">The Instance Database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2faa-138">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e2faa-138">-InstanceName</span></span>
<span data-ttu-id="e2faa-139">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e2faa-139">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2faa-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2faa-140">-Name</span></span>
<span data-ttu-id="e2faa-141">Имя базы данных экземпляра для восстановления.</span><span class="sxs-lookup"><span data-stu-id="e2faa-141">The instance database name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2faa-142">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="e2faa-142">-PointInTime</span></span>
<span data-ttu-id="e2faa-143">Момент времени, в который нужно восстановить базу данных.</span><span class="sxs-lookup"><span data-stu-id="e2faa-143">The point in time to restore the database to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2faa-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2faa-144">-ResourceGroupName</span></span>
<span data-ttu-id="e2faa-145">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2faa-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2faa-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2faa-146">-ResourceId</span></span>
<span data-ttu-id="e2faa-147">Идентификатор ресурса экземпляра базы данных, который нужно восстановить</span><span class="sxs-lookup"><span data-stu-id="e2faa-147">The resource id of Instance Database object to restore</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2faa-148">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e2faa-148">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="e2faa-149">Имя целевой базы данных экземпляра для восстановления.</span><span class="sxs-lookup"><span data-stu-id="e2faa-149">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="e2faa-150">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="e2faa-150">-TargetInstanceName</span></span>
<span data-ttu-id="e2faa-151">Имя целевого экземпляра, в который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="e2faa-151">The name of the target instance to restore to.</span></span>
<span data-ttu-id="e2faa-152">Если он не указан, целевой экземпляр совпадает с исходным экземпляром.</span><span class="sxs-lookup"><span data-stu-id="e2faa-152">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2faa-153">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2faa-153">-TargetResourceGroupName</span></span>
<span data-ttu-id="e2faa-154">Имя целевой группы ресурсов, в которую будет восстановлено значение.</span><span class="sxs-lookup"><span data-stu-id="e2faa-154">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="e2faa-155">Если этот элемент не указан, Целевая группа ресурсов совпадает с исходной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2faa-155">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2faa-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2faa-156">-Confirm</span></span>
<span data-ttu-id="e2faa-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2faa-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2faa-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2faa-158">-WhatIf</span></span>
<span data-ttu-id="e2faa-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2faa-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2faa-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2faa-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2faa-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2faa-161">CommonParameters</span></span>
<span data-ttu-id="e2faa-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2faa-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2faa-163">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2faa-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2faa-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2faa-164">INPUTS</span></span>

### <span data-ttu-id="e2faa-165">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e2faa-165">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="e2faa-166">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e2faa-166">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="e2faa-167">System. String</span><span class="sxs-lookup"><span data-stu-id="e2faa-167">System.String</span></span>

## <span data-ttu-id="e2faa-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2faa-168">OUTPUTS</span></span>

### <span data-ttu-id="e2faa-169">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e2faa-169">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e2faa-170">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2faa-170">NOTES</span></span>

## <span data-ttu-id="e2faa-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2faa-171">RELATED LINKS</span></span>
