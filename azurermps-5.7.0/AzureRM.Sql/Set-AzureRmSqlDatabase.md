---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: b0493433f7419039acacd696748b3c5f9518aef5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561379"
---
# <span data-ttu-id="32bb9-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="32bb9-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="32bb9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32bb9-102">SYNOPSIS</span></span>
<span data-ttu-id="32bb9-103">Задает свойства базы данных или перемещает существующую базу данных в эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="32bb9-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32bb9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32bb9-104">SYNTAX</span></span>

### <span data-ttu-id="32bb9-105">Обновление</span><span class="sxs-lookup"><span data-stu-id="32bb9-105">Update</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32bb9-106">Переименовав</span><span class="sxs-lookup"><span data-stu-id="32bb9-106">Rename</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32bb9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32bb9-107">DESCRIPTION</span></span>
<span data-ttu-id="32bb9-108">Командлет **Set-AzureRmSqlDatabase** задает свойства базы данных в базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="32bb9-108">The **Set-AzureRmSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="32bb9-109">Этот командлет может изменить уровень служб ( *выпуск* ), уровень производительности ( *RequestedServiceObjectiveName* ) и максимальный размер хранилища ( *MaxSizeBytes* ) для базы данных.</span><span class="sxs-lookup"><span data-stu-id="32bb9-109">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="32bb9-110">Кроме того, вы можете указать параметр *ElasticPoolName* , чтобы переместить базу данных в эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="32bb9-110">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="32bb9-111">Если база данных уже находится в пуле эластичных БД, вы можете использовать параметр *RequestedServiceObjectiveName* , чтобы переместить базу данных из эластичного пула и на уровень производительности для одной базы данных.</span><span class="sxs-lookup"><span data-stu-id="32bb9-111">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="32bb9-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32bb9-112">EXAMPLES</span></span>

### <span data-ttu-id="32bb9-113">Пример 1: обновление базы данных на стандартную базу данных S2</span><span class="sxs-lookup"><span data-stu-id="32bb9-113">Example 1: Update a database to a Standard S2 database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S2"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S2
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="32bb9-114">Эта команда обновляет базу данных с именем Database01 на стандартную базу данных S2 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="32bb9-114">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="32bb9-115">Пример 2: Добавление базы данных в эластичный пул</span><span class="sxs-lookup"><span data-stu-id="32bb9-115">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="32bb9-116">Эта команда добавляет базу данных с именем Database01 в пул эластичных БД с именем ElasticPool01, размещенный на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="32bb9-116">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="32bb9-117">Пример 3: изменение максимального размера хранилища базы данных</span><span class="sxs-lookup"><span data-stu-id="32bb9-117">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 1099511627776
Status                        : Online
CreationDate                  : 8/24/2017 9:00:37 AM
CurrentServiceObjectiveId     : 789681b8-ca10-4eb0-bdf2-e0b050601b40
CurrentServiceObjectiveName   : S3
RequestedServiceObjectiveId   : 789681b8-ca10-4eb0-bdf2-e0b050601b40
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="32bb9-118">Эта команда обновляет базу данных с именем Database01, чтобы установить максимальный размер в 1 ТБ.</span><span class="sxs-lookup"><span data-stu-id="32bb9-118">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="32bb9-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32bb9-119">PARAMETERS</span></span>

