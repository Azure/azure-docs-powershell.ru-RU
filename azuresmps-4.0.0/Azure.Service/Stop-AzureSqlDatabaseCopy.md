---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076403"
---
# <span data-ttu-id="f83b9-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f83b9-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="f83b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f83b9-102">SYNOPSIS</span></span>
<span data-ttu-id="f83b9-103">Завершает отношение непрерывного копирования.</span><span class="sxs-lookup"><span data-stu-id="f83b9-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="f83b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f83b9-104">SYNTAX</span></span>

### <span data-ttu-id="f83b9-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f83b9-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f83b9-106">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="f83b9-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f83b9-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f83b9-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f83b9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f83b9-108">DESCRIPTION</span></span>
<span data-ttu-id="f83b9-109">Командлет **Stop-AzureSqlDatabaseCopy** завершает связь непрерывного копирования.</span><span class="sxs-lookup"><span data-stu-id="f83b9-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="f83b9-110">Этот командлет останавливает перемещение данных между исходной базой данных и дополнительной или целевой базой данных, а затем изменяет состояние базы данных-получателя на автономную базу данных в Интернете.</span><span class="sxs-lookup"><span data-stu-id="f83b9-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="f83b9-111">Существует два способа завершить отношение непрерывного копирования, прекращение или запланированное прекращение и принудительное прекращение с возможной потерей данных.</span><span class="sxs-lookup"><span data-stu-id="f83b9-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="f83b9-112">На сервере, на котором размещается исходная база данных, вы можете запустить этот командлет в режиме завершения или принудительного завершения.</span><span class="sxs-lookup"><span data-stu-id="f83b9-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="f83b9-113">На сервере, на котором размещается база данных получателя, необходимо использовать режим принудительного завершения.</span><span class="sxs-lookup"><span data-stu-id="f83b9-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="f83b9-114">Запланированное прекращение ожиданий до тех пор, пока все зафиксированные транзакции в исходной базе данных не будут реплицированы в базу данных-получатель после выполнения командлета.</span><span class="sxs-lookup"><span data-stu-id="f83b9-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="f83b9-115">Принудительное прекращение не ждет репликации всех незавершенных транзакций и может привести к потере данных в базе данных получателя.</span><span class="sxs-lookup"><span data-stu-id="f83b9-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="f83b9-116">Несмотря на то, что состояние репликации — ОЖИДАНИе, только принудительное завершение может успешно завершить связь непрерывного копирования.</span><span class="sxs-lookup"><span data-stu-id="f83b9-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="f83b9-117">Если состояние репликации — ОЖИДАНИе, оконечное значение, которое не было принудительно, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f83b9-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="f83b9-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f83b9-118">EXAMPLES</span></span>

### <span data-ttu-id="f83b9-119">Пример 1: прекращение связи непрерывной копии</span><span class="sxs-lookup"><span data-stu-id="f83b9-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="f83b9-120">Эта команда завершает связь непрерывной копии для базы данных "заказы" на сервере с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="f83b9-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="f83b9-121">Сервер с именем bk0b8kf658 размещает базу данных получателя.</span><span class="sxs-lookup"><span data-stu-id="f83b9-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="f83b9-122">Пример 2: принудительное прекращение связи непрерывной копии</span><span class="sxs-lookup"><span data-stu-id="f83b9-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="f83b9-123">Первая команда получает отношение копирования базы данных "заказы" на сервере с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="f83b9-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="f83b9-124">Вторая команда принудительно завершает связь непрерывной копии с сервера, на котором размещается база данных-получатель.</span><span class="sxs-lookup"><span data-stu-id="f83b9-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="f83b9-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f83b9-125">PARAMETERS</span></span>

