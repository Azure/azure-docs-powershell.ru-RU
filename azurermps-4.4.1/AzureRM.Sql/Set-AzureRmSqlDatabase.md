---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: 3d36c94ebcc1b733559f9fb4075fb20e4ec67144
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732677"
---
# <span data-ttu-id="42a7a-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="42a7a-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="42a7a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42a7a-102">SYNOPSIS</span></span>
<span data-ttu-id="42a7a-103">Задает свойства базы данных или перемещает существующую базу данных в эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="42a7a-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42a7a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42a7a-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42a7a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42a7a-105">DESCRIPTION</span></span>
<span data-ttu-id="42a7a-106">Командлет **Set-AzureRmSqlDatabase** задает свойства для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="42a7a-106">The **Set-AzureRmSqlDatabase** cmdlet sets properties for an Azure SQL database.</span></span>
<span data-ttu-id="42a7a-107">Кроме того, вы можете указать параметр *ElasticPoolName* , чтобы переместить базу данных в эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="42a7a-107">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span>
<span data-ttu-id="42a7a-108">Если база данных уже находится в пуле эластичных БД, можно использовать параметр *RequestedServiceObjectiveName* для назначения уровня производительности.</span><span class="sxs-lookup"><span data-stu-id="42a7a-108">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to assign a performance level.</span></span>

## <span data-ttu-id="42a7a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42a7a-109">EXAMPLES</span></span>

### <span data-ttu-id="42a7a-110">Пример 1: обновление базы данных на стандартную базу данных S2</span><span class="sxs-lookup"><span data-stu-id="42a7a-110">Example 1: Update a database to a Standard S2 database</span></span>
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

<span data-ttu-id="42a7a-111">Эта команда обновляет базу данных с именем Database01 на стандартную базу данных S2 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="42a7a-111">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="42a7a-112">Пример 2: Добавление базы данных в эластичный пул</span><span class="sxs-lookup"><span data-stu-id="42a7a-112">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="42a7a-113">Эта команда добавляет базу данных с именем Database01 в пул эластичных БД с именем ElasticPool01, размещенный на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="42a7a-113">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

## <span data-ttu-id="42a7a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42a7a-114">PARAMETERS</span></span>

### <span data-ttu-id="42a7a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="42a7a-115">-DatabaseName</span></span>
<span data-ttu-id="42a7a-116">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="42a7a-116">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="42a7a-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="42a7a-117">-Edition</span></span>
<span data-ttu-id="42a7a-118">Указывает выпуск для базы данных.</span><span class="sxs-lookup"><span data-stu-id="42a7a-118">Specifies the edition for the database.</span></span>
<span data-ttu-id="42a7a-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="42a7a-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="42a7a-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="42a7a-120">None</span></span>
- <span data-ttu-id="42a7a-121">Версию</span><span class="sxs-lookup"><span data-stu-id="42a7a-121">Premium</span></span>
- <span data-ttu-id="42a7a-122">Базового</span><span class="sxs-lookup"><span data-stu-id="42a7a-122">Basic</span></span>
- <span data-ttu-id="42a7a-123">Стандартная</span><span class="sxs-lookup"><span data-stu-id="42a7a-123">Standard</span></span>
- <span data-ttu-id="42a7a-124">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="42a7a-124">DataWarehouse</span></span>
- <span data-ttu-id="42a7a-125">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="42a7a-125">Free</span></span>

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

### <span data-ttu-id="42a7a-126">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="42a7a-126">-ElasticPoolName</span></span>
<span data-ttu-id="42a7a-127">Указывает имя эластичного пула, в который нужно переместить базу данных.</span><span class="sxs-lookup"><span data-stu-id="42a7a-127">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="42a7a-128">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="42a7a-128">-MaxSizeBytes</span></span>
<span data-ttu-id="42a7a-129">Указание нового максимального размера базы данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="42a7a-129">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="42a7a-130">Вы можете указать либо этот параметр, либо *MaxSizeGB*.</span><span class="sxs-lookup"><span data-stu-id="42a7a-130">You can specify either this parameter or *MaxSizeGB*.</span></span>
<span data-ttu-id="42a7a-131">Для приемлемых значений в выпуске просмотрите параметр *MaxSizeGB* .</span><span class="sxs-lookup"><span data-stu-id="42a7a-131">See the *MaxSizeGB* parameter for acceptable values per edition.</span></span>

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

### <span data-ttu-id="42a7a-132">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="42a7a-132">-ReadScale</span></span>
<span data-ttu-id="42a7a-133">Параметр Read Scale (масштаб чтения), назначаемый базе данных Azure SQL. (Включено или отключено)</span><span class="sxs-lookup"><span data-stu-id="42a7a-133">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="42a7a-134">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="42a7a-134">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="42a7a-135">Указывает имя цели обслуживания, которую нужно назначить базе данных.</span><span class="sxs-lookup"><span data-stu-id="42a7a-135">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="42a7a-136">Сведения о цели обслуживания можно найти на [уровнях служб базы данных Azure SQL Server и уровне производительности](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) в сетевой библиотеке разработчиков Microsoft.</span><span class="sxs-lookup"><span data-stu-id="42a7a-136">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="42a7a-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42a7a-137">-ResourceGroupName</span></span>
<span data-ttu-id="42a7a-138">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="42a7a-138">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="42a7a-139">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="42a7a-139">-ServerName</span></span>
<span data-ttu-id="42a7a-140">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="42a7a-140">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="42a7a-141">-Теги</span><span class="sxs-lookup"><span data-stu-id="42a7a-141">-Tags</span></span>
<span data-ttu-id="42a7a-142">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="42a7a-142">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="42a7a-143">Например:</span><span class="sxs-lookup"><span data-stu-id="42a7a-143">For example:</span></span>

<span data-ttu-id="42a7a-144">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="42a7a-144">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="42a7a-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42a7a-145">-Confirm</span></span>
<span data-ttu-id="42a7a-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="42a7a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42a7a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42a7a-147">-WhatIf</span></span>
<span data-ttu-id="42a7a-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="42a7a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42a7a-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="42a7a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42a7a-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42a7a-150">-DefaultProfile</span></span>
<span data-ttu-id="42a7a-151">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42a7a-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42a7a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42a7a-152">CommonParameters</span></span>
<span data-ttu-id="42a7a-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42a7a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42a7a-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42a7a-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42a7a-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42a7a-155">INPUTS</span></span>

## <span data-ttu-id="42a7a-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42a7a-156">OUTPUTS</span></span>

### <span data-ttu-id="42a7a-157">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="42a7a-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="42a7a-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="42a7a-158">NOTES</span></span>

## <span data-ttu-id="42a7a-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42a7a-159">RELATED LINKS</span></span>

[<span data-ttu-id="42a7a-160">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="42a7a-160">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="42a7a-161">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="42a7a-161">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="42a7a-162">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="42a7a-162">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="42a7a-163">Возобновить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="42a7a-163">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="42a7a-164">Приостановить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="42a7a-164">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="42a7a-165">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="42a7a-165">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
