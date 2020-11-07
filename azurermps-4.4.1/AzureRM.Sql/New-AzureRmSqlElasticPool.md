---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 454aac300aa3b34cbc435df455100d64c5d0abdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735140"
---
# <span data-ttu-id="55c1e-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="55c1e-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="55c1e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="55c1e-103">Создание пула эластичных баз данных для базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="55c1e-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55c1e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55c1e-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55c1e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55c1e-105">DESCRIPTION</span></span>
<span data-ttu-id="55c1e-106">Командлет **New-AzureRmSqlElasticPool** создает пул эластичных баз данных для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="55c1e-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="55c1e-107">Для нескольких параметров ( *-DTU,-DatabaseDtuMin и-DatabaseDtuMax* ) необходимо, чтобы значение было задано в списке допустимых значений для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="55c1e-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="55c1e-108">Например, параметр-DatabaseDtuMax для стандартного пула 100 eDTU может иметь только значение 10, 20, 50 или 100.</span><span class="sxs-lookup"><span data-stu-id="55c1e-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="55c1e-109">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="55c1e-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="55c1e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55c1e-110">EXAMPLES</span></span>

### <span data-ttu-id="55c1e-111">Пример 1: создание эластичного пула</span><span class="sxs-lookup"><span data-stu-id="55c1e-111">Example 1: Create an elastic pool</span></span>
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

<span data-ttu-id="55c1e-112">Эта команда создает эластичный пул на уровне стандартных служб с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="55c1e-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="55c1e-113">Сервер с именем Server01, назначенный группе ресурсов Azure с именем ResourceGroup01, в которой хранится пул эластичных БД in.</span><span class="sxs-lookup"><span data-stu-id="55c1e-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="55c1e-114">Команда задает значения свойства DTU для пула и баз данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="55c1e-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="55c1e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55c1e-115">PARAMETERS</span></span>

### <span data-ttu-id="55c1e-116">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="55c1e-116">-DatabaseDtuMax</span></span>
<span data-ttu-id="55c1e-117">Указывает максимальное количество единиц пропускной способности базы данных (DTU), которые может использовать любая единственная база данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="55c1e-117">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="55c1e-118">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="55c1e-118">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="55c1e-119">Базового.</span><span class="sxs-lookup"><span data-stu-id="55c1e-119">Basic.</span></span> <span data-ttu-id="55c1e-120">5 DTU</span><span class="sxs-lookup"><span data-stu-id="55c1e-120">5 DTUs</span></span>
- <span data-ttu-id="55c1e-121">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="55c1e-121">Standard.</span></span> <span data-ttu-id="55c1e-122">100 DTU</span><span class="sxs-lookup"><span data-stu-id="55c1e-122">100 DTUs</span></span>
- <span data-ttu-id="55c1e-123">Версию.</span><span class="sxs-lookup"><span data-stu-id="55c1e-123">Premium.</span></span> <span data-ttu-id="55c1e-124">125 DTU</span><span class="sxs-lookup"><span data-stu-id="55c1e-124">125 DTUs</span></span>

<span data-ttu-id="55c1e-125">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="55c1e-125">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


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

### <span data-ttu-id="55c1e-126">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="55c1e-126">-DatabaseDtuMin</span></span>
<span data-ttu-id="55c1e-127">Указывает минимальное количество DTU, которое будет гарантировано для всех баз данных в пуле для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="55c1e-127">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="55c1e-128">Значением по умолчанию является нуль (0).</span><span class="sxs-lookup"><span data-stu-id="55c1e-128">The default value is zero (0).</span></span>

<span data-ttu-id="55c1e-129">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="55c1e-129">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="55c1e-130">-DTU</span><span class="sxs-lookup"><span data-stu-id="55c1e-130">-Dtu</span></span>
<span data-ttu-id="55c1e-131">Указывает общее количество общих DTU для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="55c1e-131">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="55c1e-132">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="55c1e-132">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="55c1e-133">Базового.</span><span class="sxs-lookup"><span data-stu-id="55c1e-133">Basic.</span></span>
<span data-ttu-id="55c1e-134">100 DTU</span><span class="sxs-lookup"><span data-stu-id="55c1e-134">100 DTUs</span></span>
- <span data-ttu-id="55c1e-135">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="55c1e-135">Standard.</span></span>
<span data-ttu-id="55c1e-136">100 DTU</span><span class="sxs-lookup"><span data-stu-id="55c1e-136">100 DTUs</span></span>
- <span data-ttu-id="55c1e-137">Версию.</span><span class="sxs-lookup"><span data-stu-id="55c1e-137">Premium.</span></span>
<span data-ttu-id="55c1e-138">125 DTU</span><span class="sxs-lookup"><span data-stu-id="55c1e-138">125 DTUs</span></span>

