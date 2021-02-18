---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7716587787515221a6e016436a6e3d030c1ab0eb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405624"
---
# <span data-ttu-id="47cae-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="47cae-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="47cae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47cae-102">SYNOPSIS</span></span>
<span data-ttu-id="47cae-103">Прерывает непрерывное копирование.</span><span class="sxs-lookup"><span data-stu-id="47cae-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="47cae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="47cae-104">SYNTAX</span></span>

### <span data-ttu-id="47cae-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="47cae-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47cae-106">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="47cae-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47cae-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="47cae-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47cae-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47cae-108">DESCRIPTION</span></span>
<span data-ttu-id="47cae-109">**Cmdlet Stop-AzureSqlDataCopy** завершает непрерывное копирование.</span><span class="sxs-lookup"><span data-stu-id="47cae-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="47cae-110">Этот cmdlet останавливает перемещение данных между конечной и вторичной или целевой базой данных, а затем меняет состояние вторичной базы данных на отдельное сетевое.</span><span class="sxs-lookup"><span data-stu-id="47cae-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="47cae-111">Существует два способа прекращения непрерывной связи, прекращения или запланированного прекращения действия и принудительных расторжения отношений в связи с возможной потерей данных.</span><span class="sxs-lookup"><span data-stu-id="47cae-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="47cae-112">На сервере, на котором размещена базовая база данных, этот cmdlet можно запустить в режиме расторжения или принудительных расторжения.</span><span class="sxs-lookup"><span data-stu-id="47cae-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="47cae-113">На сервере, на котором размещена вторичная база данных, необходимо использовать режим принудительного прекращения действия.</span><span class="sxs-lookup"><span data-stu-id="47cae-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="47cae-114">Запланированное завершение будет реплицировано во вторичную базу данных до тех пор, пока все все транзакции, запланированные в базе данных, на момент запуска этого cmdlet не будут реплицированы во вторичную базу данных.</span><span class="sxs-lookup"><span data-stu-id="47cae-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="47cae-115">Принудительный расторжение не ждет репликации всех оставшиеся транзакций и может привести к потере данных во вторичной базе данных.</span><span class="sxs-lookup"><span data-stu-id="47cae-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="47cae-116">Во время ожидания состояния репликации только принудительное прекращение связи может привести к завершению непрерывной копии.</span><span class="sxs-lookup"><span data-stu-id="47cae-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="47cae-117">Если ожидается статус репликации, расторжение, которое не является принудительным, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="47cae-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="47cae-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="47cae-118">EXAMPLES</span></span>

### <span data-ttu-id="47cae-119">Пример 1. Прекращение непрерывной связи копирования</span><span class="sxs-lookup"><span data-stu-id="47cae-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="47cae-120">Эта команда прерывает непрерывное копирование базы данных "Заказы" на сервере lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="47cae-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="47cae-121">На сервере bk0b8kf658 размещена вторичная база данных.</span><span class="sxs-lookup"><span data-stu-id="47cae-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="47cae-122">Пример 2. Прекращение связи непрерывной копии</span><span class="sxs-lookup"><span data-stu-id="47cae-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="47cae-123">Первая команда получает отношение копирования базы данных с именем Orders на сервере lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="47cae-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="47cae-124">Вторая команда прерывает связь непрерывной копии с сервера, на котором размещена вторичная база данных.</span><span class="sxs-lookup"><span data-stu-id="47cae-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="47cae-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47cae-125">PARAMETERS</span></span>

### <span data-ttu-id="47cae-126">-Database</span><span class="sxs-lookup"><span data-stu-id="47cae-126">-Database</span></span>
<span data-ttu-id="47cae-127">Определяет объект, который представляет исходный источник базы SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="47cae-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="47cae-128">Этот cmdlet завершает непрерывное копирование базы данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="47cae-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="47cae-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="47cae-129">-DatabaseCopy</span></span>
<span data-ttu-id="47cae-130">Определяет объект, который представляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="47cae-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="47cae-131">Этот cmdlet завершает непрерывное копирование базы данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="47cae-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="47cae-132">Этот параметр принимает входные данные конвейера.</span><span class="sxs-lookup"><span data-stu-id="47cae-132">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="47cae-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="47cae-133">-DatabaseName</span></span>
<span data-ttu-id="47cae-134">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="47cae-134">Specifies the name of a database.</span></span>
<span data-ttu-id="47cae-135">Этот cmdlet завершает непрерывное копирование базы данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="47cae-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="47cae-136">-Force</span><span class="sxs-lookup"><span data-stu-id="47cae-136">-Force</span></span>
<span data-ttu-id="47cae-137">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="47cae-137">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="47cae-138">-ForcedTermination</span><span class="sxs-lookup"><span data-stu-id="47cae-138">-ForcedTermination</span></span>
<span data-ttu-id="47cae-139">Указывает на то, что этот cmdlet приводит к принудительному прекращению отношения непрерывной копии.</span><span class="sxs-lookup"><span data-stu-id="47cae-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="47cae-140">Принудительный выход из компании может привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="47cae-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="47cae-141">Чтобы выполнить этот cmdlet на сервере, на котором размещена целевая база данных, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="47cae-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="47cae-142">Чтобы выполнить этот cmdlet на сервере, на котором размещена базовая база данных, если она недоступна, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="47cae-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

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

