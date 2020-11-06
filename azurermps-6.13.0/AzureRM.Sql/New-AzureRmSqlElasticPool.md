---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 5b1901ef5d06d24e6561861dca3c8e1d89185d14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563936"
---
# <span data-ttu-id="4d995-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4d995-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="4d995-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d995-102">SYNOPSIS</span></span>
<span data-ttu-id="4d995-103">Создание пула эластичных баз данных для базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="4d995-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d995-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d995-104">SYNTAX</span></span>

### <span data-ttu-id="4d995-105">DtuBasedPool (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4d995-105">DtuBasedPool (Default)</span></span>
```
New-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d995-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="4d995-106">VcoreBasedPool</span></span>
```
New-AzureRmSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d995-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d995-107">DESCRIPTION</span></span>
<span data-ttu-id="4d995-108">Командлет **New-AzureRmSqlElasticPool** создает пул эластичных баз данных для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4d995-108">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="4d995-109">Для нескольких параметров ( *-DTU,-DatabaseDtuMin и-DatabaseDtuMax* ) необходимо, чтобы значение было задано в списке допустимых значений для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="4d995-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="4d995-110">Например, параметр-DatabaseDtuMax для стандартного пула 100 eDTU может иметь только значение 10, 20, 50 или 100.</span><span class="sxs-lookup"><span data-stu-id="4d995-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="4d995-111">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="4d995-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="4d995-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d995-112">EXAMPLES</span></span>

### <span data-ttu-id="4d995-113">Пример 1: создание эластичного пула</span><span class="sxs-lookup"><span data-stu-id="4d995-113">Example 1: Create an elastic pool</span></span>
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

<span data-ttu-id="4d995-114">Эта команда создает эластичный пул на уровне стандартных служб с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="4d995-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="4d995-115">Сервер с именем Server01, назначенный группе ресурсов Azure с именем ResourceGroup01, в которой хранится пул эластичных БД in.</span><span class="sxs-lookup"><span data-stu-id="4d995-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="4d995-116">Команда задает значения свойства DTU для пула и баз данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="4d995-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="4d995-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d995-117">PARAMETERS</span></span>

