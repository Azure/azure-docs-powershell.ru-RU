---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: dd69e345e5e2bac5ebab0ec4e45c03501ccc8139
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906474"
---
# <span data-ttu-id="c88e0-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c88e0-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="c88e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c88e0-102">SYNOPSIS</span></span>
<span data-ttu-id="c88e0-103">Задает свойства базы данных или перемещает существующую базу данных в эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="c88e0-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="c88e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c88e0-104">SYNTAX</span></span>

### <span data-ttu-id="c88e0-105">Обновление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c88e0-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c88e0-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="c88e0-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c88e0-107">Переименовав</span><span class="sxs-lookup"><span data-stu-id="c88e0-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c88e0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c88e0-108">DESCRIPTION</span></span>
<span data-ttu-id="c88e0-109">Командлет **Set-AzSqlDatabase** задает свойства базы данных в базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c88e0-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="c88e0-110">Этот командлет может изменить уровень служб ( *выпуск* ), уровень производительности ( *RequestedServiceObjectiveName* ) и максимальный размер хранилища ( *MaxSizeBytes* ) для базы данных.</span><span class="sxs-lookup"><span data-stu-id="c88e0-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="c88e0-111">Кроме того, вы можете указать параметр *ElasticPoolName* , чтобы переместить базу данных в эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="c88e0-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="c88e0-112">Если база данных уже находится в пуле эластичных БД, вы можете использовать параметр *RequestedServiceObjectiveName* , чтобы переместить базу данных из эластичного пула и на уровень производительности для одной базы данных.</span><span class="sxs-lookup"><span data-stu-id="c88e0-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="c88e0-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c88e0-113">EXAMPLES</span></span>

### <span data-ttu-id="c88e0-114">Пример 1: обновление базы данных до стандартной базы данных S0</span><span class="sxs-lookup"><span data-stu-id="c88e0-114">Example 1: Update a database to a Standard S0 database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S0"
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
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="c88e0-115">Эта команда обновляет базу данных с именем Database01 на стандартную базу данных S0 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="c88e0-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="c88e0-116">Пример 2: Добавление базы данных в эластичный пул</span><span class="sxs-lookup"><span data-stu-id="c88e0-116">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="c88e0-117">Эта команда добавляет базу данных с именем Database01 в пул эластичных БД с именем ElasticPool01, размещенный на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="c88e0-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="c88e0-118">Пример 3: изменение максимального размера хранилища базы данных</span><span class="sxs-lookup"><span data-stu-id="c88e0-118">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
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

<span data-ttu-id="c88e0-119">Эта команда обновляет базу данных с именем Database01, чтобы установить максимальный размер в 1 ТБ.</span><span class="sxs-lookup"><span data-stu-id="c88e0-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="c88e0-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c88e0-120">PARAMETERS</span></span>

### <span data-ttu-id="c88e0-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c88e0-121">-AsJob</span></span>
<span data-ttu-id="c88e0-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c88e0-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-123">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="c88e0-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="c88e0-124">Задержка автоматической паузы (в минутах) для базы данных (только для серверов),-1, чтобы отказаться от нее</span><span class="sxs-lookup"><span data-stu-id="c88e0-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-125">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="c88e0-125">-ComputeGeneration</span></span>
<span data-ttu-id="c88e0-126">Вычислено поколение, которое необходимо назначить.</span><span class="sxs-lookup"><span data-stu-id="c88e0-126">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-127">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="c88e0-127">-ComputeModel</span></span>
<span data-ttu-id="c88e0-128">Вычисляемая модель базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c88e0-128">Computed model of Azure Sql database.</span></span> <span data-ttu-id="c88e0-129">Неподготовленный или настроенный сервер</span><span class="sxs-lookup"><span data-stu-id="c88e0-129">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c88e0-130">-DatabaseName</span></span>
<span data-ttu-id="c88e0-131">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="c88e0-131">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c88e0-132">-DefaultProfile</span></span>
<span data-ttu-id="c88e0-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c88e0-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-134">-Edition</span><span class="sxs-lookup"><span data-stu-id="c88e0-134">-Edition</span></span>
<span data-ttu-id="c88e0-135">Указывает выпуск для базы данных.</span><span class="sxs-lookup"><span data-stu-id="c88e0-135">Specifies the edition for the database.</span></span>
<span data-ttu-id="c88e0-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c88e0-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c88e0-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="c88e0-137">None</span></span>
- <span data-ttu-id="c88e0-138">Базового</span><span class="sxs-lookup"><span data-stu-id="c88e0-138">Basic</span></span>
- <span data-ttu-id="c88e0-139">Стандартная</span><span class="sxs-lookup"><span data-stu-id="c88e0-139">Standard</span></span>
- <span data-ttu-id="c88e0-140">Версию</span><span class="sxs-lookup"><span data-stu-id="c88e0-140">Premium</span></span>
- <span data-ttu-id="c88e0-141">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="c88e0-141">DataWarehouse</span></span>
- <span data-ttu-id="c88e0-142">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="c88e0-142">Free</span></span>
- <span data-ttu-id="c88e0-143">Показателя</span><span class="sxs-lookup"><span data-stu-id="c88e0-143">Stretch</span></span>
- <span data-ttu-id="c88e0-144">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="c88e0-144">GeneralPurpose</span></span>
- <span data-ttu-id="c88e0-145">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="c88e0-145">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-146">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c88e0-146">-ElasticPoolName</span></span>
<span data-ttu-id="c88e0-147">Указывает имя эластичного пула, в который нужно переместить базу данных.</span><span class="sxs-lookup"><span data-stu-id="c88e0-147">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c88e0-148">-LicenseType</span></span>
<span data-ttu-id="c88e0-149">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c88e0-149">The license type for the Azure Sql database.</span></span> <span data-ttu-id="c88e0-150">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c88e0-150">Possible values are:</span></span>
- <span data-ttu-id="c88e0-151">BasePrice — гибридное выгодное преимущество (AHB) для существующих владельцев лицензий SQL Server применяется скидка.</span><span class="sxs-lookup"><span data-stu-id="c88e0-151">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="c88e0-152">Стоимость базы данных для существующих владельцев лицензий SQL Server будет снижена.</span><span class="sxs-lookup"><span data-stu-id="c88e0-152">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="c88e0-153">LicenseIncluded-(AHB) для существующих владельцев лицензий SQL Server не применяется скидка на гибридные льготы для использования в Azure.</span><span class="sxs-lookup"><span data-stu-id="c88e0-153">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="c88e0-154">Цена базы данных будет включать в себя новые затраты на лицензирование SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c88e0-154">Database price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-155">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="c88e0-155">-MaxSizeBytes</span></span>
<span data-ttu-id="c88e0-156">Максимальный размер базы данных Azure SQL в байтах.</span><span class="sxs-lookup"><span data-stu-id="c88e0-156">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-157">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="c88e0-157">-MinimumCapacity</span></span>
<span data-ttu-id="c88e0-158">Минимальная емкость, которую база данных будет всегда выделена, если она не была приостановлена.</span><span class="sxs-lookup"><span data-stu-id="c88e0-158">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="c88e0-159">Только для баз данных Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c88e0-159">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: Update, VcoreBasedDatabase
Aliases: MinVCore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-160">-NewName</span><span class="sxs-lookup"><span data-stu-id="c88e0-160">-NewName</span></span>
<span data-ttu-id="c88e0-161">Новое имя, в которое нужно переименовать базу данных.</span><span class="sxs-lookup"><span data-stu-id="c88e0-161">The new name to rename the database to.</span></span>

