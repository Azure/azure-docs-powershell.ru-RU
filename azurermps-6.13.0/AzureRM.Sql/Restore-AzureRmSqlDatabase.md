---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: b4c444233701a6ecfe66eb77f90dade618c9e08f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565327"
---
# <span data-ttu-id="51d4b-101">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="51d4b-101">Restore-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="51d4b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="51d4b-103">Восстанавливает базу данных SQL.</span><span class="sxs-lookup"><span data-stu-id="51d4b-103">Restores a SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51d4b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51d4b-104">SYNTAX</span></span>

### <span data-ttu-id="51d4b-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="51d4b-105">FromPointInTimeBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51d4b-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="51d4b-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51d4b-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="51d4b-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51d4b-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="51d4b-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51d4b-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="51d4b-109">FromGeoBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51d4b-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="51d4b-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51d4b-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="51d4b-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51d4b-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="51d4b-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51d4b-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51d4b-113">DESCRIPTION</span></span>
<span data-ttu-id="51d4b-114">Командлет **RESTORE-AzureRmSqlDatabase** восстанавливает базу данных SQL из резервной копии с геоизбыточностью, резервной копии удаленной базы данных, длительной резервной копии хранения или момента времени в действующей базе данных.</span><span class="sxs-lookup"><span data-stu-id="51d4b-114">The **Restore-AzureRmSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="51d4b-115">Восстановленная база данных будет создана как новая.</span><span class="sxs-lookup"><span data-stu-id="51d4b-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="51d4b-116">Вы можете создать эластичную базу данных SQL, указав параметр *ElasticPoolName* в существующем пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="51d4b-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="51d4b-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51d4b-117">EXAMPLES</span></span>

### <span data-ttu-id="51d4b-118">Пример 1: восстановление базы данных на момент времени</span><span class="sxs-lookup"><span data-stu-id="51d4b-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="51d4b-119">Первая команда получает базу данных SQL с именем Database01 и сохраняет ее в переменной $Database.</span><span class="sxs-lookup"><span data-stu-id="51d4b-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="51d4b-120">Вторая команда восстанавливает базу данных $Database из указанного резервного копирования на момент времени в базу данных с именем RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="51d4b-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="51d4b-121">Пример 2: восстановление базы данных из состояния на момент времени в пул эластичных БД</span><span class="sxs-lookup"><span data-stu-id="51d4b-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="51d4b-122">Первая команда получает базу данных SQL с именем Database01 и сохраняет ее в переменной $Database.</span><span class="sxs-lookup"><span data-stu-id="51d4b-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="51d4b-123">Вторая команда восстанавливает базу данных $Database из указанного резервного копирования на момент времени в базу данных SQL с именем RestoredDatabase в пуле эластичных БД с именем elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="51d4b-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="51d4b-124">Пример 3: восстановление удаленной базы данных</span><span class="sxs-lookup"><span data-stu-id="51d4b-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="51d4b-125">Первая команда получает удаленную резервную копию базы данных, которую вы хотите восстановить, с помощью [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="51d4b-125">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="51d4b-126">Вторая команда запускает восстановление из удаленной резервной копии базы данных с помощью командлета [RESTORE-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="51d4b-126">The second command starts the restore from the deleted database backup by using the [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="51d4b-127">Если параметр-PointInTime не указан, база данных будет восстановлена до времени удаления.</span><span class="sxs-lookup"><span data-stu-id="51d4b-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="51d4b-128">Пример 4: восстановление удаленной базы данных в пуле эластичных БД</span><span class="sxs-lookup"><span data-stu-id="51d4b-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="51d4b-129">Первая команда получает удаленную резервную копию базы данных, которую вы хотите восстановить, с помощью [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="51d4b-129">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="51d4b-130">Вторая команда запускает восстановление из удаленной резервной копии базы данных с помощью [RESTORE-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span><span class="sxs-lookup"><span data-stu-id="51d4b-130">The second command starts the restore from the deleted database backup by using [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span></span> <span data-ttu-id="51d4b-131">Если параметр-PointInTime не указан, база данных будет восстановлена до времени удаления.</span><span class="sxs-lookup"><span data-stu-id="51d4b-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="51d4b-132">Пример 5: Geo-Restore базы данных</span><span class="sxs-lookup"><span data-stu-id="51d4b-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="51d4b-133">Первая команда получает геоизбыточное резервное копирование базы данных с именем Database01 и сохраняет его в переменной $GeoBackup.</span><span class="sxs-lookup"><span data-stu-id="51d4b-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="51d4b-134">Вторая команда восстанавливает резервную копию в $GeoBackup на базу данных SQL с именем RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="51d4b-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="51d4b-135">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51d4b-135">PARAMETERS</span></span>

