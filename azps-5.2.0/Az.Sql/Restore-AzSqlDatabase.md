---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: c4bca877138f07c5bd3b0b5303ab09c39eb700a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327154"
---
# <span data-ttu-id="411a9-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="411a9-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="411a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="411a9-102">SYNOPSIS</span></span>
<span data-ttu-id="411a9-103">Восстановление базы SQL.</span><span class="sxs-lookup"><span data-stu-id="411a9-103">Restores a SQL database.</span></span>

## <span data-ttu-id="411a9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="411a9-104">SYNTAX</span></span>

### <span data-ttu-id="411a9-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="411a9-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="411a9-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="411a9-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="411a9-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="411a9-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="411a9-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="411a9-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="411a9-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="411a9-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="411a9-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="411a9-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="411a9-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="411a9-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="411a9-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="411a9-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="411a9-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="411a9-113">DESCRIPTION</span></span>
<span data-ttu-id="411a9-114">Для восстановления базы данных **AzSqlData** можно восстановить базу данных SQL из геоизбыточной резервной копии, резервной копии удаленной базы данных, долгосрочной резервной копии или точки времени в базе данных в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="411a9-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="411a9-115">Восстановленная база данных создается как новая.</span><span class="sxs-lookup"><span data-stu-id="411a9-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="411a9-116">Вы можете создать эластичную SQL базы данных, *задав параметр "ЭластичнаяPoolName"* в существующем эластичном пуле.</span><span class="sxs-lookup"><span data-stu-id="411a9-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="411a9-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="411a9-117">EXAMPLES</span></span>

### <span data-ttu-id="411a9-118">Пример 1. Восстановление базы данных за один момент времени</span><span class="sxs-lookup"><span data-stu-id="411a9-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="411a9-119">Первая команда получает базу SQL Database01, а затем сохраняет ее в переменной $Database.</span><span class="sxs-lookup"><span data-stu-id="411a9-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="411a9-120">Вторая команда восстанавливает базу данных в $Database заданную резервную копию за данный момент времени в базу данных с именем RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="411a9-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="411a9-121">Пример 2. Восстановление базы данных из точки времени в эластичный пул</span><span class="sxs-lookup"><span data-stu-id="411a9-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="411a9-122">Первая команда получает базу SQL Database01, а затем сохраняет ее в переменной $Database.</span><span class="sxs-lookup"><span data-stu-id="411a9-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="411a9-123">Вторая команда восстанавливает базу данных в $Database из указанной заданной период резервной копии в базу SQL "ВосстановленнаяБазаданных" в эластичном пуле, который называется "эластичный пул01".</span><span class="sxs-lookup"><span data-stu-id="411a9-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="411a9-124">Пример 3. Восстановление удаленной базы данных</span><span class="sxs-lookup"><span data-stu-id="411a9-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="411a9-125">Первая команда получает удаленную резервную копию базы данных, которую вы хотите восстановить, с помощью [Get-AzSqlDeletedDatabaseBackup.](./Get-AzSqlDeletedDatabaseBackup.md)</span><span class="sxs-lookup"><span data-stu-id="411a9-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="411a9-126">Вторая команда запускает восстановление из удаленной резервной копии базы данных с помощью командлета [Restore-AzSqlDatabase.](./Restore-AzSqlDatabase.md)</span><span class="sxs-lookup"><span data-stu-id="411a9-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="411a9-127">Если параметр -PointInTime не указан, база данных будет восстановлена до времени удаления.</span><span class="sxs-lookup"><span data-stu-id="411a9-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="411a9-128">Пример 4. Восстановление удаленной базы данных в эластичный пул</span><span class="sxs-lookup"><span data-stu-id="411a9-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="411a9-129">Первая команда получает удаленную резервную копию базы данных, которую вы хотите восстановить, с помощью [Get-AzSqlDeletedDatabaseBackup.](./Get-AzSqlDeletedDatabaseBackup.md)</span><span class="sxs-lookup"><span data-stu-id="411a9-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="411a9-130">Вторая команда запускает восстановление из удаленной резервной копии базы данных с помощью [restore-AzSqlDatabase.](./Restore-AzSqlDatabase.md)</span><span class="sxs-lookup"><span data-stu-id="411a9-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="411a9-131">Если параметр -PointInTime не указан, база данных будет восстановлена до времени удаления.</span><span class="sxs-lookup"><span data-stu-id="411a9-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="411a9-132">Пример 5. Geo-Restore базы данных</span><span class="sxs-lookup"><span data-stu-id="411a9-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="411a9-133">Первая команда получает гео избыточное резервное копирование для базы данных Database01, а затем сохраняет ее в $GeoBackup переменной.</span><span class="sxs-lookup"><span data-stu-id="411a9-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="411a9-134">Вторая команда восстанавливает резервную копию в $GeoBackup в SQL с именем RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="411a9-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="411a9-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="411a9-135">PARAMETERS</span></span>