### <span data-ttu-id="32bb9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32bb9-120">-AsJob</span></span>
<span data-ttu-id="32bb9-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="32bb9-121">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="32bb9-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="32bb9-122">-DatabaseName</span></span>
<span data-ttu-id="32bb9-123">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="32bb9-123">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32bb9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32bb9-124">-DefaultProfile</span></span>
<span data-ttu-id="32bb9-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="32bb9-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bb9-126">-Edition</span><span class="sxs-lookup"><span data-stu-id="32bb9-126">-Edition</span></span>
<span data-ttu-id="32bb9-127">Указывает выпуск для базы данных.</span><span class="sxs-lookup"><span data-stu-id="32bb9-127">Specifies the edition for the database.</span></span>
<span data-ttu-id="32bb9-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="32bb9-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="32bb9-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="32bb9-129">None</span></span>
- <span data-ttu-id="32bb9-130">Версию</span><span class="sxs-lookup"><span data-stu-id="32bb9-130">Premium</span></span>
- <span data-ttu-id="32bb9-131">Базового</span><span class="sxs-lookup"><span data-stu-id="32bb9-131">Basic</span></span>
- <span data-ttu-id="32bb9-132">Стандартная</span><span class="sxs-lookup"><span data-stu-id="32bb9-132">Standard</span></span>
- <span data-ttu-id="32bb9-133">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="32bb9-133">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: Update
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bb9-134">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="32bb9-134">-ElasticPoolName</span></span>
<span data-ttu-id="32bb9-135">Указывает имя эластичного пула, в который нужно переместить базу данных.</span><span class="sxs-lookup"><span data-stu-id="32bb9-135">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bb9-136">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="32bb9-136">-MaxSizeBytes</span></span>
<span data-ttu-id="32bb9-137">Максимальный размер базы данных Azure SQL в байтах.</span><span class="sxs-lookup"><span data-stu-id="32bb9-137">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bb9-138">-NewName</span><span class="sxs-lookup"><span data-stu-id="32bb9-138">-NewName</span></span>
<span data-ttu-id="32bb9-139">Новое имя, в которое нужно переименовать базу данных.</span><span class="sxs-lookup"><span data-stu-id="32bb9-139">The new name to rename the database to.</span></span>

```yaml
Type: String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bb9-140">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="32bb9-140">-ReadScale</span></span>
<span data-ttu-id="32bb9-141">Параметр Read Scale (масштаб чтения), назначаемый базе данных Azure SQL. (Включено или отключено)</span><span class="sxs-lookup"><span data-stu-id="32bb9-141">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: DatabaseReadScale
Parameter Sets: Update
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bb9-142">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="32bb9-142">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="32bb9-143">Указывает имя цели обслуживания, которую нужно назначить базе данных.</span><span class="sxs-lookup"><span data-stu-id="32bb9-143">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="32bb9-144">Сведения о цели обслуживания можно найти на [уровнях служб базы данных Azure SQL Server и уровне производительности](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) в сетевой библиотеке разработчиков Microsoft.</span><span class="sxs-lookup"><span data-stu-id="32bb9-144">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bb9-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32bb9-145">-ResourceGroupName</span></span>
<span data-ttu-id="32bb9-146">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="32bb9-146">Specifies the name of resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32bb9-147">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="32bb9-147">-ServerName</span></span>
<span data-ttu-id="32bb9-148">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="32bb9-148">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32bb9-149">-Теги</span><span class="sxs-lookup"><span data-stu-id="32bb9-149">-Tags</span></span>
<span data-ttu-id="32bb9-150">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="32bb9-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="32bb9-151">Например:</span><span class="sxs-lookup"><span data-stu-id="32bb9-151">For example:</span></span>

<span data-ttu-id="32bb9-152">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="32bb9-152">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Update
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bb9-153">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="32bb9-153">-ZoneRedundant</span></span>
<span data-ttu-id="32bb9-154">Избыточность зоны, связываемая с базой данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="32bb9-154">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bb9-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32bb9-155">-Confirm</span></span>
<span data-ttu-id="32bb9-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32bb9-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32bb9-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32bb9-157">-WhatIf</span></span>
<span data-ttu-id="32bb9-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="32bb9-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32bb9-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="32bb9-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32bb9-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32bb9-160">CommonParameters</span></span>
<span data-ttu-id="32bb9-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32bb9-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32bb9-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32bb9-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32bb9-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32bb9-163">INPUTS</span></span>

### <span data-ttu-id="32bb9-164">Ничего</span><span class="sxs-lookup"><span data-stu-id="32bb9-164">None</span></span>
<span data-ttu-id="32bb9-165">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="32bb9-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="32bb9-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32bb9-166">OUTPUTS</span></span>

### <span data-ttu-id="32bb9-167">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="32bb9-167">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="32bb9-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="32bb9-168">NOTES</span></span>

## <span data-ttu-id="32bb9-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32bb9-169">RELATED LINKS</span></span>

[<span data-ttu-id="32bb9-170">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="32bb9-170">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="32bb9-171">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="32bb9-171">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="32bb9-172">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="32bb9-172">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="32bb9-173">Возобновить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="32bb9-173">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="32bb9-174">Приостановить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="32bb9-174">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="32bb9-175">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="32bb9-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
