---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 22b74b3dcd76577d7c864a3779d12c8474c431a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559452"
---
# <span data-ttu-id="f24c4-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f24c4-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="f24c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f24c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f24c4-103">Создает базу данных или эластичную базу данных.</span><span class="sxs-lookup"><span data-stu-id="f24c4-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f24c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f24c4-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f24c4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f24c4-105">DESCRIPTION</span></span>
<span data-ttu-id="f24c4-106">Командлет **New-AzureRmSqlDatabase** создает базу данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f24c4-106">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>

<span data-ttu-id="f24c4-107">Вы также можете создать эластичную базу данных, указав параметр *ElasticPoolName* в существующем пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="f24c4-107">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="f24c4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f24c4-108">EXAMPLES</span></span>

### <span data-ttu-id="f24c4-109">Пример 1: создание базы данных на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="f24c4-109">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="f24c4-110">Эта команда создает базу данных с именем Database01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="f24c4-110">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="f24c4-111">Пример 2: Создание эластичной базы данных на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="f24c4-111">Example 2: Create an elastic database on a specified server</span></span>
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

<span data-ttu-id="f24c4-112">Эта команда создает базу данных с именем Database01 в пуле эластичных БД с именем ElasticPool01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="f24c4-112">This command creates a database named Database01 in the elastic pool named ElasticPool01 on server Server01.</span></span>

## <span data-ttu-id="f24c4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f24c4-113">PARAMETERS</span></span>

### <span data-ttu-id="f24c4-114">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="f24c4-114">-CatalogCollation</span></span>
<span data-ttu-id="f24c4-115">Задает имена параметров сортировки каталога базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f24c4-115">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="f24c4-116">-CollationName</span><span class="sxs-lookup"><span data-stu-id="f24c4-116">-CollationName</span></span>
<span data-ttu-id="f24c4-117">Задает имя параметров сортировки базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f24c4-117">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="f24c4-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f24c4-118">-DatabaseName</span></span>
<span data-ttu-id="f24c4-119">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="f24c4-119">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="f24c4-120">-Edition</span><span class="sxs-lookup"><span data-stu-id="f24c4-120">-Edition</span></span>
<span data-ttu-id="f24c4-121">Указывает выпуск, назначаемый базе данных.</span><span class="sxs-lookup"><span data-stu-id="f24c4-121">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="f24c4-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f24c4-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f24c4-123">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="f24c4-123">Default</span></span>
- <span data-ttu-id="f24c4-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="f24c4-124">None</span></span>
- <span data-ttu-id="f24c4-125">Версию</span><span class="sxs-lookup"><span data-stu-id="f24c4-125">Premium</span></span>
- <span data-ttu-id="f24c4-126">Базового</span><span class="sxs-lookup"><span data-stu-id="f24c4-126">Basic</span></span>
- <span data-ttu-id="f24c4-127">Стандартная</span><span class="sxs-lookup"><span data-stu-id="f24c4-127">Standard</span></span>
- <span data-ttu-id="f24c4-128">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="f24c4-128">DataWarehouse</span></span>
- <span data-ttu-id="f24c4-129">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="f24c4-129">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f24c4-130">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f24c4-130">-ElasticPoolName</span></span>
<span data-ttu-id="f24c4-131">Указывает имя эластичного пула, в который нужно добавить базу данных.</span><span class="sxs-lookup"><span data-stu-id="f24c4-131">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="f24c4-132">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="f24c4-132">-MaxSizeBytes</span></span>
<span data-ttu-id="f24c4-133">Указывает максимальный размер базы данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="f24c4-133">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="f24c4-134">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="f24c4-134">-ReadScale</span></span>
<span data-ttu-id="f24c4-135">Параметр Read Scale (масштаб чтения), назначаемый базе данных Azure SQL. (Включено или отключено)</span><span class="sxs-lookup"><span data-stu-id="f24c4-135">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="f24c4-136">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="f24c4-136">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="f24c4-137">Указывает имя цели обслуживания, которую нужно назначить базе данных.</span><span class="sxs-lookup"><span data-stu-id="f24c4-137">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="f24c4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f24c4-138">-ResourceGroupName</span></span>
<span data-ttu-id="f24c4-139">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="f24c4-139">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f24c4-140">-SampleName</span><span class="sxs-lookup"><span data-stu-id="f24c4-140">-SampleName</span></span>
<span data-ttu-id="f24c4-141">Имя схемы, применяемой при создании базы данных.</span><span class="sxs-lookup"><span data-stu-id="f24c4-141">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="f24c4-142">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f24c4-142">-ServerName</span></span>
<span data-ttu-id="f24c4-143">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="f24c4-143">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="f24c4-144">-Теги</span><span class="sxs-lookup"><span data-stu-id="f24c4-144">-Tags</span></span>
<span data-ttu-id="f24c4-145">Задает словарь пар "ключ-значение" в виде хэш-таблицы, которую этот командлет свяжет с новой базой данных.</span><span class="sxs-lookup"><span data-stu-id="f24c4-145">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="f24c4-146">Например:</span><span class="sxs-lookup"><span data-stu-id="f24c4-146">For example:</span></span>

<span data-ttu-id="f24c4-147">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="f24c4-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f24c4-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f24c4-148">-Confirm</span></span>
<span data-ttu-id="f24c4-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f24c4-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f24c4-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f24c4-150">-WhatIf</span></span>
<span data-ttu-id="f24c4-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f24c4-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f24c4-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f24c4-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f24c4-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f24c4-153">-DefaultProfile</span></span>
<span data-ttu-id="f24c4-154">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f24c4-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f24c4-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f24c4-155">CommonParameters</span></span>
<span data-ttu-id="f24c4-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f24c4-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f24c4-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f24c4-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f24c4-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f24c4-158">INPUTS</span></span>

## <span data-ttu-id="f24c4-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f24c4-159">OUTPUTS</span></span>

### <span data-ttu-id="f24c4-160">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f24c4-160">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f24c4-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="f24c4-161">NOTES</span></span>

## <span data-ttu-id="f24c4-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f24c4-162">RELATED LINKS</span></span>

[<span data-ttu-id="f24c4-163">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f24c4-163">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="f24c4-164">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f24c4-164">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f24c4-165">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="f24c4-165">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="f24c4-166">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f24c4-166">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="f24c4-167">Возобновить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f24c4-167">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="f24c4-168">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f24c4-168">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="f24c4-169">Приостановить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f24c4-169">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="f24c4-170">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="f24c4-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
