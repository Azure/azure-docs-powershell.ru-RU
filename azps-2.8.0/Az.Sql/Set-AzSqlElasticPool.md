---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: d78ca6ef2e342982dc6f5e53e8fff4de606dd5ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906317"
---
# <span data-ttu-id="37fd6-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="37fd6-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="37fd6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37fd6-102">SYNOPSIS</span></span>
<span data-ttu-id="37fd6-103">Изменяет свойства пула эластичных баз данных в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="37fd6-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="37fd6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37fd6-104">SYNTAX</span></span>

### <span data-ttu-id="37fd6-105">DtuBasedPool (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="37fd6-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37fd6-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="37fd6-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37fd6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37fd6-107">DESCRIPTION</span></span>
<span data-ttu-id="37fd6-108">Командлет **Set-AzSqlElasticPool** задает свойства для пула эластичных БД в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="37fd6-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="37fd6-109">Этот командлет может изменить eDTUs для каждого пула ( *DTU* ), максимальный размер хранилища для пула ( *StorageMB* ), максимум eDTUs на базу данных ( *DatabaseDtuMax* ) и минимальный eDTUs на базу данных ( *DatabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="37fd6-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatabaseDtuMin* ).</span></span>
<span data-ttu-id="37fd6-110">Для нескольких параметров ( *-DTU,-DatabaseDtuMin и-DatabaseDtuMax* ) необходимо, чтобы значение было задано в списке допустимых значений для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="37fd6-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="37fd6-111">Например, параметр-DatabaseDtuMax для стандартного пула 100 eDTU может иметь только значение 10, 20, 50 или 100.</span><span class="sxs-lookup"><span data-stu-id="37fd6-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="37fd6-112">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="37fd6-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="37fd6-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37fd6-113">EXAMPLES</span></span>

### <span data-ttu-id="37fd6-114">Пример 1: изменение свойств эластичного пула</span><span class="sxs-lookup"><span data-stu-id="37fd6-114">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="37fd6-115">Эта команда изменяет свойства пула эластичных БД с именем elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="37fd6-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="37fd6-116">Команда задает количество DTU для эластичного пула в 1000 и устанавливает минимальные и максимальные значения DTU.</span><span class="sxs-lookup"><span data-stu-id="37fd6-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="37fd6-117">Пример 2: изменение максимального размера хранилища эластичного пула</span><span class="sxs-lookup"><span data-stu-id="37fd6-117">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="37fd6-118">Эта команда изменяет свойства пула эластичных БД с именем elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="37fd6-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="37fd6-119">Команда задает максимальный объем хранилища для пула эластичных БД равным 2 ТБ.</span><span class="sxs-lookup"><span data-stu-id="37fd6-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="37fd6-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37fd6-120">PARAMETERS</span></span>

### <span data-ttu-id="37fd6-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37fd6-121">-AsJob</span></span>
<span data-ttu-id="37fd6-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="37fd6-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37fd6-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="37fd6-123">-ComputeGeneration</span></span>
<span data-ttu-id="37fd6-124">Вычислено поколение, которое необходимо назначить.</span><span class="sxs-lookup"><span data-stu-id="37fd6-124">The compute generation to assign.</span></span>

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

### <span data-ttu-id="37fd6-125">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="37fd6-125">-DatabaseDtuMax</span></span>
<span data-ttu-id="37fd6-126">Указывает максимальное количество DTU, которое может использовать любая единственная база данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="37fd6-126">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="37fd6-127">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="37fd6-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="37fd6-128">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="37fd6-128">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="37fd6-129">Базового.</span><span class="sxs-lookup"><span data-stu-id="37fd6-129">Basic.</span></span>  <span data-ttu-id="37fd6-130">5 DTU</span><span class="sxs-lookup"><span data-stu-id="37fd6-130">5 DTUs</span></span>
- <span data-ttu-id="37fd6-131">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="37fd6-131">Standard.</span></span> <span data-ttu-id="37fd6-132">100 DTU</span><span class="sxs-lookup"><span data-stu-id="37fd6-132">100 DTUs</span></span>
- <span data-ttu-id="37fd6-133">Версию.</span><span class="sxs-lookup"><span data-stu-id="37fd6-133">Premium.</span></span> <span data-ttu-id="37fd6-134">125 DTU</span><span class="sxs-lookup"><span data-stu-id="37fd6-134">125 DTUs</span></span>

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

### <span data-ttu-id="37fd6-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="37fd6-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="37fd6-136">Указывает минимальное количество DTU, которое будет гарантировано для всех баз данных в пуле для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="37fd6-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="37fd6-137">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="37fd6-137">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="37fd6-138">Значением по умолчанию является нуль (0).</span><span class="sxs-lookup"><span data-stu-id="37fd6-138">The default value is zero (0).</span></span>

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

