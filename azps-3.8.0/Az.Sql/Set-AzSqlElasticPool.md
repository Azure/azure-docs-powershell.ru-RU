---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: a40b5bd15681342975ddb080fa12fbaac9bcf60e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912601"
---
# <span data-ttu-id="bd555-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bd555-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="bd555-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd555-102">SYNOPSIS</span></span>
<span data-ttu-id="bd555-103">Изменяет свойства пула эластичных баз данных в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="bd555-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="bd555-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd555-104">SYNTAX</span></span>

### <span data-ttu-id="bd555-105">DtuBasedPool (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd555-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd555-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="bd555-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd555-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd555-107">DESCRIPTION</span></span>
<span data-ttu-id="bd555-108">Командлет **Set-AzSqlElasticPool** задает свойства для пула эластичных БД в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="bd555-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="bd555-109">Этот командлет может изменить eDTUs для каждого пула ( *DTU* ), максимальный размер хранилища для пула ( *StorageMB* ), максимум eDTUs на базу данных ( *DatabaseDtuMax* ) и минимальный eDTUs на базу данных ( *DatabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="bd555-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatabaseDtuMin* ).</span></span>
<span data-ttu-id="bd555-110">Для нескольких параметров ( *-DTU,-DatabaseDtuMin и-DatabaseDtuMax* ) необходимо, чтобы значение было задано в списке допустимых значений для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="bd555-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="bd555-111">Например, параметр-DatabaseDtuMax для стандартного пула 100 eDTU может иметь только значение 10, 20, 50 или 100.</span><span class="sxs-lookup"><span data-stu-id="bd555-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="bd555-112">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="bd555-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="bd555-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd555-113">EXAMPLES</span></span>