### <span data-ttu-id="51d4b-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51d4b-136">-AsJob</span></span>
<span data-ttu-id="51d4b-137">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="51d4b-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51d4b-138">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="51d4b-138">-ComputeGeneration</span></span>
<span data-ttu-id="51d4b-139">Вычислено поколение, назначаемое восстановленной базе данных.</span><span class="sxs-lookup"><span data-stu-id="51d4b-139">The compute generation to assign to the restored database</span></span>

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

### <span data-ttu-id="51d4b-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51d4b-140">-DefaultProfile</span></span>
<span data-ttu-id="51d4b-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="51d4b-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51d4b-142">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="51d4b-142">-DeletionDate</span></span>
<span data-ttu-id="51d4b-143">Указывает дату удаления как объект **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="51d4b-143">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="51d4b-144">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="51d4b-144">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="51d4b-145">-Edition</span><span class="sxs-lookup"><span data-stu-id="51d4b-145">-Edition</span></span>
<span data-ttu-id="51d4b-146">Указывает выпуск базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="51d4b-146">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="51d4b-147">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="51d4b-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="51d4b-148">Ничего</span><span class="sxs-lookup"><span data-stu-id="51d4b-148">None</span></span>
- <span data-ttu-id="51d4b-149">Базового</span><span class="sxs-lookup"><span data-stu-id="51d4b-149">Basic</span></span>
- <span data-ttu-id="51d4b-150">Стандартная</span><span class="sxs-lookup"><span data-stu-id="51d4b-150">Standard</span></span>
- <span data-ttu-id="51d4b-151">Версию</span><span class="sxs-lookup"><span data-stu-id="51d4b-151">Premium</span></span>
- <span data-ttu-id="51d4b-152">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="51d4b-152">DataWarehouse</span></span>
- <span data-ttu-id="51d4b-153">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="51d4b-153">Free</span></span>
- <span data-ttu-id="51d4b-154">Показателя</span><span class="sxs-lookup"><span data-stu-id="51d4b-154">Stretch</span></span>
- <span data-ttu-id="51d4b-155">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="51d4b-155">GeneralPurpose</span></span>
- <span data-ttu-id="51d4b-156">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="51d4b-156">BusinessCritical</span></span>

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

### <span data-ttu-id="51d4b-157">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="51d4b-157">-ElasticPoolName</span></span>
<span data-ttu-id="51d4b-158">Указывает имя эластичного пула, в который нужно добавить базу данных SQL.</span><span class="sxs-lookup"><span data-stu-id="51d4b-158">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

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

### <span data-ttu-id="51d4b-159">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="51d4b-159">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="51d4b-160">Указывает на то, что этот командлет восстанавливает базу данных из резервной копии удаленной базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="51d4b-160">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="51d4b-161">Вы можете использовать командлет Get-AzureRMSqlDeletedDatabaseBackup для получения резервной копии удаленной базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="51d4b-161">You can use the Get-AzureRMSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

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

### <span data-ttu-id="51d4b-162">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="51d4b-162">-FromGeoBackup</span></span>
<span data-ttu-id="51d4b-163">Указывает на то, что этот командлет восстанавливает базу данных SQL из резервной копии с избыточностью.</span><span class="sxs-lookup"><span data-stu-id="51d4b-163">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="51d4b-164">Вы можете использовать командлет Get-AzureRMSqlDatabaseGeoBackup, чтобы получить геоизбыточную резервную копию.</span><span class="sxs-lookup"><span data-stu-id="51d4b-164">You can use the Get-AzureRMSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

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

### <span data-ttu-id="51d4b-165">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="51d4b-165">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="51d4b-166">Указывает на то, что этот командлет восстанавливает базу данных SQL из резервной копии длительного хранения.</span><span class="sxs-lookup"><span data-stu-id="51d4b-166">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

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

