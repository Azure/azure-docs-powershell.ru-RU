---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: c4bca877138f07c5bd3b0b5303ab09c39eb700a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235489"
---
# <span data-ttu-id="eb3c3-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eb3c3-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="eb3c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb3c3-102">SYNOPSIS</span></span>
<span data-ttu-id="eb3c3-103">Восстановление базы SQL.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-103">Restores a SQL database.</span></span>

## <span data-ttu-id="eb3c3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eb3c3-104">SYNTAX</span></span>

### <span data-ttu-id="eb3c3-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="eb3c3-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb3c3-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="eb3c3-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb3c3-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="eb3c3-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb3c3-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="eb3c3-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb3c3-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="eb3c3-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb3c3-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="eb3c3-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb3c3-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="eb3c3-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb3c3-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="eb3c3-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb3c3-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb3c3-113">DESCRIPTION</span></span>
<span data-ttu-id="eb3c3-114">Для восстановления базы данных **azSqlData** можно восстановить базу данных SQL из геоизбыточной резервной копии, резервной копии удаленной базы данных, долгосрочной резервной копии или точки времени в базе данных в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="eb3c3-115">Восстановленная база данных создается как новая.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="eb3c3-116">Вы можете создать эластичную SQL базы данных, *задав параметр "ЭластичнаяPoolName"* в существующем эластичном пуле.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="eb3c3-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eb3c3-117">EXAMPLES</span></span>

### <span data-ttu-id="eb3c3-118">Пример 1. Восстановление базы данных за один момент времени</span><span class="sxs-lookup"><span data-stu-id="eb3c3-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="eb3c3-119">Первая команда получает базу SQL Database01, а затем сохраняет ее в переменной $Database.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="eb3c3-120">Вторая команда восстанавливает базу данных в $Database заданную резервную копию за данный момент времени в базу данных с именем RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="eb3c3-121">Пример 2. Восстановление базы данных из точки времени в эластичный пул</span><span class="sxs-lookup"><span data-stu-id="eb3c3-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="eb3c3-122">Первая команда получает базу SQL Database01, а затем сохраняет ее в переменной $Database.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="eb3c3-123">Вторая команда восстанавливает базу данных в $Database из указанной заданной период резервной копии в базу SQL "ВосстановленнаяБазаданных" в эластичном пуле, который называется "эластичный пул01".</span><span class="sxs-lookup"><span data-stu-id="eb3c3-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="eb3c3-124">Пример 3. Восстановление удаленной базы данных</span><span class="sxs-lookup"><span data-stu-id="eb3c3-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="eb3c3-125">Первая команда получает удаленную резервную копию базы данных, которую вы хотите восстановить, с помощью [Get-AzSqlDeletedDatabaseBackup.](./Get-AzSqlDeletedDatabaseBackup.md)</span><span class="sxs-lookup"><span data-stu-id="eb3c3-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="eb3c3-126">Вторая команда запускает восстановление из удаленной резервной копии базы данных с помощью командлета [Restore-AzSqlDatabase.](./Restore-AzSqlDatabase.md)</span><span class="sxs-lookup"><span data-stu-id="eb3c3-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="eb3c3-127">Если параметр -PointInTime не указан, база данных будет восстановлена до времени удаления.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="eb3c3-128">Пример 4. Восстановление удаленной базы данных в эластичный пул</span><span class="sxs-lookup"><span data-stu-id="eb3c3-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="eb3c3-129">Первая команда получает удаленную резервную копию базы данных, которую вы хотите восстановить, с помощью [Get-AzSqlDeletedDatabaseBackup.](./Get-AzSqlDeletedDatabaseBackup.md)</span><span class="sxs-lookup"><span data-stu-id="eb3c3-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="eb3c3-130">Вторая команда запускает восстановление из удаленной резервной копии базы данных с помощью [restore-AzSqlDatabase.](./Restore-AzSqlDatabase.md)</span><span class="sxs-lookup"><span data-stu-id="eb3c3-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="eb3c3-131">Если параметр -PointInTime не указан, база данных будет восстановлена до времени удаления.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="eb3c3-132">Пример 5. Geo-Restore базы данных</span><span class="sxs-lookup"><span data-stu-id="eb3c3-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="eb3c3-133">Первая команда получает гео избыточное резервное копирование для базы данных Database01, а затем сохраняет ее в $GeoBackup переменной.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="eb3c3-134">Вторая команда восстанавливает резервную копию в $GeoBackup в SQL с именем RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="eb3c3-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb3c3-135">PARAMETERS</span></span>

