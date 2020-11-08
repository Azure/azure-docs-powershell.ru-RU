---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075426"
---
# <span data-ttu-id="4e86c-101">Start-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="4e86c-101">Start-AzureSqlDatabaseRestore</span></span>

## <span data-ttu-id="4e86c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e86c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e86c-103">Выполняет восстановление базы данных на момент времени.</span><span class="sxs-lookup"><span data-stu-id="4e86c-103">Performs a point in time restore of a database.</span></span>

## <span data-ttu-id="4e86c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e86c-104">SYNTAX</span></span>

### <span data-ttu-id="4e86c-105">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="4e86c-105">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4e86c-106">BySourceRestorableDroppedDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="4e86c-106">BySourceRestorableDroppedDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4e86c-107">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e86c-107">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4e86c-108">BySourceRestorableDroppedDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e86c-108">BySourceRestorableDroppedDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4e86c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e86c-109">DESCRIPTION</span></span>
<span data-ttu-id="4e86c-110">Командлет **Start-AzureSqlDatabaseRestore** выполняет восстановление базовой, стандартной или расширенной базы данных на момент времени.</span><span class="sxs-lookup"><span data-stu-id="4e86c-110">The **Start-AzureSqlDatabaseRestore** cmdlet performs a point in time restore of a Basic, Standard or Premium database.</span></span>
<span data-ttu-id="4e86c-111">База данных Azure SQL сохраняет основные резервные копии базы данных 7 дней, Standard в течение 14 дней и Premium в течение 35 дней.</span><span class="sxs-lookup"><span data-stu-id="4e86c-111">Azure SQL Database retains Basic database backups 7 days, Standard for 14 days, and Premium for 35 days.</span></span>
<span data-ttu-id="4e86c-112">Операция восстановления создает новую базу данных.</span><span class="sxs-lookup"><span data-stu-id="4e86c-112">The restore operation creates a new database.</span></span>
<span data-ttu-id="4e86c-113">Если исходная база данных не удалена, параметр *SourceDatabaseName* и *TargetDatabaseName* должен иметь разные значения.</span><span class="sxs-lookup"><span data-stu-id="4e86c-113">If the source database is not deleted, the *SourceDatabaseName* and *TargetDatabaseName* parameter must have different values.</span></span>

<span data-ttu-id="4e86c-114">База данных SQL Azure в настоящее время не поддерживает восстановление на нескольких серверах.</span><span class="sxs-lookup"><span data-stu-id="4e86c-114">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="4e86c-115">Имена исходного и целевого серверов должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="4e86c-115">The source and target server names must be the same.</span></span>

## <span data-ttu-id="4e86c-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e86c-116">EXAMPLES</span></span>

### <span data-ttu-id="4e86c-117">Пример 1: восстановление базы данных, указанной как объект, на определенный момент времени</span><span class="sxs-lookup"><span data-stu-id="4e86c-117">Example 1: Restore a database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="4e86c-118">Первая команда получает объект базы данных с именем Database17 на сервере с именем Server01 и сохраняет его в переменной $Database.</span><span class="sxs-lookup"><span data-stu-id="4e86c-118">The first command gets a database object for the database named Database17 on the server named Server01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="4e86c-119">Вторая команда восстанавливает базу данных в определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="4e86c-119">The second command restores the database to a specific point in time.</span></span>
<span data-ttu-id="4e86c-120">Команда задает имя для новой базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e86c-120">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="4e86c-121">Пример 2: восстановление базы данных, указанной по имени, на определенный момент времени</span><span class="sxs-lookup"><span data-stu-id="4e86c-121">Example 2: Restore a database specified by name to a point in time</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="4e86c-122">Эта команда восстанавливает базу данных с именем Database17 на определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="4e86c-122">This command restores the database named Database17 to a specific point in time.</span></span>
<span data-ttu-id="4e86c-123">Команда задает имя для новой базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e86c-123">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="4e86c-124">Пример 3: восстановление удаленной базы данных, указанной в качестве объекта, на определенный момент времени</span><span class="sxs-lookup"><span data-stu-id="4e86c-124">Example 3: Restore a dropped database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

<span data-ttu-id="4e86c-125">Первая команда получает объект базы данных с именем Database01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="4e86c-125">The first command gets a database object for the database named Database01 on the server named Server01.</span></span>
<span data-ttu-id="4e86c-126">Команда задает параметр *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="4e86c-126">The command specifies the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="4e86c-127">Таким образом, командлет возвращает restorable удаленную базу данных с указанной точкой восстановления.</span><span class="sxs-lookup"><span data-stu-id="4e86c-127">Therefore, the cmdlet gets restorable dropped database the specified restore point.</span></span>
<span data-ttu-id="4e86c-128">Команда сохраняет этот объект базы данных в переменной $Database.</span><span class="sxs-lookup"><span data-stu-id="4e86c-128">The command stores that database object in the $Database variable.</span></span>

<span data-ttu-id="4e86c-129">Вторая команда восстанавливает удаленную базу данных, указанную в $Database.</span><span class="sxs-lookup"><span data-stu-id="4e86c-129">The second command restores the dropped database specified by $Database.</span></span>
<span data-ttu-id="4e86c-130">Команда задает имя для новой базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e86c-130">The command specifies at name for the new database.</span></span>

## <span data-ttu-id="4e86c-131">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e86c-131">PARAMETERS</span></span>

