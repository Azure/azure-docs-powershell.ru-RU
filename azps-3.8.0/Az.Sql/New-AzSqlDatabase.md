---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: 32329ac1e36c74c08dcf25f8f8b4295e81633e90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065222"
---
# <span data-ttu-id="61cce-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="61cce-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="61cce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61cce-102">SYNOPSIS</span></span>
<span data-ttu-id="61cce-103">Создает базу данных или эластичную базу данных.</span><span class="sxs-lookup"><span data-stu-id="61cce-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="61cce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61cce-104">SYNTAX</span></span>

### <span data-ttu-id="61cce-105">DtuBasedDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61cce-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61cce-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="61cce-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61cce-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61cce-107">DESCRIPTION</span></span>
<span data-ttu-id="61cce-108">Командлет **New-AzSqlDatabase** создает базу данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="61cce-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="61cce-109">Вы также можете создать эластичную базу данных, указав параметр *ElasticPoolName* в существующем пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="61cce-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="61cce-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61cce-110">EXAMPLES</span></span>

### <span data-ttu-id="61cce-111">Пример 1: создание базы данных на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="61cce-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="61cce-112">Эта команда создает базу данных с именем Database01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="61cce-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="61cce-113">Пример 2: Создание эластичной базы данных на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="61cce-113">Example 2: Create an elastic database on a specified server</span></span>
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

<span data-ttu-id="61cce-114">Эта команда создает базу данных с именем Database02 в пуле эластичных БД с именем ElasticPool01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="61cce-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="61cce-115">Пример 3: создание базы данных Vcore на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="61cce-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="61cce-116">Эта команда создает базу данных Vcore с именем Database03 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="61cce-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="61cce-117">Пример 4: создание базы данных, не отменяя сервер, на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="61cce-117">Example 4: Create an Serverless database on the specified server</span></span>
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

<span data-ttu-id="61cce-118">Эта команда создает серверную базу данных с именем Database04 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="61cce-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="61cce-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61cce-119">PARAMETERS</span></span>

### <span data-ttu-id="61cce-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61cce-120">-AsJob</span></span>
<span data-ttu-id="61cce-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="61cce-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61cce-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="61cce-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="61cce-123">Задержка автоматической паузы (в минутах) для базы данных (только для серверов),-1, чтобы отказаться от нее</span><span class="sxs-lookup"><span data-stu-id="61cce-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="61cce-124">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="61cce-124">-CatalogCollation</span></span>
<span data-ttu-id="61cce-125">Задает имена параметров сортировки каталога базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="61cce-125">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="61cce-126">-CollationName</span><span class="sxs-lookup"><span data-stu-id="61cce-126">-CollationName</span></span>
<span data-ttu-id="61cce-127">Задает имя параметров сортировки базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="61cce-127">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="61cce-128">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="61cce-128">-ComputeGeneration</span></span>
<span data-ttu-id="61cce-129">Вычислено поколение, которое необходимо назначить.</span><span class="sxs-lookup"><span data-stu-id="61cce-129">The compute generation to assign.</span></span>

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

### <span data-ttu-id="61cce-130">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="61cce-130">-ComputeModel</span></span>
<span data-ttu-id="61cce-131">Модель вычисления для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="61cce-131">The compute model for Azure Sql database.</span></span> <span data-ttu-id="61cce-132">Неподготовленный или настроенный сервер</span><span class="sxs-lookup"><span data-stu-id="61cce-132">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="61cce-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="61cce-133">-DatabaseName</span></span>
<span data-ttu-id="61cce-134">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="61cce-134">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="61cce-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61cce-135">-DefaultProfile</span></span>
<span data-ttu-id="61cce-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="61cce-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61cce-137">-Edition</span><span class="sxs-lookup"><span data-stu-id="61cce-137">-Edition</span></span>
<span data-ttu-id="61cce-138">Указывает выпуск, назначаемый базе данных.</span><span class="sxs-lookup"><span data-stu-id="61cce-138">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="61cce-139">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="61cce-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="61cce-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="61cce-140">None</span></span>
- <span data-ttu-id="61cce-141">Базового</span><span class="sxs-lookup"><span data-stu-id="61cce-141">Basic</span></span>
- <span data-ttu-id="61cce-142">Стандартная</span><span class="sxs-lookup"><span data-stu-id="61cce-142">Standard</span></span>
- <span data-ttu-id="61cce-143">Версию</span><span class="sxs-lookup"><span data-stu-id="61cce-143">Premium</span></span>
- <span data-ttu-id="61cce-144">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="61cce-144">DataWarehouse</span></span>
- <span data-ttu-id="61cce-145">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="61cce-145">Free</span></span>
- <span data-ttu-id="61cce-146">Показателя</span><span class="sxs-lookup"><span data-stu-id="61cce-146">Stretch</span></span>
- <span data-ttu-id="61cce-147">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="61cce-147">GeneralPurpose</span></span>
- <span data-ttu-id="61cce-148">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="61cce-148">BusinessCritical</span></span>

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

