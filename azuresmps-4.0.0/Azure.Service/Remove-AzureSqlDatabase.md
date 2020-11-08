---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B3813F54-E5B7-4605-BB1C-67417FDDB076
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3f9817ebe556bc80364d012040387cca72c56c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076108"
---
# <span data-ttu-id="c6972-101">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c6972-101">Remove-AzureSqlDatabase</span></span>

## <span data-ttu-id="c6972-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6972-102">SYNOPSIS</span></span>
<span data-ttu-id="c6972-103">Удаляет базу данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c6972-103">Deletes an Azure SQL Database.</span></span>

## <span data-ttu-id="c6972-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6972-104">SYNTAX</span></span>

### <span data-ttu-id="c6972-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="c6972-105">ByNameWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6972-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="c6972-106">ByObjectWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6972-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="c6972-107">ByNameWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6972-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="c6972-108">ByObjectWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -Database <Database> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6972-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6972-109">DESCRIPTION</span></span>
<span data-ttu-id="c6972-110">Командлет **Remove-AzureSqlDatabase** удаляет базу данных Azure SQL с помощью контекста соединения сервера или имени сервера.</span><span class="sxs-lookup"><span data-stu-id="c6972-110">The **Remove-AzureSqlDatabase** cmdlet deletes an Azure SQL Database by server connection context or server name.</span></span>
<span data-ttu-id="c6972-111">Вы можете создать контекст подключения к серверу базы данных SQL Azure с помощью командлета **New-AzureSqlDatabaseServerContext** , а затем использовать его с этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="c6972-111">You can create an Azure SQL Database server connection context using the **New-AzureSqlDatabaseServerContext** cmdlet, and then use it with this cmdlet.</span></span>

<span data-ttu-id="c6972-112">При удалении базы данных с указанием имени сервера базы данных Azure SQL командлет **Remove-AzureSqlDatabase** использует имя и текущую информацию о подписке Azure для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="c6972-112">When you delete a database by specifying an Azure SQL Database server name, the **Remove-AzureSqlDatabase** cmdlet uses the name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="c6972-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6972-113">EXAMPLES</span></span>

### <span data-ttu-id="c6972-114">Пример 1: Удаление базы данных</span><span class="sxs-lookup"><span data-stu-id="c6972-114">Example 1: Remove a database</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="c6972-115">Эта команда удаляет базу данных с именем Database01 из контекста подключения к серверу базы данных SQL Azure $Context.</span><span class="sxs-lookup"><span data-stu-id="c6972-115">This command removes the database named Database01 from the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="c6972-116">Пример 2: Удаление базы данных с помощью имени сервера</span><span class="sxs-lookup"><span data-stu-id="c6972-116">Example 2: Remove a database by using a server name</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="c6972-117">Эта команда удаляет базу данных с именем Database01 из сервера базы данных SQL Azure с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="c6972-117">This command removes the database named Database01 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="c6972-118">Пример 3: Удаление базы данных с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="c6972-118">Example 3: Remove a database by using the pipeline</span></span>
```
PS C:\> $Database01 | Remove-AzureSqlDatabase -ConnectionContext $Context
PS C:\> $Database01 | Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="c6972-119">В этом примере показан альтернативный способ передачи объекта базы данных через конвейер.</span><span class="sxs-lookup"><span data-stu-id="c6972-119">This example demonstrates the alternative method of passing the database object through the pipeline.</span></span>

## <span data-ttu-id="c6972-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6972-120">PARAMETERS</span></span>

### <span data-ttu-id="c6972-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="c6972-121">-ConnectionContext</span></span>
<span data-ttu-id="c6972-122">Указывает контекст подключения сервера, с которого этот командлет удаляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="c6972-122">Specifies the connection context of a server from which this cmdlet removes a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6972-123">-База данных</span><span class="sxs-lookup"><span data-stu-id="c6972-123">-Database</span></span>
<span data-ttu-id="c6972-124">Указывает объект, представляющий базу данных, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c6972-124">Specifies an object that represents the database that this cmdlet removes.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6972-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c6972-125">-DatabaseName</span></span>
<span data-ttu-id="c6972-126">Указывает имя базы данных, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c6972-126">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6972-127">-Force</span><span class="sxs-lookup"><span data-stu-id="c6972-127">-Force</span></span>
<span data-ttu-id="c6972-128">Разрешает выполнение действия без запроса подтверждения у пользователя.</span><span class="sxs-lookup"><span data-stu-id="c6972-128">Allows the action to complete without prompting the user for confirmation.</span></span>

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

### <span data-ttu-id="c6972-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="c6972-129">-Profile</span></span>
<span data-ttu-id="c6972-130">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c6972-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c6972-131">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c6972-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c6972-132">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="c6972-132">-ServerName</span></span>
<span data-ttu-id="c6972-133">Указывает имя сервера, на котором этот командлет удаляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="c6972-133">Specifies the name of the server on which this cmdlet deletes the database.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6972-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6972-134">-Confirm</span></span>
<span data-ttu-id="c6972-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c6972-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6972-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6972-136">-WhatIf</span></span>
<span data-ttu-id="c6972-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c6972-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6972-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c6972-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6972-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6972-139">CommonParameters</span></span>
<span data-ttu-id="c6972-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6972-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6972-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6972-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6972-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6972-142">INPUTS</span></span>

### <span data-ttu-id="c6972-143">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="c6972-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="c6972-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6972-144">OUTPUTS</span></span>

## <span data-ttu-id="c6972-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6972-145">NOTES</span></span>
* <span data-ttu-id="c6972-146">Из-за серьезности операции по умолчанию этот командлет запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c6972-146">Because of the severity of the operation, by default, this cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="c6972-147">Для пропуска подтверждения укажите параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="c6972-147">To skip confirmation, specify the *Force* parameter.</span></span>

## <span data-ttu-id="c6972-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6972-148">RELATED LINKS</span></span>

[<span data-ttu-id="c6972-149">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="c6972-149">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="c6972-150">Удаление базы данных</span><span class="sxs-lookup"><span data-stu-id="c6972-150">Delete Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505705.aspx)

[<span data-ttu-id="c6972-151">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="c6972-151">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="c6972-152">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c6972-152">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="c6972-153">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c6972-153">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="c6972-154">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="c6972-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="c6972-155">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c6972-155">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