### <span data-ttu-id="51d4b-167">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="51d4b-167">-FromPointInTimeBackup</span></span>
<span data-ttu-id="51d4b-168">Указывает на то, что этот командлет восстанавливает базу данных SQL из резервной копии на момент времени.</span><span class="sxs-lookup"><span data-stu-id="51d4b-168">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

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

### <span data-ttu-id="51d4b-169">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="51d4b-169">-LicenseType</span></span>
<span data-ttu-id="51d4b-170">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="51d4b-170">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="51d4b-171">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="51d4b-171">-PointInTime</span></span>
<span data-ttu-id="51d4b-172">Задает момент времени в виде объекта **DateTime** , на который вы хотите восстановить базу данных SQL.</span><span class="sxs-lookup"><span data-stu-id="51d4b-172">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="51d4b-173">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="51d4b-173">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="51d4b-174">Используйте этот параметр вместе с параметром *FromPointInTimeBackup* .</span><span class="sxs-lookup"><span data-stu-id="51d4b-174">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

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

### <span data-ttu-id="51d4b-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51d4b-175">-ResourceGroupName</span></span>
<span data-ttu-id="51d4b-176">Указывает имя группы ресурсов, к которой этот командлет назначает базу данных SQL.</span><span class="sxs-lookup"><span data-stu-id="51d4b-176">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="51d4b-177">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51d4b-177">-ResourceId</span></span>
<span data-ttu-id="51d4b-178">Указывает идентификатор ресурса для восстановления.</span><span class="sxs-lookup"><span data-stu-id="51d4b-178">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="51d4b-179">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="51d4b-179">-ServerName</span></span>
<span data-ttu-id="51d4b-180">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="51d4b-180">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="51d4b-181">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="51d4b-181">-ServiceObjectiveName</span></span>
<span data-ttu-id="51d4b-182">Указывает имя цели обслуживания.</span><span class="sxs-lookup"><span data-stu-id="51d4b-182">Specifies the name of the service objective.</span></span>

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

### <span data-ttu-id="51d4b-183">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="51d4b-183">-TargetDatabaseName</span></span>
<span data-ttu-id="51d4b-184">Указывает имя базы данных, в которую будет восстановлено значение.</span><span class="sxs-lookup"><span data-stu-id="51d4b-184">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="51d4b-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="51d4b-185">-VCore</span></span>
<span data-ttu-id="51d4b-186">Vcore номера восстановленной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="51d4b-186">The Vcore numbers of the restored Azure Sql Database.</span></span>

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

### <span data-ttu-id="51d4b-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51d4b-187">CommonParameters</span></span>
<span data-ttu-id="51d4b-188">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51d4b-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51d4b-189">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51d4b-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51d4b-190">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51d4b-190">INPUTS</span></span>

### <span data-ttu-id="51d4b-191">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="51d4b-191">System.DateTime</span></span>

### <span data-ttu-id="51d4b-192">System. String</span><span class="sxs-lookup"><span data-stu-id="51d4b-192">System.String</span></span>

## <span data-ttu-id="51d4b-193">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51d4b-193">OUTPUTS</span></span>

### <span data-ttu-id="51d4b-194">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="51d4b-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="51d4b-195">Пуск</span><span class="sxs-lookup"><span data-stu-id="51d4b-195">NOTES</span></span>

## <span data-ttu-id="51d4b-196">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51d4b-196">RELATED LINKS</span></span>

[<span data-ttu-id="51d4b-197">Восстановление базы данных SQL Azure из сбоя</span><span class="sxs-lookup"><span data-stu-id="51d4b-197">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="51d4b-198">Восстановление базы данных SQL Azure из пользовательской ошибки</span><span class="sxs-lookup"><span data-stu-id="51d4b-198">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="51d4b-199">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="51d4b-199">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="51d4b-200">Get-AzureRMSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="51d4b-200">Get-AzureRMSqlDatabaseGeoBackup</span></span>](./Get-AzureRMSqlDatabaseGeoBackup.md)

[<span data-ttu-id="51d4b-201">Get-AzureRMSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="51d4b-201">Get-AzureRMSqlDeletedDatabaseBackup</span></span>](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="51d4b-202">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="51d4b-202">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

