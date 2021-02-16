---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95e276bf6af11698a4b3b82077175ec2ede2d7dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402428"
---
# <span data-ttu-id="c93be-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c93be-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="c93be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c93be-102">SYNOPSIS</span></span>
<span data-ttu-id="c93be-103">Проверяет состояние связей копирования.</span><span class="sxs-lookup"><span data-stu-id="c93be-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="c93be-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c93be-104">SYNTAX</span></span>

### <span data-ttu-id="c93be-105">ByServerNameOnly (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c93be-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c93be-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c93be-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c93be-107">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="c93be-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c93be-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c93be-108">DESCRIPTION</span></span>
<span data-ttu-id="c93be-109">**Cmdlet Get-AzureSqlDataCopy** проверяет состояние одной или более активных связей копирования.</span><span class="sxs-lookup"><span data-stu-id="c93be-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="c93be-110">Запустите этот cmdlet после запуска Start-AzureSqlDatabaseCopy или Stop-AzureSqlDatabaseCopy.</span><span class="sxs-lookup"><span data-stu-id="c93be-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="c93be-111">Вы можете проверить конкретную связь копирования, все связи копирования или отфильтрованный список связей копирования, например все копии на определенном целевом сервере.</span><span class="sxs-lookup"><span data-stu-id="c93be-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="c93be-112">Этот cmdlet можно выполнить на сервере, на котором размещена базовая или целевая база данных.</span><span class="sxs-lookup"><span data-stu-id="c93be-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="c93be-113">Этот cmdlet является синхронным.</span><span class="sxs-lookup"><span data-stu-id="c93be-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="c93be-114">Этот cmdlet блокирует консоль Azure PowerShell, пока не будет возвращен объект состояния.</span><span class="sxs-lookup"><span data-stu-id="c93be-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="c93be-115">Параметры *PartnerServer* и *PartnerDatabase* необязательны.</span><span class="sxs-lookup"><span data-stu-id="c93be-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="c93be-116">Если ни один из параметров не указан, этот cmdlet возвращает таблицу результатов.</span><span class="sxs-lookup"><span data-stu-id="c93be-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="c93be-117">Чтобы увидеть состояние только для конкретной базы данных, укажите оба параметра.</span><span class="sxs-lookup"><span data-stu-id="c93be-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="c93be-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c93be-118">EXAMPLES</span></span>

### <span data-ttu-id="c93be-119">Пример 1. Просмотр состояния копии базы данных</span><span class="sxs-lookup"><span data-stu-id="c93be-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="c93be-120">Эта команда получает состояние базы данных "Заказы" на сервере lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="c93be-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="c93be-121">Параметр *PartnerServer ограничивает* эту команду сервером bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="c93be-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="c93be-122">Пример 2. Получить состояние всех копий на сервереGet состояние всех копий на сервере</span><span class="sxs-lookup"><span data-stu-id="c93be-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="c93be-123">Эта команда получает состояние всех активных копий на сервере lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="c93be-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="c93be-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c93be-124">PARAMETERS</span></span>

### <span data-ttu-id="c93be-125">-Database</span><span class="sxs-lookup"><span data-stu-id="c93be-125">-Database</span></span>
<span data-ttu-id="c93be-126">Определяет объект, который представляет исходный источник базы SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c93be-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="c93be-127">Этот cmdlet получает состояние копии базы данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="c93be-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="c93be-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c93be-128">-DatabaseCopy</span></span>
<span data-ttu-id="c93be-129">Определяет объект, который представляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="c93be-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="c93be-130">Этот cmdlet получает состояние копии базы данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="c93be-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="c93be-131">Этот параметр принимает входные данные конвейера.</span><span class="sxs-lookup"><span data-stu-id="c93be-131">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="c93be-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c93be-132">-DatabaseName</span></span>
<span data-ttu-id="c93be-133">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="c93be-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="c93be-134">Этот cmdlet возвращает состояние копии базы данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="c93be-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="c93be-135">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="c93be-135">-PartnerDatabase</span></span>
<span data-ttu-id="c93be-136">Указывает имя вторичной базы данных.</span><span class="sxs-lookup"><span data-stu-id="c93be-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="c93be-137">Если эта база данных не найдена в sys.dm_database_copies управления, этот cmdlet возвращает пустой объект состояния.</span><span class="sxs-lookup"><span data-stu-id="c93be-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

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

### <span data-ttu-id="c93be-138">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="c93be-138">-PartnerServer</span></span>
<span data-ttu-id="c93be-139">Имя сервера, на котором размещена целевая база данных.</span><span class="sxs-lookup"><span data-stu-id="c93be-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="c93be-140">Если этот сервер не найден в sys.dm_database_copies управления, этот cmdlet возвращает пустой объект состояния.</span><span class="sxs-lookup"><span data-stu-id="c93be-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

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

### <span data-ttu-id="c93be-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="c93be-141">-Profile</span></span>
<span data-ttu-id="c93be-142">Определяет профиль Azure, для которого читается этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c93be-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c93be-143">Если не указать профиль, этот cmdlet будет читать данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c93be-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c93be-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c93be-144">-ServerName</span></span>
<span data-ttu-id="c93be-145">Имя сервера, на котором находится копия базы данных.</span><span class="sxs-lookup"><span data-stu-id="c93be-145">Specifies the name of the server on which the database copy resides.</span></span>

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

### <span data-ttu-id="c93be-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c93be-146">CommonParameters</span></span>
<span data-ttu-id="c93be-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c93be-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c93be-148">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c93be-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c93be-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c93be-149">INPUTS</span></span>

### <span data-ttu-id="c93be-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c93be-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="c93be-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="c93be-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="c93be-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c93be-152">OUTPUTS</span></span>

### <span data-ttu-id="c93be-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c93be-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="c93be-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c93be-154">NOTES</span></span>
* <span data-ttu-id="c93be-155">Проверка подлинности: этот cmdlet требует проверки подлинности на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="c93be-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="c93be-156">Пример использования проверки подлинности на основе сертификата для проверки текущей подписки см. в New-AzureSqlDatabaseServerContext.</span><span class="sxs-lookup"><span data-stu-id="c93be-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="c93be-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c93be-157">RELATED LINKS</span></span>

[<span data-ttu-id="c93be-158">База SQL Azure</span><span class="sxs-lookup"><span data-stu-id="c93be-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="c93be-159">Операции для баз данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="c93be-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)



[<span data-ttu-id="c93be-160">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c93be-160">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="c93be-161">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c93be-161">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