### <span data-ttu-id="f83b9-126">-База данных</span><span class="sxs-lookup"><span data-stu-id="f83b9-126">-Database</span></span>
<span data-ttu-id="f83b9-127">Указывает объект, представляющий исходную базу данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f83b9-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="f83b9-128">Этот командлет завершает связь непрерывной копии базы данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f83b9-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f83b9-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f83b9-129">-DatabaseCopy</span></span>
<span data-ttu-id="f83b9-130">Указывает объект, представляющий базу данных.</span><span class="sxs-lookup"><span data-stu-id="f83b9-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="f83b9-131">Этот командлет завершает связь непрерывной копии базы данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f83b9-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="f83b9-132">Этот параметр принимает входные данные конвейера.</span><span class="sxs-lookup"><span data-stu-id="f83b9-132">This parameter accepts pipeline input.</span></span>

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f83b9-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f83b9-133">-DatabaseName</span></span>
<span data-ttu-id="f83b9-134">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="f83b9-134">Specifies the name of a database.</span></span>
<span data-ttu-id="f83b9-135">Этот командлет завершает связь непрерывной копии базы данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f83b9-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83b9-136">-Force</span><span class="sxs-lookup"><span data-stu-id="f83b9-136">-Force</span></span>
<span data-ttu-id="f83b9-137">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f83b9-137">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83b9-138">-ForcedTermination</span><span class="sxs-lookup"><span data-stu-id="f83b9-138">-ForcedTermination</span></span>
<span data-ttu-id="f83b9-139">Указывает на то, что этот командлет приводит к принудительному завершению связи непрерывного копирования.</span><span class="sxs-lookup"><span data-stu-id="f83b9-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="f83b9-140">Принудительное прекращение работы может привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="f83b9-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="f83b9-141">Чтобы выполнить этот командлет на сервере, на котором размещена целевая база данных, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f83b9-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="f83b9-142">Чтобы выполнить этот командлет на сервере, на котором размещается исходная база данных, необходимо указать этот параметр, если база данных-получатель недоступна.</span><span class="sxs-lookup"><span data-stu-id="f83b9-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83b9-143">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="f83b9-143">-PartnerDatabase</span></span>
<span data-ttu-id="f83b9-144">Указывает имя базы данных получателя.</span><span class="sxs-lookup"><span data-stu-id="f83b9-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="f83b9-145">Если указать имя, оно должно совпадать с именем исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="f83b9-145">If you specify a name, it must match the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83b9-146">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="f83b9-146">-PartnerServer</span></span>
<span data-ttu-id="f83b9-147">Указывает имя сервера, на котором размещена целевая база данных.</span><span class="sxs-lookup"><span data-stu-id="f83b9-147">Specifies the name of the server that hosts the target database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83b9-148">-Profile</span><span class="sxs-lookup"><span data-stu-id="f83b9-148">-Profile</span></span>
<span data-ttu-id="f83b9-149">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f83b9-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f83b9-150">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f83b9-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f83b9-151">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f83b9-151">-ServerName</span></span>
<span data-ttu-id="f83b9-152">Указывает имя сервера, на котором находится исходная база данных.</span><span class="sxs-lookup"><span data-stu-id="f83b9-152">Specifies the name of the server on which the source database resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f83b9-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f83b9-153">-Confirm</span></span>
<span data-ttu-id="f83b9-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f83b9-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83b9-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f83b9-155">-WhatIf</span></span>
<span data-ttu-id="f83b9-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f83b9-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f83b9-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f83b9-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83b9-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f83b9-158">CommonParameters</span></span>
<span data-ttu-id="f83b9-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f83b9-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f83b9-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f83b9-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f83b9-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f83b9-161">INPUTS</span></span>

### <span data-ttu-id="f83b9-162">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f83b9-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="f83b9-163">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="f83b9-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="f83b9-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f83b9-164">OUTPUTS</span></span>

### <span data-ttu-id="f83b9-165">Ничего</span><span class="sxs-lookup"><span data-stu-id="f83b9-165">None</span></span>

## <span data-ttu-id="f83b9-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="f83b9-166">NOTES</span></span>
* <span data-ttu-id="f83b9-167">Проверка подлинности: для этого командлета требуется проверка подлинности на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="f83b9-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="f83b9-168">Пример использования проверки подлинности на основе сертификатов для настройки текущей подписки можно найти в командлете **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="f83b9-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="f83b9-169">Ограничения: на сервере, на котором размещается база данных получателя, поддерживается только принудительное прекращение работы.</span><span class="sxs-lookup"><span data-stu-id="f83b9-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="f83b9-170">Последствия прекращения работы в бывшей базе данных получателя: после завершения работы база данных получателя становится независимой базой данных.</span><span class="sxs-lookup"><span data-stu-id="f83b9-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="f83b9-171">Если заполнение уже завершено в базе данных получателя, после того как вы откроете эту базу данных для получения полного доступа.</span><span class="sxs-lookup"><span data-stu-id="f83b9-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="f83b9-172">Если исходная база данных является базой данных для чтения и записи, она также становится базой данных для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f83b9-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="f83b9-173">Если в данный момент выполняется заполнение, инициализация будет прервана, а Предыдущая база данных не будет видна на сервере, на котором размещается база данных получателя.</span><span class="sxs-lookup"><span data-stu-id="f83b9-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="f83b9-174">Исходную базу данных можно выбрать в режиме "только для чтения".</span><span class="sxs-lookup"><span data-stu-id="f83b9-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="f83b9-175">Это гарантирует, что исходная и база данных синхронизируются после завершения и гарантирует, что транзакции не будут зафиксированы.</span><span class="sxs-lookup"><span data-stu-id="f83b9-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="f83b9-176">После завершения оконечного напряжения установите для источника обратно режим чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f83b9-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="f83b9-177">При необходимости вы также можете настроить для базы данных-получателя в режим чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f83b9-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="f83b9-178">Наблюдение: чтобы проверить состояние операций как в исходном, так и на целевом элементе отношения непрерывного копирования, используйте командлет **Get-AzureSqlDatabaseOperation** .</span><span class="sxs-lookup"><span data-stu-id="f83b9-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="f83b9-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f83b9-179">RELATED LINKS</span></span>

[<span data-ttu-id="f83b9-180">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="f83b9-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="f83b9-181">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="f83b9-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="f83b9-182">Остановить копирование базы данных</span><span class="sxs-lookup"><span data-stu-id="f83b9-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[<span data-ttu-id="f83b9-183">Командлеты базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="f83b9-183">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="f83b9-184">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f83b9-184">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="f83b9-185">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f83b9-185">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)


