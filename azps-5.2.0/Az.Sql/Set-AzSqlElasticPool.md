---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: cb76e0ff789f89079772d7f718c3f16c9c01d707
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395927"
---
# <span data-ttu-id="77b26-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="77b26-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="77b26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77b26-102">SYNOPSIS</span></span>
<span data-ttu-id="77b26-103">Изменяет свойства эластичного пула баз данных в Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="77b26-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="77b26-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="77b26-104">SYNTAX</span></span>

### <span data-ttu-id="77b26-105">DtuBasedPool (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77b26-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77b26-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="77b26-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77b26-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77b26-107">DESCRIPTION</span></span>
<span data-ttu-id="77b26-108">**Cmdlet Set-AzSqlElasticPool** задает свойства для эластичного пула в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="77b26-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="77b26-109">Этот cmdlet может изменять eDTUs для каждого пула *(Dtu),* максимальный размер хранилища для пула *(StorageMB),* максимальное число eDTUs для базы данных *(DatabaseDtuMax)* и минимальное значение eDTUs на базу данных *(DatabaseDtuMin).*</span><span class="sxs-lookup"><span data-stu-id="77b26-109">This cmdlet can modify the eDTUs per pool (*Dtu*), storage max size per pool (*StorageMB*), maximum eDTUs per database (*DatabaseDtuMax*), and minimum eDTUs per database (*DatabaseDtuMin*).</span></span>
<span data-ttu-id="77b26-110">Для нескольких параметров *(-Dtu, -DatabaseDtuMin и -DatabaseDtuMax)* требуется, чтобы заданное значение было задано в списке допустимого значения для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="77b26-110">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="77b26-111">Например, для пула eDTU стандартного 100 100 можно установить -DatabaseDtuMax : 10, 20, 50 или 100.</span><span class="sxs-lookup"><span data-stu-id="77b26-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="77b26-112">Подробные сведения о допустимых значениях см. в таблице для пула определенного размера в [эластичных пулах.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="77b26-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="77b26-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="77b26-113">EXAMPLES</span></span>

### <span data-ttu-id="77b26-114">Пример 1. Изменение свойств для эластичного пула</span><span class="sxs-lookup"><span data-stu-id="77b26-114">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="77b26-115">Эта команда изменяет свойства эластичного пула с именем "эластичный пул01".</span><span class="sxs-lookup"><span data-stu-id="77b26-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="77b26-116">Она задает количество DTUs для эластичного пула до 1000 и задает минимальное и максимальное количество DTUs.</span><span class="sxs-lookup"><span data-stu-id="77b26-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="77b26-117">Пример 2. Изменение максимального размера хранилища в эластичном пуле</span><span class="sxs-lookup"><span data-stu-id="77b26-117">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="77b26-118">Эта команда изменяет свойства эластичного пула с именем "эластичный пул01".</span><span class="sxs-lookup"><span data-stu-id="77b26-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="77b26-119">Команда задает максимальное хранилище для эластичного пула, т. е. 2 ТБ.</span><span class="sxs-lookup"><span data-stu-id="77b26-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="77b26-120">Пример 3</span><span class="sxs-lookup"><span data-stu-id="77b26-120">Example 3</span></span>

<span data-ttu-id="77b26-121">Изменяет свойства эластичного пула баз данных в Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="77b26-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="77b26-122">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="77b26-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="77b26-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77b26-123">PARAMETERS</span></span>

