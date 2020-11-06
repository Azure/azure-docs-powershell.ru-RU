---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: 61f66a61d14738da034644fc3dfef865c8719181
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562024"
---
# <span data-ttu-id="bac59-101">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bac59-101">Restore-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="bac59-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bac59-102">SYNOPSIS</span></span>
<span data-ttu-id="bac59-103">Восстанавливает базу данных SQL.</span><span class="sxs-lookup"><span data-stu-id="bac59-103">Restores a SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bac59-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bac59-104">SYNTAX</span></span>

### <span data-ttu-id="bac59-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="bac59-105">FromPointInTimeBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bac59-106">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="bac59-106">FromDeletedDatabaseBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bac59-107">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="bac59-107">FromGeoBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bac59-108">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="bac59-108">FromLongTermRetentionBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bac59-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bac59-109">DESCRIPTION</span></span>
<span data-ttu-id="bac59-110">Командлет **RESTORE-AzureRmSqlDatabase** восстанавливает базу данных SQL из резервной копии с геоизбыточностью, резервной копии удаленной базы данных, длительной резервной копии хранения или момента времени в действующей базе данных.</span><span class="sxs-lookup"><span data-stu-id="bac59-110">The **Restore-AzureRmSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="bac59-111">Восстановленная база данных будет создана как новая.</span><span class="sxs-lookup"><span data-stu-id="bac59-111">The restored database is created as a new database.</span></span>

<span data-ttu-id="bac59-112">Вы можете создать эластичную базу данных SQL, указав параметр *ElasticPoolName* в существующем пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="bac59-112">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="bac59-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bac59-113">EXAMPLES</span></span>

### <span data-ttu-id="bac59-114">Пример 1: восстановление базы данных на момент времени</span><span class="sxs-lookup"><span data-stu-id="bac59-114">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="bac59-115">Первая команда получает базу данных SQL с именем Database01 и сохраняет ее в переменной $Database.</span><span class="sxs-lookup"><span data-stu-id="bac59-115">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="bac59-116">Вторая команда восстанавливает базу данных $Database из указанного резервного копирования на момент времени в базу данных с именем RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="bac59-116">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="bac59-117">Пример 2: восстановление базы данных из состояния на момент времени в пул эластичных БД</span><span class="sxs-lookup"><span data-stu-id="bac59-117">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="bac59-118">Первая команда получает базу данных SQL с именем Database01 и сохраняет ее в переменной $Database.</span><span class="sxs-lookup"><span data-stu-id="bac59-118">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="bac59-119">Вторая команда восстанавливает базу данных $Database из указанного резервного копирования на момент времени в базу данных SQL с именем RestoredDatabase в пуле эластичных БД с именем elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="bac59-119">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="bac59-120">Пример 3: восстановление удаленной базы данных</span><span class="sxs-lookup"><span data-stu-id="bac59-120">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="bac59-121">Первая команда получает удаленную резервную копию базы данных, которую вы хотите восстановить, с помощью [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="bac59-121">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="bac59-122">Вторая команда запускает восстановление из удаленной резервной копии базы данных с помощью командлета [RESTORE-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="bac59-122">The second command starts the restore from the deleted database backup by using the [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="bac59-123">Если параметр-PointInTime не указан, база данных будет восстановлена до времени удаления.</span><span class="sxs-lookup"><span data-stu-id="bac59-123">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="bac59-124">Пример 4: восстановление удаленной базы данных в пуле эластичных БД</span><span class="sxs-lookup"><span data-stu-id="bac59-124">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="bac59-125">Первая команда получает удаленную резервную копию базы данных, которую вы хотите восстановить, с помощью [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="bac59-125">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="bac59-126">Вторая команда запускает восстановление из удаленной резервной копии базы данных с помощью [RESTORE-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span><span class="sxs-lookup"><span data-stu-id="bac59-126">The second command starts the restore from the deleted database backup by using [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span></span> <span data-ttu-id="bac59-127">Если параметр-PointInTime не указан, база данных будет восстановлена до времени удаления.</span><span class="sxs-lookup"><span data-stu-id="bac59-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="bac59-128">Пример 5: Geo-Restore базы данных</span><span class="sxs-lookup"><span data-stu-id="bac59-128">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="bac59-129">Первая команда получает геоизбыточное резервное копирование базы данных с именем Database01 и сохраняет его в переменной $GeoBackup.</span><span class="sxs-lookup"><span data-stu-id="bac59-129">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>

<span data-ttu-id="bac59-130">Вторая команда восстанавливает резервную копию в $GeoBackup на базу данных SQL с именем RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="bac59-130">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="bac59-131">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bac59-131">PARAMETERS</span></span>

