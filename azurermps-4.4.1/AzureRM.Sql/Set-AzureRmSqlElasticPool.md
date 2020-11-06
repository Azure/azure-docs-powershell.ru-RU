---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 512c77862c44af68b26eb300eb9a692c115b0750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562000"
---
# <span data-ttu-id="3523e-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3523e-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="3523e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3523e-102">SYNOPSIS</span></span>
<span data-ttu-id="3523e-103">Изменяет свойства пула эластичных баз данных в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3523e-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3523e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3523e-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3523e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3523e-105">DESCRIPTION</span></span>
<span data-ttu-id="3523e-106">Командлет **Set-AzureRmSqlElasticPool** изменяет свойства пула эластичных баз данных в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3523e-106">The **Set-AzureRmSqlElasticPool** cmdlet modifies properties for an elastic database pool in an Azure SQL Database.</span></span> <span data-ttu-id="3523e-107">Этот командлет может изменить минимальное количество единиц пропускной способности базы данных (DTU) на базу данных в дополнение к максимальному количеству DTU на базу данных, число DTU для пула и ограничение хранилища для пула.</span><span class="sxs-lookup"><span data-stu-id="3523e-107">This cmdlet can modify the minimum Database Throughput Units (DTUs) per database in addition to the maximum DTUs per database, the number of DTUs for the pool, and the storage limit for the pool.</span></span>

<span data-ttu-id="3523e-108">Для нескольких параметров ( *-DTU,-DatabaseDtuMin и-DatabaseDtuMax* ) необходимо, чтобы значение было задано в списке допустимых значений для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="3523e-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="3523e-109">Например, параметр-DatabaseDtuMax для стандартного пула 100 eDTU может иметь только значение 10, 20, 50 или 100.</span><span class="sxs-lookup"><span data-stu-id="3523e-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="3523e-110">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="3523e-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="3523e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3523e-111">EXAMPLES</span></span>

### <span data-ttu-id="3523e-112">Пример 1: изменение свойств эластичного пула</span><span class="sxs-lookup"><span data-stu-id="3523e-112">Example 1: Modify properties for an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 204800
Tags              :
```

<span data-ttu-id="3523e-113">Эта команда изменяет свойства пула эластичных БД с именем elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="3523e-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="3523e-114">Команда задает количество DTU для эластичного пула в 1000 и устанавливает минимальные и максимальные значения DTU.</span><span class="sxs-lookup"><span data-stu-id="3523e-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="3523e-115">Пример 2: изменение максимального хранилища эластичного пула</span><span class="sxs-lookup"><span data-stu-id="3523e-115">Example 2: Modify the max storage of an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Premium
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 2097152
Tags              :
```

<span data-ttu-id="3523e-116">Эта команда изменяет свойства пула эластичных БД с именем elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="3523e-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="3523e-117">Команда задает максимальный объем хранилища для пула эластичных БД равным 2 ТБ.</span><span class="sxs-lookup"><span data-stu-id="3523e-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="3523e-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3523e-118">PARAMETERS</span></span>

### <span data-ttu-id="3523e-119">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="3523e-119">-DatabaseDtuMax</span></span>
<span data-ttu-id="3523e-120">Указывает максимальное количество DTU, которое может использовать любая единственная база данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="3523e-120">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="3523e-121">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="3523e-121">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="3523e-122">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="3523e-122">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="3523e-123">Базового.</span><span class="sxs-lookup"><span data-stu-id="3523e-123">Basic.</span></span>  <span data-ttu-id="3523e-124">5 DTU</span><span class="sxs-lookup"><span data-stu-id="3523e-124">5 DTUs</span></span>
- <span data-ttu-id="3523e-125">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="3523e-125">Standard.</span></span> <span data-ttu-id="3523e-126">100 DTU</span><span class="sxs-lookup"><span data-stu-id="3523e-126">100 DTUs</span></span>
- <span data-ttu-id="3523e-127">Версию.</span><span class="sxs-lookup"><span data-stu-id="3523e-127">Premium.</span></span> <span data-ttu-id="3523e-128">125 DTU</span><span class="sxs-lookup"><span data-stu-id="3523e-128">125 DTUs</span></span>


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

### <span data-ttu-id="3523e-129">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="3523e-129">-DatabaseDtuMin</span></span>
<span data-ttu-id="3523e-130">Указывает минимальное количество DTU, которое будет гарантировано для всех баз данных в пуле для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="3523e-130">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="3523e-131">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="3523e-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="3523e-132">Значением по умолчанию является нуль (0).</span><span class="sxs-lookup"><span data-stu-id="3523e-132">The default value is zero (0).</span></span>

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

