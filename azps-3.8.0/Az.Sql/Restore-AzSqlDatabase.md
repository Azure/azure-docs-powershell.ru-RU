---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: 6b6c6c23fbabec663bb2e9863bb7090d5c869802
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073479"
---
# <span data-ttu-id="cf052-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cf052-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="cf052-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf052-102">SYNOPSIS</span></span>
<span data-ttu-id="cf052-103">Восстанавливает базу данных SQL.</span><span class="sxs-lookup"><span data-stu-id="cf052-103">Restores a SQL database.</span></span>

## <span data-ttu-id="cf052-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf052-104">SYNTAX</span></span>

### <span data-ttu-id="cf052-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="cf052-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf052-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="cf052-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf052-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="cf052-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf052-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="cf052-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf052-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="cf052-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf052-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="cf052-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf052-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="cf052-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf052-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="cf052-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf052-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf052-113">DESCRIPTION</span></span>
<span data-ttu-id="cf052-114">Командлет **RESTORE-AzSqlDatabase** восстанавливает базу данных SQL из резервной копии с геоизбыточностью, резервной копии удаленной базы данных, длительной резервной копии хранения или момента времени в действующей базе данных.</span><span class="sxs-lookup"><span data-stu-id="cf052-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="cf052-115">Восстановленная база данных будет создана как новая.</span><span class="sxs-lookup"><span data-stu-id="cf052-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="cf052-116">Вы можете создать эластичную базу данных SQL, указав параметр *ElasticPoolName* в существующем пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="cf052-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="cf052-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf052-117">EXAMPLES</span></span>

### <span data-ttu-id="cf052-118">Пример 1: восстановление базы данных на момент времени</span><span class="sxs-lookup"><span data-stu-id="cf052-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="cf052-119">Первая команда получает базу данных SQL с именем Database01 и сохраняет ее в переменной $Database.</span><span class="sxs-lookup"><span data-stu-id="cf052-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="cf052-120">Вторая команда восстанавливает базу данных $Database из указанного резервного копирования на момент времени в базу данных с именем RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="cf052-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="cf052-121">Пример 2: восстановление базы данных из состояния на момент времени в пул эластичных БД</span><span class="sxs-lookup"><span data-stu-id="cf052-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="cf052-122">Первая команда получает базу данных SQL с именем Database01 и сохраняет ее в переменной $Database.</span><span class="sxs-lookup"><span data-stu-id="cf052-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="cf052-123">Вторая команда восстанавливает базу данных $Database из указанного резервного копирования на момент времени в базу данных SQL с именем RestoredDatabase в пуле эластичных БД с именем elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="cf052-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="cf052-124">Пример 3: восстановление удаленной базы данных</span><span class="sxs-lookup"><span data-stu-id="cf052-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="cf052-125">Первая команда получает удаленную резервную копию базы данных, которую вы хотите восстановить, с помощью [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="cf052-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="cf052-126">Вторая команда запускает восстановление из удаленной резервной копии базы данных с помощью командлета [RESTORE-AzSqlDatabase](./Restore-AzSqlDatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="cf052-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="cf052-127">Если параметр-PointInTime не указан, база данных будет восстановлена до времени удаления.</span><span class="sxs-lookup"><span data-stu-id="cf052-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="cf052-128">Пример 4: восстановление удаленной базы данных в пуле эластичных БД</span><span class="sxs-lookup"><span data-stu-id="cf052-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="cf052-129">Первая команда получает удаленную резервную копию базы данных, которую вы хотите восстановить, с помощью [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="cf052-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="cf052-130">Вторая команда запускает восстановление из удаленной резервной копии базы данных с помощью [RESTORE-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span><span class="sxs-lookup"><span data-stu-id="cf052-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="cf052-131">Если параметр-PointInTime не указан, база данных будет восстановлена до времени удаления.</span><span class="sxs-lookup"><span data-stu-id="cf052-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="cf052-132">Пример 5: Geo-Restore базы данных</span><span class="sxs-lookup"><span data-stu-id="cf052-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="cf052-133">Первая команда получает геоизбыточное резервное копирование базы данных с именем Database01 и сохраняет его в переменной $GeoBackup.</span><span class="sxs-lookup"><span data-stu-id="cf052-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="cf052-134">Вторая команда восстанавливает резервную копию в $GeoBackup на базу данных SQL с именем RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="cf052-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="cf052-135">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf052-135">PARAMETERS</span></span>

