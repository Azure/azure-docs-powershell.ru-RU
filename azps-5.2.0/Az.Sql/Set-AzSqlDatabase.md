---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 15f9aee8e278a1b33330508a10487e3847820891
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398823"
---
# <span data-ttu-id="2f4c4-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2f4c4-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="2f4c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f4c4-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4c4-103">Задает свойства базы данных или перемещает существующую базу данных в эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="2f4c4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2f4c4-104">SYNTAX</span></span>

### <span data-ttu-id="2f4c4-105">Обновление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2f4c4-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f4c4-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="2f4c4-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f4c4-107">Переименовать</span><span class="sxs-lookup"><span data-stu-id="2f4c4-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f4c4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f4c4-108">DESCRIPTION</span></span>
<span data-ttu-id="2f4c4-109">Cmdlet **Set-AzSqlDatabase** задает свойства базы данных в базе данных Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="2f4c4-110">Этот cmdlet может изменять уровень обслуживания *(Edition),* уровень производительности *(RequestedServiceObjectiveName)* и максимальный размер хранилища *(MaxSizeBytes)* для базы данных.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-110">This cmdlet can modify the service tier (*Edition*), performance level (*RequestedServiceObjectiveName*), and storage max size (*MaxSizeBytes*) for the database.</span></span>  <span data-ttu-id="2f4c4-111">Кроме того, вы можете указать параметр *"Властивумя",* чтобы переместить базу данных в эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="2f4c4-112">Если база данных уже находится в эластичном пуле, вы можете использовать параметр *RequestedServiceObjectiveName,* чтобы переместить базу данных из него в степень производительности для одной базы данных.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="2f4c4-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2f4c4-113">EXAMPLES</span></span>

### <span data-ttu-id="2f4c4-114">Пример 1. Обновление базы данных до стандартной базы данных S0</span><span class="sxs-lookup"><span data-stu-id="2f4c4-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="2f4c4-115">Эта команда обновляет базу данных с именем Database01 до стандартной базы данных S0 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="2f4c4-116">Пример 2. Добавление базы данных в эластичный пул</span><span class="sxs-lookup"><span data-stu-id="2f4c4-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="2f4c4-117">Эта команда добавляет базу данных "База данных01" в эластичный пул с именем "ЭластичныйPool01", который содержится на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="2f4c4-118">Пример 3. Изменение максимального размера хранилища базы данных</span><span class="sxs-lookup"><span data-stu-id="2f4c4-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="2f4c4-119">Эта команда обновляет базу данных с именем Database01, устанавливая для нее максимальный размер 1 ТБ.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="2f4c4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f4c4-120">PARAMETERS</span></span>

### <span data-ttu-id="2f4c4-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f4c4-121">-AsJob</span></span>
<span data-ttu-id="2f4c4-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2f4c4-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f4c4-123">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="2f4c4-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="2f4c4-124">Автоматическая приостановка задержки в минутах для базы данных (только без сервера); -1, чтобы отказаться</span><span class="sxs-lookup"><span data-stu-id="2f4c4-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="2f4c4-125">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="2f4c4-125">-BackupStorageRedundancy</span></span>
<span data-ttu-id="2f4c4-126">Избыточность резервного копирования хранилища, используемого для хранения резервных копий SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-126">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="2f4c4-127">Доступны такие варианты: Local (Локальный), Zone (Зона) и Geo (География).</span><span class="sxs-lookup"><span data-stu-id="2f4c4-127">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="2f4c4-128">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="2f4c4-128">-ComputeGeneration</span></span>
<span data-ttu-id="2f4c4-129">Назначимое поколение компьютеров.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-129">The compute generation to assign.</span></span>

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

### <span data-ttu-id="2f4c4-130">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="2f4c4-130">-ComputeModel</span></span>
<span data-ttu-id="2f4c4-131">Вычисляемая модель базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-131">Computed model of Azure Sql database.</span></span> <span data-ttu-id="2f4c4-132">Сервер без серверов или подготовка</span><span class="sxs-lookup"><span data-stu-id="2f4c4-132">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="2f4c4-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f4c4-133">-DatabaseName</span></span>
<span data-ttu-id="2f4c4-134">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-134">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="2f4c4-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f4c4-135">-DefaultProfile</span></span>
<span data-ttu-id="2f4c4-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2f4c4-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f4c4-137">-Edition</span><span class="sxs-lookup"><span data-stu-id="2f4c4-137">-Edition</span></span>
<span data-ttu-id="2f4c4-138">Выпуск для базы данных.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-138">Specifies the edition for the database.</span></span>
<span data-ttu-id="2f4c4-139">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="2f4c4-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2f4c4-140">Нет</span><span class="sxs-lookup"><span data-stu-id="2f4c4-140">None</span></span>
- <span data-ttu-id="2f4c4-141">Базовая</span><span class="sxs-lookup"><span data-stu-id="2f4c4-141">Basic</span></span>
- <span data-ttu-id="2f4c4-142">Стандартный</span><span class="sxs-lookup"><span data-stu-id="2f4c4-142">Standard</span></span>
- <span data-ttu-id="2f4c4-143">Premium</span><span class="sxs-lookup"><span data-stu-id="2f4c4-143">Premium</span></span>
- <span data-ttu-id="2f4c4-144">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="2f4c4-144">DataWarehouse</span></span>
- <span data-ttu-id="2f4c4-145">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="2f4c4-145">Free</span></span>
- <span data-ttu-id="2f4c4-146">Растяжение</span><span class="sxs-lookup"><span data-stu-id="2f4c4-146">Stretch</span></span>
- <span data-ttu-id="2f4c4-147">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="2f4c4-147">GeneralPurpose</span></span>
- <span data-ttu-id="2f4c4-148">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="2f4c4-148">BusinessCritical</span></span>

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

