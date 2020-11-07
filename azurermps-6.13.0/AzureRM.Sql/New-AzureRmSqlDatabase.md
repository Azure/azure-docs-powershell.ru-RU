---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 7eaa753b973b887cbbddc132b998d05f3e374e3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734105"
---
# <span data-ttu-id="f2353-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f2353-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="f2353-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2353-102">SYNOPSIS</span></span>
<span data-ttu-id="f2353-103">Создает базу данных или эластичную базу данных.</span><span class="sxs-lookup"><span data-stu-id="f2353-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2353-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2353-104">SYNTAX</span></span>

### <span data-ttu-id="f2353-105">DtuBasedDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f2353-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2353-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="f2353-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2353-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2353-107">DESCRIPTION</span></span>
<span data-ttu-id="f2353-108">Командлет **New-AzureRmSqlDatabase** создает базу данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f2353-108">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="f2353-109">Вы также можете создать эластичную базу данных, указав параметр *ElasticPoolName* в существующем пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="f2353-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="f2353-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2353-110">EXAMPLES</span></span>

### <span data-ttu-id="f2353-111">Пример 1: создание базы данных на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="f2353-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="f2353-112">Эта команда создает базу данных с именем Database01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="f2353-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="f2353-113">Пример 2: Создание эластичной базы данных на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="f2353-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="f2353-114">Эта команда создает базу данных с именем Database02 в пуле эластичных БД с именем ElasticPool01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="f2353-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="f2353-115">Пример 3: создание базы данных Vcore на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="f2353-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
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

<span data-ttu-id="f2353-116">Эта команда создает базу данных Vcore с именем Database03 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="f2353-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="f2353-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2353-117">PARAMETERS</span></span>

### <span data-ttu-id="f2353-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2353-118">-AsJob</span></span>
<span data-ttu-id="f2353-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f2353-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2353-120">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="f2353-120">-CatalogCollation</span></span>
<span data-ttu-id="f2353-121">Задает имена параметров сортировки каталога базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f2353-121">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="f2353-122">-CollationName</span><span class="sxs-lookup"><span data-stu-id="f2353-122">-CollationName</span></span>
<span data-ttu-id="f2353-123">Задает имя параметров сортировки базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f2353-123">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="f2353-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="f2353-124">-ComputeGeneration</span></span>
<span data-ttu-id="f2353-125">Вычислено поколение, которое необходимо назначить.</span><span class="sxs-lookup"><span data-stu-id="f2353-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="f2353-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f2353-126">-DatabaseName</span></span>
<span data-ttu-id="f2353-127">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="f2353-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="f2353-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2353-128">-DefaultProfile</span></span>
<span data-ttu-id="f2353-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f2353-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2353-130">-Edition</span><span class="sxs-lookup"><span data-stu-id="f2353-130">-Edition</span></span>
<span data-ttu-id="f2353-131">Указывает выпуск, назначаемый базе данных.</span><span class="sxs-lookup"><span data-stu-id="f2353-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="f2353-132">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f2353-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f2353-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="f2353-133">None</span></span>
- <span data-ttu-id="f2353-134">Базового</span><span class="sxs-lookup"><span data-stu-id="f2353-134">Basic</span></span>
- <span data-ttu-id="f2353-135">Стандартная</span><span class="sxs-lookup"><span data-stu-id="f2353-135">Standard</span></span>
- <span data-ttu-id="f2353-136">Версию</span><span class="sxs-lookup"><span data-stu-id="f2353-136">Premium</span></span>
- <span data-ttu-id="f2353-137">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="f2353-137">DataWarehouse</span></span>
- <span data-ttu-id="f2353-138">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="f2353-138">Free</span></span>
- <span data-ttu-id="f2353-139">Показателя</span><span class="sxs-lookup"><span data-stu-id="f2353-139">Stretch</span></span>
- <span data-ttu-id="f2353-140">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="f2353-140">GeneralPurpose</span></span>
- <span data-ttu-id="f2353-141">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="f2353-141">BusinessCritical</span></span>

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

### <span data-ttu-id="f2353-142">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f2353-142">-ElasticPoolName</span></span>
<span data-ttu-id="f2353-143">Указывает имя эластичного пула, в который нужно добавить базу данных.</span><span class="sxs-lookup"><span data-stu-id="f2353-143">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="f2353-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f2353-144">-LicenseType</span></span>
<span data-ttu-id="f2353-145">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f2353-145">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="f2353-146">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="f2353-146">-MaxSizeBytes</span></span>
<span data-ttu-id="f2353-147">Указывает максимальный размер базы данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="f2353-147">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="f2353-148">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="f2353-148">-ReadScale</span></span>
<span data-ttu-id="f2353-149">Параметр Read Scale (масштаб чтения), назначаемый базе данных Azure SQL. (Включено или отключено)</span><span class="sxs-lookup"><span data-stu-id="f2353-149">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="f2353-150">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="f2353-150">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="f2353-151">Указывает имя цели обслуживания, которую нужно назначить базе данных.</span><span class="sxs-lookup"><span data-stu-id="f2353-151">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="f2353-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2353-152">-ResourceGroupName</span></span>
<span data-ttu-id="f2353-153">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="f2353-153">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f2353-154">-SampleName</span><span class="sxs-lookup"><span data-stu-id="f2353-154">-SampleName</span></span>
<span data-ttu-id="f2353-155">Имя схемы, применяемой при создании базы данных.</span><span class="sxs-lookup"><span data-stu-id="f2353-155">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="f2353-156">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f2353-156">-ServerName</span></span>
<span data-ttu-id="f2353-157">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="f2353-157">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="f2353-158">-Теги</span><span class="sxs-lookup"><span data-stu-id="f2353-158">-Tags</span></span>
<span data-ttu-id="f2353-159">Задает словарь пар "ключ-значение" в виде хэш-таблицы, которую этот командлет свяжет с новой базой данных.</span><span class="sxs-lookup"><span data-stu-id="f2353-159">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="f2353-160">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="f2353-160">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f2353-161">-VCore</span><span class="sxs-lookup"><span data-stu-id="f2353-161">-VCore</span></span>
<span data-ttu-id="f2353-162">Номер Vcore для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="f2353-162">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="f2353-163">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="f2353-163">-ZoneRedundant</span></span>
<span data-ttu-id="f2353-164">Избыточность зоны, связываемая с базой данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f2353-164">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="f2353-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2353-165">-Confirm</span></span>
<span data-ttu-id="f2353-166">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f2353-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2353-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2353-167">-WhatIf</span></span>
<span data-ttu-id="f2353-168">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f2353-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2353-169">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f2353-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2353-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2353-170">CommonParameters</span></span>
<span data-ttu-id="f2353-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2353-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2353-172">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2353-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2353-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2353-173">INPUTS</span></span>

### <span data-ttu-id="f2353-174">System. String</span><span class="sxs-lookup"><span data-stu-id="f2353-174">System.String</span></span>

## <span data-ttu-id="f2353-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2353-175">OUTPUTS</span></span>

### <span data-ttu-id="f2353-176">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f2353-176">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f2353-177">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2353-177">NOTES</span></span>

## <span data-ttu-id="f2353-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2353-178">RELATED LINKS</span></span>

[<span data-ttu-id="f2353-179">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f2353-179">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="f2353-180">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f2353-180">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f2353-181">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="f2353-181">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="f2353-182">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f2353-182">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="f2353-183">Возобновить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f2353-183">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="f2353-184">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f2353-184">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="f2353-185">Приостановить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f2353-185">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="f2353-186">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="f2353-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

