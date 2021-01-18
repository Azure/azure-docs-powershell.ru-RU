---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: f92af476c7a9cf642512f3aa338069ab37b1c840
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507605"
---
# <span data-ttu-id="366ee-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="366ee-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="366ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="366ee-102">SYNOPSIS</span></span>
<span data-ttu-id="366ee-103">Создает базу данных или эластичную базу данных.</span><span class="sxs-lookup"><span data-stu-id="366ee-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="366ee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="366ee-104">SYNTAX</span></span>

### <span data-ttu-id="366ee-105">DtuBasedDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="366ee-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-Force] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="366ee-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="366ee-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] [-Force] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="366ee-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="366ee-107">DESCRIPTION</span></span>
<span data-ttu-id="366ee-108">Для создания базы данных Azure SQL новый **azSqlDatabase.**</span><span class="sxs-lookup"><span data-stu-id="366ee-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="366ee-109">Вы также можете создать эластичную базу данных, задав *параметр "ЭластичнаяPoolName"* в существующем эластичном пуле.</span><span class="sxs-lookup"><span data-stu-id="366ee-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="366ee-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="366ee-110">EXAMPLES</span></span>

### <span data-ttu-id="366ee-111">Пример 1. Создание базы данных на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="366ee-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="366ee-112">Эта команда создает базу данных с именем Database01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="366ee-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="366ee-113">Пример 2. Создание эластичной базы данных на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="366ee-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="366ee-114">Эта команда создает базу данных "База данных02" в эластичном пуле Под названием "Проектный", который на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="366ee-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="366ee-115">Пример 3. Создание базы данных "Vcore" на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="366ee-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database03
Location                      : Central US
DatabaseId                    : 34d9d561-42a7-484e-bf05-62ddef8000ab
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveName   : GP_Gen4_2
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   : LicenseIncluded
Tags                          :
```

<span data-ttu-id="366ee-116">Эта команда создает базу данных VCORE с именем Database03 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="366ee-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="366ee-117">Пример 4. Создание базы данных Без сервера на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="366ee-117">Example 4: Create an Serverless database on the specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database04" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen5" -ComputeModel Serverless
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database04
Location                      : Central US
DatabaseId                    : ef5a9698-012c-4def-8d94-7f6bfb7b4f04
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 34359738368
Status                        : Online
CreationDate                  : 4/12/2019 11:20:29 PM
CurrentServiceObjectiveName   : GP_S_Gen5_2
RequestedServiceObjectiveName : GP_S_Gen5_2
ElasticPoolName               :
EarliestRestoreDate           : 4/12/2019 11:50:29 PM
Tags                          :
CreateMode                    :
ReadScale                     : Disabled
ZoneRedundant                 : False
Capacity                      : 2
Family                        : Gen5
SkuName                       : GP_S_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       : 360
MinimumCapacity          : 0.5
```

<span data-ttu-id="366ee-118">Эта команда создает базу данных Без сервера с именем Database04 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="366ee-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="366ee-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="366ee-119">PARAMETERS</span></span>

