---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076298"
---
# <span data-ttu-id="73370-101">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="73370-101">Get-AzureSqlDatabase</span></span>

## <span data-ttu-id="73370-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73370-102">SYNOPSIS</span></span>
<span data-ttu-id="73370-103">Извлекает одну или несколько баз данных.</span><span class="sxs-lookup"><span data-stu-id="73370-103">Retrieves one or more databases.</span></span>

## <span data-ttu-id="73370-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73370-104">SYNTAX</span></span>

### <span data-ttu-id="73370-105">ByConnectionContext (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73370-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="73370-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="73370-106">ByServerName</span></span>
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="73370-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73370-107">DESCRIPTION</span></span>
<span data-ttu-id="73370-108">Командлет **Get-AzureSqlDatabase** получает один или несколько экземпляров базы данных Azure SQL с сервера базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="73370-108">The **Get-AzureSqlDatabase** cmdlet retrieves one or more instances of an Azure SQL Database from an Azure SQL Database server.</span></span>
<span data-ttu-id="73370-109">Вы можете указать сервер с контекстом подключения к серверу базы данных SQL Azure, который вы создаете с помощью командлета **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="73370-109">You can specify the server with an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="73370-110">Или, если указать имя сервера базы данных SQL Azure, командлет использует текущие сведения о подписке Azure для проверки подлинности запроса на доступ к серверу.</span><span class="sxs-lookup"><span data-stu-id="73370-110">Or, if you specify the Azure SQL Database server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="73370-111">Если не указать базу данных, командлет **Get-AzureSqlDatabase** возвращает все базы данных с указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="73370-111">If you do not specify a database, the **Get-AzureSqlDatabase** cmdlet returns all databases from the specified server.</span></span>

<span data-ttu-id="73370-112">Получение restorable удаленных баз данных:</span><span class="sxs-lookup"><span data-stu-id="73370-112">Retrieving restorable dropped databases:</span></span>

<span data-ttu-id="73370-113">Извлечение restorable удаленных баз данных с помощью параметра *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="73370-113">Retrieve restorable dropped databases by using the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="73370-114">Для возврата всех restorable удаленных баз данных используйте параметр *RestorableDropped* без *DatabaseName* и *DatabaseDeletionDate*.</span><span class="sxs-lookup"><span data-stu-id="73370-114">To return all restorable dropped databases use the *RestorableDropped* parameter without *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="73370-115">Чтобы вернуть определенную restorable удаленную базу данных, используйте параметр *RestorableDropped* с параметрами *DatabaseName* и *DatabaseDeletionDate* .</span><span class="sxs-lookup"><span data-stu-id="73370-115">To return a specific restorable dropped database use the *RestorableDropped* parameter with the *DatabaseName* and *DatabaseDeletionDate* parameters.</span></span>
<span data-ttu-id="73370-116">При извлечении определенной restorable удаленной базы данных с помощью параметра *DatabaseName* необходимо также указать параметр *DatabaseDeletionDate* , а указанное значение *DatabaseDeletionDate* должно содержать миллисекунды для соответствия необходимой базе данных.</span><span class="sxs-lookup"><span data-stu-id="73370-116">When retrieving a specific restorable dropped database by using the *DatabaseName* parameter you must also include the *DatabaseDeletionDate* parameter and the specified *DatabaseDeletionDate* value must include milliseconds to match the desired database.</span></span>

<span data-ttu-id="73370-117">Командлет **Get-AzureSqlDatabase** возвращает либо все restorable удаленные базы данных на сервере, либо определенную базу данных, которая соответствует обоим параметрам *DatabaseName* и *DatabaseDeletionDate*.</span><span class="sxs-lookup"><span data-stu-id="73370-117">The **Get-AzureSqlDatabase** cmdlet returns either all restorable dropped databases on a server, or one specific database that matches both *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="73370-118">Для возврата restorable удаленным базам данных, которые удовлетворяют разным критериям, таким как все restorable удаленные базы данных с определенным именем, нужно вернуть все restorable удаленные базы данных, а затем отфильтровать результаты на клиенте.</span><span class="sxs-lookup"><span data-stu-id="73370-118">To return restorable dropped databases that satisfy different criteria, such as all restorable dropped databases of a specific name, you must return all restorable dropped databases, and then filter the results on the client.</span></span>