### <span data-ttu-id="eb3c3-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb3c3-136">-AsJob</span></span>
<span data-ttu-id="eb3c3-137">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="eb3c3-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb3c3-138">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="eb3c3-138">-BackupStorageRedundancy</span></span>
<span data-ttu-id="eb3c3-139">Избыточность резервного копирования хранилища, используемого для хранения резервных копий SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-139">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="eb3c3-140">Доступны такие варианты: Local (Локальный), Zone (Зона) и Geo (География).</span><span class="sxs-lookup"><span data-stu-id="eb3c3-140">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c3-141">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="eb3c3-141">-ComputeGeneration</span></span>
<span data-ttu-id="eb3c3-142">The compute generation to assign to the restored database</span><span class="sxs-lookup"><span data-stu-id="eb3c3-142">The compute generation to assign to the restored database</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c3-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb3c3-143">-DefaultProfile</span></span>
<span data-ttu-id="eb3c3-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eb3c3-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb3c3-145">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="eb3c3-145">-DeletionDate</span></span>
<span data-ttu-id="eb3c3-146">Дата удаления в качестве объекта **даты и** времени.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-146">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="eb3c3-147">Чтобы получить объект **даты и времени,** воспользуйтесь Get-Date..</span><span class="sxs-lookup"><span data-stu-id="eb3c3-147">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c3-148">-Edition</span><span class="sxs-lookup"><span data-stu-id="eb3c3-148">-Edition</span></span>
<span data-ttu-id="eb3c3-149">Выпуск базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-149">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="eb3c3-150">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="eb3c3-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb3c3-151">Нет</span><span class="sxs-lookup"><span data-stu-id="eb3c3-151">None</span></span>
- <span data-ttu-id="eb3c3-152">Базовая</span><span class="sxs-lookup"><span data-stu-id="eb3c3-152">Basic</span></span>
- <span data-ttu-id="eb3c3-153">Стандартный</span><span class="sxs-lookup"><span data-stu-id="eb3c3-153">Standard</span></span>
- <span data-ttu-id="eb3c3-154">Premium</span><span class="sxs-lookup"><span data-stu-id="eb3c3-154">Premium</span></span>
- <span data-ttu-id="eb3c3-155">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="eb3c3-155">DataWarehouse</span></span>
- <span data-ttu-id="eb3c3-156">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="eb3c3-156">Free</span></span>
- <span data-ttu-id="eb3c3-157">Растяжение</span><span class="sxs-lookup"><span data-stu-id="eb3c3-157">Stretch</span></span>
- <span data-ttu-id="eb3c3-158">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="eb3c3-158">GeneralPurpose</span></span>
- <span data-ttu-id="eb3c3-159">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="eb3c3-159">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c3-160">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="eb3c3-160">-ElasticPoolName</span></span>
<span data-ttu-id="eb3c3-161">Определяет имя эластичного пула, в который нужно поместить SQL базу данных.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-161">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c3-162">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="eb3c3-162">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="eb3c3-163">Указывает на то, что этот cmdlet восстанавливает базу данных из резервной копии удаленной SQL.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-163">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="eb3c3-164">Вы можете использовать Get-AzSqlDeletedDatabaseBackup для получения резервной копии удаленной SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-164">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c3-165">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="eb3c3-165">-FromGeoBackup</span></span>
<span data-ttu-id="eb3c3-166">Указывает на то, что этот SQL восстанавливает базу данных из гео избыточных резервных копий.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-166">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="eb3c3-167">Для получения гео-избыточной резервной копии можно использовать Get-AzSqlDatabaseGeoBackup- и резервную копию.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-167">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup, FromGeoBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c3-168">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="eb3c3-168">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="eb3c3-169">Указывает на то, что этот SQL восстанавливает базу данных из долгосрочной резервной копии.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-169">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c3-170">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="eb3c3-170">-FromPointInTimeBackup</span></span>
<span data-ttu-id="eb3c3-171">Указывает на то, что этот SQL восстанавливает базу данных из заданной моментарной резервной копии.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-171">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c3-172">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="eb3c3-172">-LicenseType</span></span>
<span data-ttu-id="eb3c3-173">Тип лицензии для базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-173">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="eb3c3-174">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="eb3c3-174">-PointInTime</span></span>
<span data-ttu-id="eb3c3-175">Указывает время в качестве объекта **даты** и времени, до SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-175">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="eb3c3-176">Чтобы получить объект **даты и времени,** используйте для этого cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="eb3c3-176">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="eb3c3-177">Используйте этот параметр вместе с *параметром FromPointInTimeBackup.*</span><span class="sxs-lookup"><span data-stu-id="eb3c3-177">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c3-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb3c3-178">-ResourceGroupName</span></span>
<span data-ttu-id="eb3c3-179">Задает имя группы ресурсов, которой этот SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-179">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c3-180">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb3c3-180">-ResourceId</span></span>
<span data-ttu-id="eb3c3-181">Определяет ИД ресурса, который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-181">Specifies the ID of the resource to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c3-182">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eb3c3-182">-ServerName</span></span>
<span data-ttu-id="eb3c3-183">Указывает имя сервера базы SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-183">Specifies the name of the SQL database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c3-184">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="eb3c3-184">-ServiceObjectiveName</span></span>
<span data-ttu-id="eb3c3-185">Указывает имя цели обслуживания.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-185">Specifies the name of the service objective.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c3-186">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb3c3-186">-TargetDatabaseName</span></span>
<span data-ttu-id="eb3c3-187">Имя базы данных, которая будет восстановлена.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-187">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="eb3c3-188">-VCore</span><span class="sxs-lookup"><span data-stu-id="eb3c3-188">-VCore</span></span>
<span data-ttu-id="eb3c3-189">Номера на vcore восстановленной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-189">The Vcore numbers of the restored Azure Sql Database.</span></span>

