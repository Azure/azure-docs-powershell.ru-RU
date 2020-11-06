---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 3d93b0d82a2769acce620ce97141be68c003c281
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566075"
---
# <span data-ttu-id="47990-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="47990-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="47990-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47990-102">SYNOPSIS</span></span>
<span data-ttu-id="47990-103">Создание пула эластичных баз данных для базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="47990-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47990-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47990-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47990-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47990-105">DESCRIPTION</span></span>
<span data-ttu-id="47990-106">Командлет **New-AzureRmSqlElasticPool** создает пул эластичных баз данных для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="47990-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="47990-107">Для нескольких параметров ( *-DTU,-DatabaseDtuMin и-DatabaseDtuMax* ) необходимо, чтобы значение было задано в списке допустимых значений для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="47990-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="47990-108">Например, параметр-DatabaseDtuMax для стандартного пула 100 eDTU может иметь только значение 10, 20, 50 или 100.</span><span class="sxs-lookup"><span data-stu-id="47990-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="47990-109">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="47990-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="47990-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47990-110">EXAMPLES</span></span>

### <span data-ttu-id="47990-111">Пример 1: создание эластичного пула</span><span class="sxs-lookup"><span data-stu-id="47990-111">Example 1: Create an elastic pool</span></span>
```
PS C:\>New-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="47990-112">Эта команда создает эластичный пул на уровне стандартных служб с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="47990-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="47990-113">Сервер с именем Server01, назначенный группе ресурсов Azure с именем ResourceGroup01, в которой хранится пул эластичных БД in.</span><span class="sxs-lookup"><span data-stu-id="47990-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="47990-114">Команда задает значения свойства DTU для пула и баз данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="47990-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="47990-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47990-115">PARAMETERS</span></span>

### <span data-ttu-id="47990-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47990-116">-AsJob</span></span>
<span data-ttu-id="47990-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="47990-117">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="47990-118">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="47990-118">-DatabaseDtuMax</span></span>
<span data-ttu-id="47990-119">Указывает максимальное количество единиц пропускной способности базы данных (DTU), которые может использовать любая единственная база данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="47990-119">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="47990-120">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="47990-120">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="47990-121">Базового.</span><span class="sxs-lookup"><span data-stu-id="47990-121">Basic.</span></span> <span data-ttu-id="47990-122">5 DTU</span><span class="sxs-lookup"><span data-stu-id="47990-122">5 DTUs</span></span>
- <span data-ttu-id="47990-123">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="47990-123">Standard.</span></span> <span data-ttu-id="47990-124">100 DTU</span><span class="sxs-lookup"><span data-stu-id="47990-124">100 DTUs</span></span>
- <span data-ttu-id="47990-125">Версию.</span><span class="sxs-lookup"><span data-stu-id="47990-125">Premium.</span></span> <span data-ttu-id="47990-126">125 DTU</span><span class="sxs-lookup"><span data-stu-id="47990-126">125 DTUs</span></span>

<span data-ttu-id="47990-127">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="47990-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


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

### <span data-ttu-id="47990-128">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="47990-128">-DatabaseDtuMin</span></span>
<span data-ttu-id="47990-129">Указывает минимальное количество DTU, которое будет гарантировано для всех баз данных в пуле для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="47990-129">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="47990-130">Значением по умолчанию является нуль (0).</span><span class="sxs-lookup"><span data-stu-id="47990-130">The default value is zero (0).</span></span>

<span data-ttu-id="47990-131">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="47990-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="47990-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47990-132">-DefaultProfile</span></span>
<span data-ttu-id="47990-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="47990-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47990-134">-DTU</span><span class="sxs-lookup"><span data-stu-id="47990-134">-Dtu</span></span>
<span data-ttu-id="47990-135">Указывает общее количество общих DTU для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="47990-135">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="47990-136">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="47990-136">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="47990-137">Базового.</span><span class="sxs-lookup"><span data-stu-id="47990-137">Basic.</span></span>
<span data-ttu-id="47990-138">100 DTU</span><span class="sxs-lookup"><span data-stu-id="47990-138">100 DTUs</span></span>
- <span data-ttu-id="47990-139">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="47990-139">Standard.</span></span>
<span data-ttu-id="47990-140">100 DTU</span><span class="sxs-lookup"><span data-stu-id="47990-140">100 DTUs</span></span>
- <span data-ttu-id="47990-141">Версию.</span><span class="sxs-lookup"><span data-stu-id="47990-141">Premium.</span></span>
<span data-ttu-id="47990-142">125 DTU</span><span class="sxs-lookup"><span data-stu-id="47990-142">125 DTUs</span></span>

<span data-ttu-id="47990-143">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="47990-143">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="47990-144">-Edition</span><span class="sxs-lookup"><span data-stu-id="47990-144">-Edition</span></span>
<span data-ttu-id="47990-145">Указывает выпуск базы данных SQL Azure, используемой для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="47990-145">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="47990-146">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="47990-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47990-147">Версию</span><span class="sxs-lookup"><span data-stu-id="47990-147">Premium</span></span>
- <span data-ttu-id="47990-148">Базового</span><span class="sxs-lookup"><span data-stu-id="47990-148">Basic</span></span>
- <span data-ttu-id="47990-149">Стандартная</span><span class="sxs-lookup"><span data-stu-id="47990-149">Standard</span></span>
- <span data-ttu-id="47990-150">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="47990-150">DataWarehouse</span></span>
- <span data-ttu-id="47990-151">Показателя</span><span class="sxs-lookup"><span data-stu-id="47990-151">Stretch</span></span>

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

### <span data-ttu-id="47990-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="47990-152">-ElasticPoolName</span></span>
<span data-ttu-id="47990-153">Указывает имя эластичного пула, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="47990-153">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="47990-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47990-154">-ResourceGroupName</span></span>
<span data-ttu-id="47990-155">Указывает имя группы ресурсов, к которой этот командлет назначает эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="47990-155">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="47990-156">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="47990-156">-ServerName</span></span>
<span data-ttu-id="47990-157">Указывает имя сервера, на котором размещается эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="47990-157">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="47990-158">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="47990-158">-StorageMB</span></span>
<span data-ttu-id="47990-159">Указывает предельный размер (в мегабайтах) для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="47990-159">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="47990-160">Если этот параметр не указан, этот командлет вычисляет значение, которое зависит от значения параметра *DTU* .</span><span class="sxs-lookup"><span data-stu-id="47990-160">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="47990-161">Просмотр возможных значений для просмотра [eDTU и ограничений хранилища](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) .</span><span class="sxs-lookup"><span data-stu-id="47990-161">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="47990-162">-Теги</span><span class="sxs-lookup"><span data-stu-id="47990-162">-Tags</span></span>
<span data-ttu-id="47990-163">Задает словарь пар "ключ-значение" в виде хэш-таблицы, которую этот командлет связывает с пулом эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="47990-163">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="47990-164">Например:</span><span class="sxs-lookup"><span data-stu-id="47990-164">For example:</span></span>

<span data-ttu-id="47990-165">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="47990-165">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="47990-166">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="47990-166">-ZoneRedundant</span></span>
<span data-ttu-id="47990-167">Резервирование зоны, связанное с пулом эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="47990-167">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="47990-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47990-168">-Confirm</span></span>
<span data-ttu-id="47990-169">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="47990-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47990-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47990-170">-WhatIf</span></span>
<span data-ttu-id="47990-171">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="47990-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47990-172">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="47990-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47990-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47990-173">CommonParameters</span></span>
<span data-ttu-id="47990-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47990-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47990-175">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47990-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47990-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47990-176">INPUTS</span></span>

### <span data-ttu-id="47990-177">Ничего</span><span class="sxs-lookup"><span data-stu-id="47990-177">None</span></span>
<span data-ttu-id="47990-178">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="47990-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="47990-179">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47990-179">OUTPUTS</span></span>

### <span data-ttu-id="47990-180">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="47990-180">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="47990-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="47990-181">NOTES</span></span>

## <span data-ttu-id="47990-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47990-182">RELATED LINKS</span></span>

[<span data-ttu-id="47990-183">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="47990-183">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="47990-184">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="47990-184">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="47990-185">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="47990-185">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="47990-186">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="47990-186">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="47990-187">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="47990-187">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="47990-188">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="47990-188">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