### <span data-ttu-id="37fd6-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="37fd6-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="37fd6-140">Максимальный номер VCore, который любая база данных SqlAzure может использовать в пуле.</span><span class="sxs-lookup"><span data-stu-id="37fd6-140">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="37fd6-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="37fd6-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="37fd6-142">Минимальный номер VCore, который любая база данных SqlAzure может использовать в пуле.</span><span class="sxs-lookup"><span data-stu-id="37fd6-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="37fd6-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37fd6-143">-DefaultProfile</span></span>
<span data-ttu-id="37fd6-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="37fd6-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37fd6-145">-DTU</span><span class="sxs-lookup"><span data-stu-id="37fd6-145">-Dtu</span></span>
<span data-ttu-id="37fd6-146">Указывает общее количество общих DTU для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="37fd6-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="37fd6-147">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="37fd6-147">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="37fd6-148">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="37fd6-148">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="37fd6-149">Базового.</span><span class="sxs-lookup"><span data-stu-id="37fd6-149">Basic.</span></span> <span data-ttu-id="37fd6-150">100 DTU</span><span class="sxs-lookup"><span data-stu-id="37fd6-150">100 DTUs</span></span>
- <span data-ttu-id="37fd6-151">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="37fd6-151">Standard.</span></span> <span data-ttu-id="37fd6-152">100 DTU</span><span class="sxs-lookup"><span data-stu-id="37fd6-152">100 DTUs</span></span>
- <span data-ttu-id="37fd6-153">Версию.</span><span class="sxs-lookup"><span data-stu-id="37fd6-153">Premium.</span></span> <span data-ttu-id="37fd6-154">125 DTU</span><span class="sxs-lookup"><span data-stu-id="37fd6-154">125 DTUs</span></span>

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

### <span data-ttu-id="37fd6-155">-Edition</span><span class="sxs-lookup"><span data-stu-id="37fd6-155">-Edition</span></span>
<span data-ttu-id="37fd6-156">Указывает выпуск базы данных SQL Azure для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="37fd6-156">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="37fd6-157">Изменить выпуск нельзя.</span><span class="sxs-lookup"><span data-stu-id="37fd6-157">You cannot change the edition.</span></span> <span data-ttu-id="37fd6-158">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37fd6-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37fd6-159">Ничего</span><span class="sxs-lookup"><span data-stu-id="37fd6-159">None</span></span>
- <span data-ttu-id="37fd6-160">Базового</span><span class="sxs-lookup"><span data-stu-id="37fd6-160">Basic</span></span>
- <span data-ttu-id="37fd6-161">Стандартная</span><span class="sxs-lookup"><span data-stu-id="37fd6-161">Standard</span></span>
- <span data-ttu-id="37fd6-162">Версию</span><span class="sxs-lookup"><span data-stu-id="37fd6-162">Premium</span></span>
- <span data-ttu-id="37fd6-163">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="37fd6-163">DataWarehouse</span></span>
- <span data-ttu-id="37fd6-164">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="37fd6-164">Free</span></span>
- <span data-ttu-id="37fd6-165">Показателя</span><span class="sxs-lookup"><span data-stu-id="37fd6-165">Stretch</span></span>
- <span data-ttu-id="37fd6-166">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="37fd6-166">GeneralPurpose</span></span>
- <span data-ttu-id="37fd6-167">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="37fd6-167">BusinessCritical</span></span>

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

### <span data-ttu-id="37fd6-168">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="37fd6-168">-ElasticPoolName</span></span>
<span data-ttu-id="37fd6-169">Указывает имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="37fd6-169">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="37fd6-170">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="37fd6-170">-LicenseType</span></span>
<span data-ttu-id="37fd6-171">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="37fd6-171">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="37fd6-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37fd6-172">-ResourceGroupName</span></span>
<span data-ttu-id="37fd6-173">Указывает имя группы ресурсов, которой назначен эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="37fd6-173">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="37fd6-174">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="37fd6-174">-ServerName</span></span>
<span data-ttu-id="37fd6-175">Указывает имя сервера, на котором размещается эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="37fd6-175">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="37fd6-176">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="37fd6-176">-StorageMB</span></span>
<span data-ttu-id="37fd6-177">Указывает предельный размер (в мегабайтах) для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="37fd6-177">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="37fd6-178">Дополнительные сведения можно найти в командлетах New-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="37fd6-178">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="37fd6-179">-Теги</span><span class="sxs-lookup"><span data-stu-id="37fd6-179">-Tags</span></span>
<span data-ttu-id="37fd6-180">Указывает словарь пар "ключ-значение", который этот командлет связывает с пулом эластичных БД в форме хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="37fd6-180">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="37fd6-181">Например: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="37fd6-181">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="37fd6-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="37fd6-182">-VCore</span></span>
<span data-ttu-id="37fd6-183">Общее количество общего числа Vcore для пула эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="37fd6-183">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="37fd6-184">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="37fd6-184">-ZoneRedundant</span></span>
<span data-ttu-id="37fd6-185">Резервирование зоны, связанное с пулом эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="37fd6-185">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="37fd6-186">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37fd6-186">-Confirm</span></span>
<span data-ttu-id="37fd6-187">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="37fd6-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37fd6-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37fd6-188">-WhatIf</span></span>
<span data-ttu-id="37fd6-189">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="37fd6-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37fd6-190">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="37fd6-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37fd6-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37fd6-191">CommonParameters</span></span>
<span data-ttu-id="37fd6-192">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37fd6-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37fd6-193">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37fd6-193">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37fd6-194">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37fd6-194">INPUTS</span></span>

### <span data-ttu-id="37fd6-195">System. String</span><span class="sxs-lookup"><span data-stu-id="37fd6-195">System.String</span></span>

## <span data-ttu-id="37fd6-196">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37fd6-196">OUTPUTS</span></span>

### <span data-ttu-id="37fd6-197">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="37fd6-197">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="37fd6-198">Пуск</span><span class="sxs-lookup"><span data-stu-id="37fd6-198">NOTES</span></span>

## <span data-ttu-id="37fd6-199">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37fd6-199">RELATED LINKS</span></span>

[<span data-ttu-id="37fd6-200">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="37fd6-200">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="37fd6-201">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="37fd6-201">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="37fd6-202">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="37fd6-202">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="37fd6-203">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="37fd6-203">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="37fd6-204">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="37fd6-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
