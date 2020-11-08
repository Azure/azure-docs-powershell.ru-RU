---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075973"
---
# <span data-ttu-id="a7e7a-101">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a7e7a-101">New-AzureSqlDatabase</span></span>

## <span data-ttu-id="a7e7a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e7a-103">Создает базу данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-103">Creates an Azure SQL Database.</span></span>

## <span data-ttu-id="a7e7a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7e7a-104">SYNTAX</span></span>

### <span data-ttu-id="a7e7a-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="a7e7a-105">ByConnectionContext</span></span>
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7e7a-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="a7e7a-106">ByServerName</span></span>
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7e7a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7e7a-107">DESCRIPTION</span></span>
<span data-ttu-id="a7e7a-108">Командлет **New-AzureSqlDatabase** создает базу данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-108">The **New-AzureSqlDatabase** cmdlet creates an Azure SQL Database.</span></span>
<span data-ttu-id="a7e7a-109">Вы можете указать сервер, используя контекст подключения к серверу базы данных SQL Azure, созданный с помощью командлета **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="a7e7a-109">You can specify the server by using an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="a7e7a-110">Или, если указать имя сервера, командлет использует текущие сведения о подписке Azure для проверки подлинности запроса на доступ к серверу.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-110">Or, if you specify the server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="a7e7a-111">Когда вы создаете новую базу данных, указав сервер базы данных Azure SQL, командлет **New-AzureSqlDatabase** создает временный контекст подключения, используя указанное имя сервера и текущую информацию о подписке Azure для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-111">When you create a new database by specifying an Azure SQL Database server, the **New-AzureSqlDatabase** cmdlet creates a temporary connection context using the specified server name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="a7e7a-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7e7a-112">EXAMPLES</span></span>

### <span data-ttu-id="a7e7a-113">Пример 1: создание базы данных</span><span class="sxs-lookup"><span data-stu-id="a7e7a-113">Example 1: Create a database</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="a7e7a-114">Эта команда создает базу данных Azure SQL с именем Database1 для контекста подключения к серверу базы данных SQL Azure $Context.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-114">This command creates an Azure SQL Database named Database1, for the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="a7e7a-115">Пример 2: создание базы данных в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="a7e7a-115">Example 2: Create a database in the current subscription</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="a7e7a-116">В этом примере создается база данных с именем Database1 на указанном сервере базы данных SQL Azure с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-116">This example creates a database named Database1, in the specified Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="a7e7a-117">Командлет использует текущие сведения о подписке Azure для проверки подлинности запроса на доступ к серверу.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-117">The cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

## <span data-ttu-id="a7e7a-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7e7a-118">PARAMETERS</span></span>

### <span data-ttu-id="a7e7a-119">-Параметры сортировки</span><span class="sxs-lookup"><span data-stu-id="a7e7a-119">-Collation</span></span>
<span data-ttu-id="a7e7a-120">Задает параметры сортировки для новой базы данных.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-120">Specifies a collation for the new database.</span></span>

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

### <span data-ttu-id="a7e7a-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="a7e7a-121">-ConnectionContext</span></span>
<span data-ttu-id="a7e7a-122">Указывает контекст подключения сервера, на котором этот командлет создает базу данных.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-122">Specifies the connection context of a server where this cmdlet creates a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7e7a-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a7e7a-123">-DatabaseName</span></span>
<span data-ttu-id="a7e7a-124">Указывает имя новой базы данных.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-124">Specifies the name of the new database.</span></span>

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

### <span data-ttu-id="a7e7a-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="a7e7a-125">-Edition</span></span>
<span data-ttu-id="a7e7a-126">Указывает выпуск для новой базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-126">Specifies the edition for the new Azure SQL Database.</span></span>
<span data-ttu-id="a7e7a-127">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a7e7a-127">Valid values are:</span></span> 

- <span data-ttu-id="a7e7a-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="a7e7a-128">None</span></span>
- <span data-ttu-id="a7e7a-129">Сайта</span><span class="sxs-lookup"><span data-stu-id="a7e7a-129">Web</span></span>
- <span data-ttu-id="a7e7a-130">Деловы</span><span class="sxs-lookup"><span data-stu-id="a7e7a-130">Business</span></span>
- <span data-ttu-id="a7e7a-131">Базового</span><span class="sxs-lookup"><span data-stu-id="a7e7a-131">Basic</span></span>
- <span data-ttu-id="a7e7a-132">Стандартная</span><span class="sxs-lookup"><span data-stu-id="a7e7a-132">Standard</span></span>
-  <span data-ttu-id="a7e7a-133">Версию</span><span class="sxs-lookup"><span data-stu-id="a7e7a-133">Premium</span></span>

<span data-ttu-id="a7e7a-134">По умолчанию используется значение Web.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-134">The default value is Web.</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e7a-135">-Force</span><span class="sxs-lookup"><span data-stu-id="a7e7a-135">-Force</span></span>
<span data-ttu-id="a7e7a-136">Разрешает выполнение действия без запроса подтверждения у пользователя.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-136">Allows the action to complete without prompting the user for confirmation.</span></span>

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