### <span data-ttu-id="2f4c4-149">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2f4c4-149">-ElasticPoolName</span></span>
<span data-ttu-id="2f4c4-150">Определяет имя эластичного пула, в который нужно переместить базу данных.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-150">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="2f4c4-151">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="2f4c4-151">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="2f4c4-152">Количество дополнительных реплик для чтения, связанных с базой данных.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-152">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="2f4c4-153">Только для hyperscale edition.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-153">For Hyperscale edition only.</span></span>

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

### <span data-ttu-id="2f4c4-154">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2f4c4-154">-LicenseType</span></span>
<span data-ttu-id="2f4c4-155">Тип лицензии для базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-155">The license type for the Azure Sql database.</span></span> <span data-ttu-id="2f4c4-156">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="2f4c4-156">Possible values are:</span></span>
- <span data-ttu-id="2f4c4-157">BasePrice — скидка на Azure Hybrid Benefit (AHB) для существующих SQL Server лицензий применяется.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-157">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="2f4c4-158">Цена базы данных будет дисконтна для существующих SQL Server лицензий.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-158">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="2f4c4-159">LicenseIncluded — скидка на azure Hybrid Benefit (AHB) для существующих SQL Server лицензий не применяется.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-159">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="2f4c4-160">Цена базы данных будет включать новые SQL Server стоимость лицензий.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-160">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="2f4c4-161">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="2f4c4-161">-MaxSizeBytes</span></span>
<span data-ttu-id="2f4c4-162">Максимальный размер базы данных Azure SQL вбайтов.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-162">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="2f4c4-163">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="2f4c4-163">-MinimumCapacity</span></span>
<span data-ttu-id="2f4c4-164">Минимальная пропускная способность, выделенная для базы данных, если не приостановлена.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-164">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="2f4c4-165">Только для серверных баз данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-165">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="2f4c4-166">-NewName</span><span class="sxs-lookup"><span data-stu-id="2f4c4-166">-NewName</span></span>
<span data-ttu-id="2f4c4-167">Новое имя, которое нужно переименовать базу данных.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-167">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="2f4c4-168">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="2f4c4-168">-ReadScale</span></span>
<span data-ttu-id="2f4c4-169">Если эта возможность включена, соединения, для которые настроено чтение в строке подключения приложения, могут быть маршрутизироваться на вторичную реплику для чтения.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-169">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="2f4c4-170">Это свойство можно настроить только для баз данных премиум- и бизнес-критических версий.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-170">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="2f4c4-171">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="2f4c4-171">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="2f4c4-172">Указывает имя цели обслуживания, которая будет назначаться базе данных.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-172">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="2f4c4-173">Сведения о цели обслуживания см. в SQL и уровнях производительности службы баз данных [Azure](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-173">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="2f4c4-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f4c4-174">-ResourceGroupName</span></span>
<span data-ttu-id="2f4c4-175">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-175">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="2f4c4-176">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="2f4c4-176">-SecondaryType</span></span>
<span data-ttu-id="2f4c4-177">Дополнительный тип базы данных, если он является дополнительным.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-177">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="2f4c4-178">Допустимые значения: Geo и Named.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-178">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="2f4c4-179">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2f4c4-179">-ServerName</span></span>
<span data-ttu-id="2f4c4-180">Имя сервера, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-180">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="2f4c4-181">-Теги</span><span class="sxs-lookup"><span data-stu-id="2f4c4-181">-Tags</span></span>
<span data-ttu-id="2f4c4-182">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-182">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2f4c4-183">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="2f4c4-183">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2f4c4-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="2f4c4-184">-VCore</span></span>
<span data-ttu-id="2f4c4-185">Номер VCORE для базы данных Azure Sql</span><span class="sxs-lookup"><span data-stu-id="2f4c4-185">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="2f4c4-186">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="2f4c4-186">-ZoneRedundant</span></span>
<span data-ttu-id="2f4c4-187">Избыточность зоны, которая связывается с базой данных Sql Azure</span><span class="sxs-lookup"><span data-stu-id="2f4c4-187">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="2f4c4-188">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f4c4-188">-Confirm</span></span>
<span data-ttu-id="2f4c4-189">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f4c4-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f4c4-190">-WhatIf</span></span>
<span data-ttu-id="2f4c4-191">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f4c4-192">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f4c4-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4c4-193">CommonParameters</span></span>
<span data-ttu-id="2f4c4-194">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f4c4-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4c4-195">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f4c4-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4c4-196">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f4c4-196">INPUTS</span></span>

### <span data-ttu-id="2f4c4-197">System.String</span><span class="sxs-lookup"><span data-stu-id="2f4c4-197">System.String</span></span>

## <span data-ttu-id="2f4c4-198">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2f4c4-198">OUTPUTS</span></span>

### <span data-ttu-id="2f4c4-199">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2f4c4-199">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="2f4c4-200">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2f4c4-200">NOTES</span></span>

## <span data-ttu-id="2f4c4-201">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f4c4-201">RELATED LINKS</span></span>

[<span data-ttu-id="2f4c4-202">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2f4c4-202">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="2f4c4-203">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2f4c4-203">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="2f4c4-204">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2f4c4-204">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="2f4c4-205">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2f4c4-205">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="2f4c4-206">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2f4c4-206">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="2f4c4-207">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="2f4c4-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