### <span data-ttu-id="4e86c-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="4e86c-132">-PointInTime</span></span>
<span data-ttu-id="4e86c-133">Указывает точку восстановления, в которую нужно восстановить базу данных.</span><span class="sxs-lookup"><span data-stu-id="4e86c-133">Specifies the restore point to which to restore the database.</span></span>
<span data-ttu-id="4e86c-134">По завершении операции восстановления база данных восстанавливается в состояние, которое оно указывает на дату и время, указанные этим параметром.</span><span class="sxs-lookup"><span data-stu-id="4e86c-134">When the restore operation finishes, the database is restored to the state it was at the date and time that this parameter specifies.</span></span>
<span data-ttu-id="4e86c-135">По умолчанию для реальной базы данных этот параметр установлен на текущее время, а для удаленной базы данных этот командлет использует время удаления базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e86c-135">By default, for a live database this set to the current time, and for a dropped database, this cmdlet uses the time when the database was dropped.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e86c-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="4e86c-136">-Profile</span></span>
<span data-ttu-id="4e86c-137">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4e86c-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4e86c-138">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4e86c-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e86c-139">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="4e86c-139">-RestorableDropped</span></span>
<span data-ttu-id="4e86c-140">Указывает на то, что этот командлет восстанавливает удаленную базу данных restorable.</span><span class="sxs-lookup"><span data-stu-id="4e86c-140">Indicates that this cmdlet restores a restorable dropped database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e86c-141">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="4e86c-141">-SourceDatabase</span></span>
<span data-ttu-id="4e86c-142">Указывает имя базы данных, которая восстанавливается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4e86c-142">Specifies the name of the database that this cmdlet restores.</span></span>

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e86c-143">-SourceDatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="4e86c-143">-SourceDatabaseDeletionDate</span></span>
<span data-ttu-id="4e86c-144">Указывает дату и время удаления базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e86c-144">Specifies the date and time when the database was deleted.</span></span>
<span data-ttu-id="4e86c-145">Если указать время, совпадающее с фактическим временем удаления базы данных, необходимо включить миллисекунды.</span><span class="sxs-lookup"><span data-stu-id="4e86c-145">You must include milliseconds when you specify the time to match the actual database deletion time.</span></span>

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e86c-146">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e86c-146">-SourceDatabaseName</span></span>
<span data-ttu-id="4e86c-147">Указывает имя базы данных Live, которое восстанавливается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4e86c-147">Specifies the name of the live database that this cmdlet restores.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e86c-148">-SourceRestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="4e86c-148">-SourceRestorableDroppedDatabase</span></span>
<span data-ttu-id="4e86c-149">Указывает объект, представляющий restorable удаленную базу данных, которая восстанавливается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4e86c-149">Specifies an object that represents the restorable dropped database that this cmdlet restores.</span></span>
<span data-ttu-id="4e86c-150">Чтобы получить объект **RestorableDroppedDatabase** , используйте командлет Get-AzureSqlDatabase и укажите параметр *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="4e86c-150">To obtain a **RestorableDroppedDatabase** object, use the Get-AzureSqlDatabase cmdlet, and specify the *RestorableDropped* parameter.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e86c-151">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="4e86c-151">-SourceServerName</span></span>
<span data-ttu-id="4e86c-152">Указывает имя сервера, на котором находится база данных источника и что она запущена, или на которой была выполнена удаленная база данных.</span><span class="sxs-lookup"><span data-stu-id="4e86c-152">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e86c-153">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e86c-153">-TargetDatabaseName</span></span>
<span data-ttu-id="4e86c-154">Указывает имя новой базы данных, созданной операцией восстановления.</span><span class="sxs-lookup"><span data-stu-id="4e86c-154">Specifies the name of the new database that the restore operation creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e86c-155">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="4e86c-155">-TargetServerName</span></span>
<span data-ttu-id="4e86c-156">Указывает имя сервера, на который этот командлет восстанавливает базу данных.</span><span class="sxs-lookup"><span data-stu-id="4e86c-156">Specifies the name of the server to which this cmdlet restores the database.</span></span>

<span data-ttu-id="4e86c-157">База данных SQL Azure в настоящее время не поддерживает восстановление на нескольких серверах.</span><span class="sxs-lookup"><span data-stu-id="4e86c-157">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="4e86c-158">Имена исходного и целевого серверов должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="4e86c-158">The source and target server names must be the same.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e86c-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e86c-159">CommonParameters</span></span>
<span data-ttu-id="4e86c-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e86c-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e86c-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e86c-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e86c-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e86c-162">INPUTS</span></span>

### <span data-ttu-id="4e86c-163">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="4e86c-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

### <span data-ttu-id="4e86c-164">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="4e86c-164">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="4e86c-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e86c-165">OUTPUTS</span></span>

### <span data-ttu-id="4e86c-166">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. RestoreDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="4e86c-166">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestoreDatabaseOperation</span></span>

## <span data-ttu-id="4e86c-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e86c-167">NOTES</span></span>
* <span data-ttu-id="4e86c-168">Для запуска этого командлета необходимо использовать проверку подлинности на основе сертификатов.</span><span class="sxs-lookup"><span data-stu-id="4e86c-168">You must use certificate based authentication to run this cmdlet.</span></span> <span data-ttu-id="4e86c-169">На компьютере, на котором запускается этот командлет, выполните следующие команды:</span><span class="sxs-lookup"><span data-stu-id="4e86c-169">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="4e86c-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e86c-170">RELATED LINKS</span></span>

[<span data-ttu-id="4e86c-171">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="4e86c-171">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="4e86c-172">Создание запроса на восстановление базы данных</span><span class="sxs-lookup"><span data-stu-id="4e86c-172">Create Database Restore Request</span></span>](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[<span data-ttu-id="4e86c-173">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="4e86c-173">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="4e86c-174">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4e86c-174">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)