### <span data-ttu-id="411a9-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="411a9-136">-AsJob</span></span>
<span data-ttu-id="411a9-137">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="411a9-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="411a9-138">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="411a9-138">-BackupStorageRedundancy</span></span>
<span data-ttu-id="411a9-139">Избыточность резервного копирования хранилища, используемого для хранения резервных копий SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="411a9-139">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="411a9-140">Доступны такие варианты: Local (Локальный), Zone (Зона) и Geo (География).</span><span class="sxs-lookup"><span data-stu-id="411a9-140">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="411a9-141">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="411a9-141">-ComputeGeneration</span></span>
<span data-ttu-id="411a9-142">The compute generation to assign to the restored database</span><span class="sxs-lookup"><span data-stu-id="411a9-142">The compute generation to assign to the restored database</span></span>

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

### <span data-ttu-id="411a9-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="411a9-143">-DefaultProfile</span></span>
<span data-ttu-id="411a9-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="411a9-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="411a9-145">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="411a9-145">-DeletionDate</span></span>
<span data-ttu-id="411a9-146">Дата удаления в качестве объекта **даты и** времени.</span><span class="sxs-lookup"><span data-stu-id="411a9-146">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="411a9-147">Чтобы получить объект **даты и времени,** воспользуйтесь Get-Date.</span><span class="sxs-lookup"><span data-stu-id="411a9-147">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="411a9-148">-Edition</span><span class="sxs-lookup"><span data-stu-id="411a9-148">-Edition</span></span>
<span data-ttu-id="411a9-149">Выпуск базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="411a9-149">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="411a9-150">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="411a9-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="411a9-151">Нет</span><span class="sxs-lookup"><span data-stu-id="411a9-151">None</span></span>
- <span data-ttu-id="411a9-152">Базовая</span><span class="sxs-lookup"><span data-stu-id="411a9-152">Basic</span></span>
- <span data-ttu-id="411a9-153">Стандартный</span><span class="sxs-lookup"><span data-stu-id="411a9-153">Standard</span></span>
- <span data-ttu-id="411a9-154">Premium</span><span class="sxs-lookup"><span data-stu-id="411a9-154">Premium</span></span>
- <span data-ttu-id="411a9-155">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="411a9-155">DataWarehouse</span></span>
- <span data-ttu-id="411a9-156">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="411a9-156">Free</span></span>
- <span data-ttu-id="411a9-157">Растяжение</span><span class="sxs-lookup"><span data-stu-id="411a9-157">Stretch</span></span>
- <span data-ttu-id="411a9-158">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="411a9-158">GeneralPurpose</span></span>
- <span data-ttu-id="411a9-159">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="411a9-159">BusinessCritical</span></span>

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

### <span data-ttu-id="411a9-160">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="411a9-160">-ElasticPoolName</span></span>
<span data-ttu-id="411a9-161">Определяет имя эластичного пула, в который нужно поместить SQL базу данных.</span><span class="sxs-lookup"><span data-stu-id="411a9-161">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

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

### <span data-ttu-id="411a9-162">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="411a9-162">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="411a9-163">Указывает на то, что этот cmdlet восстанавливает базу данных из резервной копии удаленной SQL.</span><span class="sxs-lookup"><span data-stu-id="411a9-163">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="411a9-164">Вы можете использовать Get-AzSqlDeletedDatabaseBackup для получения резервной копии удаленной SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="411a9-164">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

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

### <span data-ttu-id="411a9-165">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="411a9-165">-FromGeoBackup</span></span>
<span data-ttu-id="411a9-166">Указывает на то, что этот SQL восстанавливает базу данных из гео избыточных резервных копий.</span><span class="sxs-lookup"><span data-stu-id="411a9-166">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="411a9-167">Для получения гео-избыточной резервной копии можно использовать Get-AzSqlDatabaseGeoBackup- и резервную копию.</span><span class="sxs-lookup"><span data-stu-id="411a9-167">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

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

