---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 8fed3f32f5ff0a9920b87438b75cb25cee7c9217
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246673"
---
# <span data-ttu-id="81d0f-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="81d0f-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="81d0f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="81d0f-103">Создание пула эластичных баз данных для базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="81d0f-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="81d0f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81d0f-104">SYNTAX</span></span>

### <span data-ttu-id="81d0f-105">DtuBasedPool (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="81d0f-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81d0f-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="81d0f-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81d0f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81d0f-107">DESCRIPTION</span></span>
<span data-ttu-id="81d0f-108">Командлет **New-AzSqlElasticPool** создает пул эластичных баз данных для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="81d0f-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="81d0f-109">Для нескольких параметров ( *-DTU,-DatabaseDtuMin и-DatabaseDtuMax* ) необходимо, чтобы значение было задано в списке допустимых значений для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="81d0f-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="81d0f-110">Например, параметр-DatabaseDtuMax для стандартного пула 100 eDTU может иметь только значение 10, 20, 50 или 100.</span><span class="sxs-lookup"><span data-stu-id="81d0f-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="81d0f-111">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="81d0f-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="81d0f-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81d0f-112">EXAMPLES</span></span>

### <span data-ttu-id="81d0f-113">Пример 1: создание пула эластичных БД DTU</span><span class="sxs-lookup"><span data-stu-id="81d0f-113">Example 1: Create a DTU elastic pool</span></span>

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

<span data-ttu-id="81d0f-114">Эта команда создает эластичный пул на уровне стандартных служб с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="81d0f-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="81d0f-115">Сервер с именем Server01, назначенный группе ресурсов Azure с именем ResourceGroup01, в которой хранится пул эластичных БД in.</span><span class="sxs-lookup"><span data-stu-id="81d0f-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="81d0f-116">Команда задает значения свойства DTU для пула и баз данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="81d0f-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="81d0f-117">Пример 2: создание эластичного пула vCore</span><span class="sxs-lookup"><span data-stu-id="81d0f-117">Example 2: Create a vCore elastic pool</span></span>

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

<span data-ttu-id="81d0f-118">Эта команда создает эластичный пул на уровне службы GengeralPurpose с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="81d0f-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="81d0f-119">Сервер с именем Server01, назначенный группе ресурсов Azure с именем ResourceGroup01, в которой хранится пул эластичных БД in.</span><span class="sxs-lookup"><span data-stu-id="81d0f-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="81d0f-120">Команда задает значения свойства vCore для пула и базы данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="81d0f-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="81d0f-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="81d0f-121">Example 3</span></span>

<span data-ttu-id="81d0f-122">Создание пула эластичных баз данных для базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="81d0f-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="81d0f-123">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="81d0f-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="81d0f-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81d0f-124">PARAMETERS</span></span>

### <span data-ttu-id="81d0f-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81d0f-125">-AsJob</span></span>
<span data-ttu-id="81d0f-126">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="81d0f-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81d0f-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="81d0f-127">-ComputeGeneration</span></span>
<span data-ttu-id="81d0f-128">Вычислено поколение, которое необходимо назначить.</span><span class="sxs-lookup"><span data-stu-id="81d0f-128">The compute generation to assign.</span></span>

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

### <span data-ttu-id="81d0f-129">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="81d0f-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="81d0f-130">Указывает максимальное количество единиц пропускной способности базы данных (DTU), которые может использовать любая единственная база данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="81d0f-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="81d0f-131">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="81d0f-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="81d0f-132">Базового.</span><span class="sxs-lookup"><span data-stu-id="81d0f-132">Basic.</span></span> <span data-ttu-id="81d0f-133">5 DTU</span><span class="sxs-lookup"><span data-stu-id="81d0f-133">5 DTUs</span></span>
- <span data-ttu-id="81d0f-134">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="81d0f-134">Standard.</span></span> <span data-ttu-id="81d0f-135">100 DTU</span><span class="sxs-lookup"><span data-stu-id="81d0f-135">100 DTUs</span></span>
- <span data-ttu-id="81d0f-136">Версию.</span><span class="sxs-lookup"><span data-stu-id="81d0f-136">Premium.</span></span> <span data-ttu-id="81d0f-137">125 DTU для получения подробных сведений о допустимых значениях, ознакомьтесь с таблицей для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) .</span><span class="sxs-lookup"><span data-stu-id="81d0f-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="81d0f-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="81d0f-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="81d0f-139">Указывает минимальное количество DTU, которое будет гарантировано для всех баз данных в пуле для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="81d0f-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="81d0f-140">Значением по умолчанию является нуль (0).</span><span class="sxs-lookup"><span data-stu-id="81d0f-140">The default value is zero (0).</span></span>
<span data-ttu-id="81d0f-141">Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="81d0f-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="81d0f-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="81d0f-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="81d0f-143">Максимальный номер VCore, который любая база данных SqlAzure может использовать в пуле.</span><span class="sxs-lookup"><span data-stu-id="81d0f-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="81d0f-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="81d0f-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="81d0f-145">Минимальный номер VCore, который любая база данных SqlAzure может использовать в пуле.</span><span class="sxs-lookup"><span data-stu-id="81d0f-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="81d0f-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d0f-146">-DefaultProfile</span></span>
<span data-ttu-id="81d0f-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="81d0f-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81d0f-148">-DTU</span><span class="sxs-lookup"><span data-stu-id="81d0f-148">-Dtu</span></span>
<span data-ttu-id="81d0f-149">Указывает общее количество общих DTU для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="81d0f-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="81d0f-150">Значения по умолчанию для разных выпусков описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="81d0f-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="81d0f-151">Базового.</span><span class="sxs-lookup"><span data-stu-id="81d0f-151">Basic.</span></span>
<span data-ttu-id="81d0f-152">100 DTU</span><span class="sxs-lookup"><span data-stu-id="81d0f-152">100 DTUs</span></span>
- <span data-ttu-id="81d0f-153">Стандартная.</span><span class="sxs-lookup"><span data-stu-id="81d0f-153">Standard.</span></span>
<span data-ttu-id="81d0f-154">100 DTU</span><span class="sxs-lookup"><span data-stu-id="81d0f-154">100 DTUs</span></span>
- <span data-ttu-id="81d0f-155">Версию.</span><span class="sxs-lookup"><span data-stu-id="81d0f-155">Premium.</span></span>
<span data-ttu-id="81d0f-156">125 DTU для получения сведений о допустимых значениях, ознакомьтесь с таблицей для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="81d0f-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="81d0f-157">-Edition</span><span class="sxs-lookup"><span data-stu-id="81d0f-157">-Edition</span></span>
<span data-ttu-id="81d0f-158">Указывает выпуск базы данных SQL Azure, используемой для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="81d0f-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="81d0f-159">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="81d0f-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="81d0f-160">Ничего</span><span class="sxs-lookup"><span data-stu-id="81d0f-160">None</span></span>
- <span data-ttu-id="81d0f-161">Базового</span><span class="sxs-lookup"><span data-stu-id="81d0f-161">Basic</span></span>
- <span data-ttu-id="81d0f-162">Стандартная</span><span class="sxs-lookup"><span data-stu-id="81d0f-162">Standard</span></span>
- <span data-ttu-id="81d0f-163">Версию</span><span class="sxs-lookup"><span data-stu-id="81d0f-163">Premium</span></span>
- <span data-ttu-id="81d0f-164">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="81d0f-164">DataWarehouse</span></span>
- <span data-ttu-id="81d0f-165">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="81d0f-165">Free</span></span>
- <span data-ttu-id="81d0f-166">Показателя</span><span class="sxs-lookup"><span data-stu-id="81d0f-166">Stretch</span></span>
- <span data-ttu-id="81d0f-167">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="81d0f-167">GeneralPurpose</span></span>
- <span data-ttu-id="81d0f-168">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="81d0f-168">BusinessCritical</span></span>

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