### <span data-ttu-id="bac59-132">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="bac59-132">-DeletionDate</span></span>
<span data-ttu-id="bac59-133">Указывает дату удаления как объект **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="bac59-133">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="bac59-134">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="bac59-134">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bac59-135">-Edition</span><span class="sxs-lookup"><span data-stu-id="bac59-135">-Edition</span></span>
<span data-ttu-id="bac59-136">Указывает выпуск базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="bac59-136">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="bac59-137">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bac59-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bac59-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="bac59-138">None</span></span>
- <span data-ttu-id="bac59-139">Версию</span><span class="sxs-lookup"><span data-stu-id="bac59-139">Premium</span></span>
- <span data-ttu-id="bac59-140">Базового</span><span class="sxs-lookup"><span data-stu-id="bac59-140">Basic</span></span>
- <span data-ttu-id="bac59-141">Стандартная</span><span class="sxs-lookup"><span data-stu-id="bac59-141">Standard</span></span>
- <span data-ttu-id="bac59-142">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="bac59-142">DataWarehouse</span></span>
- <span data-ttu-id="bac59-143">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="bac59-143">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bac59-144">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="bac59-144">-ElasticPoolName</span></span>
<span data-ttu-id="bac59-145">Указывает имя эластичного пула, в который нужно добавить базу данных SQL.</span><span class="sxs-lookup"><span data-stu-id="bac59-145">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bac59-146">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="bac59-146">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="bac59-147">Указывает на то, что этот командлет восстанавливает базу данных из резервной копии удаленной базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="bac59-147">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="bac59-148">Вы можете использовать командлет Get-AzureRMSqlDeletedDatabaseBackup для получения резервной копии удаленной базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="bac59-148">You can use the Get-AzureRMSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bac59-149">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="bac59-149">-FromGeoBackup</span></span>
<span data-ttu-id="bac59-150">Указывает на то, что этот командлет восстанавливает базу данных SQL из резервной копии с избыточностью.</span><span class="sxs-lookup"><span data-stu-id="bac59-150">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="bac59-151">Вы можете использовать командлет Get-AzureRMSqlDatabaseGeoBackup, чтобы получить геоизбыточную резервную копию.</span><span class="sxs-lookup"><span data-stu-id="bac59-151">You can use the Get-AzureRMSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bac59-152">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="bac59-152">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="bac59-153">Указывает на то, что этот командлет восстанавливает базу данных SQL из резервной копии длительного хранения.</span><span class="sxs-lookup"><span data-stu-id="bac59-153">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bac59-154">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="bac59-154">-FromPointInTimeBackup</span></span>
<span data-ttu-id="bac59-155">Указывает на то, что этот командлет восстанавливает базу данных SQL из резервной копии на момент времени.</span><span class="sxs-lookup"><span data-stu-id="bac59-155">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bac59-156">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="bac59-156">-PointInTime</span></span>
<span data-ttu-id="bac59-157">Задает момент времени в виде объекта **DateTime** , на который вы хотите восстановить базу данных SQL.</span><span class="sxs-lookup"><span data-stu-id="bac59-157">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="bac59-158">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="bac59-158">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>

<span data-ttu-id="bac59-159">Используйте этот параметр вместе с параметром *FromPointInTimeBackup* .</span><span class="sxs-lookup"><span data-stu-id="bac59-159">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bac59-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bac59-160">-ResourceGroupName</span></span>
<span data-ttu-id="bac59-161">Указывает имя группы ресурсов, к которой этот командлет назначает базу данных SQL.</span><span class="sxs-lookup"><span data-stu-id="bac59-161">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="bac59-162">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bac59-162">-ResourceId</span></span>
<span data-ttu-id="bac59-163">Указывает идентификатор ресурса для восстановления.</span><span class="sxs-lookup"><span data-stu-id="bac59-163">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="bac59-164">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="bac59-164">-ServerName</span></span>
<span data-ttu-id="bac59-165">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="bac59-165">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="bac59-166">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="bac59-166">-ServiceObjectiveName</span></span>
<span data-ttu-id="bac59-167">Указывает имя цели обслуживания.</span><span class="sxs-lookup"><span data-stu-id="bac59-167">Specifies the name of the service objective.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bac59-168">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="bac59-168">-TargetDatabaseName</span></span>
<span data-ttu-id="bac59-169">Указывает имя базы данных, в которую будет восстановлено значение.</span><span class="sxs-lookup"><span data-stu-id="bac59-169">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="bac59-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac59-170">-DefaultProfile</span></span>
<span data-ttu-id="bac59-171">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bac59-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bac59-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac59-172">CommonParameters</span></span>
<span data-ttu-id="bac59-173">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bac59-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac59-174">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bac59-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac59-175">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bac59-175">INPUTS</span></span>

## <span data-ttu-id="bac59-176">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bac59-176">OUTPUTS</span></span>

### <span data-ttu-id="bac59-177">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="bac59-177">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="bac59-178">Пуск</span><span class="sxs-lookup"><span data-stu-id="bac59-178">NOTES</span></span>

## <span data-ttu-id="bac59-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bac59-179">RELATED LINKS</span></span>

[<span data-ttu-id="bac59-180">Восстановление базы данных SQL Azure из сбоя</span><span class="sxs-lookup"><span data-stu-id="bac59-180">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="bac59-181">Восстановление базы данных SQL Azure из пользовательской ошибки</span><span class="sxs-lookup"><span data-stu-id="bac59-181">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="bac59-182">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bac59-182">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="bac59-183">Get-AzureRMSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="bac59-183">Get-AzureRMSqlDatabaseGeoBackup</span></span>](./Get-AzureRMSqlDatabaseGeoBackup.md)

[<span data-ttu-id="bac59-184">Get-AzureRMSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="bac59-184">Get-AzureRMSqlDeletedDatabaseBackup</span></span>](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="bac59-185">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="bac59-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

