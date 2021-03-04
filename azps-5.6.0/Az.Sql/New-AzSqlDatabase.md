---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: c4ccb57292fd4abc2c9b6fd14c5e4492047a2e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956595"
---
# <span data-ttu-id="2edb6-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2edb6-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="2edb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2edb6-102">SYNOPSIS</span></span>
<span data-ttu-id="2edb6-103">Создает базу данных или эластичную базу данных.</span><span class="sxs-lookup"><span data-stu-id="2edb6-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="2edb6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2edb6-104">SYNTAX</span></span>

### <span data-ttu-id="2edb6-105">DtuBasedDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2edb6-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-Force] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2edb6-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="2edb6-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] [-Force] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2edb6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2edb6-107">DESCRIPTION</span></span>
<span data-ttu-id="2edb6-108">Для создания базы данных Azure создается SQL **AzSqlDatabase.**</span><span class="sxs-lookup"><span data-stu-id="2edb6-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="2edb6-109">Вы также можете создать эластичную базу данных, задав *параметр "ЭластичнаяPoolName"* в существующем эластичном пуле.</span><span class="sxs-lookup"><span data-stu-id="2edb6-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="2edb6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2edb6-110">EXAMPLES</span></span>

### <span data-ttu-id="2edb6-111">Пример 1. Создание базы данных на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="2edb6-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="2edb6-112">Эта команда создает базу данных с именем Database01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="2edb6-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="2edb6-113">Пример 2. Создание эластичной базы данных на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="2edb6-113">Example 2: Create an elastic database on a specified server</span></span>
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

<span data-ttu-id="2edb6-114">Эта команда создает базу данных с именем Database02 в эластичном пуле Под названием "ЭластичнаяPool01" на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="2edb6-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="2edb6-115">Пример 3. Создание базы данных "Vcore" на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="2edb6-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="2edb6-116">Эта команда создает базу данных VCORE с именем Database03 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="2edb6-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="2edb6-117">Пример 4. Создание базы данных Без сервера на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="2edb6-117">Example 4: Create an Serverless database on the specified server</span></span>
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

<span data-ttu-id="2edb6-118">Эта команда создает базу данных Без сервера с именем Database04 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="2edb6-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="2edb6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2edb6-119">PARAMETERS</span></span>

### <span data-ttu-id="2edb6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2edb6-120">-AsJob</span></span>
<span data-ttu-id="2edb6-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2edb6-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2edb6-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="2edb6-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="2edb6-123">Автоматическая приостановка задержки в минутах для базы данных (только для серверов); -1, чтобы отказаться</span><span class="sxs-lookup"><span data-stu-id="2edb6-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="2edb6-124">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="2edb6-124">-BackupStorageRedundancy</span></span>
<span data-ttu-id="2edb6-125">Избыточность резервного копирования хранилища, используемого для хранения резервных копий SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="2edb6-125">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="2edb6-126">Доступны такие варианты: "Локальный", "Зона" и "Гео".</span><span class="sxs-lookup"><span data-stu-id="2edb6-126">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="2edb6-127">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="2edb6-127">-CatalogCollation</span></span>
<span data-ttu-id="2edb6-128">Указывает имя для каталога SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="2edb6-128">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="2edb6-129">-CollationName</span><span class="sxs-lookup"><span data-stu-id="2edb6-129">-CollationName</span></span>
<span data-ttu-id="2edb6-130">Определяет имя для SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="2edb6-130">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="2edb6-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="2edb6-131">-ComputeGeneration</span></span>
<span data-ttu-id="2edb6-132">Назначимое поколение компьютеров.</span><span class="sxs-lookup"><span data-stu-id="2edb6-132">The compute generation to assign.</span></span>

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