### <span data-ttu-id="81d0f-169">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="81d0f-169">-ElasticPoolName</span></span>
<span data-ttu-id="81d0f-170">Указывает имя эластичного пула, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="81d0f-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="81d0f-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="81d0f-171">-LicenseType</span></span>
<span data-ttu-id="81d0f-172">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="81d0f-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="81d0f-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d0f-173">-ResourceGroupName</span></span>
<span data-ttu-id="81d0f-174">Указывает имя группы ресурсов, к которой этот командлет назначает эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="81d0f-174">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="81d0f-175">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="81d0f-175">-ServerName</span></span>
<span data-ttu-id="81d0f-176">Указывает имя сервера, на котором размещается эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="81d0f-176">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="81d0f-177">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="81d0f-177">-StorageMB</span></span>
<span data-ttu-id="81d0f-178">Указывает предельный размер (в мегабайтах) для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="81d0f-178">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="81d0f-179">Если этот параметр не указан, этот командлет вычисляет значение, которое зависит от значения параметра *DTU* .</span><span class="sxs-lookup"><span data-stu-id="81d0f-179">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="81d0f-180">Просмотр возможных значений для просмотра [eDTU и ограничений хранилища](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) .</span><span class="sxs-lookup"><span data-stu-id="81d0f-180">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="81d0f-181">-Теги</span><span class="sxs-lookup"><span data-stu-id="81d0f-181">-Tags</span></span>
<span data-ttu-id="81d0f-182">Задает словарь пар "ключ-значение" в виде хэш-таблицы, которую этот командлет связывает с пулом эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="81d0f-182">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="81d0f-183">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="81d0f-183">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="81d0f-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="81d0f-184">-VCore</span></span>
<span data-ttu-id="81d0f-185">Общее количество общего числа Vcores для пула эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="81d0f-185">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="81d0f-186">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="81d0f-186">-ZoneRedundant</span></span>
<span data-ttu-id="81d0f-187">Резервирование зоны, связанное с пулом эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="81d0f-187">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="81d0f-188">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81d0f-188">-Confirm</span></span>
<span data-ttu-id="81d0f-189">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="81d0f-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81d0f-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81d0f-190">-WhatIf</span></span>
<span data-ttu-id="81d0f-191">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="81d0f-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81d0f-192">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="81d0f-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81d0f-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d0f-193">CommonParameters</span></span>
<span data-ttu-id="81d0f-194">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81d0f-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d0f-195">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81d0f-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d0f-196">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81d0f-196">INPUTS</span></span>

### <span data-ttu-id="81d0f-197">System. String</span><span class="sxs-lookup"><span data-stu-id="81d0f-197">System.String</span></span>

## <span data-ttu-id="81d0f-198">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81d0f-198">OUTPUTS</span></span>

### <span data-ttu-id="81d0f-199">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="81d0f-199">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="81d0f-200">Пуск</span><span class="sxs-lookup"><span data-stu-id="81d0f-200">NOTES</span></span>

## <span data-ttu-id="81d0f-201">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81d0f-201">RELATED LINKS</span></span>

[<span data-ttu-id="81d0f-202">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="81d0f-202">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="81d0f-203">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="81d0f-203">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="81d0f-204">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="81d0f-204">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="81d0f-205">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="81d0f-205">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="81d0f-206">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="81d0f-206">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="81d0f-207">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="81d0f-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