<span data-ttu-id="55c1e-139">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="55c1e-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="55c1e-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="55c1e-140">-Edition</span></span>
<span data-ttu-id="55c1e-141">Указывает выпуск базы данных SQL Azure, используемой для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="55c1e-141">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="55c1e-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="55c1e-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="55c1e-143">Версию</span><span class="sxs-lookup"><span data-stu-id="55c1e-143">Premium</span></span>
- <span data-ttu-id="55c1e-144">Базового</span><span class="sxs-lookup"><span data-stu-id="55c1e-144">Basic</span></span>
- <span data-ttu-id="55c1e-145">Стандартная</span><span class="sxs-lookup"><span data-stu-id="55c1e-145">Standard</span></span>
- <span data-ttu-id="55c1e-146">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="55c1e-146">DataWarehouse</span></span>
- <span data-ttu-id="55c1e-147">Показателя</span><span class="sxs-lookup"><span data-stu-id="55c1e-147">Stretch</span></span>
- <span data-ttu-id="55c1e-148">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="55c1e-148">Free</span></span>
- <span data-ttu-id="55c1e-149">PremiumRS</span><span class="sxs-lookup"><span data-stu-id="55c1e-149">PremiumRS</span></span>

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

### <span data-ttu-id="55c1e-150">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="55c1e-150">-ElasticPoolName</span></span>
<span data-ttu-id="55c1e-151">Указывает имя эластичного пула, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="55c1e-151">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="55c1e-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55c1e-152">-ResourceGroupName</span></span>
<span data-ttu-id="55c1e-153">Указывает имя группы ресурсов, к которой этот командлет назначает эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="55c1e-153">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="55c1e-154">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="55c1e-154">-ServerName</span></span>
<span data-ttu-id="55c1e-155">Указывает имя сервера, на котором размещается эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="55c1e-155">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="55c1e-156">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="55c1e-156">-StorageMB</span></span>
<span data-ttu-id="55c1e-157">Указывает предельный размер (в мегабайтах) для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="55c1e-157">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="55c1e-158">Если этот параметр не указан, этот командлет вычисляет значение, которое зависит от значения параметра *DTU* .</span><span class="sxs-lookup"><span data-stu-id="55c1e-158">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="55c1e-159">Просмотр возможных значений для просмотра [eDTU и ограничений хранилища](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) .</span><span class="sxs-lookup"><span data-stu-id="55c1e-159">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="55c1e-160">-Теги</span><span class="sxs-lookup"><span data-stu-id="55c1e-160">-Tags</span></span>
<span data-ttu-id="55c1e-161">Задает словарь пар "ключ-значение" в виде хэш-таблицы, которую этот командлет связывает с пулом эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="55c1e-161">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="55c1e-162">Например:</span><span class="sxs-lookup"><span data-stu-id="55c1e-162">For example:</span></span>

<span data-ttu-id="55c1e-163">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="55c1e-163">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="55c1e-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55c1e-164">-Confirm</span></span>
<span data-ttu-id="55c1e-165">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="55c1e-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55c1e-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55c1e-166">-WhatIf</span></span>
<span data-ttu-id="55c1e-167">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="55c1e-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55c1e-168">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="55c1e-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55c1e-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55c1e-169">-DefaultProfile</span></span>
<span data-ttu-id="55c1e-170">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55c1e-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55c1e-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c1e-171">CommonParameters</span></span>
<span data-ttu-id="55c1e-172">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55c1e-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c1e-173">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55c1e-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c1e-174">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55c1e-174">INPUTS</span></span>

## <span data-ttu-id="55c1e-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55c1e-175">OUTPUTS</span></span>

### <span data-ttu-id="55c1e-176">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="55c1e-176">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="55c1e-177">Пуск</span><span class="sxs-lookup"><span data-stu-id="55c1e-177">NOTES</span></span>

## <span data-ttu-id="55c1e-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55c1e-178">RELATED LINKS</span></span>

[<span data-ttu-id="55c1e-179">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="55c1e-179">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="55c1e-180">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="55c1e-180">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="55c1e-181">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="55c1e-181">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="55c1e-182">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="55c1e-182">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="55c1e-183">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="55c1e-183">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="55c1e-184">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="55c1e-184">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