### <span data-ttu-id="2edb6-133">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="2edb6-133">-ComputeModel</span></span>
<span data-ttu-id="2edb6-134">Модель вычислений для базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="2edb6-134">The compute model for Azure Sql database.</span></span> <span data-ttu-id="2edb6-135">Сервер без серверов или подготовка</span><span class="sxs-lookup"><span data-stu-id="2edb6-135">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="2edb6-136">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2edb6-136">-DatabaseName</span></span>
<span data-ttu-id="2edb6-137">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="2edb6-137">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="2edb6-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2edb6-138">-DefaultProfile</span></span>
<span data-ttu-id="2edb6-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2edb6-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2edb6-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="2edb6-140">-Edition</span></span>
<span data-ttu-id="2edb6-141">Выпуск, который нужно назначить базе данных.</span><span class="sxs-lookup"><span data-stu-id="2edb6-141">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="2edb6-142">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="2edb6-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2edb6-143">Нет</span><span class="sxs-lookup"><span data-stu-id="2edb6-143">None</span></span>
- <span data-ttu-id="2edb6-144">Базовая</span><span class="sxs-lookup"><span data-stu-id="2edb6-144">Basic</span></span>
- <span data-ttu-id="2edb6-145">Стандартный</span><span class="sxs-lookup"><span data-stu-id="2edb6-145">Standard</span></span>
- <span data-ttu-id="2edb6-146">Premium</span><span class="sxs-lookup"><span data-stu-id="2edb6-146">Premium</span></span>
- <span data-ttu-id="2edb6-147">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="2edb6-147">DataWarehouse</span></span>
- <span data-ttu-id="2edb6-148">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="2edb6-148">Free</span></span>
- <span data-ttu-id="2edb6-149">Растяжение</span><span class="sxs-lookup"><span data-stu-id="2edb6-149">Stretch</span></span>
- <span data-ttu-id="2edb6-150">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="2edb6-150">GeneralPurpose</span></span>
- <span data-ttu-id="2edb6-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="2edb6-151">BusinessCritical</span></span>

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

### <span data-ttu-id="2edb6-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2edb6-152">-ElasticPoolName</span></span>
<span data-ttu-id="2edb6-153">Определяет имя эластичного пула, в который нужно поместить базу данных.</span><span class="sxs-lookup"><span data-stu-id="2edb6-153">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="2edb6-154">-Force</span><span class="sxs-lookup"><span data-stu-id="2edb6-154">-Force</span></span>
<span data-ttu-id="2edb6-155">Пропустить сообщение подтверждения для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="2edb6-155">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2edb6-156">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="2edb6-156">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="2edb6-157">Количество дополнительных реплик для чтения, связанных с базой данных, в которую могут маршрутизироваться подключения намерением приложения в чтение.</span><span class="sxs-lookup"><span data-stu-id="2edb6-157">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="2edb6-158">Это свойство можно настроить только для баз данных hyperscale edition.</span><span class="sxs-lookup"><span data-stu-id="2edb6-158">This property is only settable for Hyperscale edition databases.</span></span>

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

### <span data-ttu-id="2edb6-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2edb6-159">-LicenseType</span></span>
<span data-ttu-id="2edb6-160">Тип лицензии для базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="2edb6-160">The license type for the Azure Sql database.</span></span> <span data-ttu-id="2edb6-161">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="2edb6-161">Possible values are:</span></span>
- <span data-ttu-id="2edb6-162">BasePrice — скидка на гибридное преимущество Azure (AHB) для существующих SQL Server лицензий применяется.</span><span class="sxs-lookup"><span data-stu-id="2edb6-162">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="2edb6-163">Цена базы данных будет дисконтна для существующих SQL Server лицензий.</span><span class="sxs-lookup"><span data-stu-id="2edb6-163">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="2edb6-164">LicenseIncluded — скидка на azure Hybrid Benefit (AHB) для существующих SQL Server лицензий не применяется.</span><span class="sxs-lookup"><span data-stu-id="2edb6-164">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="2edb6-165">Цена базы данных будет включать новую стоимость SQL Server лицензий.</span><span class="sxs-lookup"><span data-stu-id="2edb6-165">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="2edb6-166">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2edb6-166">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="2edb6-167">The Maintenance configuration id for the SQL Database.</span><span class="sxs-lookup"><span data-stu-id="2edb6-167">The Maintenance configuration id for the SQL Database.</span></span>

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

