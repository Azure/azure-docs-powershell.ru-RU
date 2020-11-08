---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 82F4DB8F-8DAF-40D2-8031-3EDBF5D08417
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6274d3851042c15791707807471ae1bc6a2733ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075865"
---
# <span data-ttu-id="ebbb5-101">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ebbb5-101">Set-AzureSqlDatabase</span></span>

## <span data-ttu-id="ebbb5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebbb5-102">SYNOPSIS</span></span>
<span data-ttu-id="ebbb5-103">Задает свойства для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-103">Sets properties for an Azure SQL Database.</span></span>

## <span data-ttu-id="ebbb5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebbb5-104">SYNTAX</span></span>

### <span data-ttu-id="ebbb5-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="ebbb5-105">ByNameWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebbb5-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="ebbb5-106">ByObjectWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebbb5-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="ebbb5-107">ByNameWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebbb5-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="ebbb5-108">ByObjectWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -Database <Database> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebbb5-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebbb5-109">DESCRIPTION</span></span>
<span data-ttu-id="ebbb5-110">Командлет **Set-AzureSqlDatabase** задает свойства для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-110">The **Set-AzureSqlDatabase** cmdlet sets properties for an Azure SQL Database.</span></span>
<span data-ttu-id="ebbb5-111">Вы можете указать базу данных по имени или передать объект базы данных SQL Azure через конвейер.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-111">You can specify the database by name, or pass an Azure SQL Database object through the pipeline.</span></span>
<span data-ttu-id="ebbb5-112">Вы можете указать сервер по имени или передать контекст подключения к серверу базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-112">You can specify the server by name, or pass an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="ebbb5-113">Создайте контекст подключения, выполнив командлет **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="ebbb5-113">Create a connection context by running the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="ebbb5-114">Если вы укажете сервер по имени, командлет использует текущие сведения о подписке Azure для проверки подлинности запроса.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-114">If you specify the server by name, the cmdlet uses the current Azure subscription information to authenticate the request.</span></span>

## <span data-ttu-id="ebbb5-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebbb5-115">EXAMPLES</span></span>

### <span data-ttu-id="ebbb5-116">Пример 1: изменение размера базы данных с помощью контекста подключения</span><span class="sxs-lookup"><span data-stu-id="ebbb5-116">Example 1: Change the size of a database by using a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ConnectionContext $Context -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="ebbb5-117">В этом примере изменяется размер базы данных с именем Database01 на 20 ГБ в контексте подключения к серверу базы данных SQL Azure $Context.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-117">This example changes the size of the database named Database01 to 20 GB, in the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="ebbb5-118">Пример 2: изменение размера базы данных с помощью имени сервера</span><span class="sxs-lookup"><span data-stu-id="ebbb5-118">Example 2: Change the size of a database by using a server name</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ServerName "lpqd0zbr8y" -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="ebbb5-119">В этом примере изменяется размер базы данных с именем Database01 на 20 ГБ на сервере с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-119">This example changes the size of the database named Database01 to 20 GB in the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="ebbb5-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebbb5-120">PARAMETERS</span></span>

### <span data-ttu-id="ebbb5-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="ebbb5-121">-ConnectionContext</span></span>
<span data-ttu-id="ebbb5-122">Указывает контекст подключения сервера.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-122">Specifies the connection context of a server.</span></span>

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

### <span data-ttu-id="ebbb5-123">-База данных</span><span class="sxs-lookup"><span data-stu-id="ebbb5-123">-Database</span></span>
<span data-ttu-id="ebbb5-124">Указывает объект, представляющий базу данных SQL Azure, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-124">Specifies an object that represents the Azure SQL Database that this cmdlet modifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebbb5-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ebbb5-125">-DatabaseName</span></span>
<span data-ttu-id="ebbb5-126">Указывает имя базы данных, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-126">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ebbb5-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="ebbb5-127">-Edition</span></span>
<span data-ttu-id="ebbb5-128">Указывает новый выпуск для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-128">Specifies the new edition for the Azure SQL Database.</span></span>
<span data-ttu-id="ebbb5-129">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="ebbb5-129">Valid values are:</span></span> 

- <span data-ttu-id="ebbb5-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="ebbb5-130">None</span></span>
- <span data-ttu-id="ebbb5-131">Сайта</span><span class="sxs-lookup"><span data-stu-id="ebbb5-131">Web</span></span>
- <span data-ttu-id="ebbb5-132">Деловы</span><span class="sxs-lookup"><span data-stu-id="ebbb5-132">Business</span></span>
- <span data-ttu-id="ebbb5-133">Базового</span><span class="sxs-lookup"><span data-stu-id="ebbb5-133">Basic</span></span>
- <span data-ttu-id="ebbb5-134">Стандартная</span><span class="sxs-lookup"><span data-stu-id="ebbb5-134">Standard</span></span>
-  <span data-ttu-id="ebbb5-135">Версию</span><span class="sxs-lookup"><span data-stu-id="ebbb5-135">Premium</span></span>

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

