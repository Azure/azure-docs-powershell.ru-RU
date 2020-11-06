---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: 283b12ca63f92086369f273b1f04d5e3f0cd1716
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560020"
---
# <span data-ttu-id="e2f7e-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e2f7e-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="e2f7e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f7e-103">Задает свойства базы данных или перемещает существующую базу данных в эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2f7e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2f7e-104">SYNTAX</span></span>

### <span data-ttu-id="e2f7e-105">Обновление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2f7e-105">Update (Default)</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2f7e-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="e2f7e-106">VcoreBasedDatabase</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2f7e-107">Переименовав</span><span class="sxs-lookup"><span data-stu-id="e2f7e-107">Rename</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2f7e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2f7e-108">DESCRIPTION</span></span>
<span data-ttu-id="e2f7e-109">Командлет **Set-AzureRmSqlDatabase** задает свойства базы данных в базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-109">The **Set-AzureRmSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="e2f7e-110">Этот командлет может изменить уровень служб ( *выпуск* ), уровень производительности ( *RequestedServiceObjectiveName* ) и максимальный размер хранилища ( *MaxSizeBytes* ) для базы данных.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="e2f7e-111">Кроме того, вы можете указать параметр *ElasticPoolName* , чтобы переместить базу данных в эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="e2f7e-112">Если база данных уже находится в пуле эластичных БД, вы можете использовать параметр *RequestedServiceObjectiveName* , чтобы переместить базу данных из эластичного пула и на уровень производительности для одной базы данных.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="e2f7e-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2f7e-113">EXAMPLES</span></span>

### <span data-ttu-id="e2f7e-114">Пример 1: обновление базы данных на стандартную базу данных S2</span><span class="sxs-lookup"><span data-stu-id="e2f7e-114">Example 1: Update a database to a Standard S2 database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S2"
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
CurrentServiceObjectiveName   : S2
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="e2f7e-115">Эта команда обновляет базу данных с именем Database01 на стандартную базу данных S2 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-115">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="e2f7e-116">Пример 2: Добавление базы данных в эластичный пул</span><span class="sxs-lookup"><span data-stu-id="e2f7e-116">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="e2f7e-117">Эта команда добавляет базу данных с именем Database01 в пул эластичных БД с именем ElasticPool01, размещенный на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="e2f7e-118">Пример 3: изменение максимального размера хранилища базы данных</span><span class="sxs-lookup"><span data-stu-id="e2f7e-118">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
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

<span data-ttu-id="e2f7e-119">Эта команда обновляет базу данных с именем Database01, чтобы установить максимальный размер в 1 ТБ.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="e2f7e-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2f7e-120">PARAMETERS</span></span>

### <span data-ttu-id="e2f7e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2f7e-121">-AsJob</span></span>
<span data-ttu-id="e2f7e-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e2f7e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2f7e-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="e2f7e-123">-ComputeGeneration</span></span>
<span data-ttu-id="e2f7e-124">Вычислено поколение, которое необходимо назначить.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-124">The compute generation to assign.</span></span>

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

### <span data-ttu-id="e2f7e-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e2f7e-125">-DatabaseName</span></span>
<span data-ttu-id="e2f7e-126">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-126">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="e2f7e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2f7e-127">-DefaultProfile</span></span>
<span data-ttu-id="e2f7e-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e2f7e-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2f7e-129">-Edition</span><span class="sxs-lookup"><span data-stu-id="e2f7e-129">-Edition</span></span>
<span data-ttu-id="e2f7e-130">Указывает выпуск для базы данных.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-130">Specifies the edition for the database.</span></span>
<span data-ttu-id="e2f7e-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e2f7e-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e2f7e-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="e2f7e-132">None</span></span>
- <span data-ttu-id="e2f7e-133">Базового</span><span class="sxs-lookup"><span data-stu-id="e2f7e-133">Basic</span></span>
- <span data-ttu-id="e2f7e-134">Стандартная</span><span class="sxs-lookup"><span data-stu-id="e2f7e-134">Standard</span></span>
- <span data-ttu-id="e2f7e-135">Версию</span><span class="sxs-lookup"><span data-stu-id="e2f7e-135">Premium</span></span>
- <span data-ttu-id="e2f7e-136">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="e2f7e-136">DataWarehouse</span></span>
- <span data-ttu-id="e2f7e-137">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="e2f7e-137">Free</span></span>
- <span data-ttu-id="e2f7e-138">Показателя</span><span class="sxs-lookup"><span data-stu-id="e2f7e-138">Stretch</span></span>
- <span data-ttu-id="e2f7e-139">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="e2f7e-139">GeneralPurpose</span></span>
- <span data-ttu-id="e2f7e-140">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="e2f7e-140">BusinessCritical</span></span>

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