```yaml
Type: System.Int32
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c3-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb3c3-190">-Confirm</span></span>
<span data-ttu-id="eb3c3-191">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb3c3-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb3c3-192">-WhatIf</span></span>
<span data-ttu-id="eb3c3-193">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-193">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb3c3-194">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb3c3-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb3c3-195">CommonParameters</span></span>
<span data-ttu-id="eb3c3-196">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb3c3-197">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb3c3-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb3c3-198">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb3c3-198">INPUTS</span></span>

### <span data-ttu-id="eb3c3-199">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="eb3c3-199">System.DateTime</span></span>

### <span data-ttu-id="eb3c3-200">System.String</span><span class="sxs-lookup"><span data-stu-id="eb3c3-200">System.String</span></span>

## <span data-ttu-id="eb3c3-201">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eb3c3-201">OUTPUTS</span></span>

### <span data-ttu-id="eb3c3-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="eb3c3-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="eb3c3-203">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eb3c3-203">NOTES</span></span>

## <span data-ttu-id="eb3c3-204">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb3c3-204">RELATED LINKS</span></span>

[<span data-ttu-id="eb3c3-205">Восстановление базы данных Azure SQL из-за простоя</span><span class="sxs-lookup"><span data-stu-id="eb3c3-205">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="eb3c3-206">Восстановление базы данных Azure SQL после ошибки пользователя</span><span class="sxs-lookup"><span data-stu-id="eb3c3-206">Recover an Azure SQL Database from a user error</span></span>](http://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="eb3c3-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eb3c3-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="eb3c3-208">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="eb3c3-208">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="eb3c3-209">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="eb3c3-209">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="eb3c3-210">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="eb3c3-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