## <span data-ttu-id="73370-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73370-119">EXAMPLES</span></span>

### <span data-ttu-id="73370-120">Пример 1: получение всех баз данных на сервере</span><span class="sxs-lookup"><span data-stu-id="73370-120">Example 1: Retrieve all databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="73370-121">Эта команда извлекает все базы данных на сервере с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="73370-121">This command retrieves all databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="73370-122">Пример 2: получение всех удаленных баз данных restorable на сервере</span><span class="sxs-lookup"><span data-stu-id="73370-122">Example 2: Retrieve all restorable dropped databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

<span data-ttu-id="73370-123">Эта команда извлекает все удаленные базы данных restorable на сервере с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="73370-123">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="73370-124">Пример 3: получение базы данных с сервера, указанного контекстом подключения</span><span class="sxs-lookup"><span data-stu-id="73370-124">Example 3: Retrieve a database from a server specified by a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="73370-125">Эта команда извлекает базу данных с именем Database01 с сервера, указанного контекстом подключения $Context.</span><span class="sxs-lookup"><span data-stu-id="73370-125">This command retrieves database named Database01 from the server specified by the connection context $Context.</span></span>

### <span data-ttu-id="73370-126">Пример 4: сохранение объекта базы данных в переменной</span><span class="sxs-lookup"><span data-stu-id="73370-126">Example 4: Store a database object in a variable</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="73370-127">Эта команда извлекает базу данных с именем Database01 с сервера с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="73370-127">This command retrieves database named Database01 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="73370-128">Объект базы данных сохраняется в переменной $Database 01.</span><span class="sxs-lookup"><span data-stu-id="73370-128">The command stores the database object in the $Database01 variable.</span></span>

### <span data-ttu-id="73370-129">Пример 5: получение restorable удаленной базы данных</span><span class="sxs-lookup"><span data-stu-id="73370-129">Example 5: Retrieve a restorable dropped database</span></span>
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

<span data-ttu-id="73370-130">Эта команда извлекает restorable удаленную базу данных с именем Database01, которая была удалена на 11/9/2012 с сервера с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="73370-130">This command retrieves the restorable dropped database named Database01 that was deleted on 11/9/2012 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="73370-131">Эта команда сохраняет результаты в переменной $DroppedDB.</span><span class="sxs-lookup"><span data-stu-id="73370-131">This command stores the results in the $DroppedDB variable.</span></span>

### <span data-ttu-id="73370-132">Пример 6: получение всех restorable удаленных баз данных на сервере и фильтрация результатов</span><span class="sxs-lookup"><span data-stu-id="73370-132">Example 6: Retrieve all restorable dropped databases on a server and filter the results</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

<span data-ttu-id="73370-133">Эта команда извлекает все удаленные базы данных restorable на сервере с именем lpqd0zbr8y, а затем фильтрует результаты только для баз данных с именем ContactDB.</span><span class="sxs-lookup"><span data-stu-id="73370-133">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y, and then filters the results to only the databases named ContactDB.</span></span>

## <span data-ttu-id="73370-134">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73370-134">PARAMETERS</span></span>

### <span data-ttu-id="73370-135">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="73370-135">-ConnectionContext</span></span>
<span data-ttu-id="73370-136">Указывает контекст подключения сервера, с которого требуется получить базу данных.</span><span class="sxs-lookup"><span data-stu-id="73370-136">Specifies the connection context of a server from which to retrieve a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73370-137">-База данных</span><span class="sxs-lookup"><span data-stu-id="73370-137">-Database</span></span>
<span data-ttu-id="73370-138">Указывает объект, представляющий базу данных, которую этот командлет извлекает.</span><span class="sxs-lookup"><span data-stu-id="73370-138">Specifies an object that represents the database that this cmdlet retrieves.</span></span>

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73370-139">-DatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="73370-139">-DatabaseDeletionDate</span></span>
<span data-ttu-id="73370-140">Указывает дату и время удаления.</span><span class="sxs-lookup"><span data-stu-id="73370-140">Specifies the date and time of a deletion.</span></span>
<span data-ttu-id="73370-141">Если указан параметр *RestorableDropped* , укажите этот параметр, чтобы получить restorable удаленную базу данных, исходя из даты и времени удаления.</span><span class="sxs-lookup"><span data-stu-id="73370-141">If you specify the *RestorableDropped* parameter, specify this parameter to retrieve a restorable dropped database based on the deletion date and time.</span></span>