### <span data-ttu-id="ebbb5-136">-Force</span><span class="sxs-lookup"><span data-stu-id="ebbb5-136">-Force</span></span>
<span data-ttu-id="ebbb5-137">Позволяет выполнить действие без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-137">Allows the action to complete without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ebbb5-138">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="ebbb5-138">-MaxSizeBytes</span></span>
<span data-ttu-id="ebbb5-139">Указание нового максимального размера базы данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-139">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="ebbb5-140">Вы можете указать либо этот параметр, либо параметр *MaxSizeGB* .</span><span class="sxs-lookup"><span data-stu-id="ebbb5-140">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="ebbb5-141">Для приемлемых значений в соответствии с выпуском ознакомьтесь с параметром *MaxSizeGB* .</span><span class="sxs-lookup"><span data-stu-id="ebbb5-141">See the *MaxSizeGB* parameter for acceptable values based on edition.</span></span>

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

### <span data-ttu-id="ebbb5-142">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="ebbb5-142">-MaxSizeGB</span></span>
<span data-ttu-id="ebbb5-143">Задает новый максимальный размер базы данных в гигабайтах.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-143">Specifies the new maximum size for the database in gigabytes.</span></span>
<span data-ttu-id="ebbb5-144">Вы можете указать либо этот параметр, либо параметр *MaxSizeBytes* .</span><span class="sxs-lookup"><span data-stu-id="ebbb5-144">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="ebbb5-145">Приемлемые значения зависят от выпуска.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-145">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="ebbb5-146">Основные значения выпусков: 1 или 2</span><span class="sxs-lookup"><span data-stu-id="ebbb5-146">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="ebbb5-147">Стандартные значения выпуска: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 или 250</span><span class="sxs-lookup"><span data-stu-id="ebbb5-147">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="ebbb5-148">Расширенные значения выпуска: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300 и 400</span><span class="sxs-lookup"><span data-stu-id="ebbb5-148">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="ebbb5-149">Значения веб-выпуска: 1 или 5</span><span class="sxs-lookup"><span data-stu-id="ebbb5-149">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="ebbb5-150">Значения для выпуска Business Edition: 10, 20, 30, 40, 50, 100 или 150</span><span class="sxs-lookup"><span data-stu-id="ebbb5-150">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

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

### <span data-ttu-id="ebbb5-151">-NewDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ebbb5-151">-NewDatabaseName</span></span>
<span data-ttu-id="ebbb5-152">Указывает новое имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-152">Specifies the new name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebbb5-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebbb5-153">-PassThru</span></span>
<span data-ttu-id="ebbb5-154">Возвращает обновленную базу данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-154">Returns the updated Azure SQL Database.</span></span>

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

### <span data-ttu-id="ebbb5-155">-Profile</span><span class="sxs-lookup"><span data-stu-id="ebbb5-155">-Profile</span></span>
<span data-ttu-id="ebbb5-156">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ebbb5-157">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ebbb5-158">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ebbb5-158">-ServerName</span></span>
<span data-ttu-id="ebbb5-159">Указывает имя сервера, содержащего базу данных, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-159">Specifies the name of the server that contains the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ebbb5-160">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="ebbb5-160">-ServiceObjective</span></span>
<span data-ttu-id="ebbb5-161">Указывает объект, который представляет новую цель обслуживания (уровень производительности) для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-161">Specifies an object representing the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="ebbb5-162">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="ebbb5-162">Valid values are:</span></span> 

- <span data-ttu-id="ebbb5-163">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="ebbb5-163">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="ebbb5-164">Стандартный (S0): f1173c43-91bd-4AAA-973c-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="ebbb5-164">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="ebbb5-165">Стандартный (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="ebbb5-165">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="ebbb5-166">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="ebbb5-166">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="ebbb5-167">\* Стандартный (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="ebbb5-167">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="ebbb5-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="ebbb5-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="ebbb5-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="ebbb5-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="ebbb5-170">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="ebbb5-170">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="ebbb5-171">\* Стандартный (S3) является частью последнего обновления базы данных SQL версии 12 (Предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="ebbb5-171">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="ebbb5-172">Дополнительные сведения можно найти в разделе новые возможности предварительного просмотра базы данных SQL Azure версии 12 https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="ebbb5-172">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

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

### <span data-ttu-id="ebbb5-173">-Sync</span><span class="sxs-lookup"><span data-stu-id="ebbb5-173">-Sync</span></span>
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

### <span data-ttu-id="ebbb5-174">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebbb5-174">-Confirm</span></span>
<span data-ttu-id="ebbb5-175">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebbb5-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebbb5-176">-WhatIf</span></span>
<span data-ttu-id="ebbb5-177">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebbb5-178">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebbb5-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebbb5-179">CommonParameters</span></span>
<span data-ttu-id="ebbb5-180">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebbb5-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebbb5-181">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebbb5-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebbb5-182">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebbb5-182">INPUTS</span></span>

### <span data-ttu-id="ebbb5-183">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="ebbb5-183">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="ebbb5-184">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebbb5-184">OUTPUTS</span></span>

### <span data-ttu-id="ebbb5-185">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="ebbb5-185">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="ebbb5-186">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebbb5-186">NOTES</span></span>

## <span data-ttu-id="ebbb5-187">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebbb5-187">RELATED LINKS</span></span>

[<span data-ttu-id="ebbb5-188">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="ebbb5-188">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="ebbb5-189">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="ebbb5-189">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="ebbb5-190">Обновить базу данных</span><span class="sxs-lookup"><span data-stu-id="ebbb5-190">Update Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505718.aspx)

[<span data-ttu-id="ebbb5-191">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ebbb5-191">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="ebbb5-192">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ebbb5-192">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="ebbb5-193">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ebbb5-193">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="ebbb5-194">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="ebbb5-194">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


