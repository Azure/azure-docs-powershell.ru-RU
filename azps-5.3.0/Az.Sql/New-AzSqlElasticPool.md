---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 8fed3f32f5ff0a9920b87438b75cb25cee7c9217
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505913"
---
# <span data-ttu-id="6153f-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6153f-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="6153f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6153f-102">SYNOPSIS</span></span>
<span data-ttu-id="6153f-103">Создается эластичный пул баз данных для SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="6153f-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="6153f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6153f-104">SYNTAX</span></span>

### <span data-ttu-id="6153f-105">DtuBasedPool (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6153f-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6153f-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="6153f-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6153f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6153f-107">DESCRIPTION</span></span>
<span data-ttu-id="6153f-108">Для базы данных Azure SQL создается эластичный пул базы данных **New-AzSqlElasticPool.**</span><span class="sxs-lookup"><span data-stu-id="6153f-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="6153f-109">Для нескольких параметров *(-Dtu, -DatabaseDtuMin и -DatabaseDtuMax)* требуется, чтобы заданное значение было задано в списке допустимого значения для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="6153f-109">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="6153f-110">Например, для пула eDTU стандартного 100 100 можно установить -DatabaseDtuMax : 10, 20, 50 или 100.</span><span class="sxs-lookup"><span data-stu-id="6153f-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="6153f-111">Подробные сведения о допустимых значениях см. в таблице для пула определенного размера в [эластичных пулах.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="6153f-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="6153f-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6153f-112">EXAMPLES</span></span>

### <span data-ttu-id="6153f-113">Пример 1. Создание эластичного пула DTU</span><span class="sxs-lookup"><span data-stu-id="6153f-113">Example 1: Create a DTU elastic pool</span></span>

```powershell
PS C:\>New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
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

<span data-ttu-id="6153f-114">Эта команда создает эластичный пул в стандартном уровне обслуживания Под названием "ЭластичнаяPool01".</span><span class="sxs-lookup"><span data-stu-id="6153f-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="6153f-115">Сервер с именем server01, который назначен группе ресурсов Azure с именем ResourceGroup01, размещен в этом пуле.</span><span class="sxs-lookup"><span data-stu-id="6153f-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="6153f-116">Команда определяет значения свойств DTU для пула и баз данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="6153f-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="6153f-117">Пример 2. Создание эластичного пула vCore</span><span class="sxs-lookup"><span data-stu-id="6153f-117">Example 2: Create a vCore elastic pool</span></span>

```powershell
PS C:\> New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "GeneralPurpose" -vCore 2 -ComputeGeneration Gen5
ResourceId          : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/server01/elasticPools/ElasticPool01
ResourceGroupName   : ResourceGroup01
ServerName          : Server01
ElasticPoolName     : ElasticPool01
Location            : Central US
CreationDate        : 8/29/2019 2:16:40 AM
State               : Ready
Edition             : GeneralPurpose
SkuName             : GP_Gen5
Dtu                 : 2
DatabaseDtuMax      : 2
DatabaseDtuMin      : 0
Capacity            : 2
DatabaseCapacityMin : 0
DatabaseCapacityMax : 2
Family              : Gen5
MaxSizeBytes        : 34359738368
StorageMB           : 32768
Tags                :
```

<span data-ttu-id="6153f-118">Эта команда создает эластичный пул на уровне службы GengeralPurpose под названием "99Pool01".</span><span class="sxs-lookup"><span data-stu-id="6153f-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="6153f-119">Сервер с именем server01, который назначен группе ресурсов Azure с именем ResourceGroup01, размещен в этом пуле.</span><span class="sxs-lookup"><span data-stu-id="6153f-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="6153f-120">Команда определяет значения свойств vCore для пула и баз данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="6153f-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="6153f-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6153f-121">Example 3</span></span>

<span data-ttu-id="6153f-122">Создается эластичный пул баз данных для SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="6153f-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="6153f-123">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="6153f-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="6153f-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6153f-124">PARAMETERS</span></span>

### <span data-ttu-id="6153f-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6153f-125">-AsJob</span></span>
<span data-ttu-id="6153f-126">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6153f-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6153f-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="6153f-127">-ComputeGeneration</span></span>
<span data-ttu-id="6153f-128">Назначимое поколение компьютеров.</span><span class="sxs-lookup"><span data-stu-id="6153f-128">The compute generation to assign.</span></span>

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

### <span data-ttu-id="6153f-129">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="6153f-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="6153f-130">Указывает максимальное количество единиц пропускной способности (DTUs), которое может использовать любая база данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="6153f-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="6153f-131">Значения по умолчанию для разных выпусков следуют за следующими:</span><span class="sxs-lookup"><span data-stu-id="6153f-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="6153f-132">Базовая.</span><span class="sxs-lookup"><span data-stu-id="6153f-132">Basic.</span></span> <span data-ttu-id="6153f-133">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="6153f-133">5 DTUs</span></span>
- <span data-ttu-id="6153f-134">Стандартный.</span><span class="sxs-lookup"><span data-stu-id="6153f-134">Standard.</span></span> <span data-ttu-id="6153f-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="6153f-135">100 DTUs</span></span>
- <span data-ttu-id="6153f-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="6153f-136">Premium.</span></span> <span data-ttu-id="6153f-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="6153f-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="6153f-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="6153f-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="6153f-139">Указывает минимальное количество DTUs, которое обеспечивается эластичным пулом для всех баз данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="6153f-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="6153f-140">Значение по умолчанию — нуль (0).</span><span class="sxs-lookup"><span data-stu-id="6153f-140">The default value is zero (0).</span></span>
<span data-ttu-id="6153f-141">Подробные сведения о допустимых значениях см. в таблице для пула определенного размера в [эластичных пулах.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="6153f-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="6153f-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="6153f-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="6153f-143">Максимальное число VCore, доступного для базы данных SqlAzure в пуле.</span><span class="sxs-lookup"><span data-stu-id="6153f-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="6153f-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="6153f-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="6153f-145">Минимальное число VCore, который может использовать любая база данных SqlAzure в пуле.</span><span class="sxs-lookup"><span data-stu-id="6153f-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="6153f-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6153f-146">-DefaultProfile</span></span>
<span data-ttu-id="6153f-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6153f-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6153f-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="6153f-148">-Dtu</span></span>
<span data-ttu-id="6153f-149">Определяет общее количество общих DTUs для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="6153f-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="6153f-150">Значения по умолчанию для разных выпусков следуют за следующими:</span><span class="sxs-lookup"><span data-stu-id="6153f-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="6153f-151">Базовая.</span><span class="sxs-lookup"><span data-stu-id="6153f-151">Basic.</span></span>
<span data-ttu-id="6153f-152">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="6153f-152">100 DTUs</span></span>
- <span data-ttu-id="6153f-153">Стандартный.</span><span class="sxs-lookup"><span data-stu-id="6153f-153">Standard.</span></span>
<span data-ttu-id="6153f-154">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="6153f-154">100 DTUs</span></span>
- <span data-ttu-id="6153f-155">Premium.</span><span class="sxs-lookup"><span data-stu-id="6153f-155">Premium.</span></span>
<span data-ttu-id="6153f-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="6153f-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="6153f-157">-Edition</span><span class="sxs-lookup"><span data-stu-id="6153f-157">-Edition</span></span>
<span data-ttu-id="6153f-158">Выпуск базы данных Azure SQL, используемой для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="6153f-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="6153f-159">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="6153f-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6153f-160">Нет</span><span class="sxs-lookup"><span data-stu-id="6153f-160">None</span></span>
- <span data-ttu-id="6153f-161">Базовая</span><span class="sxs-lookup"><span data-stu-id="6153f-161">Basic</span></span>
- <span data-ttu-id="6153f-162">Стандартный</span><span class="sxs-lookup"><span data-stu-id="6153f-162">Standard</span></span>
- <span data-ttu-id="6153f-163">Premium</span><span class="sxs-lookup"><span data-stu-id="6153f-163">Premium</span></span>
- <span data-ttu-id="6153f-164">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="6153f-164">DataWarehouse</span></span>
- <span data-ttu-id="6153f-165">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="6153f-165">Free</span></span>
- <span data-ttu-id="6153f-166">Растяжение</span><span class="sxs-lookup"><span data-stu-id="6153f-166">Stretch</span></span>
- <span data-ttu-id="6153f-167">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="6153f-167">GeneralPurpose</span></span>
- <span data-ttu-id="6153f-168">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="6153f-168">BusinessCritical</span></span>

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

### <span data-ttu-id="6153f-169">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6153f-169">-ElasticPoolName</span></span>
<span data-ttu-id="6153f-170">Определяет имя эластичного пула, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6153f-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6153f-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6153f-171">-LicenseType</span></span>
<span data-ttu-id="6153f-172">Тип лицензии для базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="6153f-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="6153f-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6153f-173">-ResourceGroupName</span></span>
<span data-ttu-id="6153f-174">Задает имя группы ресурсов, которой этот cmdlet назначает эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="6153f-174">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="6153f-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6153f-175">-ServerName</span></span>
<span data-ttu-id="6153f-176">Указывает имя сервера, на котором размещено эластичное пул.</span><span class="sxs-lookup"><span data-stu-id="6153f-176">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="6153f-177">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="6153f-177">-StorageMB</span></span>
<span data-ttu-id="6153f-178">Определяет ограничение хранилища в мегабайтах для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="6153f-178">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="6153f-179">Если этот параметр не задан, этот cmdlet вычисляет значение, которое зависит от значения *параметра Dtu.*</span><span class="sxs-lookup"><span data-stu-id="6153f-179">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="6153f-180">Возможные [значения см. в eDTU](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) и ограничениях хранилища.</span><span class="sxs-lookup"><span data-stu-id="6153f-180">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="6153f-181">-Теги</span><span class="sxs-lookup"><span data-stu-id="6153f-181">-Tags</span></span>
<span data-ttu-id="6153f-182">Словарь пар "ключ-значение" в виде hash table, которую этот cmdlet связывает с эластичным пулом.</span><span class="sxs-lookup"><span data-stu-id="6153f-182">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="6153f-183">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="6153f-183">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6153f-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="6153f-184">-VCore</span></span>
<span data-ttu-id="6153f-185">Общее общее количество vcores для Sql Azure Elastic Pool.</span><span class="sxs-lookup"><span data-stu-id="6153f-185">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="6153f-186">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="6153f-186">-ZoneRedundant</span></span>
<span data-ttu-id="6153f-187">Избыточность зоны, которая связывается с azure Sql Elastic Pool</span><span class="sxs-lookup"><span data-stu-id="6153f-187">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="6153f-188">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6153f-188">-Confirm</span></span>
<span data-ttu-id="6153f-189">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6153f-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6153f-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6153f-190">-WhatIf</span></span>
<span data-ttu-id="6153f-191">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6153f-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6153f-192">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6153f-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6153f-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6153f-193">CommonParameters</span></span>
<span data-ttu-id="6153f-194">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6153f-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6153f-195">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6153f-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6153f-196">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6153f-196">INPUTS</span></span>

### <span data-ttu-id="6153f-197">System.String</span><span class="sxs-lookup"><span data-stu-id="6153f-197">System.String</span></span>

## <span data-ttu-id="6153f-198">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6153f-198">OUTPUTS</span></span>

### <span data-ttu-id="6153f-199">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="6153f-199">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="6153f-200">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6153f-200">NOTES</span></span>

## <span data-ttu-id="6153f-201">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6153f-201">RELATED LINKS</span></span>

[<span data-ttu-id="6153f-202">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6153f-202">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="6153f-203">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="6153f-203">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="6153f-204">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="6153f-204">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="6153f-205">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6153f-205">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="6153f-206">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6153f-206">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="6153f-207">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="6153f-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
