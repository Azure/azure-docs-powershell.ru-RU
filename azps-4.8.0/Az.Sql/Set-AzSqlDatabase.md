---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: f236c00f50d9ec74a98def114d08ab851e5a89f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243888"
---
# <span data-ttu-id="194c8-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="194c8-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="194c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="194c8-102">SYNOPSIS</span></span>
<span data-ttu-id="194c8-103">Задает свойства базы данных или перемещает существующую базу данных в эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="194c8-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="194c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="194c8-104">SYNTAX</span></span>

### <span data-ttu-id="194c8-105">Обновление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="194c8-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="194c8-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="194c8-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="194c8-107">Переименовав</span><span class="sxs-lookup"><span data-stu-id="194c8-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="194c8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="194c8-108">DESCRIPTION</span></span>
<span data-ttu-id="194c8-109">Командлет **Set-AzSqlDatabase** задает свойства базы данных в базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="194c8-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="194c8-110">Этот командлет может изменить уровень служб ( *выпуск* ), уровень производительности ( *RequestedServiceObjectiveName* ) и максимальный размер хранилища ( *MaxSizeBytes* ) для базы данных.</span><span class="sxs-lookup"><span data-stu-id="194c8-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="194c8-111">Кроме того, вы можете указать параметр *ElasticPoolName* , чтобы переместить базу данных в эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="194c8-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="194c8-112">Если база данных уже находится в пуле эластичных БД, вы можете использовать параметр *RequestedServiceObjectiveName* , чтобы переместить базу данных из эластичного пула и на уровень производительности для одной базы данных.</span><span class="sxs-lookup"><span data-stu-id="194c8-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="194c8-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="194c8-113">EXAMPLES</span></span>

### <span data-ttu-id="194c8-114">Пример 1: обновление базы данных до стандартной базы данных S0</span><span class="sxs-lookup"><span data-stu-id="194c8-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="194c8-115">Эта команда обновляет базу данных с именем Database01 на стандартную базу данных S0 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="194c8-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="194c8-116">Пример 2: Добавление базы данных в эластичный пул</span><span class="sxs-lookup"><span data-stu-id="194c8-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="194c8-117">Эта команда добавляет базу данных с именем Database01 в пул эластичных БД с именем ElasticPool01, размещенный на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="194c8-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="194c8-118">Пример 3: изменение максимального размера хранилища базы данных</span><span class="sxs-lookup"><span data-stu-id="194c8-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="194c8-119">Эта команда обновляет базу данных с именем Database01, чтобы установить максимальный размер в 1 ТБ.</span><span class="sxs-lookup"><span data-stu-id="194c8-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="194c8-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="194c8-120">PARAMETERS</span></span>

### <span data-ttu-id="194c8-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="194c8-121">-AsJob</span></span>
<span data-ttu-id="194c8-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="194c8-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="194c8-123">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="194c8-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="194c8-124">Задержка автоматической паузы (в минутах) для базы данных (только для серверов),-1, чтобы отказаться от нее</span><span class="sxs-lookup"><span data-stu-id="194c8-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="194c8-125">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="194c8-125">-BackupStorageRedundancy</span></span>
<span data-ttu-id="194c8-126">Избыточное резервное хранилище, используемое для хранения резервных копий базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="194c8-126">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="194c8-127">Доступны следующие параметры: local, Zone и Geo.</span><span class="sxs-lookup"><span data-stu-id="194c8-127">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="194c8-128">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="194c8-128">-ComputeGeneration</span></span>
<span data-ttu-id="194c8-129">Вычислено поколение, которое необходимо назначить.</span><span class="sxs-lookup"><span data-stu-id="194c8-129">The compute generation to assign.</span></span>

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

