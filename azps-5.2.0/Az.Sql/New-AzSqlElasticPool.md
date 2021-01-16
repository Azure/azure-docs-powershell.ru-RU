---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 8fed3f32f5ff0a9920b87438b75cb25cee7c9217
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411996"
---
# <span data-ttu-id="b28a6-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b28a6-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="b28a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b28a6-102">SYNOPSIS</span></span>
<span data-ttu-id="b28a6-103">Создается эластичный пул базы данных для SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="b28a6-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="b28a6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b28a6-104">SYNTAX</span></span>

### <span data-ttu-id="b28a6-105">DtuBasedPool (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b28a6-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b28a6-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="b28a6-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b28a6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b28a6-107">DESCRIPTION</span></span>
<span data-ttu-id="b28a6-108">Для базы данных Azure SQL создается эластичный пул базы данных **New-AzSqlElasticPool.**</span><span class="sxs-lookup"><span data-stu-id="b28a6-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="b28a6-109">Для нескольких параметров *(-Dtu, -DatabaseDtuMin и -DatabaseDtuMax)* требуется, чтобы заданное значение было задано в списке допустимого значения для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="b28a6-109">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="b28a6-110">Например, для пула eDTU стандартного 100 100 можно установить -DatabaseDtuMax : 10, 20, 50 или 100.</span><span class="sxs-lookup"><span data-stu-id="b28a6-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="b28a6-111">Подробные сведения о допустимых значениях см. в таблице для пула определенного размера в [эластичных пулах.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="b28a6-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="b28a6-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b28a6-112">EXAMPLES</span></span>

### <span data-ttu-id="b28a6-113">Пример 1. Создание эластичного пула DTU</span><span class="sxs-lookup"><span data-stu-id="b28a6-113">Example 1: Create a DTU elastic pool</span></span>

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

<span data-ttu-id="b28a6-114">Эта команда создает эластичный пул в стандартном уровне обслуживания Под названием "ЭластичнаяPool01".</span><span class="sxs-lookup"><span data-stu-id="b28a6-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="b28a6-115">Сервер с именем server01, который назначен группе ресурсов Azure с именем ResourceGroup01, размещен в этом пуле.</span><span class="sxs-lookup"><span data-stu-id="b28a6-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="b28a6-116">Команда определяет значения свойств DTU для пула и баз данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="b28a6-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="b28a6-117">Пример 2. Создание эластичного пула vCore</span><span class="sxs-lookup"><span data-stu-id="b28a6-117">Example 2: Create a vCore elastic pool</span></span>

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

<span data-ttu-id="b28a6-118">Эта команда создает эластичный пул на уровне службы GengeralPurpose под названием "99Pool01".</span><span class="sxs-lookup"><span data-stu-id="b28a6-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="b28a6-119">Сервер с именем server01, который назначен группе ресурсов Azure с именем ResourceGroup01, размещен в этом пуле.</span><span class="sxs-lookup"><span data-stu-id="b28a6-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="b28a6-120">Команда определяет значения свойств vCore для пула и баз данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="b28a6-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="b28a6-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b28a6-121">Example 3</span></span>

<span data-ttu-id="b28a6-122">Создается эластичный пул базы данных для SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="b28a6-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="b28a6-123">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="b28a6-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="b28a6-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b28a6-124">PARAMETERS</span></span>

### <span data-ttu-id="b28a6-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b28a6-125">-AsJob</span></span>
<span data-ttu-id="b28a6-126">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b28a6-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b28a6-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="b28a6-127">-ComputeGeneration</span></span>
<span data-ttu-id="b28a6-128">Назначимое поколение компьютеров.</span><span class="sxs-lookup"><span data-stu-id="b28a6-128">The compute generation to assign.</span></span>

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

### <span data-ttu-id="b28a6-129">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="b28a6-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="b28a6-130">Указывает максимальное количество единиц пропускной способности (DTUs), которое может использовать любая база данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="b28a6-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="b28a6-131">Значения по умолчанию для разных выпусков следуют за следующими:</span><span class="sxs-lookup"><span data-stu-id="b28a6-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="b28a6-132">Базовая.</span><span class="sxs-lookup"><span data-stu-id="b28a6-132">Basic.</span></span> <span data-ttu-id="b28a6-133">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="b28a6-133">5 DTUs</span></span>
- <span data-ttu-id="b28a6-134">Стандартный.</span><span class="sxs-lookup"><span data-stu-id="b28a6-134">Standard.</span></span> <span data-ttu-id="b28a6-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="b28a6-135">100 DTUs</span></span>
- <span data-ttu-id="b28a6-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="b28a6-136">Premium.</span></span> <span data-ttu-id="b28a6-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="b28a6-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="b28a6-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="b28a6-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="b28a6-139">Указывает минимальное количество DTUs, которое обеспечивается эластичным пулом для всех баз данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="b28a6-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="b28a6-140">Значение по умолчанию — нуль (0).</span><span class="sxs-lookup"><span data-stu-id="b28a6-140">The default value is zero (0).</span></span>
<span data-ttu-id="b28a6-141">Подробные сведения о допустимых значениях см. в таблице для пула определенного размера в [эластичных пулах.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="b28a6-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="b28a6-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="b28a6-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="b28a6-143">Максимальное число VCore, доступного для базы данных SqlAzure в пуле.</span><span class="sxs-lookup"><span data-stu-id="b28a6-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="b28a6-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="b28a6-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="b28a6-145">Минимальное число VCore, который может использовать любая база данных SqlAzure в пуле.</span><span class="sxs-lookup"><span data-stu-id="b28a6-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="b28a6-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b28a6-146">-DefaultProfile</span></span>
<span data-ttu-id="b28a6-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b28a6-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b28a6-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="b28a6-148">-Dtu</span></span>
<span data-ttu-id="b28a6-149">Определяет общее количество общих DTUs для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="b28a6-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="b28a6-150">Значения по умолчанию для разных выпусков следуют за следующими:</span><span class="sxs-lookup"><span data-stu-id="b28a6-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="b28a6-151">Базовая.</span><span class="sxs-lookup"><span data-stu-id="b28a6-151">Basic.</span></span>
<span data-ttu-id="b28a6-152">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="b28a6-152">100 DTUs</span></span>
- <span data-ttu-id="b28a6-153">Стандартный.</span><span class="sxs-lookup"><span data-stu-id="b28a6-153">Standard.</span></span>
<span data-ttu-id="b28a6-154">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="b28a6-154">100 DTUs</span></span>
- <span data-ttu-id="b28a6-155">Premium.</span><span class="sxs-lookup"><span data-stu-id="b28a6-155">Premium.</span></span>
<span data-ttu-id="b28a6-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="b28a6-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="b28a6-157">-Edition</span><span class="sxs-lookup"><span data-stu-id="b28a6-157">-Edition</span></span>
<span data-ttu-id="b28a6-158">Выпуск базы данных Azure SQL, используемой для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="b28a6-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="b28a6-159">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="b28a6-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b28a6-160">Нет</span><span class="sxs-lookup"><span data-stu-id="b28a6-160">None</span></span>
- <span data-ttu-id="b28a6-161">Базовая</span><span class="sxs-lookup"><span data-stu-id="b28a6-161">Basic</span></span>
- <span data-ttu-id="b28a6-162">Стандартный</span><span class="sxs-lookup"><span data-stu-id="b28a6-162">Standard</span></span>
- <span data-ttu-id="b28a6-163">Premium</span><span class="sxs-lookup"><span data-stu-id="b28a6-163">Premium</span></span>
- <span data-ttu-id="b28a6-164">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="b28a6-164">DataWarehouse</span></span>
- <span data-ttu-id="b28a6-165">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="b28a6-165">Free</span></span>
- <span data-ttu-id="b28a6-166">Растяжение</span><span class="sxs-lookup"><span data-stu-id="b28a6-166">Stretch</span></span>
- <span data-ttu-id="b28a6-167">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="b28a6-167">GeneralPurpose</span></span>
- <span data-ttu-id="b28a6-168">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="b28a6-168">BusinessCritical</span></span>

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

### <span data-ttu-id="b28a6-169">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b28a6-169">-ElasticPoolName</span></span>
<span data-ttu-id="b28a6-170">Определяет имя эластичного пула, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b28a6-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b28a6-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b28a6-171">-LicenseType</span></span>
<span data-ttu-id="b28a6-172">Тип лицензии для базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="b28a6-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="b28a6-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b28a6-173">-ResourceGroupName</span></span>
<span data-ttu-id="b28a6-174">Задает имя группы ресурсов, которой этот cmdlet назначает эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="b28a6-174">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="b28a6-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b28a6-175">-ServerName</span></span>
<span data-ttu-id="b28a6-176">Указывает имя сервера, на котором размещено эластичное пул.</span><span class="sxs-lookup"><span data-stu-id="b28a6-176">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="b28a6-177">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="b28a6-177">-StorageMB</span></span>
<span data-ttu-id="b28a6-178">Ограничение хранилища в мегабайтах для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="b28a6-178">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="b28a6-179">Если этот параметр не задан, этот cmdlet вычисляет значение, которое зависит от значения *параметра Dtu.*</span><span class="sxs-lookup"><span data-stu-id="b28a6-179">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="b28a6-180">Возможные [значения см. в eDTU](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) и ограничениях хранилища.</span><span class="sxs-lookup"><span data-stu-id="b28a6-180">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="b28a6-181">-Теги</span><span class="sxs-lookup"><span data-stu-id="b28a6-181">-Tags</span></span>
<span data-ttu-id="b28a6-182">Словарь пар "ключ-значение" в виде hash table, которую этот cmdlet связывает с эластичным пулом.</span><span class="sxs-lookup"><span data-stu-id="b28a6-182">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="b28a6-183">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="b28a6-183">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b28a6-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="b28a6-184">-VCore</span></span>
<span data-ttu-id="b28a6-185">Общее общее количество vcores для Sql Azure Elastic Pool.</span><span class="sxs-lookup"><span data-stu-id="b28a6-185">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="b28a6-186">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="b28a6-186">-ZoneRedundant</span></span>
<span data-ttu-id="b28a6-187">Избыточность зоны, которая связывается с azure Sql Elastic Pool</span><span class="sxs-lookup"><span data-stu-id="b28a6-187">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="b28a6-188">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b28a6-188">-Confirm</span></span>
<span data-ttu-id="b28a6-189">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b28a6-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b28a6-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b28a6-190">-WhatIf</span></span>
<span data-ttu-id="b28a6-191">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b28a6-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b28a6-192">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b28a6-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b28a6-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b28a6-193">CommonParameters</span></span>
<span data-ttu-id="b28a6-194">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b28a6-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b28a6-195">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b28a6-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b28a6-196">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b28a6-196">INPUTS</span></span>

### <span data-ttu-id="b28a6-197">System.String</span><span class="sxs-lookup"><span data-stu-id="b28a6-197">System.String</span></span>

## <span data-ttu-id="b28a6-198">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b28a6-198">OUTPUTS</span></span>

### <span data-ttu-id="b28a6-199">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="b28a6-199">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="b28a6-200">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b28a6-200">NOTES</span></span>

## <span data-ttu-id="b28a6-201">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b28a6-201">RELATED LINKS</span></span>

[<span data-ttu-id="b28a6-202">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b28a6-202">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="b28a6-203">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="b28a6-203">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="b28a6-204">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="b28a6-204">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="b28a6-205">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b28a6-205">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="b28a6-206">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b28a6-206">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="b28a6-207">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="b28a6-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