### <span data-ttu-id="4d995-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d995-118">-AsJob</span></span>
<span data-ttu-id="4d995-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4d995-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d995-120">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="4d995-120">-ComputeGeneration</span></span>
<span data-ttu-id="4d995-121">Вычислено поколение, которое необходимо назначить.</span><span class="sxs-lookup"><span data-stu-id="4d995-121">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d995-122">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="4d995-122">-DatabaseDtuMax</span></span>
<span data-ttu-id="4d995-123">Указывает максимальное количество единиц пропускной способности базы данных (DTU), которые может использовать любая единственная база данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="4d995-123">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="4d995-124">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="4d995-124">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="4d995-125">Базового.</span><span class="sxs-lookup"><span data-stu-id="4d995-125">Basic.</span></span> <span data-ttu-id="4d995-126">5 DTU</span><span class="sxs-lookup"><span data-stu-id="4d995-126">5 DTUs</span></span>
- <span data-ttu-id="4d995-127">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="4d995-127">Standard.</span></span> <span data-ttu-id="4d995-128">100 DTU</span><span class="sxs-lookup"><span data-stu-id="4d995-128">100 DTUs</span></span>
- <span data-ttu-id="4d995-129">Версию.</span><span class="sxs-lookup"><span data-stu-id="4d995-129">Premium.</span></span> <span data-ttu-id="4d995-130">125 DTU для получения подробных сведений о допустимых значениях, ознакомьтесь с таблицей для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) .</span><span class="sxs-lookup"><span data-stu-id="4d995-130">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d995-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="4d995-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="4d995-132">Указывает минимальное количество DTU, которое будет гарантировано для всех баз данных в пуле для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="4d995-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="4d995-133">Значением по умолчанию является нуль (0).</span><span class="sxs-lookup"><span data-stu-id="4d995-133">The default value is zero (0).</span></span>
<span data-ttu-id="4d995-134">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="4d995-134">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d995-135">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="4d995-135">-DatabaseVCoreMax</span></span>
<span data-ttu-id="4d995-136">Maxmium VCore число, которое может использовать любая SqlAzure база данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="4d995-136">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d995-137">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="4d995-137">-DatabaseVCoreMin</span></span>
<span data-ttu-id="4d995-138">Минимальный номер VCore, который любая база данных SqlAzure может использовать в пуле.</span><span class="sxs-lookup"><span data-stu-id="4d995-138">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d995-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d995-139">-DefaultProfile</span></span>
<span data-ttu-id="4d995-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4d995-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d995-141">-DTU</span><span class="sxs-lookup"><span data-stu-id="4d995-141">-Dtu</span></span>
<span data-ttu-id="4d995-142">Указывает общее количество общих DTU для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="4d995-142">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="4d995-143">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="4d995-143">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="4d995-144">Базового.</span><span class="sxs-lookup"><span data-stu-id="4d995-144">Basic.</span></span>
<span data-ttu-id="4d995-145">100 DTU</span><span class="sxs-lookup"><span data-stu-id="4d995-145">100 DTUs</span></span>
- <span data-ttu-id="4d995-146">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="4d995-146">Standard.</span></span>
<span data-ttu-id="4d995-147">100 DTU</span><span class="sxs-lookup"><span data-stu-id="4d995-147">100 DTUs</span></span>
- <span data-ttu-id="4d995-148">Версию.</span><span class="sxs-lookup"><span data-stu-id="4d995-148">Premium.</span></span>
<span data-ttu-id="4d995-149">125 DTU для получения сведений о допустимых значениях, ознакомьтесь с таблицей для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="4d995-149">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d995-150">-Edition</span><span class="sxs-lookup"><span data-stu-id="4d995-150">-Edition</span></span>
<span data-ttu-id="4d995-151">Указывает выпуск базы данных SQL Azure, используемой для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="4d995-151">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="4d995-152">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4d995-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4d995-153">Ничего</span><span class="sxs-lookup"><span data-stu-id="4d995-153">None</span></span>
- <span data-ttu-id="4d995-154">Базового</span><span class="sxs-lookup"><span data-stu-id="4d995-154">Basic</span></span>
- <span data-ttu-id="4d995-155">Стандартная</span><span class="sxs-lookup"><span data-stu-id="4d995-155">Standard</span></span>
- <span data-ttu-id="4d995-156">Версию</span><span class="sxs-lookup"><span data-stu-id="4d995-156">Premium</span></span>
- <span data-ttu-id="4d995-157">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="4d995-157">DataWarehouse</span></span>
- <span data-ttu-id="4d995-158">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="4d995-158">Free</span></span>
- <span data-ttu-id="4d995-159">Показателя</span><span class="sxs-lookup"><span data-stu-id="4d995-159">Stretch</span></span>
- <span data-ttu-id="4d995-160">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="4d995-160">GeneralPurpose</span></span>
- <span data-ttu-id="4d995-161">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="4d995-161">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d995-162">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4d995-162">-ElasticPoolName</span></span>
<span data-ttu-id="4d995-163">Указывает имя эластичного пула, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4d995-163">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d995-164">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4d995-164">-LicenseType</span></span>
<span data-ttu-id="4d995-165">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4d995-165">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="4d995-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d995-166">-ResourceGroupName</span></span>
<span data-ttu-id="4d995-167">Указывает имя группы ресурсов, к которой этот командлет назначает эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="4d995-167">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="4d995-168">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="4d995-168">-ServerName</span></span>
<span data-ttu-id="4d995-169">Указывает имя сервера, на котором размещается эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="4d995-169">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="4d995-170">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="4d995-170">-StorageMB</span></span>
<span data-ttu-id="4d995-171">Указывает предельный размер (в мегабайтах) для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="4d995-171">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="4d995-172">Если этот параметр не указан, этот командлет вычисляет значение, которое зависит от значения параметра *DTU* .</span><span class="sxs-lookup"><span data-stu-id="4d995-172">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="4d995-173">Просмотр возможных значений для просмотра [eDTU и ограничений хранилища](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) .</span><span class="sxs-lookup"><span data-stu-id="4d995-173">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="4d995-174">-Теги</span><span class="sxs-lookup"><span data-stu-id="4d995-174">-Tags</span></span>
<span data-ttu-id="4d995-175">Задает словарь пар "ключ-значение" в виде хэш-таблицы, которую этот командлет связывает с пулом эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="4d995-175">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="4d995-176">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="4d995-176">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4d995-177">-VCore</span><span class="sxs-lookup"><span data-stu-id="4d995-177">-VCore</span></span>
<span data-ttu-id="4d995-178">Общее количество общего числа Vcores для пула эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4d995-178">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d995-179">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="4d995-179">-ZoneRedundant</span></span>
<span data-ttu-id="4d995-180">Резервирование зоны, связанное с пулом эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4d995-180">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="4d995-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d995-181">-Confirm</span></span>
<span data-ttu-id="4d995-182">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4d995-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d995-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d995-183">-WhatIf</span></span>
<span data-ttu-id="4d995-184">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4d995-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d995-185">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4d995-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d995-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d995-186">CommonParameters</span></span>
<span data-ttu-id="4d995-187">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d995-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d995-188">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d995-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d995-189">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d995-189">INPUTS</span></span>

### <span data-ttu-id="4d995-190">System. String</span><span class="sxs-lookup"><span data-stu-id="4d995-190">System.String</span></span>

## <span data-ttu-id="4d995-191">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d995-191">OUTPUTS</span></span>

### <span data-ttu-id="4d995-192">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="4d995-192">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="4d995-193">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d995-193">NOTES</span></span>

## <span data-ttu-id="4d995-194">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d995-194">RELATED LINKS</span></span>

[<span data-ttu-id="4d995-195">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4d995-195">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="4d995-196">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="4d995-196">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="4d995-197">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="4d995-197">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="4d995-198">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4d995-198">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="4d995-199">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4d995-199">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="4d995-200">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="4d995-200">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