<span data-ttu-id="73370-142">Параметр *DatabaseDeletionDate* должен содержать миллисекунды в соответствии со временем нужной базы данных.</span><span class="sxs-lookup"><span data-stu-id="73370-142">The *DatabaseDeletionDate* parameter must include milliseconds to match the time of the desired database.</span></span>
<span data-ttu-id="73370-143">Если задать значение без миллисекунд, база данных не будет найдена.</span><span class="sxs-lookup"><span data-stu-id="73370-143">Specifying a value without milliseconds results in the database not being found.</span></span>

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

### <span data-ttu-id="73370-144">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="73370-144">-DatabaseName</span></span>
<span data-ttu-id="73370-145">Указывает имя базы данных, которую этот командлет извлекает.</span><span class="sxs-lookup"><span data-stu-id="73370-145">Specifies the name of the database that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="73370-146">-Profile</span><span class="sxs-lookup"><span data-stu-id="73370-146">-Profile</span></span>
<span data-ttu-id="73370-147">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="73370-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="73370-148">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="73370-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="73370-149">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="73370-149">-RestorableDropped</span></span>
<span data-ttu-id="73370-150">Указывает на то, что этот командлет возвращает объекты *RestorableDroppedDatabase* , а не объекты *базы данных* .</span><span class="sxs-lookup"><span data-stu-id="73370-150">Indicates that this cmdlet returns *RestorableDroppedDatabase* objects instead of *Database* objects.</span></span>
<span data-ttu-id="73370-151">Вы можете использовать параметр *DatabaseDeletionDate* , чтобы выбрать определенную restorable удаленную базу данных.</span><span class="sxs-lookup"><span data-stu-id="73370-151">You can use the *DatabaseDeletionDate* parameter to select a specific restorable dropped database.</span></span>

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

### <span data-ttu-id="73370-152">-RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="73370-152">-RestorableDroppedDatabase</span></span>
<span data-ttu-id="73370-153">Указывает объект, представляющий restorable удаленную базу данных, которую этот командлет извлекает.</span><span class="sxs-lookup"><span data-stu-id="73370-153">Specifies an object that represents the restorable dropped database that this cmdlet retrieves.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73370-154">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="73370-154">-ServerName</span></span>
<span data-ttu-id="73370-155">Указывает имя сервера, содержащего базу данных, которую этот командлет извлекает.</span><span class="sxs-lookup"><span data-stu-id="73370-155">Specifies the name of the server that contains the database that this cmdlet retrieves.</span></span>
<span data-ttu-id="73370-156">Командлет использует текущую подписку Azure для доступа к серверу.</span><span class="sxs-lookup"><span data-stu-id="73370-156">The cmdlet uses the current Azure subscription to access the server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73370-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73370-157">CommonParameters</span></span>
<span data-ttu-id="73370-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73370-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73370-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73370-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73370-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73370-160">INPUTS</span></span>

### <span data-ttu-id="73370-161">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="73370-161">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="73370-162">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="73370-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

## <span data-ttu-id="73370-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73370-163">OUTPUTS</span></span>

### <span data-ttu-id="73370-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span><span class="sxs-lookup"><span data-stu-id="73370-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span></span>
<span data-ttu-id="73370-165">Этот командлет возвращает объект *базы данных* , если не указан параметр *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="73370-165">This cmdlet returns a *Database* object if you do not specify the *RestorableDropped* parameter.</span></span>

### <span data-ttu-id="73370-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span><span class="sxs-lookup"><span data-stu-id="73370-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span></span>
<span data-ttu-id="73370-167">Этот командлет возвращает объект *RestorableDroppedDatabase* , если указан параметр *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="73370-167">This cmdlet returns a *RestorableDroppedDatabase* object if you specify the *RestorableDropped* parameter.</span></span>

## <span data-ttu-id="73370-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="73370-168">NOTES</span></span>

## <span data-ttu-id="73370-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73370-169">RELATED LINKS</span></span>

[<span data-ttu-id="73370-170">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="73370-170">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="73370-171">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="73370-171">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="73370-172">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="73370-172">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="73370-173">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="73370-173">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="73370-174">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="73370-174">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="73370-175">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="73370-175">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