### <span data-ttu-id="a7e7a-137">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="a7e7a-137">-MaxSizeBytes</span></span>
<span data-ttu-id="a7e7a-138">Указывает максимальный размер базы данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-138">Specifies the maximum size of the database in bytes.</span></span>
<span data-ttu-id="a7e7a-139">Вы можете указать либо этот параметр, либо параметр *MaxSizeGB* .</span><span class="sxs-lookup"><span data-stu-id="a7e7a-139">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="a7e7a-140">Посмотрите описание параметра *MaxSizeGB* для приемлемых значений в соответствии с выпуском.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-140">See the *MaxSizeGB* parameter description for acceptable values based on edition.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e7a-141">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="a7e7a-141">-MaxSizeGB</span></span>
<span data-ttu-id="a7e7a-142">Задает максимальный размер базы данных в гигабайтах.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-142">Specifies the maximum size of the database in gigabytes.</span></span>
<span data-ttu-id="a7e7a-143">Вы можете указать либо этот параметр, либо параметр *MaxSizeBytes* .</span><span class="sxs-lookup"><span data-stu-id="a7e7a-143">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="a7e7a-144">Приемлемые значения зависят от выпуска.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-144">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="a7e7a-145">Основные значения выпусков: 1 или 2</span><span class="sxs-lookup"><span data-stu-id="a7e7a-145">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="a7e7a-146">Стандартные значения выпуска: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 или 250</span><span class="sxs-lookup"><span data-stu-id="a7e7a-146">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="a7e7a-147">Расширенные значения выпуска: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300 и 400</span><span class="sxs-lookup"><span data-stu-id="a7e7a-147">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="a7e7a-148">Значения веб-выпуска: 1 или 5</span><span class="sxs-lookup"><span data-stu-id="a7e7a-148">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="a7e7a-149">Значения для выпуска Business Edition: 10, 20, 30, 40, 50, 100 или 150</span><span class="sxs-lookup"><span data-stu-id="a7e7a-149">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e7a-150">-Profile</span><span class="sxs-lookup"><span data-stu-id="a7e7a-150">-Profile</span></span>
<span data-ttu-id="a7e7a-151">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a7e7a-152">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a7e7a-153">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="a7e7a-153">-ServerName</span></span>
<span data-ttu-id="a7e7a-154">Указывает имя сервера базы данных SQL Azure, на котором будет содержаться новая база данных.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-154">Specifies the name of the Azure SQL Database server to contain the new database.</span></span>

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

### <span data-ttu-id="a7e7a-155">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="a7e7a-155">-ServiceObjective</span></span>
<span data-ttu-id="a7e7a-156">Указывает объект, который представляет новую цель обслуживания (уровень производительности) для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-156">Specifies an object that represent the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="a7e7a-157">Это значение представляет уровень ресурсов, назначенных этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-157">This value represents the level of resources assigned to this database.</span></span>
<span data-ttu-id="a7e7a-158">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a7e7a-158">Valid values are:</span></span> 

<span data-ttu-id="a7e7a-159">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c Standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 \* Standard (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2</span><span class="sxs-lookup"><span data-stu-id="a7e7a-159">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 \*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="a7e7a-160">\* Стандартный (S3) является частью последнего обновления базы данных SQL версии 12 (Предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="a7e7a-160">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="a7e7a-161">Дополнительные сведения можно найти в разделе новые возможности предварительного просмотра базы данных SQL Azure версии 12 https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="a7e7a-161">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e7a-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7e7a-162">-Confirm</span></span>
<span data-ttu-id="a7e7a-163">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7e7a-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7e7a-164">-WhatIf</span></span>
<span data-ttu-id="a7e7a-165">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7e7a-166">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7e7a-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e7a-167">CommonParameters</span></span>
<span data-ttu-id="a7e7a-168">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e7a-169">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7e7a-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e7a-170">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7e7a-170">INPUTS</span></span>

## <span data-ttu-id="a7e7a-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7e7a-171">OUTPUTS</span></span>

### <span data-ttu-id="a7e7a-172">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="a7e7a-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="a7e7a-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7e7a-173">NOTES</span></span>
* <span data-ttu-id="a7e7a-174">Чтобы удалить базу данных, созданную с помощью **New-AzureSqlDatabase** , используйте командлет Remove-AzureSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="a7e7a-174">To delete a database that was created by **New-AzureSqlDatabase** , use the Remove-AzureSqlDatabase cmdlet.</span></span>

## <span data-ttu-id="a7e7a-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7e7a-175">RELATED LINKS</span></span>

[<span data-ttu-id="a7e7a-176">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="a7e7a-176">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="a7e7a-177">Создание базы данных</span><span class="sxs-lookup"><span data-stu-id="a7e7a-177">Create Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[<span data-ttu-id="a7e7a-178">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="a7e7a-178">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="a7e7a-179">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a7e7a-179">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="a7e7a-180">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="a7e7a-180">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="a7e7a-181">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a7e7a-181">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="a7e7a-182">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a7e7a-182">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