### <span data-ttu-id="bd555-114">Пример 1: изменение свойств эластичного пула</span><span class="sxs-lookup"><span data-stu-id="bd555-114">Example 1: Modify properties for an elastic pool</span></span>
```
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
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

<span data-ttu-id="bd555-115">Эта команда изменяет свойства пула эластичных БД с именем elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="bd555-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="bd555-116">Команда задает количество DTU для эластичного пула в 1000 и устанавливает минимальные и максимальные значения DTU.</span><span class="sxs-lookup"><span data-stu-id="bd555-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="bd555-117">Пример 2: изменение максимального размера хранилища эластичного пула</span><span class="sxs-lookup"><span data-stu-id="bd555-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
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

<span data-ttu-id="bd555-118">Эта команда изменяет свойства пула эластичных БД с именем elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="bd555-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="bd555-119">Команда задает максимальный объем хранилища для пула эластичных БД равным 2 ТБ.</span><span class="sxs-lookup"><span data-stu-id="bd555-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="bd555-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd555-120">PARAMETERS</span></span>

### <span data-ttu-id="bd555-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd555-121">-AsJob</span></span>
<span data-ttu-id="bd555-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bd555-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd555-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="bd555-123">-ComputeGeneration</span></span>
<span data-ttu-id="bd555-124">Вычислено поколение, которое необходимо назначить.</span><span class="sxs-lookup"><span data-stu-id="bd555-124">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd555-125">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="bd555-125">-DatabaseDtuMax</span></span>
<span data-ttu-id="bd555-126">Указывает максимальное количество DTU, которое может использовать любая единственная база данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="bd555-126">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="bd555-127">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="bd555-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="bd555-128">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="bd555-128">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="bd555-129">Базового.</span><span class="sxs-lookup"><span data-stu-id="bd555-129">Basic.</span></span>  <span data-ttu-id="bd555-130">5 DTU</span><span class="sxs-lookup"><span data-stu-id="bd555-130">5 DTUs</span></span>
- <span data-ttu-id="bd555-131">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="bd555-131">Standard.</span></span> <span data-ttu-id="bd555-132">100 DTU</span><span class="sxs-lookup"><span data-stu-id="bd555-132">100 DTUs</span></span>
- <span data-ttu-id="bd555-133">Версию.</span><span class="sxs-lookup"><span data-stu-id="bd555-133">Premium.</span></span> <span data-ttu-id="bd555-134">125 DTU</span><span class="sxs-lookup"><span data-stu-id="bd555-134">125 DTUs</span></span>

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

### <span data-ttu-id="bd555-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="bd555-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="bd555-136">Указывает минимальное количество DTU, которое будет гарантировано для всех баз данных в пуле для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="bd555-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="bd555-137">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="bd555-137">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="bd555-138">Значением по умолчанию является нуль (0).</span><span class="sxs-lookup"><span data-stu-id="bd555-138">The default value is zero (0).</span></span>

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

### <span data-ttu-id="bd555-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="bd555-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="bd555-140">Максимальный номер VCore, который любая база данных SqlAzure может использовать в пуле.</span><span class="sxs-lookup"><span data-stu-id="bd555-140">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="bd555-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="bd555-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="bd555-142">Минимальный номер VCore, который любая база данных SqlAzure может использовать в пуле.</span><span class="sxs-lookup"><span data-stu-id="bd555-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="bd555-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd555-143">-DefaultProfile</span></span>
<span data-ttu-id="bd555-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bd555-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd555-145">-DTU</span><span class="sxs-lookup"><span data-stu-id="bd555-145">-Dtu</span></span>
<span data-ttu-id="bd555-146">Указывает общее количество общих DTU для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="bd555-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="bd555-147">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="bd555-147">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="bd555-148">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="bd555-148">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="bd555-149">Базового.</span><span class="sxs-lookup"><span data-stu-id="bd555-149">Basic.</span></span> <span data-ttu-id="bd555-150">100 DTU</span><span class="sxs-lookup"><span data-stu-id="bd555-150">100 DTUs</span></span>
- <span data-ttu-id="bd555-151">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="bd555-151">Standard.</span></span> <span data-ttu-id="bd555-152">100 DTU</span><span class="sxs-lookup"><span data-stu-id="bd555-152">100 DTUs</span></span>
- <span data-ttu-id="bd555-153">Версию.</span><span class="sxs-lookup"><span data-stu-id="bd555-153">Premium.</span></span> <span data-ttu-id="bd555-154">125 DTU</span><span class="sxs-lookup"><span data-stu-id="bd555-154">125 DTUs</span></span>

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

### <span data-ttu-id="bd555-155">-Edition</span><span class="sxs-lookup"><span data-stu-id="bd555-155">-Edition</span></span>
<span data-ttu-id="bd555-156">Указывает выпуск базы данных SQL Azure для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="bd555-156">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="bd555-157">Изменить выпуск нельзя.</span><span class="sxs-lookup"><span data-stu-id="bd555-157">You cannot change the edition.</span></span> <span data-ttu-id="bd555-158">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bd555-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bd555-159">Ничего</span><span class="sxs-lookup"><span data-stu-id="bd555-159">None</span></span>
- <span data-ttu-id="bd555-160">Базового</span><span class="sxs-lookup"><span data-stu-id="bd555-160">Basic</span></span>
- <span data-ttu-id="bd555-161">Стандартная</span><span class="sxs-lookup"><span data-stu-id="bd555-161">Standard</span></span>
- <span data-ttu-id="bd555-162">Версию</span><span class="sxs-lookup"><span data-stu-id="bd555-162">Premium</span></span>
- <span data-ttu-id="bd555-163">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="bd555-163">DataWarehouse</span></span>
- <span data-ttu-id="bd555-164">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="bd555-164">Free</span></span>
- <span data-ttu-id="bd555-165">Показателя</span><span class="sxs-lookup"><span data-stu-id="bd555-165">Stretch</span></span>
- <span data-ttu-id="bd555-166">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="bd555-166">GeneralPurpose</span></span>
- <span data-ttu-id="bd555-167">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="bd555-167">BusinessCritical</span></span>

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

### <span data-ttu-id="bd555-168">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="bd555-168">-ElasticPoolName</span></span>
<span data-ttu-id="bd555-169">Указывает имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="bd555-169">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="bd555-170">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="bd555-170">-LicenseType</span></span>
<span data-ttu-id="bd555-171">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bd555-171">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="bd555-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd555-172">-ResourceGroupName</span></span>
<span data-ttu-id="bd555-173">Указывает имя группы ресурсов, которой назначен эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="bd555-173">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="bd555-174">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="bd555-174">-ServerName</span></span>
<span data-ttu-id="bd555-175">Указывает имя сервера, на котором размещается эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="bd555-175">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="bd555-176">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="bd555-176">-StorageMB</span></span>
<span data-ttu-id="bd555-177">Указывает предельный размер (в мегабайтах) для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="bd555-177">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="bd555-178">Дополнительные сведения можно найти в командлетах New-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="bd555-178">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="bd555-179">-Теги</span><span class="sxs-lookup"><span data-stu-id="bd555-179">-Tags</span></span>
<span data-ttu-id="bd555-180">Указывает словарь пар "ключ-значение", который этот командлет связывает с пулом эластичных БД в форме хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="bd555-180">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="bd555-181">Например: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="bd555-181">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="bd555-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="bd555-182">-VCore</span></span>
<span data-ttu-id="bd555-183">Общее количество общего числа Vcore для пула эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bd555-183">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd555-184">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="bd555-184">-ZoneRedundant</span></span>
<span data-ttu-id="bd555-185">Резервирование зоны, связанное с пулом эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bd555-185">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="bd555-186">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd555-186">-Confirm</span></span>
<span data-ttu-id="bd555-187">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bd555-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd555-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd555-188">-WhatIf</span></span>
<span data-ttu-id="bd555-189">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bd555-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd555-190">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bd555-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd555-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd555-191">CommonParameters</span></span>
<span data-ttu-id="bd555-192">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd555-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd555-193">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd555-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd555-194">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd555-194">INPUTS</span></span>

### <span data-ttu-id="bd555-195">System. String</span><span class="sxs-lookup"><span data-stu-id="bd555-195">System.String</span></span>

## <span data-ttu-id="bd555-196">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd555-196">OUTPUTS</span></span>

### <span data-ttu-id="bd555-197">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="bd555-197">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="bd555-198">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd555-198">NOTES</span></span>

## <span data-ttu-id="bd555-199">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd555-199">RELATED LINKS</span></span>

[<span data-ttu-id="bd555-200">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bd555-200">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="bd555-201">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="bd555-201">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="bd555-202">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="bd555-202">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="bd555-203">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bd555-203">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="bd555-204">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="bd555-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