### <span data-ttu-id="2edb6-168">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="2edb6-168">-MaxSizeBytes</span></span>
<span data-ttu-id="2edb6-169">Максимальный размер базы данных в этихбайтах.</span><span class="sxs-lookup"><span data-stu-id="2edb6-169">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="2edb6-170">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="2edb6-170">-MinimumCapacity</span></span>
<span data-ttu-id="2edb6-171">Минимальная пропускная способность, выделенная для базы данных, если не приостановлена.</span><span class="sxs-lookup"><span data-stu-id="2edb6-171">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="2edb6-172">Только для серверных баз данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="2edb6-172">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="2edb6-173">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="2edb6-173">-ReadScale</span></span>
<span data-ttu-id="2edb6-174">Если эта возможность включена, соединения, для которые настроено чтение в строке подключения, могут быть маршрутизируемы на вторичную реплику для чтения.</span><span class="sxs-lookup"><span data-stu-id="2edb6-174">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="2edb6-175">Это свойство можно настроить только для баз данных премиум- и бизнес-критических версий.</span><span class="sxs-lookup"><span data-stu-id="2edb6-175">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="2edb6-176">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="2edb6-176">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="2edb6-177">Указывает имя цели обслуживания, которая будет назначаться базе данных.</span><span class="sxs-lookup"><span data-stu-id="2edb6-177">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="2edb6-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2edb6-178">-ResourceGroupName</span></span>
<span data-ttu-id="2edb6-179">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="2edb6-179">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="2edb6-180">-SampleName</span><span class="sxs-lookup"><span data-stu-id="2edb6-180">-SampleName</span></span>
<span data-ttu-id="2edb6-181">Имя образца схемы, применяемого при создании базы данных.</span><span class="sxs-lookup"><span data-stu-id="2edb6-181">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="2edb6-182">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="2edb6-182">-SecondaryType</span></span>
<span data-ttu-id="2edb6-183">Дополнительный тип базы данных, если она является вторичной.</span><span class="sxs-lookup"><span data-stu-id="2edb6-183">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="2edb6-184">Допустимые значения: Geo и Named.</span><span class="sxs-lookup"><span data-stu-id="2edb6-184">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="2edb6-185">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2edb6-185">-ServerName</span></span>
<span data-ttu-id="2edb6-186">Имя сервера, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="2edb6-186">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="2edb6-187">-Теги</span><span class="sxs-lookup"><span data-stu-id="2edb6-187">-Tags</span></span>
<span data-ttu-id="2edb6-188">Словарь пар "ключ-значение" в виде hash table, которую этот cmdlet связывает с новой базой данных.</span><span class="sxs-lookup"><span data-stu-id="2edb6-188">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="2edb6-189">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="2edb6-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2edb6-190">-VCore</span><span class="sxs-lookup"><span data-stu-id="2edb6-190">-VCore</span></span>
<span data-ttu-id="2edb6-191">Номер VCORE для базы данных Azure Sql</span><span class="sxs-lookup"><span data-stu-id="2edb6-191">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="2edb6-192">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="2edb6-192">-ZoneRedundant</span></span>
<span data-ttu-id="2edb6-193">Избыточность зоны, которая связывается с базой данных Sql Azure</span><span class="sxs-lookup"><span data-stu-id="2edb6-193">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="2edb6-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2edb6-194">-Confirm</span></span>
<span data-ttu-id="2edb6-195">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2edb6-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2edb6-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2edb6-196">-WhatIf</span></span>
<span data-ttu-id="2edb6-197">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2edb6-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2edb6-198">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2edb6-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2edb6-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2edb6-199">CommonParameters</span></span>
<span data-ttu-id="2edb6-200">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2edb6-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2edb6-201">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2edb6-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2edb6-202">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2edb6-202">INPUTS</span></span>

### <span data-ttu-id="2edb6-203">System.String</span><span class="sxs-lookup"><span data-stu-id="2edb6-203">System.String</span></span>

## <span data-ttu-id="2edb6-204">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2edb6-204">OUTPUTS</span></span>

### <span data-ttu-id="2edb6-205">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2edb6-205">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="2edb6-206">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2edb6-206">NOTES</span></span>

## <span data-ttu-id="2edb6-207">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2edb6-207">RELATED LINKS</span></span>

[<span data-ttu-id="2edb6-208">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2edb6-208">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="2edb6-209">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2edb6-209">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="2edb6-210">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="2edb6-210">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="2edb6-211">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2edb6-211">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="2edb6-212">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2edb6-212">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="2edb6-213">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2edb6-213">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="2edb6-214">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2edb6-214">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="2edb6-215">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="2edb6-215">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

