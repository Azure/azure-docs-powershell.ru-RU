---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: d625e28b0007a9dc99434f0257a910ea804e3644
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970211"
---
# <span data-ttu-id="6b5cc-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6b5cc-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="6b5cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b5cc-102">SYNOPSIS</span></span>
<span data-ttu-id="6b5cc-103">Создается эластичный пул баз данных для SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="6b5cc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6b5cc-104">SYNTAX</span></span>

### <span data-ttu-id="6b5cc-105">DtuBasedPool (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6b5cc-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b5cc-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="6b5cc-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b5cc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b5cc-107">DESCRIPTION</span></span>
<span data-ttu-id="6b5cc-108">Для базы данных Azure SQL создается эластичный пул базы данных **New-AzSqlElasticPool.**</span><span class="sxs-lookup"><span data-stu-id="6b5cc-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="6b5cc-109">Для нескольких параметров *(-Dtu, -DatabaseDtuMin и -DatabaseDtuMax)* требуется, чтобы заданное значение было задано в списке допустимого значения для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-109">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="6b5cc-110">Например, для пула eDTU стандартного 100 100 можно установить -DatabaseDtuMax : 10, 20, 50 или 100.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="6b5cc-111">Подробные сведения о допустимых значениях см. в таблице для пула определенного размера в [эластичных пулах.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="6b5cc-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="6b5cc-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6b5cc-112">EXAMPLES</span></span>

### <span data-ttu-id="6b5cc-113">Пример 1. Создание эластичного пула DTU</span><span class="sxs-lookup"><span data-stu-id="6b5cc-113">Example 1: Create a DTU elastic pool</span></span>

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

<span data-ttu-id="6b5cc-114">Эта команда создает эластичный пул в стандартном уровне обслуживания Под названием "ЭластичнаяPool01".</span><span class="sxs-lookup"><span data-stu-id="6b5cc-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="6b5cc-115">Сервер с именем server01, который назначен группе ресурсов Azure с именем ResourceGroup01, размещен в этом пуле.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="6b5cc-116">Команда определяет значения свойств DTU для пула и баз данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="6b5cc-117">Пример 2. Создание эластичного пула vCore</span><span class="sxs-lookup"><span data-stu-id="6b5cc-117">Example 2: Create a vCore elastic pool</span></span>

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

<span data-ttu-id="6b5cc-118">Эта команда создает эластичный пул на уровне службы GengeralPurpose под названием "99Pool01".</span><span class="sxs-lookup"><span data-stu-id="6b5cc-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="6b5cc-119">Сервер с именем server01, который назначен группе ресурсов Azure с именем ResourceGroup01, размещен в этом пуле.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="6b5cc-120">Команда определяет значения свойств vCore для пула и баз данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="6b5cc-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6b5cc-121">Example 3</span></span>

<span data-ttu-id="6b5cc-122">Создается эластичный пул баз данных для SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="6b5cc-123">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="6b5cc-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="6b5cc-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b5cc-124">PARAMETERS</span></span>

### <span data-ttu-id="6b5cc-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b5cc-125">-AsJob</span></span>
<span data-ttu-id="6b5cc-126">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6b5cc-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b5cc-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="6b5cc-127">-ComputeGeneration</span></span>
<span data-ttu-id="6b5cc-128">Назначимое поколение компьютеров.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-128">The compute generation to assign.</span></span>

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

### <span data-ttu-id="6b5cc-129">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="6b5cc-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="6b5cc-130">Указывает максимальное количество единиц пропускной способности (DTUs), которое может использовать любая база данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="6b5cc-131">Значения по умолчанию для разных выпусков следуют за следующими:</span><span class="sxs-lookup"><span data-stu-id="6b5cc-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="6b5cc-132">Базовая.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-132">Basic.</span></span> <span data-ttu-id="6b5cc-133">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="6b5cc-133">5 DTUs</span></span>
- <span data-ttu-id="6b5cc-134">Стандартный.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-134">Standard.</span></span> <span data-ttu-id="6b5cc-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="6b5cc-135">100 DTUs</span></span>
- <span data-ttu-id="6b5cc-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-136">Premium.</span></span> <span data-ttu-id="6b5cc-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="6b5cc-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="6b5cc-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="6b5cc-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="6b5cc-139">Указывает минимальное количество DTUs, которое обеспечивается эластичным пулом для всех баз данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="6b5cc-140">Значение по умолчанию — нуль (0).</span><span class="sxs-lookup"><span data-stu-id="6b5cc-140">The default value is zero (0).</span></span>
<span data-ttu-id="6b5cc-141">Подробные сведения о допустимых значениях см. в таблице для пула определенного размера в [эластичных пулах.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="6b5cc-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="6b5cc-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="6b5cc-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="6b5cc-143">Максимальное число VCore, доступного для базы данных SqlAzure в пуле.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="6b5cc-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="6b5cc-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="6b5cc-145">Минимальное число VCore, который может использовать любая база данных SqlAzure в пуле.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="6b5cc-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b5cc-146">-DefaultProfile</span></span>
<span data-ttu-id="6b5cc-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6b5cc-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b5cc-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="6b5cc-148">-Dtu</span></span>
<span data-ttu-id="6b5cc-149">Определяет общее количество общих DTUs для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="6b5cc-150">Значения по умолчанию для разных выпусков следуют за следующими:</span><span class="sxs-lookup"><span data-stu-id="6b5cc-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="6b5cc-151">Базовая.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-151">Basic.</span></span>
<span data-ttu-id="6b5cc-152">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="6b5cc-152">100 DTUs</span></span>
- <span data-ttu-id="6b5cc-153">Стандартный.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-153">Standard.</span></span>
<span data-ttu-id="6b5cc-154">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="6b5cc-154">100 DTUs</span></span>
- <span data-ttu-id="6b5cc-155">Premium.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-155">Premium.</span></span>
<span data-ttu-id="6b5cc-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="6b5cc-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="6b5cc-157">-Edition</span><span class="sxs-lookup"><span data-stu-id="6b5cc-157">-Edition</span></span>
<span data-ttu-id="6b5cc-158">Выпуск базы данных Azure SQL, используемой для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="6b5cc-159">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="6b5cc-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6b5cc-160">Нет</span><span class="sxs-lookup"><span data-stu-id="6b5cc-160">None</span></span>
- <span data-ttu-id="6b5cc-161">Базовая</span><span class="sxs-lookup"><span data-stu-id="6b5cc-161">Basic</span></span>
- <span data-ttu-id="6b5cc-162">Стандартный</span><span class="sxs-lookup"><span data-stu-id="6b5cc-162">Standard</span></span>
- <span data-ttu-id="6b5cc-163">Premium</span><span class="sxs-lookup"><span data-stu-id="6b5cc-163">Premium</span></span>
- <span data-ttu-id="6b5cc-164">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="6b5cc-164">DataWarehouse</span></span>
- <span data-ttu-id="6b5cc-165">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="6b5cc-165">Free</span></span>
- <span data-ttu-id="6b5cc-166">Растяжение</span><span class="sxs-lookup"><span data-stu-id="6b5cc-166">Stretch</span></span>
- <span data-ttu-id="6b5cc-167">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="6b5cc-167">GeneralPurpose</span></span>
- <span data-ttu-id="6b5cc-168">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="6b5cc-168">BusinessCritical</span></span>

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

### <span data-ttu-id="6b5cc-169">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6b5cc-169">-ElasticPoolName</span></span>
<span data-ttu-id="6b5cc-170">Определяет имя эластичного пула, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6b5cc-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6b5cc-171">-LicenseType</span></span>
<span data-ttu-id="6b5cc-172">Тип лицензии для базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="6b5cc-173">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6b5cc-173">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="6b5cc-174">The Maintenance configuration id for the SQL Elastic Pool.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-174">The Maintenance configuration id for the SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="6b5cc-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b5cc-175">-ResourceGroupName</span></span>
<span data-ttu-id="6b5cc-176">Задает имя группы ресурсов, которой этот cmdlet назначает эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-176">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="6b5cc-177">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6b5cc-177">-ServerName</span></span>
<span data-ttu-id="6b5cc-178">Указывает имя сервера, на котором размещен эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="6b5cc-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="6b5cc-179">-StorageMB</span></span>
<span data-ttu-id="6b5cc-180">Определяет ограничение хранилища в мегабайтах для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="6b5cc-181">Если этот параметр не задан, этот cmdlet вычисляет значение, которое зависит от значения *параметра Dtu.*</span><span class="sxs-lookup"><span data-stu-id="6b5cc-181">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="6b5cc-182">Возможные [значения см. в eDTU](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) и ограничениях хранилища.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-182">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="6b5cc-183">-Теги</span><span class="sxs-lookup"><span data-stu-id="6b5cc-183">-Tags</span></span>
<span data-ttu-id="6b5cc-184">Словарь пар "ключ-значение" в виде hash table, которую этот cmdlet связывает с эластичным пулом.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-184">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="6b5cc-185">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="6b5cc-185">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6b5cc-186">-VCore</span><span class="sxs-lookup"><span data-stu-id="6b5cc-186">-VCore</span></span>
<span data-ttu-id="6b5cc-187">Общее общее количество vcores для Sql Azure Вячесть Пул.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-187">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="6b5cc-188">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="6b5cc-188">-ZoneRedundant</span></span>
<span data-ttu-id="6b5cc-189">Избыточность зоны, которая связывается с azure Sql Elastic Pool</span><span class="sxs-lookup"><span data-stu-id="6b5cc-189">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="6b5cc-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b5cc-190">-Confirm</span></span>
<span data-ttu-id="6b5cc-191">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b5cc-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b5cc-192">-WhatIf</span></span>
<span data-ttu-id="6b5cc-193">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b5cc-194">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b5cc-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b5cc-195">CommonParameters</span></span>
<span data-ttu-id="6b5cc-196">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b5cc-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b5cc-197">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b5cc-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b5cc-198">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b5cc-198">INPUTS</span></span>

### <span data-ttu-id="6b5cc-199">System.String</span><span class="sxs-lookup"><span data-stu-id="6b5cc-199">System.String</span></span>

## <span data-ttu-id="6b5cc-200">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6b5cc-200">OUTPUTS</span></span>

### <span data-ttu-id="6b5cc-201">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="6b5cc-201">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="6b5cc-202">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6b5cc-202">NOTES</span></span>

## <span data-ttu-id="6b5cc-203">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b5cc-203">RELATED LINKS</span></span>

[<span data-ttu-id="6b5cc-204">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6b5cc-204">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="6b5cc-205">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="6b5cc-205">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="6b5cc-206">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="6b5cc-206">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="6b5cc-207">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6b5cc-207">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="6b5cc-208">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6b5cc-208">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="6b5cc-209">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="6b5cc-209">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
