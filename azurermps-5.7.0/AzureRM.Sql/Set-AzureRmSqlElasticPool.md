---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 563cddc1723f0706eb5cdde691e9ab960e871989
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566055"
---
# <span data-ttu-id="17d5a-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="17d5a-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="17d5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="17d5a-103">Изменяет свойства пула эластичных баз данных в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="17d5a-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17d5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17d5a-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17d5a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17d5a-105">DESCRIPTION</span></span>
<span data-ttu-id="17d5a-106">Командлет **Set-AzureRmSqlElasticPool** задает свойства для пула эластичных БД в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="17d5a-106">The **Set-AzureRmSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="17d5a-107">Этот командлет может изменить eDTUs для каждого пула ( *DTU* ), максимальный размер хранилища для пула ( *StorageMB* ), максимум eDTUs на базу данных ( *DatabaseDtuMax* ) и минимальный eDTUs на базу данных ( *DatqabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="17d5a-107">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatqabaseDtuMin* ).</span></span>

<span data-ttu-id="17d5a-108">Для нескольких параметров ( *-DTU,-DatabaseDtuMin и-DatabaseDtuMax* ) необходимо, чтобы значение было задано в списке допустимых значений для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="17d5a-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="17d5a-109">Например, параметр-DatabaseDtuMax для стандартного пула 100 eDTU может иметь только значение 10, 20, 50 или 100.</span><span class="sxs-lookup"><span data-stu-id="17d5a-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="17d5a-110">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="17d5a-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="17d5a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17d5a-111">EXAMPLES</span></span>

### <span data-ttu-id="17d5a-112">Пример 1: изменение свойств эластичного пула</span><span class="sxs-lookup"><span data-stu-id="17d5a-112">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="17d5a-113">Эта команда изменяет свойства пула эластичных БД с именем elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="17d5a-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="17d5a-114">Команда задает количество DTU для эластичного пула в 1000 и устанавливает минимальные и максимальные значения DTU.</span><span class="sxs-lookup"><span data-stu-id="17d5a-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="17d5a-115">Пример 2: изменение максимального размера хранилища эластичного пула</span><span class="sxs-lookup"><span data-stu-id="17d5a-115">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="17d5a-116">Эта команда изменяет свойства пула эластичных БД с именем elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="17d5a-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="17d5a-117">Команда задает максимальный объем хранилища для пула эластичных БД равным 2 ТБ.</span><span class="sxs-lookup"><span data-stu-id="17d5a-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="17d5a-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17d5a-118">PARAMETERS</span></span>

### <span data-ttu-id="17d5a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17d5a-119">-AsJob</span></span>
<span data-ttu-id="17d5a-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="17d5a-120">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="17d5a-121">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="17d5a-121">-DatabaseDtuMax</span></span>
<span data-ttu-id="17d5a-122">Указывает максимальное количество DTU, которое может использовать любая единственная база данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="17d5a-122">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="17d5a-123">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="17d5a-123">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="17d5a-124">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="17d5a-124">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="17d5a-125">Базового.</span><span class="sxs-lookup"><span data-stu-id="17d5a-125">Basic.</span></span>  <span data-ttu-id="17d5a-126">5 DTU</span><span class="sxs-lookup"><span data-stu-id="17d5a-126">5 DTUs</span></span>
- <span data-ttu-id="17d5a-127">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="17d5a-127">Standard.</span></span> <span data-ttu-id="17d5a-128">100 DTU</span><span class="sxs-lookup"><span data-stu-id="17d5a-128">100 DTUs</span></span>
- <span data-ttu-id="17d5a-129">Версию.</span><span class="sxs-lookup"><span data-stu-id="17d5a-129">Premium.</span></span> <span data-ttu-id="17d5a-130">125 DTU</span><span class="sxs-lookup"><span data-stu-id="17d5a-130">125 DTUs</span></span>


