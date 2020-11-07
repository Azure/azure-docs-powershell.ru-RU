---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: a27d8c91f7262e83b139b6662a1f5f401f964b56
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911818"
---
# <span data-ttu-id="b7c2a-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b7c2a-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="b7c2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c2a-103">Создание пула эластичных баз данных для базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="b7c2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7c2a-104">SYNTAX</span></span>

### <span data-ttu-id="b7c2a-105">DtuBasedPool (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b7c2a-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7c2a-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="b7c2a-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7c2a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7c2a-107">DESCRIPTION</span></span>
<span data-ttu-id="b7c2a-108">Командлет **New-AzSqlElasticPool** создает пул эластичных баз данных для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="b7c2a-109">Для нескольких параметров ( *-DTU,-DatabaseDtuMin и-DatabaseDtuMax* ) необходимо, чтобы значение было задано в списке допустимых значений для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="b7c2a-110">Например, параметр-DatabaseDtuMax для стандартного пула 100 eDTU может иметь только значение 10, 20, 50 или 100.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="b7c2a-111">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="b7c2a-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="b7c2a-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7c2a-112">EXAMPLES</span></span>

### <span data-ttu-id="b7c2a-113">Пример 1: создание пула эластичных БД DTU</span><span class="sxs-lookup"><span data-stu-id="b7c2a-113">Example 1: Create a DTU elastic pool</span></span>

```
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

<span data-ttu-id="b7c2a-114">Эта команда создает эластичный пул на уровне стандартных служб с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="b7c2a-115">Сервер с именем Server01, назначенный группе ресурсов Azure с именем ResourceGroup01, в которой хранится пул эластичных БД in.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="b7c2a-116">Команда задает значения свойства DTU для пула и баз данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="b7c2a-117">Пример 2: создание эластичного пула vCore</span><span class="sxs-lookup"><span data-stu-id="b7c2a-117">Example 2: Create a vCore elastic pool</span></span>

```
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

<span data-ttu-id="b7c2a-118">Эта команда создает эластичный пул на уровне службы GengeralPurpose с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="b7c2a-119">Сервер с именем Server01, назначенный группе ресурсов Azure с именем ResourceGroup01, в которой хранится пул эластичных БД in.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="b7c2a-120">Команда задает значения свойства vCore для пула и базы данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="b7c2a-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7c2a-121">PARAMETERS</span></span>

### <span data-ttu-id="b7c2a-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7c2a-122">-AsJob</span></span>
<span data-ttu-id="b7c2a-123">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b7c2a-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7c2a-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="b7c2a-124">-ComputeGeneration</span></span>
<span data-ttu-id="b7c2a-125">Вычислено поколение, которое необходимо назначить.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="b7c2a-126">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="b7c2a-126">-DatabaseDtuMax</span></span>
<span data-ttu-id="b7c2a-127">Указывает максимальное количество единиц пропускной способности базы данных (DTU), которые может использовать любая единственная база данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-127">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="b7c2a-128">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-128">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="b7c2a-129">Базового.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-129">Basic.</span></span> <span data-ttu-id="b7c2a-130">5 DTU</span><span class="sxs-lookup"><span data-stu-id="b7c2a-130">5 DTUs</span></span>
- <span data-ttu-id="b7c2a-131">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-131">Standard.</span></span> <span data-ttu-id="b7c2a-132">100 DTU</span><span class="sxs-lookup"><span data-stu-id="b7c2a-132">100 DTUs</span></span>
- <span data-ttu-id="b7c2a-133">Версию.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-133">Premium.</span></span> <span data-ttu-id="b7c2a-134">125 DTU для получения подробных сведений о допустимых значениях, ознакомьтесь с таблицей для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) .</span><span class="sxs-lookup"><span data-stu-id="b7c2a-134">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="b7c2a-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="b7c2a-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="b7c2a-136">Указывает минимальное количество DTU, которое будет гарантировано для всех баз данных в пуле для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="b7c2a-137">Значением по умолчанию является нуль (0).</span><span class="sxs-lookup"><span data-stu-id="b7c2a-137">The default value is zero (0).</span></span>
<span data-ttu-id="b7c2a-138">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="b7c2a-138">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="b7c2a-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="b7c2a-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="b7c2a-140">Максимальный номер VCore, который любая база данных SqlAzure может использовать в пуле.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-140">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="b7c2a-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="b7c2a-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="b7c2a-142">Минимальный номер VCore, который любая база данных SqlAzure может использовать в пуле.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="b7c2a-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c2a-143">-DefaultProfile</span></span>
<span data-ttu-id="b7c2a-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b7c2a-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7c2a-145">-DTU</span><span class="sxs-lookup"><span data-stu-id="b7c2a-145">-Dtu</span></span>
<span data-ttu-id="b7c2a-146">Указывает общее количество общих DTU для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="b7c2a-147">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-147">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="b7c2a-148">Базового.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-148">Basic.</span></span>
<span data-ttu-id="b7c2a-149">100 DTU</span><span class="sxs-lookup"><span data-stu-id="b7c2a-149">100 DTUs</span></span>
- <span data-ttu-id="b7c2a-150">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-150">Standard.</span></span>
<span data-ttu-id="b7c2a-151">100 DTU</span><span class="sxs-lookup"><span data-stu-id="b7c2a-151">100 DTUs</span></span>
- <span data-ttu-id="b7c2a-152">Версию.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-152">Premium.</span></span>
<span data-ttu-id="b7c2a-153">125 DTU для получения сведений о допустимых значениях, ознакомьтесь с таблицей для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="b7c2a-153">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="b7c2a-154">-Edition</span><span class="sxs-lookup"><span data-stu-id="b7c2a-154">-Edition</span></span>
<span data-ttu-id="b7c2a-155">Указывает выпуск базы данных SQL Azure, используемой для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-155">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="b7c2a-156">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b7c2a-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7c2a-157">Ничего</span><span class="sxs-lookup"><span data-stu-id="b7c2a-157">None</span></span>
- <span data-ttu-id="b7c2a-158">Базового</span><span class="sxs-lookup"><span data-stu-id="b7c2a-158">Basic</span></span>
- <span data-ttu-id="b7c2a-159">Стандартная</span><span class="sxs-lookup"><span data-stu-id="b7c2a-159">Standard</span></span>
- <span data-ttu-id="b7c2a-160">Версию</span><span class="sxs-lookup"><span data-stu-id="b7c2a-160">Premium</span></span>
- <span data-ttu-id="b7c2a-161">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="b7c2a-161">DataWarehouse</span></span>
- <span data-ttu-id="b7c2a-162">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="b7c2a-162">Free</span></span>
- <span data-ttu-id="b7c2a-163">Показателя</span><span class="sxs-lookup"><span data-stu-id="b7c2a-163">Stretch</span></span>
- <span data-ttu-id="b7c2a-164">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="b7c2a-164">GeneralPurpose</span></span>
- <span data-ttu-id="b7c2a-165">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="b7c2a-165">BusinessCritical</span></span>

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