### <span data-ttu-id="194c8-130">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="194c8-130">-ComputeModel</span></span>
<span data-ttu-id="194c8-131">Вычисляемая модель базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="194c8-131">Computed model of Azure Sql database.</span></span> <span data-ttu-id="194c8-132">Неподготовленный или настроенный сервер</span><span class="sxs-lookup"><span data-stu-id="194c8-132">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="194c8-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="194c8-133">-DatabaseName</span></span>
<span data-ttu-id="194c8-134">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="194c8-134">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="194c8-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="194c8-135">-DefaultProfile</span></span>
<span data-ttu-id="194c8-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="194c8-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="194c8-137">-Edition</span><span class="sxs-lookup"><span data-stu-id="194c8-137">-Edition</span></span>
<span data-ttu-id="194c8-138">Указывает выпуск для базы данных.</span><span class="sxs-lookup"><span data-stu-id="194c8-138">Specifies the edition for the database.</span></span>
<span data-ttu-id="194c8-139">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="194c8-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="194c8-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="194c8-140">None</span></span>
- <span data-ttu-id="194c8-141">Базового</span><span class="sxs-lookup"><span data-stu-id="194c8-141">Basic</span></span>
- <span data-ttu-id="194c8-142">Стандартная</span><span class="sxs-lookup"><span data-stu-id="194c8-142">Standard</span></span>
- <span data-ttu-id="194c8-143">Версию</span><span class="sxs-lookup"><span data-stu-id="194c8-143">Premium</span></span>
- <span data-ttu-id="194c8-144">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="194c8-144">DataWarehouse</span></span>
- <span data-ttu-id="194c8-145">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="194c8-145">Free</span></span>
- <span data-ttu-id="194c8-146">Показателя</span><span class="sxs-lookup"><span data-stu-id="194c8-146">Stretch</span></span>
- <span data-ttu-id="194c8-147">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="194c8-147">GeneralPurpose</span></span>
- <span data-ttu-id="194c8-148">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="194c8-148">BusinessCritical</span></span>

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

### <span data-ttu-id="194c8-149">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="194c8-149">-ElasticPoolName</span></span>
<span data-ttu-id="194c8-150">Указывает имя эластичного пула, в который нужно переместить базу данных.</span><span class="sxs-lookup"><span data-stu-id="194c8-150">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="194c8-151">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="194c8-151">-LicenseType</span></span>
<span data-ttu-id="194c8-152">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="194c8-152">The license type for the Azure Sql database.</span></span> <span data-ttu-id="194c8-153">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="194c8-153">Possible values are:</span></span>
- <span data-ttu-id="194c8-154">BasePrice — гибридное выгодное преимущество (AHB) для существующих владельцев лицензий SQL Server применяется скидка.</span><span class="sxs-lookup"><span data-stu-id="194c8-154">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="194c8-155">Стоимость базы данных для существующих владельцев лицензий SQL Server будет снижена.</span><span class="sxs-lookup"><span data-stu-id="194c8-155">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="194c8-156">LicenseIncluded-(AHB) для существующих владельцев лицензий SQL Server не применяется скидка на гибридные льготы для использования в Azure.</span><span class="sxs-lookup"><span data-stu-id="194c8-156">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="194c8-157">Цена базы данных будет включать в себя новые затраты на лицензирование SQL Server.</span><span class="sxs-lookup"><span data-stu-id="194c8-157">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="194c8-158">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="194c8-158">-MaxSizeBytes</span></span>
<span data-ttu-id="194c8-159">Максимальный размер базы данных Azure SQL в байтах.</span><span class="sxs-lookup"><span data-stu-id="194c8-159">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="194c8-160">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="194c8-160">-MinimumCapacity</span></span>
<span data-ttu-id="194c8-161">Минимальная емкость, которую база данных будет всегда выделена, если она не была приостановлена.</span><span class="sxs-lookup"><span data-stu-id="194c8-161">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="194c8-162">Только для баз данных Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="194c8-162">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: Update, VcoreBasedDatabase
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="194c8-163">-NewName</span><span class="sxs-lookup"><span data-stu-id="194c8-163">-NewName</span></span>
<span data-ttu-id="194c8-164">Новое имя, в которое нужно переименовать базу данных.</span><span class="sxs-lookup"><span data-stu-id="194c8-164">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="194c8-165">-ReadReplicaCount</span><span class="sxs-lookup"><span data-stu-id="194c8-165">-ReadReplicaCount</span></span>
<span data-ttu-id="194c8-166">Количество вторичных реплик (только для чтения), связанных с базой данных.</span><span class="sxs-lookup"><span data-stu-id="194c8-166">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="194c8-167">Только для среды с масштабированием.</span><span class="sxs-lookup"><span data-stu-id="194c8-167">For Hyperscale edition only.</span></span>

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