### <span data-ttu-id="3523e-133">-DTU</span><span class="sxs-lookup"><span data-stu-id="3523e-133">-Dtu</span></span>
<span data-ttu-id="3523e-134">Указывает общее количество общих DTU для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="3523e-134">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="3523e-135">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="3523e-135">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="3523e-136">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="3523e-136">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="3523e-137">Базового.</span><span class="sxs-lookup"><span data-stu-id="3523e-137">Basic.</span></span> <span data-ttu-id="3523e-138">100 DTU</span><span class="sxs-lookup"><span data-stu-id="3523e-138">100 DTUs</span></span>
- <span data-ttu-id="3523e-139">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="3523e-139">Standard.</span></span> <span data-ttu-id="3523e-140">100 DTU</span><span class="sxs-lookup"><span data-stu-id="3523e-140">100 DTUs</span></span>
- <span data-ttu-id="3523e-141">Версию.</span><span class="sxs-lookup"><span data-stu-id="3523e-141">Premium.</span></span> <span data-ttu-id="3523e-142">125 DTU</span><span class="sxs-lookup"><span data-stu-id="3523e-142">125 DTUs</span></span>

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

### <span data-ttu-id="3523e-143">-Edition</span><span class="sxs-lookup"><span data-stu-id="3523e-143">-Edition</span></span>
<span data-ttu-id="3523e-144">Указывает выпуск базы данных SQL Azure для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="3523e-144">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="3523e-145">Изменить выпуск нельзя.</span><span class="sxs-lookup"><span data-stu-id="3523e-145">You cannot change the edition.</span></span> <span data-ttu-id="3523e-146">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3523e-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3523e-147">Ничего</span><span class="sxs-lookup"><span data-stu-id="3523e-147">None</span></span>
- <span data-ttu-id="3523e-148">Базового</span><span class="sxs-lookup"><span data-stu-id="3523e-148">Basic</span></span>
- <span data-ttu-id="3523e-149">Стандартная</span><span class="sxs-lookup"><span data-stu-id="3523e-149">Standard</span></span>
- <span data-ttu-id="3523e-150">Версию</span><span class="sxs-lookup"><span data-stu-id="3523e-150">Premium</span></span>
- <span data-ttu-id="3523e-151">PremiumRS</span><span class="sxs-lookup"><span data-stu-id="3523e-151">PremiumRS</span></span>
- <span data-ttu-id="3523e-152">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="3523e-152">DataWarehouse</span></span>
- <span data-ttu-id="3523e-153">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="3523e-153">Free</span></span>

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

### <span data-ttu-id="3523e-154">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3523e-154">-ElasticPoolName</span></span>
<span data-ttu-id="3523e-155">Указывает имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="3523e-155">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="3523e-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3523e-156">-ResourceGroupName</span></span>
<span data-ttu-id="3523e-157">Указывает имя группы ресурсов, которой назначен эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="3523e-157">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="3523e-158">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3523e-158">-ServerName</span></span>
<span data-ttu-id="3523e-159">Указывает имя сервера, на котором размещается эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="3523e-159">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="3523e-160">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="3523e-160">-StorageMB</span></span>
<span data-ttu-id="3523e-161">Указывает предельный размер (в мегабайтах) для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="3523e-161">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="3523e-162">Дополнительные сведения можно найти в командлетах New-AzureRmSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="3523e-162">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="3523e-163">-Теги</span><span class="sxs-lookup"><span data-stu-id="3523e-163">-Tags</span></span>
<span data-ttu-id="3523e-164">Указывает словарь пар "ключ-значение", который этот командлет связывает с пулом эластичных БД в форме хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="3523e-164">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="3523e-165">Например:</span><span class="sxs-lookup"><span data-stu-id="3523e-165">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

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

### <span data-ttu-id="3523e-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3523e-166">-Confirm</span></span>
<span data-ttu-id="3523e-167">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3523e-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3523e-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3523e-168">-WhatIf</span></span>
<span data-ttu-id="3523e-169">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3523e-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3523e-170">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3523e-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3523e-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3523e-171">-DefaultProfile</span></span>
<span data-ttu-id="3523e-172">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3523e-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3523e-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3523e-173">CommonParameters</span></span>
<span data-ttu-id="3523e-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3523e-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3523e-175">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3523e-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3523e-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3523e-176">INPUTS</span></span>

## <span data-ttu-id="3523e-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3523e-177">OUTPUTS</span></span>

### <span data-ttu-id="3523e-178">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="3523e-178">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="3523e-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="3523e-179">NOTES</span></span>

## <span data-ttu-id="3523e-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3523e-180">RELATED LINKS</span></span>

[<span data-ttu-id="3523e-181">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3523e-181">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="3523e-182">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="3523e-182">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="3523e-183">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="3523e-183">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="3523e-184">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3523e-184">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="3523e-185">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="3523e-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