```yaml
Type: System.String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-162">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="c88e0-162">-ReadScale</span></span>
<span data-ttu-id="c88e0-163">Параметр Read Scale (масштаб чтения), назначаемый базе данных Azure SQL. (Включено или отключено)</span><span class="sxs-lookup"><span data-stu-id="c88e0-163">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: Update, VcoreBasedDatabase
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-164">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="c88e0-164">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="c88e0-165">Указывает имя цели обслуживания, которую нужно назначить базе данных.</span><span class="sxs-lookup"><span data-stu-id="c88e0-165">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="c88e0-166">Сведения о цели обслуживания можно найти на [уровнях служб базы данных Azure SQL Server и уровне производительности](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) в сетевой библиотеке разработчиков Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c88e0-166">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c88e0-167">-ResourceGroupName</span></span>
<span data-ttu-id="c88e0-168">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="c88e0-168">Specifies the name of resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-169">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="c88e0-169">-ServerName</span></span>
<span data-ttu-id="c88e0-170">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="c88e0-170">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-171">-Теги</span><span class="sxs-lookup"><span data-stu-id="c88e0-171">-Tags</span></span>
<span data-ttu-id="c88e0-172">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="c88e0-172">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c88e0-173">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="c88e0-173">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update, VcoreBasedDatabase
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-174">-VCore</span><span class="sxs-lookup"><span data-stu-id="c88e0-174">-VCore</span></span>
<span data-ttu-id="c88e0-175">Номер Vcore для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="c88e0-175">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-176">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="c88e0-176">-ZoneRedundant</span></span>
<span data-ttu-id="c88e0-177">Избыточность зоны, связываемая с базой данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c88e0-177">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-178">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c88e0-178">-Confirm</span></span>
<span data-ttu-id="c88e0-179">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c88e0-179">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c88e0-180">-WhatIf</span></span>
<span data-ttu-id="c88e0-181">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c88e0-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c88e0-182">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c88e0-182">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c88e0-183">CommonParameters</span></span>
<span data-ttu-id="c88e0-184">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c88e0-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c88e0-185">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c88e0-185">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c88e0-186">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c88e0-186">INPUTS</span></span>

### <span data-ttu-id="c88e0-187">System. String</span><span class="sxs-lookup"><span data-stu-id="c88e0-187">System.String</span></span>

## <span data-ttu-id="c88e0-188">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c88e0-188">OUTPUTS</span></span>

### <span data-ttu-id="c88e0-189">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="c88e0-189">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="c88e0-190">Пуск</span><span class="sxs-lookup"><span data-stu-id="c88e0-190">NOTES</span></span>

## <span data-ttu-id="c88e0-191">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c88e0-191">RELATED LINKS</span></span>

[<span data-ttu-id="c88e0-192">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c88e0-192">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="c88e0-193">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c88e0-193">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="c88e0-194">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c88e0-194">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="c88e0-195">Возобновить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c88e0-195">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="c88e0-196">Приостановить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c88e0-196">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="c88e0-197">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="c88e0-197">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