```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d5a-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="17d5a-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="17d5a-132">Указывает минимальное количество DTU, которое будет гарантировано для всех баз данных в пуле для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="17d5a-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="17d5a-133">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="17d5a-133">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="17d5a-134">Значением по умолчанию является нуль (0).</span><span class="sxs-lookup"><span data-stu-id="17d5a-134">The default value is zero (0).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d5a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17d5a-135">-DefaultProfile</span></span>
<span data-ttu-id="17d5a-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="17d5a-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17d5a-137">-DTU</span><span class="sxs-lookup"><span data-stu-id="17d5a-137">-Dtu</span></span>
<span data-ttu-id="17d5a-138">Указывает общее количество общих DTU для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="17d5a-138">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="17d5a-139">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="17d5a-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="17d5a-140">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="17d5a-140">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="17d5a-141">Базового.</span><span class="sxs-lookup"><span data-stu-id="17d5a-141">Basic.</span></span> <span data-ttu-id="17d5a-142">100 DTU</span><span class="sxs-lookup"><span data-stu-id="17d5a-142">100 DTUs</span></span>
- <span data-ttu-id="17d5a-143">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="17d5a-143">Standard.</span></span> <span data-ttu-id="17d5a-144">100 DTU</span><span class="sxs-lookup"><span data-stu-id="17d5a-144">100 DTUs</span></span>
- <span data-ttu-id="17d5a-145">Версию.</span><span class="sxs-lookup"><span data-stu-id="17d5a-145">Premium.</span></span> <span data-ttu-id="17d5a-146">125 DTU</span><span class="sxs-lookup"><span data-stu-id="17d5a-146">125 DTUs</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d5a-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="17d5a-147">-Edition</span></span>
<span data-ttu-id="17d5a-148">Указывает выпуск базы данных SQL Azure для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="17d5a-148">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="17d5a-149">Изменить выпуск нельзя.</span><span class="sxs-lookup"><span data-stu-id="17d5a-149">You cannot change the edition.</span></span> <span data-ttu-id="17d5a-150">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="17d5a-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="17d5a-151">Ничего</span><span class="sxs-lookup"><span data-stu-id="17d5a-151">None</span></span>
- <span data-ttu-id="17d5a-152">Базового</span><span class="sxs-lookup"><span data-stu-id="17d5a-152">Basic</span></span>
- <span data-ttu-id="17d5a-153">Стандартная</span><span class="sxs-lookup"><span data-stu-id="17d5a-153">Standard</span></span>
- <span data-ttu-id="17d5a-154">Версию</span><span class="sxs-lookup"><span data-stu-id="17d5a-154">Premium</span></span>
- <span data-ttu-id="17d5a-155">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="17d5a-155">DataWarehouse</span></span>

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

### <span data-ttu-id="17d5a-156">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="17d5a-156">-ElasticPoolName</span></span>
<span data-ttu-id="17d5a-157">Указывает имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="17d5a-157">Specifies the name of the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17d5a-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17d5a-158">-ResourceGroupName</span></span>
<span data-ttu-id="17d5a-159">Указывает имя группы ресурсов, которой назначен эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="17d5a-159">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="17d5a-160">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="17d5a-160">-ServerName</span></span>
<span data-ttu-id="17d5a-161">Указывает имя сервера, на котором размещается эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="17d5a-161">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="17d5a-162">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="17d5a-162">-StorageMB</span></span>
<span data-ttu-id="17d5a-163">Указывает предельный размер (в мегабайтах) для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="17d5a-163">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="17d5a-164">Дополнительные сведения можно найти в командлетах New-AzureRmSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="17d5a-164">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d5a-165">-Теги</span><span class="sxs-lookup"><span data-stu-id="17d5a-165">-Tags</span></span>
<span data-ttu-id="17d5a-166">Указывает словарь пар "ключ-значение", который этот командлет связывает с пулом эластичных БД в форме хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="17d5a-166">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="17d5a-167">Например:</span><span class="sxs-lookup"><span data-stu-id="17d5a-167">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

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

### <span data-ttu-id="17d5a-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="17d5a-168">-ZoneRedundant</span></span>
<span data-ttu-id="17d5a-169">Резервирование зоны, связанное с пулом эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="17d5a-169">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="17d5a-170">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17d5a-170">-Confirm</span></span>
<span data-ttu-id="17d5a-171">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="17d5a-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17d5a-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17d5a-172">-WhatIf</span></span>
<span data-ttu-id="17d5a-173">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="17d5a-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17d5a-174">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="17d5a-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17d5a-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17d5a-175">CommonParameters</span></span>
<span data-ttu-id="17d5a-176">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17d5a-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17d5a-177">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17d5a-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17d5a-178">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17d5a-178">INPUTS</span></span>

### <span data-ttu-id="17d5a-179">Ничего</span><span class="sxs-lookup"><span data-stu-id="17d5a-179">None</span></span>
<span data-ttu-id="17d5a-180">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="17d5a-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="17d5a-181">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17d5a-181">OUTPUTS</span></span>

### <span data-ttu-id="17d5a-182">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="17d5a-182">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="17d5a-183">Пуск</span><span class="sxs-lookup"><span data-stu-id="17d5a-183">NOTES</span></span>

## <span data-ttu-id="17d5a-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17d5a-184">RELATED LINKS</span></span>

[<span data-ttu-id="17d5a-185">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="17d5a-185">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="17d5a-186">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="17d5a-186">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="17d5a-187">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="17d5a-187">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="17d5a-188">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="17d5a-188">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="17d5a-189">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="17d5a-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