### <span data-ttu-id="cf052-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf052-136">-AsJob</span></span>
<span data-ttu-id="cf052-137">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cf052-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf052-138">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="cf052-138">-ComputeGeneration</span></span>
<span data-ttu-id="cf052-139">Вычислено поколение, назначаемое восстановленной базе данных.</span><span class="sxs-lookup"><span data-stu-id="cf052-139">The compute generation to assign to the restored database</span></span>

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

### <span data-ttu-id="cf052-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf052-140">-DefaultProfile</span></span>
<span data-ttu-id="cf052-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cf052-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf052-142">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="cf052-142">-DeletionDate</span></span>
<span data-ttu-id="cf052-143">Указывает дату удаления как объект **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="cf052-143">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="cf052-144">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="cf052-144">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="cf052-145">-Edition</span><span class="sxs-lookup"><span data-stu-id="cf052-145">-Edition</span></span>
<span data-ttu-id="cf052-146">Указывает выпуск базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="cf052-146">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="cf052-147">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cf052-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cf052-148">Ничего</span><span class="sxs-lookup"><span data-stu-id="cf052-148">None</span></span>
- <span data-ttu-id="cf052-149">Базового</span><span class="sxs-lookup"><span data-stu-id="cf052-149">Basic</span></span>
- <span data-ttu-id="cf052-150">Стандартная</span><span class="sxs-lookup"><span data-stu-id="cf052-150">Standard</span></span>
- <span data-ttu-id="cf052-151">Версию</span><span class="sxs-lookup"><span data-stu-id="cf052-151">Premium</span></span>
- <span data-ttu-id="cf052-152">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="cf052-152">DataWarehouse</span></span>
- <span data-ttu-id="cf052-153">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="cf052-153">Free</span></span>
- <span data-ttu-id="cf052-154">Показателя</span><span class="sxs-lookup"><span data-stu-id="cf052-154">Stretch</span></span>
- <span data-ttu-id="cf052-155">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="cf052-155">GeneralPurpose</span></span>
- <span data-ttu-id="cf052-156">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="cf052-156">BusinessCritical</span></span>

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

### <span data-ttu-id="cf052-157">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="cf052-157">-ElasticPoolName</span></span>
<span data-ttu-id="cf052-158">Указывает имя эластичного пула, в который нужно добавить базу данных SQL.</span><span class="sxs-lookup"><span data-stu-id="cf052-158">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

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

### <span data-ttu-id="cf052-159">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="cf052-159">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="cf052-160">Указывает на то, что этот командлет восстанавливает базу данных из резервной копии удаленной базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="cf052-160">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="cf052-161">Вы можете использовать командлет Get-AzSqlDeletedDatabaseBackup для получения резервной копии удаленной базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="cf052-161">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

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

### <span data-ttu-id="cf052-162">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="cf052-162">-FromGeoBackup</span></span>
<span data-ttu-id="cf052-163">Указывает на то, что этот командлет восстанавливает базу данных SQL из резервной копии с избыточностью.</span><span class="sxs-lookup"><span data-stu-id="cf052-163">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="cf052-164">Вы можете использовать командлет Get-AzSqlDatabaseGeoBackup, чтобы получить геоизбыточную резервную копию.</span><span class="sxs-lookup"><span data-stu-id="cf052-164">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

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

