---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: ff474116854838c40a4862cf93f4d017ccdf4527
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728908"
---
# <span data-ttu-id="e02c1-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e02c1-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="e02c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e02c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e02c1-103">Создает базу данных или эластичную базу данных.</span><span class="sxs-lookup"><span data-stu-id="e02c1-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="e02c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e02c1-104">SYNTAX</span></span>

### <span data-ttu-id="e02c1-105">DtuBasedDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e02c1-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e02c1-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="e02c1-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e02c1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e02c1-107">DESCRIPTION</span></span>
<span data-ttu-id="e02c1-108">Командлет **New-AzSqlDatabase** создает базу данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e02c1-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="e02c1-109">Вы также можете создать эластичную базу данных, указав параметр *ElasticPoolName* в существующем пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="e02c1-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="e02c1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e02c1-110">EXAMPLES</span></span>

### <span data-ttu-id="e02c1-111">Пример 1: создание базы данных на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="e02c1-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="e02c1-112">Эта команда создает базу данных с именем Database01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="e02c1-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="e02c1-113">Пример 2: Создание эластичной базы данных на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="e02c1-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="e02c1-114">Эта команда создает базу данных с именем Database02 в пуле эластичных БД с именем ElasticPool01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="e02c1-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="e02c1-115">Пример 3: создание базы данных Vcore на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="e02c1-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="e02c1-116">Эта команда создает базу данных Vcore с именем Database03 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="e02c1-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="e02c1-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e02c1-117">PARAMETERS</span></span>

### <span data-ttu-id="e02c1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e02c1-118">-AsJob</span></span>
<span data-ttu-id="e02c1-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e02c1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e02c1-120">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="e02c1-120">-CatalogCollation</span></span>
<span data-ttu-id="e02c1-121">Задает имена параметров сортировки каталога базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="e02c1-121">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="e02c1-122">-CollationName</span><span class="sxs-lookup"><span data-stu-id="e02c1-122">-CollationName</span></span>
<span data-ttu-id="e02c1-123">Задает имя параметров сортировки базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="e02c1-123">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="e02c1-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="e02c1-124">-ComputeGeneration</span></span>
<span data-ttu-id="e02c1-125">Вычислено поколение, которое необходимо назначить.</span><span class="sxs-lookup"><span data-stu-id="e02c1-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="e02c1-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e02c1-126">-DatabaseName</span></span>
<span data-ttu-id="e02c1-127">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="e02c1-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="e02c1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02c1-128">-DefaultProfile</span></span>
<span data-ttu-id="e02c1-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e02c1-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e02c1-130">-Edition</span><span class="sxs-lookup"><span data-stu-id="e02c1-130">-Edition</span></span>
<span data-ttu-id="e02c1-131">Указывает выпуск, назначаемый базе данных.</span><span class="sxs-lookup"><span data-stu-id="e02c1-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="e02c1-132">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e02c1-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e02c1-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="e02c1-133">None</span></span>
- <span data-ttu-id="e02c1-134">Базового</span><span class="sxs-lookup"><span data-stu-id="e02c1-134">Basic</span></span>
- <span data-ttu-id="e02c1-135">Стандартная</span><span class="sxs-lookup"><span data-stu-id="e02c1-135">Standard</span></span>
- <span data-ttu-id="e02c1-136">Версию</span><span class="sxs-lookup"><span data-stu-id="e02c1-136">Premium</span></span>
- <span data-ttu-id="e02c1-137">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="e02c1-137">DataWarehouse</span></span>
- <span data-ttu-id="e02c1-138">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="e02c1-138">Free</span></span>
- <span data-ttu-id="e02c1-139">Показателя</span><span class="sxs-lookup"><span data-stu-id="e02c1-139">Stretch</span></span>
- <span data-ttu-id="e02c1-140">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="e02c1-140">GeneralPurpose</span></span>
- <span data-ttu-id="e02c1-141">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="e02c1-141">BusinessCritical</span></span>

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

