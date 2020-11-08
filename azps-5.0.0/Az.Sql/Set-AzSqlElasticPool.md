---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: cb76e0ff789f89079772d7f718c3f16c9c01d707
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248796"
---
# <span data-ttu-id="350fa-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="350fa-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="350fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="350fa-102">SYNOPSIS</span></span>
<span data-ttu-id="350fa-103">Изменяет свойства пула эластичных баз данных в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="350fa-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="350fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="350fa-104">SYNTAX</span></span>

### <span data-ttu-id="350fa-105">DtuBasedPool (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="350fa-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="350fa-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="350fa-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="350fa-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="350fa-107">DESCRIPTION</span></span>
<span data-ttu-id="350fa-108">Командлет **Set-AzSqlElasticPool** задает свойства для пула эластичных БД в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="350fa-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="350fa-109">Этот командлет может изменить eDTUs для каждого пула ( *DTU* ), максимальный размер хранилища для пула ( *StorageMB* ), максимум eDTUs на базу данных ( *DatabaseDtuMax* ) и минимальный eDTUs на базу данных ( *DatabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="350fa-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatabaseDtuMin* ).</span></span>
<span data-ttu-id="350fa-110">Для нескольких параметров ( *-DTU,-DatabaseDtuMin и-DatabaseDtuMax* ) необходимо, чтобы значение было задано в списке допустимых значений для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="350fa-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="350fa-111">Например, параметр-DatabaseDtuMax для стандартного пула 100 eDTU может иметь только значение 10, 20, 50 или 100.</span><span class="sxs-lookup"><span data-stu-id="350fa-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="350fa-112">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="350fa-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="350fa-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="350fa-113">EXAMPLES</span></span>

### <span data-ttu-id="350fa-114">Пример 1: изменение свойств эластичного пула</span><span class="sxs-lookup"><span data-stu-id="350fa-114">Example 1: Modify properties for an elastic pool</span></span>
```powershell
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

<span data-ttu-id="350fa-115">Эта команда изменяет свойства пула эластичных БД с именем elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="350fa-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="350fa-116">Команда задает количество DTU для эластичного пула в 1000 и устанавливает минимальные и максимальные значения DTU.</span><span class="sxs-lookup"><span data-stu-id="350fa-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="350fa-117">Пример 2: изменение максимального размера хранилища эластичного пула</span><span class="sxs-lookup"><span data-stu-id="350fa-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```powershell
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

<span data-ttu-id="350fa-118">Эта команда изменяет свойства пула эластичных БД с именем elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="350fa-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="350fa-119">Команда задает максимальный объем хранилища для пула эластичных БД равным 2 ТБ.</span><span class="sxs-lookup"><span data-stu-id="350fa-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="350fa-120">Пример 3</span><span class="sxs-lookup"><span data-stu-id="350fa-120">Example 3</span></span>

<span data-ttu-id="350fa-121">Изменяет свойства пула эластичных баз данных в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="350fa-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="350fa-122">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="350fa-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="350fa-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="350fa-123">PARAMETERS</span></span>

### <span data-ttu-id="350fa-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="350fa-124">-AsJob</span></span>
<span data-ttu-id="350fa-125">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="350fa-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="350fa-126">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="350fa-126">-ComputeGeneration</span></span>
<span data-ttu-id="350fa-127">Вычислено поколение, которое необходимо назначить.</span><span class="sxs-lookup"><span data-stu-id="350fa-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="350fa-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="350fa-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="350fa-129">Указывает максимальное количество DTU, которое может использовать любая единственная база данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="350fa-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="350fa-130">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="350fa-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="350fa-131">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="350fa-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="350fa-132">Базового.</span><span class="sxs-lookup"><span data-stu-id="350fa-132">Basic.</span></span>  <span data-ttu-id="350fa-133">5 DTU</span><span class="sxs-lookup"><span data-stu-id="350fa-133">5 DTUs</span></span>
- <span data-ttu-id="350fa-134">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="350fa-134">Standard.</span></span> <span data-ttu-id="350fa-135">100 DTU</span><span class="sxs-lookup"><span data-stu-id="350fa-135">100 DTUs</span></span>
- <span data-ttu-id="350fa-136">Версию.</span><span class="sxs-lookup"><span data-stu-id="350fa-136">Premium.</span></span> <span data-ttu-id="350fa-137">125 DTU</span><span class="sxs-lookup"><span data-stu-id="350fa-137">125 DTUs</span></span>

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

