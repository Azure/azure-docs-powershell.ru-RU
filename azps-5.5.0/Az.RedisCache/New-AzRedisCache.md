---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217865"
---
# <span data-ttu-id="8fa07-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8fa07-101">New-AzRedisCache</span></span>

## <span data-ttu-id="8fa07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fa07-102">SYNOPSIS</span></span>
<span data-ttu-id="8fa07-103">Создает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="8fa07-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="8fa07-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8fa07-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8fa07-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fa07-105">DESCRIPTION</span></span>
<span data-ttu-id="8fa07-106">Для **создания кэша Azure Redis создается cmdlet New-AzRedisCache.**</span><span class="sxs-lookup"><span data-stu-id="8fa07-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="8fa07-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8fa07-107">EXAMPLES</span></span>

### <span data-ttu-id="8fa07-108">Пример 1. Создание кэша Redis</span><span class="sxs-lookup"><span data-stu-id="8fa07-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="8fa07-109">Эта команда создает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="8fa07-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="8fa07-110">Пример 2. Создание стандартного кэша redis SKU</span><span class="sxs-lookup"><span data-stu-id="8fa07-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]} 
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="8fa07-111">Эта команда создает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="8fa07-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="8fa07-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fa07-112">PARAMETERS</span></span>

### <span data-ttu-id="8fa07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fa07-113">-DefaultProfile</span></span>
<span data-ttu-id="8fa07-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8fa07-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fa07-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="8fa07-115">-EnableNonSslPort</span></span>
<span data-ttu-id="8fa07-116">Указывает, включен ли порт, не sSL.</span><span class="sxs-lookup"><span data-stu-id="8fa07-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="8fa07-117">Значение по умолчанию — $False (не SSL-порт отключен).</span><span class="sxs-lookup"><span data-stu-id="8fa07-117">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa07-118">-Location</span><span class="sxs-lookup"><span data-stu-id="8fa07-118">-Location</span></span>
<span data-ttu-id="8fa07-119">Определяет место, в котором нужно создать кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="8fa07-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="8fa07-120">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="8fa07-120">Valid values are:</span></span> 
- <span data-ttu-id="8fa07-121">Северный Центр США</span><span class="sxs-lookup"><span data-stu-id="8fa07-121">North Central US</span></span>
- <span data-ttu-id="8fa07-122">Южный Центр США</span><span class="sxs-lookup"><span data-stu-id="8fa07-122">South Central US</span></span>
- <span data-ttu-id="8fa07-123">Центральная часть США</span><span class="sxs-lookup"><span data-stu-id="8fa07-123">Central US</span></span>
- <span data-ttu-id="8fa07-124">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="8fa07-124">West Europe</span></span>
- <span data-ttu-id="8fa07-125">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="8fa07-125">North Europe</span></span>
- <span data-ttu-id="8fa07-126">Запад США</span><span class="sxs-lookup"><span data-stu-id="8fa07-126">West US</span></span>
- <span data-ttu-id="8fa07-127">Восток США</span><span class="sxs-lookup"><span data-stu-id="8fa07-127">East US</span></span>
- <span data-ttu-id="8fa07-128">Восток США 2</span><span class="sxs-lookup"><span data-stu-id="8fa07-128">East US 2</span></span>
- <span data-ttu-id="8fa07-129">Восточная Япония</span><span class="sxs-lookup"><span data-stu-id="8fa07-129">Japan East</span></span>
- <span data-ttu-id="8fa07-130">Западная Япония</span><span class="sxs-lookup"><span data-stu-id="8fa07-130">Japan West</span></span>
- <span data-ttu-id="8fa07-131">Южная Бразилия</span><span class="sxs-lookup"><span data-stu-id="8fa07-131">Brazil South</span></span>
- <span data-ttu-id="8fa07-132">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="8fa07-132">Southeast Asia</span></span>
- <span data-ttu-id="8fa07-133">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="8fa07-133">East Asia</span></span>
- <span data-ttu-id="8fa07-134">Восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="8fa07-134">Australia East</span></span>
- <span data-ttu-id="8fa07-135">Юго-Восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="8fa07-135">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa07-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="8fa07-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="8fa07-137">Укажите версию TLS, необходимую для подключения клиентов к кэше.</span><span class="sxs-lookup"><span data-stu-id="8fa07-137">Specify the TLS version required by clients to connect to cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa07-138">-Name</span><span class="sxs-lookup"><span data-stu-id="8fa07-138">-Name</span></span>
<span data-ttu-id="8fa07-139">Имя кэша Redis, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="8fa07-139">Specifies the name of the Redis Cache to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa07-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fa07-140">-RedisConfiguration</span></span>
<span data-ttu-id="8fa07-141">Определяет параметры конфигурации Redis.</span><span class="sxs-lookup"><span data-stu-id="8fa07-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="8fa07-142">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="8fa07-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8fa07-143">RDB-резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="8fa07-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="8fa07-144">Указывает, что сохранение данных Redis включено.</span><span class="sxs-lookup"><span data-stu-id="8fa07-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="8fa07-145">Только премиум-уровень.</span><span class="sxs-lookup"><span data-stu-id="8fa07-145">Premium tier only.</span></span>
- <span data-ttu-id="8fa07-146">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="8fa07-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="8fa07-147">Указывает строку подключения к учетной записи хранения для сохранения данных Redis.</span><span class="sxs-lookup"><span data-stu-id="8fa07-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="8fa07-148">Только премиум-уровень.</span><span class="sxs-lookup"><span data-stu-id="8fa07-148">Premium tier only.</span></span>
- <span data-ttu-id="8fa07-149">частота rdb-резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="8fa07-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="8fa07-150">Определяет частоту резервного копирования для сохранения данных Redis.</span><span class="sxs-lookup"><span data-stu-id="8fa07-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="8fa07-151">Только премиум-уровень.</span><span class="sxs-lookup"><span data-stu-id="8fa07-151">Premium tier only.</span></span> 
- <span data-ttu-id="8fa07-152">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="8fa07-152">maxmemory-reserved.</span></span>
<span data-ttu-id="8fa07-153">Настраивает память, зарезервированную для процессов, не кэшируемых.</span><span class="sxs-lookup"><span data-stu-id="8fa07-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="8fa07-154">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="8fa07-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="8fa07-155">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="8fa07-155">maxmemory-policy.</span></span>
<span data-ttu-id="8fa07-156">Настраивает политику присоединения к кэшу.</span><span class="sxs-lookup"><span data-stu-id="8fa07-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="8fa07-157">Все уровни цен.</span><span class="sxs-lookup"><span data-stu-id="8fa07-157">All pricing tiers.</span></span> 
- <span data-ttu-id="8fa07-158">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="8fa07-158">notify-keyspace-events.</span></span>
<span data-ttu-id="8fa07-159">Настраивает уведомления в области клавиш.</span><span class="sxs-lookup"><span data-stu-id="8fa07-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="8fa07-160">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="8fa07-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="8fa07-161">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="8fa07-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="8fa07-162">Оптимизация памяти для небольших типов агрегированных данных.</span><span class="sxs-lookup"><span data-stu-id="8fa07-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="8fa07-163">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="8fa07-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="8fa07-164">hash-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="8fa07-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="8fa07-165">Оптимизация памяти для небольших типов агрегированных данных.</span><span class="sxs-lookup"><span data-stu-id="8fa07-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="8fa07-166">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="8fa07-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="8fa07-167">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="8fa07-167">set-max-intset-entries.</span></span>
<span data-ttu-id="8fa07-168">Оптимизация памяти для небольших типов агрегированных данных.</span><span class="sxs-lookup"><span data-stu-id="8fa07-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="8fa07-169">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="8fa07-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="8fa07-170">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="8fa07-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="8fa07-171">Оптимизация памяти для небольших типов агрегированных данных.</span><span class="sxs-lookup"><span data-stu-id="8fa07-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="8fa07-172">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="8fa07-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="8fa07-173">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="8fa07-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="8fa07-174">Оптимизация памяти для небольших типов агрегированных данных.</span><span class="sxs-lookup"><span data-stu-id="8fa07-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="8fa07-175">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="8fa07-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="8fa07-176">базы данных.</span><span class="sxs-lookup"><span data-stu-id="8fa07-176">databases.</span></span>
<span data-ttu-id="8fa07-177">Количество баз данных.</span><span class="sxs-lookup"><span data-stu-id="8fa07-177">Configures the number of databases.</span></span>
<span data-ttu-id="8fa07-178">Это свойство можно настроить только при создании кэша.</span><span class="sxs-lookup"><span data-stu-id="8fa07-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="8fa07-179">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="8fa07-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="8fa07-180">Дополнительные сведения см. в кэше Azure Redis с помощью Azure http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8fa07-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa07-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fa07-181">-ResourceGroupName</span></span>
<span data-ttu-id="8fa07-182">Имя группы ресурсов, в которой нужно создать кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="8fa07-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa07-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="8fa07-183">-ShardCount</span></span>
<span data-ttu-id="8fa07-184">Определяет количество шардаков, которые нужно создать в кэше кластера Premium.</span><span class="sxs-lookup"><span data-stu-id="8fa07-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="8fa07-185">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="8fa07-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8fa07-186">1</span><span class="sxs-lookup"><span data-stu-id="8fa07-186">1</span></span>
- <span data-ttu-id="8fa07-187">2</span><span class="sxs-lookup"><span data-stu-id="8fa07-187">2</span></span>
- <span data-ttu-id="8fa07-188">3</span><span class="sxs-lookup"><span data-stu-id="8fa07-188">3</span></span>
- <span data-ttu-id="8fa07-189">4</span><span class="sxs-lookup"><span data-stu-id="8fa07-189">4</span></span>
- <span data-ttu-id="8fa07-190">5</span><span class="sxs-lookup"><span data-stu-id="8fa07-190">5</span></span>
- <span data-ttu-id="8fa07-191">6</span><span class="sxs-lookup"><span data-stu-id="8fa07-191">6</span></span>
- <span data-ttu-id="8fa07-192">7</span><span class="sxs-lookup"><span data-stu-id="8fa07-192">7</span></span>
- <span data-ttu-id="8fa07-193">8</span><span class="sxs-lookup"><span data-stu-id="8fa07-193">8</span></span>
- <span data-ttu-id="8fa07-194">9</span><span class="sxs-lookup"><span data-stu-id="8fa07-194">9</span></span> 
- <span data-ttu-id="8fa07-195">10</span><span class="sxs-lookup"><span data-stu-id="8fa07-195">10</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa07-196">-Size</span><span class="sxs-lookup"><span data-stu-id="8fa07-196">-Size</span></span>
<span data-ttu-id="8fa07-197">Определяет размер кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="8fa07-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="8fa07-198">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="8fa07-198">Valid values are:</span></span> 
- <span data-ttu-id="8fa07-199">P1</span><span class="sxs-lookup"><span data-stu-id="8fa07-199">P1</span></span>
- <span data-ttu-id="8fa07-200">P2</span><span class="sxs-lookup"><span data-stu-id="8fa07-200">P2</span></span>
- <span data-ttu-id="8fa07-201">P3</span><span class="sxs-lookup"><span data-stu-id="8fa07-201">P3</span></span>
- <span data-ttu-id="8fa07-202">P4</span><span class="sxs-lookup"><span data-stu-id="8fa07-202">P4</span></span>
- <span data-ttu-id="8fa07-203">P5</span><span class="sxs-lookup"><span data-stu-id="8fa07-203">P5</span></span>
- <span data-ttu-id="8fa07-204">C0</span><span class="sxs-lookup"><span data-stu-id="8fa07-204">C0</span></span>
- <span data-ttu-id="8fa07-205">C1</span><span class="sxs-lookup"><span data-stu-id="8fa07-205">C1</span></span>
- <span data-ttu-id="8fa07-206">C2</span><span class="sxs-lookup"><span data-stu-id="8fa07-206">C2</span></span>
- <span data-ttu-id="8fa07-207">C3</span><span class="sxs-lookup"><span data-stu-id="8fa07-207">C3</span></span>
- <span data-ttu-id="8fa07-208">C4</span><span class="sxs-lookup"><span data-stu-id="8fa07-208">C4</span></span>
- <span data-ttu-id="8fa07-209">C5</span><span class="sxs-lookup"><span data-stu-id="8fa07-209">C5</span></span>
- <span data-ttu-id="8fa07-210">C6</span><span class="sxs-lookup"><span data-stu-id="8fa07-210">C6</span></span>
- <span data-ttu-id="8fa07-211">250 МБ</span><span class="sxs-lookup"><span data-stu-id="8fa07-211">250MB</span></span>
- <span data-ttu-id="8fa07-212">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="8fa07-212">1GB</span></span>
- <span data-ttu-id="8fa07-213">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="8fa07-213">2.5GB</span></span>
- <span data-ttu-id="8fa07-214">6 ГБ</span><span class="sxs-lookup"><span data-stu-id="8fa07-214">6GB</span></span>
- <span data-ttu-id="8fa07-215">13 ГБ</span><span class="sxs-lookup"><span data-stu-id="8fa07-215">13GB</span></span>
- <span data-ttu-id="8fa07-216">26 ГБ</span><span class="sxs-lookup"><span data-stu-id="8fa07-216">26GB</span></span>
- <span data-ttu-id="8fa07-217">По умолчанию 53 ГБ — 1 ГБ или C1.</span><span class="sxs-lookup"><span data-stu-id="8fa07-217">53GB The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa07-218">-SKU</span><span class="sxs-lookup"><span data-stu-id="8fa07-218">-Sku</span></span>
<span data-ttu-id="8fa07-219">Определяет SKU кэша Redis, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="8fa07-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="8fa07-220">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="8fa07-220">Valid values are:</span></span> 
- <span data-ttu-id="8fa07-221">Базовая</span><span class="sxs-lookup"><span data-stu-id="8fa07-221">Basic</span></span>
- <span data-ttu-id="8fa07-222">Стандартный</span><span class="sxs-lookup"><span data-stu-id="8fa07-222">Standard</span></span>
- <span data-ttu-id="8fa07-223">Premium Значение по умолчанию — "Стандартная".</span><span class="sxs-lookup"><span data-stu-id="8fa07-223">Premium The default value is Standard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa07-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="8fa07-224">-StaticIP</span></span>
<span data-ttu-id="8fa07-225">Указывает уникальный IP-адрес в подсети для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="8fa07-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="8fa07-226">Если значение для этого параметра не задано, этот cmdlet выбирает IP-адрес из подсети.</span><span class="sxs-lookup"><span data-stu-id="8fa07-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa07-227">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8fa07-227">-SubnetId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa07-228">-Tag</span><span class="sxs-lookup"><span data-stu-id="8fa07-228">-Tag</span></span>
<span data-ttu-id="8fa07-229">Hash table which represents tags.</span><span class="sxs-lookup"><span data-stu-id="8fa07-229">A hash table which represents tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa07-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="8fa07-230">-TenantSettings</span></span>
<span data-ttu-id="8fa07-231">Этот параметр был неподготовлен.</span><span class="sxs-lookup"><span data-stu-id="8fa07-231">This parameter has been deprecated.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa07-232">-Zone</span><span class="sxs-lookup"><span data-stu-id="8fa07-232">-Zone</span></span>
<span data-ttu-id="8fa07-233">Список зон.</span><span class="sxs-lookup"><span data-stu-id="8fa07-233">List of zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa07-234">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fa07-234">-Confirm</span></span>
<span data-ttu-id="8fa07-235">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fa07-235">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa07-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fa07-236">-WhatIf</span></span>
<span data-ttu-id="8fa07-237">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fa07-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8fa07-238">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8fa07-238">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa07-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fa07-239">CommonParameters</span></span>
<span data-ttu-id="8fa07-240">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fa07-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fa07-241">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8fa07-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fa07-242">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8fa07-242">INPUTS</span></span>

### <span data-ttu-id="8fa07-243">System.String</span><span class="sxs-lookup"><span data-stu-id="8fa07-243">System.String</span></span>

### <span data-ttu-id="8fa07-244">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8fa07-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8fa07-245">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8fa07-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8fa07-246">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8fa07-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8fa07-247">System.String[]</span><span class="sxs-lookup"><span data-stu-id="8fa07-247">System.String[]</span></span>

## <span data-ttu-id="8fa07-248">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8fa07-248">OUTPUTS</span></span>

### <span data-ttu-id="8fa07-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="8fa07-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="8fa07-250">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8fa07-250">NOTES</span></span>

## <span data-ttu-id="8fa07-251">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8fa07-251">RELATED LINKS</span></span>

[<span data-ttu-id="8fa07-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8fa07-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="8fa07-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8fa07-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="8fa07-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8fa07-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


