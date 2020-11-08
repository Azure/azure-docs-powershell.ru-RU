---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076293"
---
# <span data-ttu-id="230a3-101">Get-AzureSqlDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="230a3-101">Get-AzureSqlDatabaseOperation</span></span>

## <span data-ttu-id="230a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="230a3-102">SYNOPSIS</span></span>
<span data-ttu-id="230a3-103">Возвращает состояние операций с базой данных на сервере Azure.</span><span class="sxs-lookup"><span data-stu-id="230a3-103">Gets the status of database operations on an Azure server.</span></span>

## <span data-ttu-id="230a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="230a3-104">SYNTAX</span></span>

### <span data-ttu-id="230a3-105">ByConnectionContext (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="230a3-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="230a3-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="230a3-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="230a3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="230a3-107">DESCRIPTION</span></span>
<span data-ttu-id="230a3-108">Командлет **Get-AzureSqlDatabaseOperation** получает состояние операций базы данных на указанном сервере Azure.</span><span class="sxs-lookup"><span data-stu-id="230a3-108">The **Get-AzureSqlDatabaseOperation** cmdlet gets the status of database operations on the specified Azure server.</span></span>
<span data-ttu-id="230a3-109">Если указан только параметр *ServerName* или *ConnectionContext* , командлет получает все операции с базой данных сервера.</span><span class="sxs-lookup"><span data-stu-id="230a3-109">If you specify only the *ServerName* or *ConnectionContext* parameter, the cmdlet gets all the database operations for the server.</span></span>
<span data-ttu-id="230a3-110">Если вы также указываете базу данных с помощью параметра *Database* или *DatabaseName* , этот командлет получает все операции для указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="230a3-110">If you also specify a database by using the *Database* or *DatabaseName* parameter, this cmdlet gets all the operations for the specified database.</span></span>
<span data-ttu-id="230a3-111">Если вы укажете идентификатор GUID операции, *ServerName* или *ConnectionContext* , командлет возвращает одну операцию базы данных.</span><span class="sxs-lookup"><span data-stu-id="230a3-111">If you specify an operation GUID, and *ServerName* or *ConnectionContext* , the cmdlet gets a single database operation.</span></span>

## <span data-ttu-id="230a3-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="230a3-112">EXAMPLES</span></span>

### <span data-ttu-id="230a3-113">Пример 1: получение состояния всех операций с базой данных для базы данных</span><span class="sxs-lookup"><span data-stu-id="230a3-113">Example 1: Get the status of all database operations for a database</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

<span data-ttu-id="230a3-114">Эта команда возвращает состояние всех операций с базой данных в базе данных с именем Database17 на сервере, которое указывает контекстом подключения $Context.</span><span class="sxs-lookup"><span data-stu-id="230a3-114">This command gets the status of all database operations on the database named Database17 on the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="230a3-115">Пример 2: получение состояния всех операций базы данных для сервера</span><span class="sxs-lookup"><span data-stu-id="230a3-115">Example 2: Get the status of all database operations for a server</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

<span data-ttu-id="230a3-116">Эта команда возвращает состояние всех операций с базой данных на сервере, которые $Context указывает контекстом подключения.</span><span class="sxs-lookup"><span data-stu-id="230a3-116">This command gets the status of all database operations on the server that the connection context $Context specifies.</span></span>

## <span data-ttu-id="230a3-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="230a3-117">PARAMETERS</span></span>

### <span data-ttu-id="230a3-118">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="230a3-118">-ConnectionContext</span></span>
<span data-ttu-id="230a3-119">Указывает контекст подключения сервера.</span><span class="sxs-lookup"><span data-stu-id="230a3-119">Specifies the connection context of a server.</span></span>

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

### <span data-ttu-id="230a3-120">-База данных</span><span class="sxs-lookup"><span data-stu-id="230a3-120">-Database</span></span>
<span data-ttu-id="230a3-121">Указывает объект, представляющий базу данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="230a3-121">Specifies an object that represents an Azure SQL Database.</span></span>
<span data-ttu-id="230a3-122">Если указать этот параметр, необходимо указать параметр *ServerName* или параметр *ConnectionContext* .</span><span class="sxs-lookup"><span data-stu-id="230a3-122">If you specify this parameter, you must specify the *ServerName* parameter or *ConnectionContext* parameter.</span></span>

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

### <span data-ttu-id="230a3-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="230a3-123">-DatabaseName</span></span>
<span data-ttu-id="230a3-124">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="230a3-124">Specifies the name of a database.</span></span>
<span data-ttu-id="230a3-125">Если указать этот параметр, необходимо указать параметр *ServerName* или параметр *ConnectionContext* .</span><span class="sxs-lookup"><span data-stu-id="230a3-125">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="230a3-126">-OperationGuid</span><span class="sxs-lookup"><span data-stu-id="230a3-126">-OperationGuid</span></span>
<span data-ttu-id="230a3-127">Указывает ИД операции, представляющей определенную операцию с базой данных, для которой этот командлет получает состояние.</span><span class="sxs-lookup"><span data-stu-id="230a3-127">Specifies the operation ID that represents a specific database operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="230a3-128">Идентификаторы операций можно получить, запросив все операции с базой данных для базы данных или сервера SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="230a3-128">You can obtain operation IDs by requesting all the database operations for a Azure SQL Database or server.</span></span>
<span data-ttu-id="230a3-129">Если указать этот параметр, необходимо указать параметр *ServerName* или параметр *ConnectionContext* .</span><span class="sxs-lookup"><span data-stu-id="230a3-129">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="230a3-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="230a3-130">-Profile</span></span>
<span data-ttu-id="230a3-131">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="230a3-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="230a3-132">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="230a3-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="230a3-133">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="230a3-133">-ServerName</span></span>
<span data-ttu-id="230a3-134">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="230a3-134">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="230a3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="230a3-135">CommonParameters</span></span>
<span data-ttu-id="230a3-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="230a3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="230a3-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="230a3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="230a3-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="230a3-138">INPUTS</span></span>

### <span data-ttu-id="230a3-139">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="230a3-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="230a3-140">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="230a3-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

### <span data-ttu-id="230a3-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="230a3-141">System.Guid</span></span>

## <span data-ttu-id="230a3-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="230a3-142">OUTPUTS</span></span>

### <span data-ttu-id="230a3-143">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database. DatabaseOperationResponseList []</span><span class="sxs-lookup"><span data-stu-id="230a3-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponseList[]</span></span>
<span data-ttu-id="230a3-144">Этот командлет возвращает массив объектов **DatabaseOperationResponseList** , если вы получаете несколько операций.</span><span class="sxs-lookup"><span data-stu-id="230a3-144">This cmdlet returns an array of **DatabaseOperationResponseList** objects if you get multiple operations.</span></span>

### <span data-ttu-id="230a3-145">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database. DatabaseOperationResponse</span><span class="sxs-lookup"><span data-stu-id="230a3-145">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponse</span></span>

## <span data-ttu-id="230a3-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="230a3-146">NOTES</span></span>

## <span data-ttu-id="230a3-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="230a3-147">RELATED LINKS</span></span>

[<span data-ttu-id="230a3-148">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="230a3-148">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="230a3-149">Состояние операции с базой данных</span><span class="sxs-lookup"><span data-stu-id="230a3-149">Database Operation Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[<span data-ttu-id="230a3-150">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="230a3-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="230a3-151">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="230a3-151">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="230a3-152">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="230a3-152">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