### <span data-ttu-id="411a9-168">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="411a9-168">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="411a9-169">Указывает на то, что этот SQL восстанавливает базу данных из долгосрочной резервной копии.</span><span class="sxs-lookup"><span data-stu-id="411a9-169">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

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

### <span data-ttu-id="411a9-170">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="411a9-170">-FromPointInTimeBackup</span></span>
<span data-ttu-id="411a9-171">Указывает на то, что этот SQL восстанавливает базу данных из заданной моментарной резервной копии.</span><span class="sxs-lookup"><span data-stu-id="411a9-171">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

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

### <span data-ttu-id="411a9-172">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="411a9-172">-LicenseType</span></span>
<span data-ttu-id="411a9-173">Тип лицензии для базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="411a9-173">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="411a9-174">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="411a9-174">-PointInTime</span></span>
<span data-ttu-id="411a9-175">Указывает время в качестве объекта **даты** и времени, до SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="411a9-175">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="411a9-176">Чтобы получить объект **даты и времени,** используйте для этого cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="411a9-176">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="411a9-177">Используйте этот параметр вместе с *параметром FromPointInTimeBackup.*</span><span class="sxs-lookup"><span data-stu-id="411a9-177">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

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

### <span data-ttu-id="411a9-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="411a9-178">-ResourceGroupName</span></span>
<span data-ttu-id="411a9-179">Задает имя группы ресурсов, которой этот SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="411a9-179">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="411a9-180">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="411a9-180">-ResourceId</span></span>
<span data-ttu-id="411a9-181">Определяет ИД ресурса, который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="411a9-181">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="411a9-182">-ServerName</span><span class="sxs-lookup"><span data-stu-id="411a9-182">-ServerName</span></span>
<span data-ttu-id="411a9-183">Указывает имя сервера SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="411a9-183">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="411a9-184">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="411a9-184">-ServiceObjectiveName</span></span>
<span data-ttu-id="411a9-185">Указывает имя цели обслуживания.</span><span class="sxs-lookup"><span data-stu-id="411a9-185">Specifies the name of the service objective.</span></span>

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

### <span data-ttu-id="411a9-186">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="411a9-186">-TargetDatabaseName</span></span>
<span data-ttu-id="411a9-187">Имя базы данных, которая будет восстановлена.</span><span class="sxs-lookup"><span data-stu-id="411a9-187">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="411a9-188">-VCore</span><span class="sxs-lookup"><span data-stu-id="411a9-188">-VCore</span></span>
<span data-ttu-id="411a9-189">Номера на vcore восстановленной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="411a9-189">The Vcore numbers of the restored Azure Sql Database.</span></span>

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

### <span data-ttu-id="411a9-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="411a9-190">-Confirm</span></span>
<span data-ttu-id="411a9-191">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="411a9-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="411a9-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="411a9-192">-WhatIf</span></span>
<span data-ttu-id="411a9-193">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="411a9-193">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="411a9-194">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="411a9-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="411a9-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="411a9-195">CommonParameters</span></span>
<span data-ttu-id="411a9-196">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="411a9-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="411a9-197">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="411a9-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="411a9-198">INPUTS</span><span class="sxs-lookup"><span data-stu-id="411a9-198">INPUTS</span></span>

### <span data-ttu-id="411a9-199">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="411a9-199">System.DateTime</span></span>

### <span data-ttu-id="411a9-200">System.String</span><span class="sxs-lookup"><span data-stu-id="411a9-200">System.String</span></span>

## <span data-ttu-id="411a9-201">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="411a9-201">OUTPUTS</span></span>

### <span data-ttu-id="411a9-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="411a9-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="411a9-203">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="411a9-203">NOTES</span></span>

## <span data-ttu-id="411a9-204">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="411a9-204">RELATED LINKS</span></span>

[<span data-ttu-id="411a9-205">Восстановление базы данных Azure SQL из-за простоя</span><span class="sxs-lookup"><span data-stu-id="411a9-205">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="411a9-206">Восстановление базы данных Azure SQL после ошибки пользователя</span><span class="sxs-lookup"><span data-stu-id="411a9-206">Recover an Azure SQL Database from a user error</span></span>](http://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="411a9-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="411a9-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="411a9-208">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="411a9-208">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="411a9-209">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="411a9-209">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="411a9-210">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="411a9-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

