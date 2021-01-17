---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 6d737abb6c58ea8c74085f8390d7a6acbdf54dc8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420180"
---
# <span data-ttu-id="755be-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="755be-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="755be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="755be-102">SYNOPSIS</span></span>
<span data-ttu-id="755be-103">Задает свойства базы данных или перемещает существующую базу данных в эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="755be-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="755be-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="755be-104">SYNTAX</span></span>

### <span data-ttu-id="755be-105">Обновление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="755be-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="755be-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="755be-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="755be-107">Переименовать</span><span class="sxs-lookup"><span data-stu-id="755be-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="755be-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="755be-108">DESCRIPTION</span></span>
<span data-ttu-id="755be-109">Cmdlet **Set-AzSqlDatabase** задает свойства базы данных в базе данных Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="755be-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="755be-110">Этот cmdlet может изменять уровень обслуживания *(Edition),* уровень производительности *(RequestedServiceObjectiveName)* и максимальный размер хранилища *(MaxSizeBytes)* для базы данных.</span><span class="sxs-lookup"><span data-stu-id="755be-110">This cmdlet can modify the service tier (*Edition*), performance level (*RequestedServiceObjectiveName*), and storage max size (*MaxSizeBytes*) for the database.</span></span>  <span data-ttu-id="755be-111">Кроме того, вы можете указать параметр *"Властивумя",* чтобы переместить базу данных в эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="755be-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="755be-112">Если база данных уже находится в эластичном пуле, вы можете использовать параметр *RequestedServiceObjectiveName,* чтобы переместить базу данных из него в степень производительности для одной базы данных.</span><span class="sxs-lookup"><span data-stu-id="755be-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="755be-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="755be-113">EXAMPLES</span></span>

### <span data-ttu-id="755be-114">Пример 1. Обновление базы данных до стандартной базы данных S0</span><span class="sxs-lookup"><span data-stu-id="755be-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="755be-115">Эта команда обновляет базу данных с именем Database01 до стандартной базы данных S0 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="755be-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="755be-116">Пример 2. Добавление базы данных в эластичный пул</span><span class="sxs-lookup"><span data-stu-id="755be-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="755be-117">Эта команда добавляет базу данных "База данных01" в эластичный пул с именем "ЭластичныйPool01", который содержится на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="755be-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="755be-118">Пример 3. Изменение максимального размера хранилища базы данных</span><span class="sxs-lookup"><span data-stu-id="755be-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="755be-119">Эта команда обновляет базу данных с именем Database01, устанавливая для нее максимальный размер 1 ТБ.</span><span class="sxs-lookup"><span data-stu-id="755be-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

