---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076295"
---
# <span data-ttu-id="65f11-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="65f11-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="65f11-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65f11-102">SYNOPSIS</span></span>
<span data-ttu-id="65f11-103">Проверка состояния связей при копировании.</span><span class="sxs-lookup"><span data-stu-id="65f11-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="65f11-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65f11-104">SYNTAX</span></span>

### <span data-ttu-id="65f11-105">ByServerNameOnly (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="65f11-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="65f11-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="65f11-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="65f11-107">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="65f11-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="65f11-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65f11-108">DESCRIPTION</span></span>
<span data-ttu-id="65f11-109">Командлет **Get-AzureSqlDatabaseCopy** проверяет состояние одного или нескольких активных связей копий.</span><span class="sxs-lookup"><span data-stu-id="65f11-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="65f11-110">Запустите этот командлет после запуска командлета Start-AzureSqlDatabaseCopy или Stop-AzureSqlDatabaseCopy.</span><span class="sxs-lookup"><span data-stu-id="65f11-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="65f11-111">Вы можете проверить связь с определенным копированием, все связи копий или отфильтрованный список связей копий, например все копии на конкретном целевом сервере.</span><span class="sxs-lookup"><span data-stu-id="65f11-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="65f11-112">Этот командлет можно выполнить на сервере, на котором размещается исходная или целевая база данных.</span><span class="sxs-lookup"><span data-stu-id="65f11-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="65f11-113">Этот командлет является синхронным.</span><span class="sxs-lookup"><span data-stu-id="65f11-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="65f11-114">Командлет блокирует консоль Azure PowerShell, пока не вернет объект Status.</span><span class="sxs-lookup"><span data-stu-id="65f11-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="65f11-115">Параметры *PartnerServer* и *PartnerDatabase* являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="65f11-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="65f11-116">Если не указать ни один из этих параметров, этот командлет возвращает таблицу результатов.</span><span class="sxs-lookup"><span data-stu-id="65f11-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="65f11-117">Чтобы просмотреть состояние только для определенной базы данных, укажите оба параметра.</span><span class="sxs-lookup"><span data-stu-id="65f11-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="65f11-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65f11-118">EXAMPLES</span></span>

### <span data-ttu-id="65f11-119">Пример 1: получение состояния копии базы данных</span><span class="sxs-lookup"><span data-stu-id="65f11-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="65f11-120">Эта команда получает состояние базы данных "заказы" на сервере с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="65f11-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="65f11-121">Параметр *PartnerServer* ограничивает эту команду на сервер bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="65f11-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="65f11-122">Пример 2: получение состояния всех копий на serverGet состояние всех копий на сервере</span><span class="sxs-lookup"><span data-stu-id="65f11-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="65f11-123">Эта команда возвращает состояние всех активных копий на сервере с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="65f11-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="65f11-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65f11-124">PARAMETERS</span></span>

### <span data-ttu-id="65f11-125">-База данных</span><span class="sxs-lookup"><span data-stu-id="65f11-125">-Database</span></span>
<span data-ttu-id="65f11-126">Указывает объект, представляющий исходную базу данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="65f11-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="65f11-127">Этот командлет получает состояние копирования базы данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="65f11-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="65f11-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="65f11-128">-DatabaseCopy</span></span>
<span data-ttu-id="65f11-129">Указывает объект, представляющий базу данных.</span><span class="sxs-lookup"><span data-stu-id="65f11-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="65f11-130">Этот командлет получает состояние копирования базы данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="65f11-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="65f11-131">Этот параметр принимает входные данные конвейера.</span><span class="sxs-lookup"><span data-stu-id="65f11-131">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="65f11-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="65f11-132">-DatabaseName</span></span>
<span data-ttu-id="65f11-133">Указывает имя исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="65f11-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="65f11-134">Этот командлет получает состояние копии базы данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="65f11-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65f11-135">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="65f11-135">-PartnerDatabase</span></span>
<span data-ttu-id="65f11-136">Указывает имя базы данных получателя.</span><span class="sxs-lookup"><span data-stu-id="65f11-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="65f11-137">Если эта база данных не найдена в динамическом административном представлении sys.dm_database_copies, этот командлет возвращает пустой объект Status.</span><span class="sxs-lookup"><span data-stu-id="65f11-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65f11-138">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="65f11-138">-PartnerServer</span></span>
<span data-ttu-id="65f11-139">Указывает имя сервера, на котором размещена целевая база данных.</span><span class="sxs-lookup"><span data-stu-id="65f11-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="65f11-140">Если этот сервер не найден в динамическом административном представлении sys.dm_database_copies, этот командлет возвращает пустой объект Status.</span><span class="sxs-lookup"><span data-stu-id="65f11-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65f11-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="65f11-141">-Profile</span></span>
<span data-ttu-id="65f11-142">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="65f11-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="65f11-143">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="65f11-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="65f11-144">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="65f11-144">-ServerName</span></span>
<span data-ttu-id="65f11-145">Указывает имя сервера, на котором находится копия базы данных.</span><span class="sxs-lookup"><span data-stu-id="65f11-145">Specifies the name of the server on which the database copy resides.</span></span>

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

### <span data-ttu-id="65f11-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65f11-146">CommonParameters</span></span>
<span data-ttu-id="65f11-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="65f11-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65f11-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65f11-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65f11-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65f11-149">INPUTS</span></span>

### <span data-ttu-id="65f11-150">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="65f11-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="65f11-151">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="65f11-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="65f11-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65f11-152">OUTPUTS</span></span>

### <span data-ttu-id="65f11-153">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="65f11-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="65f11-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="65f11-154">NOTES</span></span>
* <span data-ttu-id="65f11-155">Проверка подлинности: для этого командлета требуется проверка подлинности на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="65f11-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="65f11-156">Пример использования проверки подлинности на основе сертификатов для настройки текущей подписки приведен в описании командлета New-AzureSqlDatabaseServerContext.</span><span class="sxs-lookup"><span data-stu-id="65f11-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="65f11-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65f11-157">RELATED LINKS</span></span>

[<span data-ttu-id="65f11-158">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="65f11-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="65f11-159">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="65f11-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="65f11-160">Командлеты базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="65f11-160">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="65f11-161">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="65f11-161">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="65f11-162">Остановить-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="65f11-162">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