### <span data-ttu-id="47cae-143">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="47cae-143">-PartnerDatabase</span></span>
<span data-ttu-id="47cae-144">Указывает имя вторичной базы данных.</span><span class="sxs-lookup"><span data-stu-id="47cae-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="47cae-145">Если указать имя, оно должно совпадать с именем в базе данных.</span><span class="sxs-lookup"><span data-stu-id="47cae-145">If you specify a name, it must match the name of the source database.</span></span>

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

### <span data-ttu-id="47cae-146">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="47cae-146">-PartnerServer</span></span>
<span data-ttu-id="47cae-147">Имя сервера, на котором размещена целевая база данных.</span><span class="sxs-lookup"><span data-stu-id="47cae-147">Specifies the name of the server that hosts the target database.</span></span>

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

### <span data-ttu-id="47cae-148">-Profile</span><span class="sxs-lookup"><span data-stu-id="47cae-148">-Profile</span></span>
<span data-ttu-id="47cae-149">Определяет профиль Azure, для которого читается этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47cae-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="47cae-150">Если не указать профиль, этот cmdlet будет читать данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="47cae-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="47cae-151">-ServerName</span><span class="sxs-lookup"><span data-stu-id="47cae-151">-ServerName</span></span>
<span data-ttu-id="47cae-152">Указывает имя сервера, на котором находится базовая база данных.</span><span class="sxs-lookup"><span data-stu-id="47cae-152">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="47cae-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47cae-153">-Confirm</span></span>
<span data-ttu-id="47cae-154">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="47cae-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47cae-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47cae-155">-WhatIf</span></span>
<span data-ttu-id="47cae-156">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47cae-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47cae-157">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="47cae-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47cae-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47cae-158">CommonParameters</span></span>
<span data-ttu-id="47cae-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47cae-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47cae-160">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47cae-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47cae-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47cae-161">INPUTS</span></span>

### <span data-ttu-id="47cae-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="47cae-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="47cae-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="47cae-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="47cae-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47cae-164">OUTPUTS</span></span>

### <span data-ttu-id="47cae-165">Нет</span><span class="sxs-lookup"><span data-stu-id="47cae-165">None</span></span>

## <span data-ttu-id="47cae-166">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="47cae-166">NOTES</span></span>
* <span data-ttu-id="47cae-167">Проверка подлинности: этот cmdlet требует проверки подлинности на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="47cae-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="47cae-168">Пример использования проверки подлинности на основе сертификата для проверки текущей подписки см. в cmdlet **New-AzureSqlDatabaseServerContext.**</span><span class="sxs-lookup"><span data-stu-id="47cae-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="47cae-169">Ограничения: на сервере, на котором размещена вторичная база данных, поддерживается только принудительный выход из системы.</span><span class="sxs-lookup"><span data-stu-id="47cae-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="47cae-170">Влияние прекращения действия на бывшего вторичную базу данных: после прекращения работы она становится независимой базой данных.</span><span class="sxs-lookup"><span data-stu-id="47cae-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="47cae-171">Если заполнение уже выполнено во вторичной базе данных, после завершения этой базы данных она будет открыта для полного доступа.</span><span class="sxs-lookup"><span data-stu-id="47cae-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="47cae-172">Если она является базой данных для чтения и записи, бывшая вторичная база данных тоже становится доступной для чтения.</span><span class="sxs-lookup"><span data-stu-id="47cae-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="47cae-173">Если в данный момент происходит начальное значение, начальное значение будет прервано, а бывшего дополнительного база данных никогда не будет видно на сервере, на котором размещена эта база данных.</span><span class="sxs-lookup"><span data-stu-id="47cae-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="47cae-174">Вы можете настроить режим только для чтения в базе данных.</span><span class="sxs-lookup"><span data-stu-id="47cae-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="47cae-175">Это гарантирует синхронизацию исходных и дополнительных баз данных после расторжения соглашения, а также гарантирует, что во время расторжения соглашения не будут совершены никакие транзакции.</span><span class="sxs-lookup"><span data-stu-id="47cae-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="47cae-176">По окончании срока действия перенастройте источник в режим чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="47cae-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="47cae-177">При желании можно также настроить режим записи бывшего вторичная база данных.</span><span class="sxs-lookup"><span data-stu-id="47cae-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="47cae-178">Мониторинг: чтобы проверить состояние операций как в источнике, так и в целевом объекте связи непрерывной копии, используйте cmdlet **Get-AzureSqlDataBaseOperation.**</span><span class="sxs-lookup"><span data-stu-id="47cae-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="47cae-179">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47cae-179">RELATED LINKS</span></span>

[<span data-ttu-id="47cae-180">База SQL Azure</span><span class="sxs-lookup"><span data-stu-id="47cae-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="47cae-181">Операции для баз данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="47cae-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="47cae-182">Остановка копирования базы данных</span><span class="sxs-lookup"><span data-stu-id="47cae-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)



[<span data-ttu-id="47cae-183">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="47cae-183">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="47cae-184">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="47cae-184">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)