### <span data-ttu-id="366ee-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="366ee-120">-AsJob</span></span>
<span data-ttu-id="366ee-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="366ee-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="366ee-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="366ee-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="366ee-123">Автоматическая приостановка задержки в минутах для базы данных (только для серверов); -1, чтобы отказаться</span><span class="sxs-lookup"><span data-stu-id="366ee-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ee-124">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="366ee-124">-BackupStorageRedundancy</span></span>
<span data-ttu-id="366ee-125">Избыточность резервного копирования хранилища, используемого для хранения резервных копий SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="366ee-125">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="366ee-126">Доступны такие варианты: Local (Локальный), Zone (Зона) и Geo (География).</span><span class="sxs-lookup"><span data-stu-id="366ee-126">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="366ee-127">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="366ee-127">-CatalogCollation</span></span>
<span data-ttu-id="366ee-128">Указывает имя для каталога SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="366ee-128">Specifies the name of the SQL database catalog collation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ee-129">-CollationName</span><span class="sxs-lookup"><span data-stu-id="366ee-129">-CollationName</span></span>
<span data-ttu-id="366ee-130">Определяет имя для SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="366ee-130">Specifies the name of the SQL database collation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ee-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="366ee-131">-ComputeGeneration</span></span>
<span data-ttu-id="366ee-132">Назначимое поколение компьютеров.</span><span class="sxs-lookup"><span data-stu-id="366ee-132">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ee-133">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="366ee-133">-ComputeModel</span></span>
<span data-ttu-id="366ee-134">Модель вычислений для базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="366ee-134">The compute model for Azure Sql database.</span></span> <span data-ttu-id="366ee-135">Сервер без серверов или подготовка</span><span class="sxs-lookup"><span data-stu-id="366ee-135">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ee-136">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="366ee-136">-DatabaseName</span></span>
<span data-ttu-id="366ee-137">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="366ee-137">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ee-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="366ee-138">-DefaultProfile</span></span>
<span data-ttu-id="366ee-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="366ee-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="366ee-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="366ee-140">-Edition</span></span>
<span data-ttu-id="366ee-141">Выпуск, который нужно назначить базе данных.</span><span class="sxs-lookup"><span data-stu-id="366ee-141">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="366ee-142">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="366ee-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="366ee-143">Нет</span><span class="sxs-lookup"><span data-stu-id="366ee-143">None</span></span>
- <span data-ttu-id="366ee-144">Базовая</span><span class="sxs-lookup"><span data-stu-id="366ee-144">Basic</span></span>
- <span data-ttu-id="366ee-145">Стандартный</span><span class="sxs-lookup"><span data-stu-id="366ee-145">Standard</span></span>
- <span data-ttu-id="366ee-146">Premium</span><span class="sxs-lookup"><span data-stu-id="366ee-146">Premium</span></span>
- <span data-ttu-id="366ee-147">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="366ee-147">DataWarehouse</span></span>
- <span data-ttu-id="366ee-148">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="366ee-148">Free</span></span>
- <span data-ttu-id="366ee-149">Растяжение</span><span class="sxs-lookup"><span data-stu-id="366ee-149">Stretch</span></span>
- <span data-ttu-id="366ee-150">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="366ee-150">GeneralPurpose</span></span>
- <span data-ttu-id="366ee-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="366ee-151">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ee-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="366ee-152">-ElasticPoolName</span></span>
<span data-ttu-id="366ee-153">Определяет имя эластичного пула, в который нужно поместить базу данных.</span><span class="sxs-lookup"><span data-stu-id="366ee-153">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ee-154">-Force</span><span class="sxs-lookup"><span data-stu-id="366ee-154">-Force</span></span>
<span data-ttu-id="366ee-155">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="366ee-155">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="366ee-156">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="366ee-156">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="366ee-157">Количество реплицируемых реплицов, связанных с базой данных, в которую могут маршрутизироваться подключения с намерением приложения в чтение.</span><span class="sxs-lookup"><span data-stu-id="366ee-157">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="366ee-158">Это свойство можно настроить только для баз данных hyperscale edition.</span><span class="sxs-lookup"><span data-stu-id="366ee-158">This property is only settable for Hyperscale edition databases.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ReadReplicaCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ee-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="366ee-159">-LicenseType</span></span>
<span data-ttu-id="366ee-160">Тип лицензии для базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="366ee-160">The license type for the Azure Sql database.</span></span> <span data-ttu-id="366ee-161">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="366ee-161">Possible values are:</span></span>
- <span data-ttu-id="366ee-162">BasePrice — скидка на Azure Hybrid Benefit (AHB) для существующих SQL Server лицензий применяется.</span><span class="sxs-lookup"><span data-stu-id="366ee-162">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="366ee-163">Цена базы данных будет дисконтна для существующих SQL Server лицензий.</span><span class="sxs-lookup"><span data-stu-id="366ee-163">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="366ee-164">LicenseIncluded — скидка на azure Hybrid Benefit (AHB) для существующих SQL Server лицензий не применяется.</span><span class="sxs-lookup"><span data-stu-id="366ee-164">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="366ee-165">Цена базы данных будет включать новые SQL Server стоимость лицензий.</span><span class="sxs-lookup"><span data-stu-id="366ee-165">Database price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ee-166">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="366ee-166">-MaxSizeBytes</span></span>
<span data-ttu-id="366ee-167">Максимальный размер базы данных в этихбайтах.</span><span class="sxs-lookup"><span data-stu-id="366ee-167">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ee-168">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="366ee-168">-MinimumCapacity</span></span>
<span data-ttu-id="366ee-169">Минимальная пропускная способность, выделенная для базы данных, если не приостановлена.</span><span class="sxs-lookup"><span data-stu-id="366ee-169">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="366ee-170">Только для серверных баз данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="366ee-170">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ee-171">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="366ee-171">-ReadScale</span></span>
<span data-ttu-id="366ee-172">Если эта возможность включена, соединения, для которые настроено чтение в строке подключения приложения, могут быть маршрутизироваться на вторичную реплику для чтения.</span><span class="sxs-lookup"><span data-stu-id="366ee-172">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="366ee-173">Это свойство можно настроить только для баз данных премиум- и бизнес-критических версий.</span><span class="sxs-lookup"><span data-stu-id="366ee-173">This property is only settable for Premium and Business Critical databases.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ee-174">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="366ee-174">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="366ee-175">Указывает имя цели обслуживания, которая будет назначаться базе данных.</span><span class="sxs-lookup"><span data-stu-id="366ee-175">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ee-176">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="366ee-176">-ResourceGroupName</span></span>
<span data-ttu-id="366ee-177">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="366ee-177">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="366ee-178">-SampleName</span><span class="sxs-lookup"><span data-stu-id="366ee-178">-SampleName</span></span>
<span data-ttu-id="366ee-179">Имя образца схемы, применяемого при создании базы данных.</span><span class="sxs-lookup"><span data-stu-id="366ee-179">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ee-180">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="366ee-180">-SecondaryType</span></span>
<span data-ttu-id="366ee-181">Дополнительный тип базы данных, если он является дополнительным.</span><span class="sxs-lookup"><span data-stu-id="366ee-181">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="366ee-182">Допустимые значения: Geo и Named.</span><span class="sxs-lookup"><span data-stu-id="366ee-182">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="366ee-183">-ServerName</span><span class="sxs-lookup"><span data-stu-id="366ee-183">-ServerName</span></span>
<span data-ttu-id="366ee-184">Имя сервера, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="366ee-184">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="366ee-185">-Теги</span><span class="sxs-lookup"><span data-stu-id="366ee-185">-Tags</span></span>
<span data-ttu-id="366ee-186">Словарь пар "ключ-значение" в виде hash table, которую этот cmdlet связывает с новой базой данных.</span><span class="sxs-lookup"><span data-stu-id="366ee-186">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="366ee-187">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="366ee-187">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ee-188">-VCore</span><span class="sxs-lookup"><span data-stu-id="366ee-188">-VCore</span></span>
<span data-ttu-id="366ee-189">Номер VCORE для базы данных Azure Sql</span><span class="sxs-lookup"><span data-stu-id="366ee-189">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366ee-190">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="366ee-190">-ZoneRedundant</span></span>
<span data-ttu-id="366ee-191">Избыточность зоны, которая связывается с базой данных Sql Azure</span><span class="sxs-lookup"><span data-stu-id="366ee-191">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="366ee-192">-Confirm</span><span class="sxs-lookup"><span data-stu-id="366ee-192">-Confirm</span></span>
<span data-ttu-id="366ee-193">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="366ee-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="366ee-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="366ee-194">-WhatIf</span></span>
<span data-ttu-id="366ee-195">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="366ee-195">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="366ee-196">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="366ee-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="366ee-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="366ee-197">CommonParameters</span></span>
<span data-ttu-id="366ee-198">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="366ee-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="366ee-199">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="366ee-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="366ee-200">INPUTS</span><span class="sxs-lookup"><span data-stu-id="366ee-200">INPUTS</span></span>

### <span data-ttu-id="366ee-201">System.String</span><span class="sxs-lookup"><span data-stu-id="366ee-201">System.String</span></span>

## <span data-ttu-id="366ee-202">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="366ee-202">OUTPUTS</span></span>

### <span data-ttu-id="366ee-203">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="366ee-203">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="366ee-204">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="366ee-204">NOTES</span></span>

## <span data-ttu-id="366ee-205">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="366ee-205">RELATED LINKS</span></span>

[<span data-ttu-id="366ee-206">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="366ee-206">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="366ee-207">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="366ee-207">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="366ee-208">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="366ee-208">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="366ee-209">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="366ee-209">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="366ee-210">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="366ee-210">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="366ee-211">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="366ee-211">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="366ee-212">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="366ee-212">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="366ee-213">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="366ee-213">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

