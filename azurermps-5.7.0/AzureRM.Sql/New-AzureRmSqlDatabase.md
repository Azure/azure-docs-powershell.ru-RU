---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: f5fc78f3e06150f3283e35c23bf80edce4f47650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566888"
---
# <span data-ttu-id="ed2c5-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ed2c5-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="ed2c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed2c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ed2c5-103">Создает базу данных или эластичную базу данных.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed2c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed2c5-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed2c5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed2c5-105">DESCRIPTION</span></span>
<span data-ttu-id="ed2c5-106">Командлет **New-AzureRmSqlDatabase** создает базу данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-106">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>

<span data-ttu-id="ed2c5-107">Вы также можете создать эластичную базу данных, указав параметр *ElasticPoolName* в существующем пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-107">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="ed2c5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed2c5-108">EXAMPLES</span></span>

### <span data-ttu-id="ed2c5-109">Пример 1: создание базы данных на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="ed2c5-109">Example 1: Create a database on a specified server</span></span>
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
Tags                          :
```

<span data-ttu-id="ed2c5-110">Эта команда создает базу данных с именем Database01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-110">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="ed2c5-111">Пример 2: Создание эластичной базы данных на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="ed2c5-111">Example 2: Create an elastic database on a specified server</span></span>
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
Tags                          :
```

<span data-ttu-id="ed2c5-112">Эта команда создает базу данных с именем Database01 в пуле эластичных БД с именем ElasticPool01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-112">This command creates a database named Database01 in the elastic pool named ElasticPool01 on server Server01.</span></span>

## <span data-ttu-id="ed2c5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed2c5-113">PARAMETERS</span></span>

### <span data-ttu-id="ed2c5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed2c5-114">-AsJob</span></span>
<span data-ttu-id="ed2c5-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ed2c5-115">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="ed2c5-116">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="ed2c5-116">-CatalogCollation</span></span>
<span data-ttu-id="ed2c5-117">Задает имена параметров сортировки каталога базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-117">Specifies the name of the SQL database catalog collation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed2c5-118">-CollationName</span><span class="sxs-lookup"><span data-stu-id="ed2c5-118">-CollationName</span></span>
<span data-ttu-id="ed2c5-119">Задает имя параметров сортировки базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-119">Specifies the name of the SQL database collation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed2c5-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ed2c5-120">-DatabaseName</span></span>
<span data-ttu-id="ed2c5-121">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-121">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed2c5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed2c5-122">-DefaultProfile</span></span>
<span data-ttu-id="ed2c5-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ed2c5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed2c5-124">-Edition</span><span class="sxs-lookup"><span data-stu-id="ed2c5-124">-Edition</span></span>
<span data-ttu-id="ed2c5-125">Указывает выпуск, назначаемый базе данных.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-125">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="ed2c5-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ed2c5-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ed2c5-127">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="ed2c5-127">Default</span></span>
- <span data-ttu-id="ed2c5-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="ed2c5-128">None</span></span>
- <span data-ttu-id="ed2c5-129">Версию</span><span class="sxs-lookup"><span data-stu-id="ed2c5-129">Premium</span></span>
- <span data-ttu-id="ed2c5-130">Базового</span><span class="sxs-lookup"><span data-stu-id="ed2c5-130">Basic</span></span>
- <span data-ttu-id="ed2c5-131">Стандартная</span><span class="sxs-lookup"><span data-stu-id="ed2c5-131">Standard</span></span>
- <span data-ttu-id="ed2c5-132">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="ed2c5-132">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed2c5-133">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ed2c5-133">-ElasticPoolName</span></span>
<span data-ttu-id="ed2c5-134">Указывает имя эластичного пула, в который нужно добавить базу данных.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-134">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed2c5-135">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="ed2c5-135">-MaxSizeBytes</span></span>
<span data-ttu-id="ed2c5-136">Указывает максимальный размер базы данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-136">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed2c5-137">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="ed2c5-137">-ReadScale</span></span>
<span data-ttu-id="ed2c5-138">Параметр Read Scale (масштаб чтения), назначаемый базе данных Azure SQL. (Включено или отключено)</span><span class="sxs-lookup"><span data-stu-id="ed2c5-138">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed2c5-139">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="ed2c5-139">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="ed2c5-140">Указывает имя цели обслуживания, которую нужно назначить базе данных.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-140">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed2c5-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed2c5-141">-ResourceGroupName</span></span>
<span data-ttu-id="ed2c5-142">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-142">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ed2c5-143">-SampleName</span><span class="sxs-lookup"><span data-stu-id="ed2c5-143">-SampleName</span></span>
<span data-ttu-id="ed2c5-144">Имя схемы, применяемой при создании базы данных.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-144">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed2c5-145">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ed2c5-145">-ServerName</span></span>
<span data-ttu-id="ed2c5-146">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-146">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ed2c5-147">-Теги</span><span class="sxs-lookup"><span data-stu-id="ed2c5-147">-Tags</span></span>
<span data-ttu-id="ed2c5-148">Задает словарь пар "ключ-значение" в виде хэш-таблицы, которую этот командлет свяжет с новой базой данных.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-148">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="ed2c5-149">Например:</span><span class="sxs-lookup"><span data-stu-id="ed2c5-149">For example:</span></span>

<span data-ttu-id="ed2c5-150">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="ed2c5-150">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed2c5-151">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="ed2c5-151">-ZoneRedundant</span></span>
<span data-ttu-id="ed2c5-152">Избыточность зоны, связываемая с базой данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-152">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="ed2c5-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed2c5-153">-Confirm</span></span>
<span data-ttu-id="ed2c5-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed2c5-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed2c5-155">-WhatIf</span></span>
<span data-ttu-id="ed2c5-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed2c5-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed2c5-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed2c5-158">CommonParameters</span></span>
<span data-ttu-id="ed2c5-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed2c5-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed2c5-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed2c5-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed2c5-161">INPUTS</span></span>

### <span data-ttu-id="ed2c5-162">Ничего</span><span class="sxs-lookup"><span data-stu-id="ed2c5-162">None</span></span>
<span data-ttu-id="ed2c5-163">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ed2c5-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed2c5-164">OUTPUTS</span></span>

### <span data-ttu-id="ed2c5-165">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ed2c5-165">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ed2c5-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed2c5-166">NOTES</span></span>

## <span data-ttu-id="ed2c5-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed2c5-167">RELATED LINKS</span></span>

[<span data-ttu-id="ed2c5-168">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ed2c5-168">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="ed2c5-169">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ed2c5-169">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ed2c5-170">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="ed2c5-170">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="ed2c5-171">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ed2c5-171">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="ed2c5-172">Возобновить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ed2c5-172">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="ed2c5-173">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ed2c5-173">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="ed2c5-174">Приостановить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ed2c5-174">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="ed2c5-175">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="ed2c5-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