### <span data-ttu-id="b7c2a-166">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b7c2a-166">-ElasticPoolName</span></span>
<span data-ttu-id="b7c2a-167">Указывает имя эластичного пула, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-167">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b7c2a-168">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b7c2a-168">-LicenseType</span></span>
<span data-ttu-id="b7c2a-169">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-169">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="b7c2a-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c2a-170">-ResourceGroupName</span></span>
<span data-ttu-id="b7c2a-171">Указывает имя группы ресурсов, к которой этот командлет назначает эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-171">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="b7c2a-172">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="b7c2a-172">-ServerName</span></span>
<span data-ttu-id="b7c2a-173">Указывает имя сервера, на котором размещается эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-173">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="b7c2a-174">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="b7c2a-174">-StorageMB</span></span>
<span data-ttu-id="b7c2a-175">Указывает предельный размер (в мегабайтах) для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-175">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="b7c2a-176">Если этот параметр не указан, этот командлет вычисляет значение, которое зависит от значения параметра *DTU* .</span><span class="sxs-lookup"><span data-stu-id="b7c2a-176">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="b7c2a-177">Просмотр возможных значений для просмотра [eDTU и ограничений хранилища](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) .</span><span class="sxs-lookup"><span data-stu-id="b7c2a-177">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="b7c2a-178">-Теги</span><span class="sxs-lookup"><span data-stu-id="b7c2a-178">-Tags</span></span>
<span data-ttu-id="b7c2a-179">Задает словарь пар "ключ-значение" в виде хэш-таблицы, которую этот командлет связывает с пулом эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-179">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="b7c2a-180">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="b7c2a-180">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b7c2a-181">-VCore</span><span class="sxs-lookup"><span data-stu-id="b7c2a-181">-VCore</span></span>
<span data-ttu-id="b7c2a-182">Общее количество общего числа Vcores для пула эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-182">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="b7c2a-183">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="b7c2a-183">-ZoneRedundant</span></span>
<span data-ttu-id="b7c2a-184">Резервирование зоны, связанное с пулом эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-184">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="b7c2a-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7c2a-185">-Confirm</span></span>
<span data-ttu-id="b7c2a-186">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7c2a-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7c2a-187">-WhatIf</span></span>
<span data-ttu-id="b7c2a-188">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7c2a-189">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7c2a-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c2a-190">CommonParameters</span></span>
<span data-ttu-id="b7c2a-191">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7c2a-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c2a-192">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7c2a-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c2a-193">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7c2a-193">INPUTS</span></span>

### <span data-ttu-id="b7c2a-194">System. String</span><span class="sxs-lookup"><span data-stu-id="b7c2a-194">System.String</span></span>

## <span data-ttu-id="b7c2a-195">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7c2a-195">OUTPUTS</span></span>

### <span data-ttu-id="b7c2a-196">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="b7c2a-196">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="b7c2a-197">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7c2a-197">NOTES</span></span>

## <span data-ttu-id="b7c2a-198">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7c2a-198">RELATED LINKS</span></span>

[<span data-ttu-id="b7c2a-199">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b7c2a-199">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="b7c2a-200">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="b7c2a-200">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="b7c2a-201">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="b7c2a-201">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="b7c2a-202">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b7c2a-202">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="b7c2a-203">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b7c2a-203">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="b7c2a-204">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="b7c2a-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