### <span data-ttu-id="194c8-168">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="194c8-168">-ReadScale</span></span>
<span data-ttu-id="194c8-169">Если этот параметр включен, в строке подключения для подключений, для которых определена цель приложения ReadOnly, может перенаправляться в вторичную реплику ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="194c8-169">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="194c8-170">Это свойство можно задать только для баз данных Premium и бизнес-критических.</span><span class="sxs-lookup"><span data-stu-id="194c8-170">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="194c8-171">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="194c8-171">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="194c8-172">Указывает имя цели обслуживания, которую нужно назначить базе данных.</span><span class="sxs-lookup"><span data-stu-id="194c8-172">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="194c8-173">Сведения о цели обслуживания можно найти на [уровнях служб базы данных Azure SQL Server и уровне производительности](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) в сетевой библиотеке разработчиков Microsoft.</span><span class="sxs-lookup"><span data-stu-id="194c8-173">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="194c8-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="194c8-174">-ResourceGroupName</span></span>
<span data-ttu-id="194c8-175">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="194c8-175">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="194c8-176">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="194c8-176">-ServerName</span></span>
<span data-ttu-id="194c8-177">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="194c8-177">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="194c8-178">-Теги</span><span class="sxs-lookup"><span data-stu-id="194c8-178">-Tags</span></span>
<span data-ttu-id="194c8-179">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="194c8-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="194c8-180">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="194c8-180">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="194c8-181">-VCore</span><span class="sxs-lookup"><span data-stu-id="194c8-181">-VCore</span></span>
<span data-ttu-id="194c8-182">Номер Vcore для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="194c8-182">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="194c8-183">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="194c8-183">-ZoneRedundant</span></span>
<span data-ttu-id="194c8-184">Избыточность зоны, связываемая с базой данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="194c8-184">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="194c8-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="194c8-185">-Confirm</span></span>
<span data-ttu-id="194c8-186">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="194c8-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="194c8-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="194c8-187">-WhatIf</span></span>
<span data-ttu-id="194c8-188">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="194c8-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="194c8-189">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="194c8-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="194c8-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="194c8-190">CommonParameters</span></span>
<span data-ttu-id="194c8-191">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="194c8-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="194c8-192">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="194c8-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="194c8-193">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="194c8-193">INPUTS</span></span>

### <span data-ttu-id="194c8-194">System. String</span><span class="sxs-lookup"><span data-stu-id="194c8-194">System.String</span></span>

## <span data-ttu-id="194c8-195">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="194c8-195">OUTPUTS</span></span>

### <span data-ttu-id="194c8-196">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="194c8-196">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="194c8-197">Пуск</span><span class="sxs-lookup"><span data-stu-id="194c8-197">NOTES</span></span>

## <span data-ttu-id="194c8-198">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="194c8-198">RELATED LINKS</span></span>

[<span data-ttu-id="194c8-199">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="194c8-199">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="194c8-200">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="194c8-200">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="194c8-201">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="194c8-201">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="194c8-202">Возобновить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="194c8-202">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="194c8-203">Приостановить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="194c8-203">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="194c8-204">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="194c8-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