### <span data-ttu-id="350fa-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="350fa-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="350fa-139">Указывает минимальное количество DTU, которое будет гарантировано для всех баз данных в пуле для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="350fa-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="350fa-140">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="350fa-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="350fa-141">Значением по умолчанию является нуль (0).</span><span class="sxs-lookup"><span data-stu-id="350fa-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="350fa-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="350fa-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="350fa-143">Максимальный номер VCore, который любая база данных SqlAzure может использовать в пуле.</span><span class="sxs-lookup"><span data-stu-id="350fa-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="350fa-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="350fa-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="350fa-145">Минимальный номер VCore, который любая база данных SqlAzure может использовать в пуле.</span><span class="sxs-lookup"><span data-stu-id="350fa-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="350fa-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="350fa-146">-DefaultProfile</span></span>
<span data-ttu-id="350fa-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="350fa-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="350fa-148">-DTU</span><span class="sxs-lookup"><span data-stu-id="350fa-148">-Dtu</span></span>
<span data-ttu-id="350fa-149">Указывает общее количество общих DTU для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="350fa-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="350fa-150">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="350fa-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="350fa-151">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="350fa-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="350fa-152">Базового.</span><span class="sxs-lookup"><span data-stu-id="350fa-152">Basic.</span></span> <span data-ttu-id="350fa-153">100 DTU</span><span class="sxs-lookup"><span data-stu-id="350fa-153">100 DTUs</span></span>
- <span data-ttu-id="350fa-154">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="350fa-154">Standard.</span></span> <span data-ttu-id="350fa-155">100 DTU</span><span class="sxs-lookup"><span data-stu-id="350fa-155">100 DTUs</span></span>
- <span data-ttu-id="350fa-156">Версию.</span><span class="sxs-lookup"><span data-stu-id="350fa-156">Premium.</span></span> <span data-ttu-id="350fa-157">125 DTU</span><span class="sxs-lookup"><span data-stu-id="350fa-157">125 DTUs</span></span>

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

### <span data-ttu-id="350fa-158">-Edition</span><span class="sxs-lookup"><span data-stu-id="350fa-158">-Edition</span></span>
<span data-ttu-id="350fa-159">Указывает выпуск базы данных SQL Azure для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="350fa-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="350fa-160">Изменить выпуск нельзя.</span><span class="sxs-lookup"><span data-stu-id="350fa-160">You cannot change the edition.</span></span> <span data-ttu-id="350fa-161">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="350fa-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="350fa-162">Ничего</span><span class="sxs-lookup"><span data-stu-id="350fa-162">None</span></span>
- <span data-ttu-id="350fa-163">Базового</span><span class="sxs-lookup"><span data-stu-id="350fa-163">Basic</span></span>
- <span data-ttu-id="350fa-164">Стандартная</span><span class="sxs-lookup"><span data-stu-id="350fa-164">Standard</span></span>
- <span data-ttu-id="350fa-165">Версию</span><span class="sxs-lookup"><span data-stu-id="350fa-165">Premium</span></span>
- <span data-ttu-id="350fa-166">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="350fa-166">DataWarehouse</span></span>
- <span data-ttu-id="350fa-167">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="350fa-167">Free</span></span>
- <span data-ttu-id="350fa-168">Показателя</span><span class="sxs-lookup"><span data-stu-id="350fa-168">Stretch</span></span>
- <span data-ttu-id="350fa-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="350fa-169">GeneralPurpose</span></span>
- <span data-ttu-id="350fa-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="350fa-170">BusinessCritical</span></span>

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

### <span data-ttu-id="350fa-171">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="350fa-171">-ElasticPoolName</span></span>
<span data-ttu-id="350fa-172">Указывает имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="350fa-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="350fa-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="350fa-173">-LicenseType</span></span>
<span data-ttu-id="350fa-174">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="350fa-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="350fa-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="350fa-175">-ResourceGroupName</span></span>
<span data-ttu-id="350fa-176">Указывает имя группы ресурсов, которой назначен эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="350fa-176">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="350fa-177">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="350fa-177">-ServerName</span></span>
<span data-ttu-id="350fa-178">Указывает имя сервера, на котором размещается эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="350fa-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="350fa-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="350fa-179">-StorageMB</span></span>
<span data-ttu-id="350fa-180">Указывает предельный размер (в мегабайтах) для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="350fa-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="350fa-181">Дополнительные сведения можно найти в командлетах New-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="350fa-181">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="350fa-182">-Теги</span><span class="sxs-lookup"><span data-stu-id="350fa-182">-Tags</span></span>
<span data-ttu-id="350fa-183">Указывает словарь пар "ключ-значение", который этот командлет связывает с пулом эластичных БД в форме хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="350fa-183">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="350fa-184">Например: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="350fa-184">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="350fa-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="350fa-185">-VCore</span></span>
<span data-ttu-id="350fa-186">Общее количество общего числа Vcore для пула эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="350fa-186">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="350fa-187">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="350fa-187">-ZoneRedundant</span></span>
<span data-ttu-id="350fa-188">Резервирование зоны, связанное с пулом эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="350fa-188">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="350fa-189">-Confirm</span><span class="sxs-lookup"><span data-stu-id="350fa-189">-Confirm</span></span>
<span data-ttu-id="350fa-190">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="350fa-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="350fa-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="350fa-191">-WhatIf</span></span>
<span data-ttu-id="350fa-192">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="350fa-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="350fa-193">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="350fa-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="350fa-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="350fa-194">CommonParameters</span></span>
<span data-ttu-id="350fa-195">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="350fa-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="350fa-196">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="350fa-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="350fa-197">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="350fa-197">INPUTS</span></span>

### <span data-ttu-id="350fa-198">System. String</span><span class="sxs-lookup"><span data-stu-id="350fa-198">System.String</span></span>

## <span data-ttu-id="350fa-199">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="350fa-199">OUTPUTS</span></span>

### <span data-ttu-id="350fa-200">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="350fa-200">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="350fa-201">Пуск</span><span class="sxs-lookup"><span data-stu-id="350fa-201">NOTES</span></span>

## <span data-ttu-id="350fa-202">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="350fa-202">RELATED LINKS</span></span>

[<span data-ttu-id="350fa-203">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="350fa-203">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="350fa-204">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="350fa-204">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="350fa-205">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="350fa-205">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="350fa-206">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="350fa-206">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="350fa-207">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="350fa-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