### <span data-ttu-id="755be-120">Пример 4. Обновление существующей базы данных общего назначения до уровня службы hyperscale</span><span class="sxs-lookup"><span data-stu-id="755be-120">Example 4: Update a existing General Purpose database to Hyperscale service tier</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Hyperscale" -RequestedServiceObjectiveName "HS_Gen5_2"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : 56246136-839f-4171-80af-4c28142463b1
Edition                       : Hyperscale
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : -1
Status                        : Online
CreationDate                  : 12/6/2020 5:34:16 PM
CurrentServiceObjectiveId     : 00000000-0000-0000-0000-000000000000
CurrentServiceObjectiveName   : HS_Gen5_2
RequestedServiceObjectiveName : HS_Gen5_2
RequestedServiceObjectiveId   :
ElasticPoolName               :
EarliestRestoreDate           : 12/6/2020 5:34:16 PM
Tags                          : {}
ResourceId                    : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/Server01/databases/Database01
CreateMode                    :
ReadScale                     : Enabled
ZoneRedundant                 :
Capacity                      : 2
Family                        : Gen5
SkuName                       : HS_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       :
MinimumCapacity               :
ReadReplicaCount              : 1
BackupStorageRedundancy       : Geo
```

<span data-ttu-id="755be-121">Эта команда обновляет базу данных "База данных01" с уровня службы "Общее назначение" на уровень службы "Гипер шкала".</span><span class="sxs-lookup"><span data-stu-id="755be-121">This command updates a database named Database01 from General Purpose to Hyperscale service tier.</span></span>

## <span data-ttu-id="755be-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="755be-122">PARAMETERS</span></span>

### <span data-ttu-id="755be-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="755be-123">-AsJob</span></span>
<span data-ttu-id="755be-124">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="755be-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="755be-125">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="755be-125">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="755be-126">Автоматическая приостановка задержки в минутах для базы данных (только без сервера); -1, чтобы отказаться</span><span class="sxs-lookup"><span data-stu-id="755be-126">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="755be-127">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="755be-127">-BackupStorageRedundancy</span></span>
<span data-ttu-id="755be-128">Избыточность резервного копирования хранилища, используемого для хранения резервных копий SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="755be-128">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="755be-129">Доступны такие варианты: Local (Локальный), Zone (Зона) и Geo (География).</span><span class="sxs-lookup"><span data-stu-id="755be-129">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="755be-130">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="755be-130">-ComputeGeneration</span></span>
<span data-ttu-id="755be-131">Назначимое поколение компьютеров.</span><span class="sxs-lookup"><span data-stu-id="755be-131">The compute generation to assign.</span></span>

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

### <span data-ttu-id="755be-132">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="755be-132">-ComputeModel</span></span>
<span data-ttu-id="755be-133">Вычисляемая модель базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="755be-133">Computed model of Azure Sql database.</span></span> <span data-ttu-id="755be-134">Сервер без серверов или подготовка</span><span class="sxs-lookup"><span data-stu-id="755be-134">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="755be-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="755be-135">-DatabaseName</span></span>
<span data-ttu-id="755be-136">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="755be-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="755be-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="755be-137">-DefaultProfile</span></span>
<span data-ttu-id="755be-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="755be-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="755be-139">-Edition</span><span class="sxs-lookup"><span data-stu-id="755be-139">-Edition</span></span>
<span data-ttu-id="755be-140">Выпуск для базы данных.</span><span class="sxs-lookup"><span data-stu-id="755be-140">Specifies the edition for the database.</span></span>
<span data-ttu-id="755be-141">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="755be-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="755be-142">Нет</span><span class="sxs-lookup"><span data-stu-id="755be-142">None</span></span>
- <span data-ttu-id="755be-143">Базовая</span><span class="sxs-lookup"><span data-stu-id="755be-143">Basic</span></span>
- <span data-ttu-id="755be-144">Стандартный</span><span class="sxs-lookup"><span data-stu-id="755be-144">Standard</span></span>
- <span data-ttu-id="755be-145">Premium</span><span class="sxs-lookup"><span data-stu-id="755be-145">Premium</span></span>
- <span data-ttu-id="755be-146">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="755be-146">DataWarehouse</span></span>
- <span data-ttu-id="755be-147">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="755be-147">Free</span></span>
- <span data-ttu-id="755be-148">Растяжение</span><span class="sxs-lookup"><span data-stu-id="755be-148">Stretch</span></span>
- <span data-ttu-id="755be-149">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="755be-149">GeneralPurpose</span></span>
- <span data-ttu-id="755be-150">Hyperscale</span><span class="sxs-lookup"><span data-stu-id="755be-150">Hyperscale</span></span>
- <span data-ttu-id="755be-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="755be-151">BusinessCritical</span></span>

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

### <span data-ttu-id="755be-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="755be-152">-ElasticPoolName</span></span>
<span data-ttu-id="755be-153">Определяет имя эластичного пула, в который нужно переместить базу данных.</span><span class="sxs-lookup"><span data-stu-id="755be-153">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="755be-154">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="755be-154">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="755be-155">Количество дополнительных реплик для чтения, связанных с базой данных.</span><span class="sxs-lookup"><span data-stu-id="755be-155">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="755be-156">Только для hyperscale edition.</span><span class="sxs-lookup"><span data-stu-id="755be-156">For Hyperscale edition only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases: ReadReplicaCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="755be-157">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="755be-157">-LicenseType</span></span>
<span data-ttu-id="755be-158">Тип лицензии для базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="755be-158">The license type for the Azure Sql database.</span></span> <span data-ttu-id="755be-159">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="755be-159">Possible values are:</span></span>
- <span data-ttu-id="755be-160">BasePrice — скидка на Azure Hybrid Benefit (AHB) для существующих SQL Server лицензий применяется.</span><span class="sxs-lookup"><span data-stu-id="755be-160">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="755be-161">Цена базы данных будет дисконтна для существующих SQL Server лицензий.</span><span class="sxs-lookup"><span data-stu-id="755be-161">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="755be-162">LicenseIncluded — скидка на azure Hybrid Benefit (AHB) для существующих SQL Server лицензий не применяется.</span><span class="sxs-lookup"><span data-stu-id="755be-162">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="755be-163">Цена базы данных будет включать новые SQL Server стоимость лицензий.</span><span class="sxs-lookup"><span data-stu-id="755be-163">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="755be-164">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="755be-164">-MaxSizeBytes</span></span>
<span data-ttu-id="755be-165">Максимальный размер базы данных Azure SQL вбайтов.</span><span class="sxs-lookup"><span data-stu-id="755be-165">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="755be-166">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="755be-166">-MinimumCapacity</span></span>
<span data-ttu-id="755be-167">Минимальная пропускная способность, выделенная для базы данных, если не приостановлена.</span><span class="sxs-lookup"><span data-stu-id="755be-167">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="755be-168">Только для серверных баз данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="755be-168">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="755be-169">-NewName</span><span class="sxs-lookup"><span data-stu-id="755be-169">-NewName</span></span>
<span data-ttu-id="755be-170">Новое имя, которое нужно переименовать базу данных.</span><span class="sxs-lookup"><span data-stu-id="755be-170">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="755be-171">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="755be-171">-ReadScale</span></span>
<span data-ttu-id="755be-172">Если эта возможность включена, соединения, для которые настроено чтение в строке подключения приложения, могут быть маршрутизироваться на вторичную реплику для чтения.</span><span class="sxs-lookup"><span data-stu-id="755be-172">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="755be-173">Это свойство можно настроить только для баз данных премиум- и бизнес-критических версий.</span><span class="sxs-lookup"><span data-stu-id="755be-173">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="755be-174">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="755be-174">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="755be-175">Указывает имя цели обслуживания, которая будет назначаться базе данных.</span><span class="sxs-lookup"><span data-stu-id="755be-175">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="755be-176">Сведения о цели обслуживания см. в SQL и уровнях производительности службы баз данных [Azure](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="755be-176">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="755be-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="755be-177">-ResourceGroupName</span></span>
<span data-ttu-id="755be-178">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="755be-178">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="755be-179">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="755be-179">-SecondaryType</span></span>
<span data-ttu-id="755be-180">Дополнительный тип базы данных, если он является дополнительным.</span><span class="sxs-lookup"><span data-stu-id="755be-180">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="755be-181">Допустимые значения: Geo и Named.</span><span class="sxs-lookup"><span data-stu-id="755be-181">Valid values are Geo and Named.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Named, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="755be-182">-ServerName</span><span class="sxs-lookup"><span data-stu-id="755be-182">-ServerName</span></span>
<span data-ttu-id="755be-183">Имя сервера, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="755be-183">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="755be-184">-Теги</span><span class="sxs-lookup"><span data-stu-id="755be-184">-Tags</span></span>
<span data-ttu-id="755be-185">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="755be-185">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="755be-186">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="755be-186">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="755be-187">-VCore</span><span class="sxs-lookup"><span data-stu-id="755be-187">-VCore</span></span>
<span data-ttu-id="755be-188">Номер VCORE для базы данных Azure Sql</span><span class="sxs-lookup"><span data-stu-id="755be-188">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="755be-189">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="755be-189">-ZoneRedundant</span></span>
<span data-ttu-id="755be-190">Избыточность зоны, которая связывается с базой данных Sql Azure</span><span class="sxs-lookup"><span data-stu-id="755be-190">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="755be-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="755be-191">-Confirm</span></span>
<span data-ttu-id="755be-192">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="755be-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="755be-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="755be-193">-WhatIf</span></span>
<span data-ttu-id="755be-194">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="755be-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="755be-195">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="755be-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="755be-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755be-196">CommonParameters</span></span>
<span data-ttu-id="755be-197">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="755be-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755be-198">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="755be-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755be-199">INPUTS</span><span class="sxs-lookup"><span data-stu-id="755be-199">INPUTS</span></span>

### <span data-ttu-id="755be-200">System.String</span><span class="sxs-lookup"><span data-stu-id="755be-200">System.String</span></span>

## <span data-ttu-id="755be-201">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="755be-201">OUTPUTS</span></span>

### <span data-ttu-id="755be-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="755be-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="755be-203">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="755be-203">NOTES</span></span>

## <span data-ttu-id="755be-204">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="755be-204">RELATED LINKS</span></span>

[<span data-ttu-id="755be-205">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="755be-205">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="755be-206">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="755be-206">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="755be-207">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="755be-207">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="755be-208">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="755be-208">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="755be-209">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="755be-209">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="755be-210">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="755be-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