### <span data-ttu-id="61cce-149">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="61cce-149">-ElasticPoolName</span></span>
<span data-ttu-id="61cce-150">Указывает имя эластичного пула, в который нужно добавить базу данных.</span><span class="sxs-lookup"><span data-stu-id="61cce-150">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="61cce-151">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="61cce-151">-LicenseType</span></span>
<span data-ttu-id="61cce-152">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="61cce-152">The license type for the Azure Sql database.</span></span> <span data-ttu-id="61cce-153">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="61cce-153">Possible values are:</span></span>
- <span data-ttu-id="61cce-154">BasePrice — гибридное выгодное преимущество (AHB) для существующих владельцев лицензий SQL Server применяется скидка.</span><span class="sxs-lookup"><span data-stu-id="61cce-154">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="61cce-155">Стоимость базы данных для существующих владельцев лицензий SQL Server будет снижена.</span><span class="sxs-lookup"><span data-stu-id="61cce-155">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="61cce-156">LicenseIncluded-(AHB) для существующих владельцев лицензий SQL Server не применяется скидка на гибридные льготы для использования в Azure.</span><span class="sxs-lookup"><span data-stu-id="61cce-156">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="61cce-157">Цена базы данных будет включать в себя новые затраты на лицензирование SQL Server.</span><span class="sxs-lookup"><span data-stu-id="61cce-157">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="61cce-158">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="61cce-158">-MaxSizeBytes</span></span>
<span data-ttu-id="61cce-159">Указывает максимальный размер базы данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="61cce-159">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="61cce-160">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="61cce-160">-MinimumCapacity</span></span>
<span data-ttu-id="61cce-161">Минимальная емкость, которую база данных будет всегда выделена, если она не была приостановлена.</span><span class="sxs-lookup"><span data-stu-id="61cce-161">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="61cce-162">Только для баз данных Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="61cce-162">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="61cce-163">-ReadReplicaCount</span><span class="sxs-lookup"><span data-stu-id="61cce-163">-ReadReplicaCount</span></span>
<span data-ttu-id="61cce-164">Количество вторичных реплик (только для чтения), связанных с базой данных, для которых могут маршрутизироваться подключения с намерением к приложениям, поддерживающие только чтение.</span><span class="sxs-lookup"><span data-stu-id="61cce-164">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="61cce-165">Это свойство можно задать только для баз данных "линейный выпуск".</span><span class="sxs-lookup"><span data-stu-id="61cce-165">This property is only settable for Hyperscale edition databases.</span></span>

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

### <span data-ttu-id="61cce-166">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="61cce-166">-ReadScale</span></span>
<span data-ttu-id="61cce-167">Если этот параметр включен, в строке подключения для подключений, для которых определена цель приложения ReadOnly, может перенаправляться в вторичную реплику ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="61cce-167">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="61cce-168">Это свойство можно задать только для баз данных Premium и бизнес-критических.</span><span class="sxs-lookup"><span data-stu-id="61cce-168">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="61cce-169">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="61cce-169">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="61cce-170">Указывает имя цели обслуживания, которую нужно назначить базе данных.</span><span class="sxs-lookup"><span data-stu-id="61cce-170">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="61cce-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61cce-171">-ResourceGroupName</span></span>
<span data-ttu-id="61cce-172">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="61cce-172">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="61cce-173">-SampleName</span><span class="sxs-lookup"><span data-stu-id="61cce-173">-SampleName</span></span>
<span data-ttu-id="61cce-174">Имя схемы, применяемой при создании базы данных.</span><span class="sxs-lookup"><span data-stu-id="61cce-174">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="61cce-175">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="61cce-175">-ServerName</span></span>
<span data-ttu-id="61cce-176">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="61cce-176">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="61cce-177">-Теги</span><span class="sxs-lookup"><span data-stu-id="61cce-177">-Tags</span></span>
<span data-ttu-id="61cce-178">Задает словарь пар "ключ-значение" в виде хэш-таблицы, которую этот командлет свяжет с новой базой данных.</span><span class="sxs-lookup"><span data-stu-id="61cce-178">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="61cce-179">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="61cce-179">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="61cce-180">-VCore</span><span class="sxs-lookup"><span data-stu-id="61cce-180">-VCore</span></span>
<span data-ttu-id="61cce-181">Номер Vcore для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="61cce-181">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="61cce-182">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="61cce-182">-ZoneRedundant</span></span>
<span data-ttu-id="61cce-183">Избыточность зоны, связываемая с базой данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="61cce-183">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="61cce-184">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61cce-184">-Confirm</span></span>
<span data-ttu-id="61cce-185">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="61cce-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61cce-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61cce-186">-WhatIf</span></span>
<span data-ttu-id="61cce-187">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="61cce-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61cce-188">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="61cce-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61cce-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61cce-189">CommonParameters</span></span>
<span data-ttu-id="61cce-190">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61cce-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61cce-191">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61cce-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61cce-192">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61cce-192">INPUTS</span></span>

### <span data-ttu-id="61cce-193">System. String</span><span class="sxs-lookup"><span data-stu-id="61cce-193">System.String</span></span>

## <span data-ttu-id="61cce-194">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61cce-194">OUTPUTS</span></span>

### <span data-ttu-id="61cce-195">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="61cce-195">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="61cce-196">Пуск</span><span class="sxs-lookup"><span data-stu-id="61cce-196">NOTES</span></span>

## <span data-ttu-id="61cce-197">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61cce-197">RELATED LINKS</span></span>

[<span data-ttu-id="61cce-198">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="61cce-198">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="61cce-199">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="61cce-199">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="61cce-200">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="61cce-200">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="61cce-201">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="61cce-201">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="61cce-202">Возобновить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="61cce-202">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="61cce-203">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="61cce-203">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="61cce-204">Приостановить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="61cce-204">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="61cce-205">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="61cce-205">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