### <span data-ttu-id="77b26-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77b26-124">-AsJob</span></span>
<span data-ttu-id="77b26-125">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="77b26-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77b26-126">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="77b26-126">-ComputeGeneration</span></span>
<span data-ttu-id="77b26-127">Назначимое поколение компьютеров.</span><span class="sxs-lookup"><span data-stu-id="77b26-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="77b26-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="77b26-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="77b26-129">Указывает максимальное количество DTUs, которое может использовать любая база данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="77b26-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="77b26-130">Подробные сведения о допустимых значениях см. в таблице для пула определенного размера в [эластичных пулах.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="77b26-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="77b26-131">Значения по умолчанию для разных выпусков следуют за следующими:</span><span class="sxs-lookup"><span data-stu-id="77b26-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="77b26-132">Базовая.</span><span class="sxs-lookup"><span data-stu-id="77b26-132">Basic.</span></span>  <span data-ttu-id="77b26-133">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="77b26-133">5 DTUs</span></span>
- <span data-ttu-id="77b26-134">Стандартный.</span><span class="sxs-lookup"><span data-stu-id="77b26-134">Standard.</span></span> <span data-ttu-id="77b26-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="77b26-135">100 DTUs</span></span>
- <span data-ttu-id="77b26-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="77b26-136">Premium.</span></span> <span data-ttu-id="77b26-137">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="77b26-137">125 DTUs</span></span>

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

### <span data-ttu-id="77b26-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="77b26-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="77b26-139">Указывает минимальное количество DTUs, которое обеспечивается эластичным пулом для всех баз данных в пуле.</span><span class="sxs-lookup"><span data-stu-id="77b26-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="77b26-140">Подробные сведения о допустимых значениях см. в таблице для пула определенного размера в [эластичных пулах.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="77b26-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="77b26-141">Значение по умолчанию — нуль (0).</span><span class="sxs-lookup"><span data-stu-id="77b26-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="77b26-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="77b26-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="77b26-143">Максимальное число VCore, доступного для базы данных SqlAzure в пуле.</span><span class="sxs-lookup"><span data-stu-id="77b26-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="77b26-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="77b26-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="77b26-145">Минимальное число VCore, который может использовать любая база данных SqlAzure в пуле.</span><span class="sxs-lookup"><span data-stu-id="77b26-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="77b26-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77b26-146">-DefaultProfile</span></span>
<span data-ttu-id="77b26-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="77b26-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77b26-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="77b26-148">-Dtu</span></span>
<span data-ttu-id="77b26-149">Определяет общее количество общих DTUs для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="77b26-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="77b26-150">Подробные сведения о допустимых значениях см. в таблице для пула определенного размера в [эластичных пулах.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="77b26-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="77b26-151">Значения по умолчанию для разных выпусков следуют за следующими:</span><span class="sxs-lookup"><span data-stu-id="77b26-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="77b26-152">Базовая.</span><span class="sxs-lookup"><span data-stu-id="77b26-152">Basic.</span></span> <span data-ttu-id="77b26-153">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="77b26-153">100 DTUs</span></span>
- <span data-ttu-id="77b26-154">Стандартный.</span><span class="sxs-lookup"><span data-stu-id="77b26-154">Standard.</span></span> <span data-ttu-id="77b26-155">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="77b26-155">100 DTUs</span></span>
- <span data-ttu-id="77b26-156">Premium.</span><span class="sxs-lookup"><span data-stu-id="77b26-156">Premium.</span></span> <span data-ttu-id="77b26-157">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="77b26-157">125 DTUs</span></span>

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

### <span data-ttu-id="77b26-158">-Edition</span><span class="sxs-lookup"><span data-stu-id="77b26-158">-Edition</span></span>
<span data-ttu-id="77b26-159">Выпуск базы данных Azure SQL для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="77b26-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="77b26-160">Выпуск изменить нельзя.</span><span class="sxs-lookup"><span data-stu-id="77b26-160">You cannot change the edition.</span></span> <span data-ttu-id="77b26-161">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="77b26-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77b26-162">Нет</span><span class="sxs-lookup"><span data-stu-id="77b26-162">None</span></span>
- <span data-ttu-id="77b26-163">Базовая</span><span class="sxs-lookup"><span data-stu-id="77b26-163">Basic</span></span>
- <span data-ttu-id="77b26-164">Стандартный</span><span class="sxs-lookup"><span data-stu-id="77b26-164">Standard</span></span>
- <span data-ttu-id="77b26-165">Premium</span><span class="sxs-lookup"><span data-stu-id="77b26-165">Premium</span></span>
- <span data-ttu-id="77b26-166">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="77b26-166">DataWarehouse</span></span>
- <span data-ttu-id="77b26-167">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="77b26-167">Free</span></span>
- <span data-ttu-id="77b26-168">Растяжение</span><span class="sxs-lookup"><span data-stu-id="77b26-168">Stretch</span></span>
- <span data-ttu-id="77b26-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="77b26-169">GeneralPurpose</span></span>
- <span data-ttu-id="77b26-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="77b26-170">BusinessCritical</span></span>

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

### <span data-ttu-id="77b26-171">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="77b26-171">-ElasticPoolName</span></span>
<span data-ttu-id="77b26-172">Определяет имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="77b26-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="77b26-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="77b26-173">-LicenseType</span></span>
<span data-ttu-id="77b26-174">Тип лицензии для базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="77b26-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="77b26-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77b26-175">-ResourceGroupName</span></span>
<span data-ttu-id="77b26-176">Указывает имя группы ресурсов, которой назначено эластичное пул.</span><span class="sxs-lookup"><span data-stu-id="77b26-176">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="77b26-177">-ServerName</span><span class="sxs-lookup"><span data-stu-id="77b26-177">-ServerName</span></span>
<span data-ttu-id="77b26-178">Указывает имя сервера, на котором размещено эластичное пул.</span><span class="sxs-lookup"><span data-stu-id="77b26-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="77b26-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="77b26-179">-StorageMB</span></span>
<span data-ttu-id="77b26-180">Определяет ограничение хранилища в мегабайтах для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="77b26-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="77b26-181">Дополнительные сведения см. в New-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="77b26-181">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="77b26-182">-Теги</span><span class="sxs-lookup"><span data-stu-id="77b26-182">-Tags</span></span>
<span data-ttu-id="77b26-183">Определяет словарь пар "ключ-значение", который этот cmdlet связывает с пулом в форме hash table.</span><span class="sxs-lookup"><span data-stu-id="77b26-183">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="77b26-184">Например: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="77b26-184">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="77b26-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="77b26-185">-VCore</span></span>
<span data-ttu-id="77b26-186">Общее общее количество vcore для Sql Azure 109999.</span><span class="sxs-lookup"><span data-stu-id="77b26-186">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="77b26-187">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="77b26-187">-ZoneRedundant</span></span>
<span data-ttu-id="77b26-188">Избыточность зоны, которая связывается с azure Sql Elastic Pool</span><span class="sxs-lookup"><span data-stu-id="77b26-188">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="77b26-189">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77b26-189">-Confirm</span></span>
<span data-ttu-id="77b26-190">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="77b26-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77b26-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77b26-191">-WhatIf</span></span>
<span data-ttu-id="77b26-192">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77b26-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77b26-193">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="77b26-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77b26-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b26-194">CommonParameters</span></span>
<span data-ttu-id="77b26-195">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77b26-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b26-196">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77b26-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b26-197">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77b26-197">INPUTS</span></span>

### <span data-ttu-id="77b26-198">System.String</span><span class="sxs-lookup"><span data-stu-id="77b26-198">System.String</span></span>

## <span data-ttu-id="77b26-199">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="77b26-199">OUTPUTS</span></span>

### <span data-ttu-id="77b26-200">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="77b26-200">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="77b26-201">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="77b26-201">NOTES</span></span>

## <span data-ttu-id="77b26-202">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77b26-202">RELATED LINKS</span></span>

[<span data-ttu-id="77b26-203">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="77b26-203">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="77b26-204">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="77b26-204">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="77b26-205">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="77b26-205">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="77b26-206">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="77b26-206">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="77b26-207">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="77b26-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