### <span data-ttu-id="e2f7e-141">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e2f7e-141">-ElasticPoolName</span></span>
<span data-ttu-id="e2f7e-142">Указывает имя эластичного пула, в который нужно переместить базу данных.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-142">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="e2f7e-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e2f7e-143">-LicenseType</span></span>
<span data-ttu-id="e2f7e-144">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-144">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="e2f7e-145">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="e2f7e-145">-MaxSizeBytes</span></span>
<span data-ttu-id="e2f7e-146">Максимальный размер базы данных Azure SQL в байтах.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-146">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="e2f7e-147">-NewName</span><span class="sxs-lookup"><span data-stu-id="e2f7e-147">-NewName</span></span>
<span data-ttu-id="e2f7e-148">Новое имя, в которое нужно переименовать базу данных.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-148">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="e2f7e-149">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="e2f7e-149">-ReadScale</span></span>
<span data-ttu-id="e2f7e-150">Параметр Read Scale (масштаб чтения), назначаемый базе данных Azure SQL. (Включено или отключено)</span><span class="sxs-lookup"><span data-stu-id="e2f7e-150">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="e2f7e-151">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="e2f7e-151">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="e2f7e-152">Указывает имя цели обслуживания, которую нужно назначить базе данных.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-152">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="e2f7e-153">Сведения о цели обслуживания можно найти на [уровнях служб базы данных Azure SQL Server и уровне производительности](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) в сетевой библиотеке разработчиков Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-153">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="e2f7e-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2f7e-154">-ResourceGroupName</span></span>
<span data-ttu-id="e2f7e-155">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-155">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e2f7e-156">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e2f7e-156">-ServerName</span></span>
<span data-ttu-id="e2f7e-157">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-157">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="e2f7e-158">-Теги</span><span class="sxs-lookup"><span data-stu-id="e2f7e-158">-Tags</span></span>
<span data-ttu-id="e2f7e-159">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-159">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e2f7e-160">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="e2f7e-160">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e2f7e-161">-VCore</span><span class="sxs-lookup"><span data-stu-id="e2f7e-161">-VCore</span></span>
<span data-ttu-id="e2f7e-162">Номер Vcore для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="e2f7e-162">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f7e-163">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="e2f7e-163">-ZoneRedundant</span></span>
<span data-ttu-id="e2f7e-164">Избыточность зоны, связываемая с базой данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-164">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="e2f7e-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2f7e-165">-Confirm</span></span>
<span data-ttu-id="e2f7e-166">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2f7e-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2f7e-167">-WhatIf</span></span>
<span data-ttu-id="e2f7e-168">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2f7e-169">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2f7e-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f7e-170">CommonParameters</span></span>
<span data-ttu-id="e2f7e-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f7e-172">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2f7e-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f7e-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2f7e-173">INPUTS</span></span>

### <span data-ttu-id="e2f7e-174">System. String</span><span class="sxs-lookup"><span data-stu-id="e2f7e-174">System.String</span></span>

## <span data-ttu-id="e2f7e-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2f7e-175">OUTPUTS</span></span>

### <span data-ttu-id="e2f7e-176">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e2f7e-176">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="e2f7e-177">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2f7e-177">NOTES</span></span>

## <span data-ttu-id="e2f7e-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2f7e-178">RELATED LINKS</span></span>

[<span data-ttu-id="e2f7e-179">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e2f7e-179">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="e2f7e-180">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e2f7e-180">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="e2f7e-181">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e2f7e-181">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="e2f7e-182">Возобновить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e2f7e-182">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="e2f7e-183">Приостановить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e2f7e-183">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="e2f7e-184">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="e2f7e-184">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