### <span data-ttu-id="e02c1-142">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e02c1-142">-ElasticPoolName</span></span>
<span data-ttu-id="e02c1-143">Указывает имя эластичного пула, в который нужно добавить базу данных.</span><span class="sxs-lookup"><span data-stu-id="e02c1-143">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="e02c1-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e02c1-144">-LicenseType</span></span>
<span data-ttu-id="e02c1-145">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e02c1-145">The license type for the Azure Sql database.</span></span> <span data-ttu-id="e02c1-146">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e02c1-146">Possible values are:</span></span>
- <span data-ttu-id="e02c1-147">BasePrice — гибридное выгодное преимущество (AHB) для существующих владельцев лицензий SQL Server применяется скидка.</span><span class="sxs-lookup"><span data-stu-id="e02c1-147">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="e02c1-148">Стоимость базы данных для существующих владельцев лицензий SQL Server будет снижена.</span><span class="sxs-lookup"><span data-stu-id="e02c1-148">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="e02c1-149">LicenseIncluded-(AHB) для существующих владельцев лицензий SQL Server не применяется скидка на гибридные льготы для использования в Azure.</span><span class="sxs-lookup"><span data-stu-id="e02c1-149">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="e02c1-150">Цена базы данных будет включать в себя новые затраты на лицензирование SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e02c1-150">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="e02c1-151">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="e02c1-151">-MaxSizeBytes</span></span>
<span data-ttu-id="e02c1-152">Указывает максимальный размер базы данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="e02c1-152">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="e02c1-153">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="e02c1-153">-ReadScale</span></span>
<span data-ttu-id="e02c1-154">Параметр Read Scale (масштаб чтения), назначаемый базе данных Azure SQL. (Включено или отключено)</span><span class="sxs-lookup"><span data-stu-id="e02c1-154">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="e02c1-155">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="e02c1-155">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="e02c1-156">Указывает имя цели обслуживания, которую нужно назначить базе данных.</span><span class="sxs-lookup"><span data-stu-id="e02c1-156">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="e02c1-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e02c1-157">-ResourceGroupName</span></span>
<span data-ttu-id="e02c1-158">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="e02c1-158">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e02c1-159">-SampleName</span><span class="sxs-lookup"><span data-stu-id="e02c1-159">-SampleName</span></span>
<span data-ttu-id="e02c1-160">Имя схемы, применяемой при создании базы данных.</span><span class="sxs-lookup"><span data-stu-id="e02c1-160">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="e02c1-161">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e02c1-161">-ServerName</span></span>
<span data-ttu-id="e02c1-162">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="e02c1-162">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="e02c1-163">-Теги</span><span class="sxs-lookup"><span data-stu-id="e02c1-163">-Tags</span></span>
<span data-ttu-id="e02c1-164">Задает словарь пар "ключ-значение" в виде хэш-таблицы, которую этот командлет свяжет с новой базой данных.</span><span class="sxs-lookup"><span data-stu-id="e02c1-164">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="e02c1-165">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="e02c1-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e02c1-166">-VCore</span><span class="sxs-lookup"><span data-stu-id="e02c1-166">-VCore</span></span>
<span data-ttu-id="e02c1-167">Номер Vcore для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="e02c1-167">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02c1-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="e02c1-168">-ZoneRedundant</span></span>
<span data-ttu-id="e02c1-169">Избыточность зоны, связываемая с базой данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e02c1-169">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="e02c1-170">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e02c1-170">-Confirm</span></span>
<span data-ttu-id="e02c1-171">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e02c1-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e02c1-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e02c1-172">-WhatIf</span></span>
<span data-ttu-id="e02c1-173">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e02c1-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e02c1-174">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e02c1-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e02c1-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02c1-175">CommonParameters</span></span>
<span data-ttu-id="e02c1-176">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e02c1-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02c1-177">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e02c1-177">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02c1-178">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e02c1-178">INPUTS</span></span>

### <span data-ttu-id="e02c1-179">System. String</span><span class="sxs-lookup"><span data-stu-id="e02c1-179">System.String</span></span>

## <span data-ttu-id="e02c1-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e02c1-180">OUTPUTS</span></span>

### <span data-ttu-id="e02c1-181">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e02c1-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="e02c1-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="e02c1-182">NOTES</span></span>

## <span data-ttu-id="e02c1-183">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e02c1-183">RELATED LINKS</span></span>

[<span data-ttu-id="e02c1-184">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e02c1-184">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="e02c1-185">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e02c1-185">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="e02c1-186">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e02c1-186">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="e02c1-187">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e02c1-187">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="e02c1-188">Возобновить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e02c1-188">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="e02c1-189">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e02c1-189">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="e02c1-190">Приостановить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e02c1-190">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="e02c1-191">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="e02c1-191">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