### <span data-ttu-id="cf052-165">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="cf052-165">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="cf052-166">Указывает на то, что этот командлет восстанавливает базу данных SQL из резервной копии длительного хранения.</span><span class="sxs-lookup"><span data-stu-id="cf052-166">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

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

### <span data-ttu-id="cf052-167">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="cf052-167">-FromPointInTimeBackup</span></span>
<span data-ttu-id="cf052-168">Указывает на то, что этот командлет восстанавливает базу данных SQL из резервной копии на момент времени.</span><span class="sxs-lookup"><span data-stu-id="cf052-168">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

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

### <span data-ttu-id="cf052-169">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="cf052-169">-LicenseType</span></span>
<span data-ttu-id="cf052-170">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="cf052-170">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="cf052-171">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="cf052-171">-PointInTime</span></span>
<span data-ttu-id="cf052-172">Задает момент времени в виде объекта **DateTime** , на который вы хотите восстановить базу данных SQL.</span><span class="sxs-lookup"><span data-stu-id="cf052-172">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="cf052-173">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="cf052-173">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="cf052-174">Используйте этот параметр вместе с параметром *FromPointInTimeBackup* .</span><span class="sxs-lookup"><span data-stu-id="cf052-174">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

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

### <span data-ttu-id="cf052-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf052-175">-ResourceGroupName</span></span>
<span data-ttu-id="cf052-176">Указывает имя группы ресурсов, к которой этот командлет назначает базу данных SQL.</span><span class="sxs-lookup"><span data-stu-id="cf052-176">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="cf052-177">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf052-177">-ResourceId</span></span>
<span data-ttu-id="cf052-178">Указывает идентификатор ресурса для восстановления.</span><span class="sxs-lookup"><span data-stu-id="cf052-178">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="cf052-179">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="cf052-179">-ServerName</span></span>
<span data-ttu-id="cf052-180">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="cf052-180">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="cf052-181">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="cf052-181">-ServiceObjectiveName</span></span>
<span data-ttu-id="cf052-182">Указывает имя цели обслуживания.</span><span class="sxs-lookup"><span data-stu-id="cf052-182">Specifies the name of the service objective.</span></span>

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

### <span data-ttu-id="cf052-183">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="cf052-183">-TargetDatabaseName</span></span>
<span data-ttu-id="cf052-184">Указывает имя базы данных, в которую будет восстановлено значение.</span><span class="sxs-lookup"><span data-stu-id="cf052-184">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="cf052-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="cf052-185">-VCore</span></span>
<span data-ttu-id="cf052-186">Vcore номера восстановленной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="cf052-186">The Vcore numbers of the restored Azure Sql Database.</span></span>

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

### <span data-ttu-id="cf052-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf052-187">CommonParameters</span></span>
<span data-ttu-id="cf052-188">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf052-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf052-189">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf052-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf052-190">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf052-190">INPUTS</span></span>

### <span data-ttu-id="cf052-191">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="cf052-191">System.DateTime</span></span>

### <span data-ttu-id="cf052-192">System. String</span><span class="sxs-lookup"><span data-stu-id="cf052-192">System.String</span></span>

## <span data-ttu-id="cf052-193">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf052-193">OUTPUTS</span></span>

### <span data-ttu-id="cf052-194">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cf052-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="cf052-195">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf052-195">NOTES</span></span>

## <span data-ttu-id="cf052-196">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf052-196">RELATED LINKS</span></span>

[<span data-ttu-id="cf052-197">Восстановление базы данных SQL Azure из сбоя</span><span class="sxs-lookup"><span data-stu-id="cf052-197">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="cf052-198">Восстановление базы данных SQL Azure из пользовательской ошибки</span><span class="sxs-lookup"><span data-stu-id="cf052-198">Recover an Azure SQL Database from a user error</span></span>](http://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="cf052-199">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cf052-199">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="cf052-200">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="cf052-200">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="cf052-201">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="cf052-201">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="cf052-202">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="cf052-202">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

