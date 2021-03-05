---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 25469aa93f673d6a49bbbaa54fcaf22a91019d9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997366"
---
# <span data-ttu-id="d81d9-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d81d9-101">New-AzRedisCache</span></span>

## <span data-ttu-id="d81d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d81d9-102">SYNOPSIS</span></span>
<span data-ttu-id="d81d9-103">Создает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="d81d9-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="d81d9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d81d9-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d81d9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d81d9-105">DESCRIPTION</span></span>
<span data-ttu-id="d81d9-106">Для **создания кэша Azure Redis создается cmdlet New-AzRedisCache.**</span><span class="sxs-lookup"><span data-stu-id="d81d9-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="d81d9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d81d9-107">EXAMPLES</span></span>

### <span data-ttu-id="d81d9-108">Пример 1. Создание кэша Redis</span><span class="sxs-lookup"><span data-stu-id="d81d9-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="d81d9-109">Эта команда создает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="d81d9-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="d81d9-110">Пример 2. Создание стандартного кэша redis SKU</span><span class="sxs-lookup"><span data-stu-id="d81d9-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="d81d9-111">Эта команда создает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="d81d9-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="d81d9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d81d9-112">PARAMETERS</span></span>

### <span data-ttu-id="d81d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d81d9-113">-DefaultProfile</span></span>
<span data-ttu-id="d81d9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d81d9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d81d9-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="d81d9-115">-EnableNonSslPort</span></span>
<span data-ttu-id="d81d9-116">Указывает, включен ли порт, не sSL.</span><span class="sxs-lookup"><span data-stu-id="d81d9-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="d81d9-117">Значение по умолчанию — $False (не SSL-порт отключен).</span><span class="sxs-lookup"><span data-stu-id="d81d9-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="d81d9-118">-Location</span><span class="sxs-lookup"><span data-stu-id="d81d9-118">-Location</span></span>
<span data-ttu-id="d81d9-119">Определяет место, в котором нужно создать кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="d81d9-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="d81d9-120">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="d81d9-120">Valid values are:</span></span> 
- <span data-ttu-id="d81d9-121">Северный Центр США</span><span class="sxs-lookup"><span data-stu-id="d81d9-121">North Central US</span></span>
- <span data-ttu-id="d81d9-122">Южный Центр США</span><span class="sxs-lookup"><span data-stu-id="d81d9-122">South Central US</span></span>
- <span data-ttu-id="d81d9-123">Центральная часть США</span><span class="sxs-lookup"><span data-stu-id="d81d9-123">Central US</span></span>
- <span data-ttu-id="d81d9-124">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="d81d9-124">West Europe</span></span>
- <span data-ttu-id="d81d9-125">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="d81d9-125">North Europe</span></span>
- <span data-ttu-id="d81d9-126">Запад США</span><span class="sxs-lookup"><span data-stu-id="d81d9-126">West US</span></span>
- <span data-ttu-id="d81d9-127">Восток США</span><span class="sxs-lookup"><span data-stu-id="d81d9-127">East US</span></span>
- <span data-ttu-id="d81d9-128">Восток США 2</span><span class="sxs-lookup"><span data-stu-id="d81d9-128">East US 2</span></span>
- <span data-ttu-id="d81d9-129">Восточная Япония</span><span class="sxs-lookup"><span data-stu-id="d81d9-129">Japan East</span></span>
- <span data-ttu-id="d81d9-130">Западная Япония</span><span class="sxs-lookup"><span data-stu-id="d81d9-130">Japan West</span></span>
- <span data-ttu-id="d81d9-131">Южная Бразилия</span><span class="sxs-lookup"><span data-stu-id="d81d9-131">Brazil South</span></span>
- <span data-ttu-id="d81d9-132">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="d81d9-132">Southeast Asia</span></span>
- <span data-ttu-id="d81d9-133">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="d81d9-133">East Asia</span></span>
- <span data-ttu-id="d81d9-134">Восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="d81d9-134">Australia East</span></span>
- <span data-ttu-id="d81d9-135">Юго-Восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="d81d9-135">Australia Southeast</span></span>

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

### <span data-ttu-id="d81d9-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="d81d9-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="d81d9-137">Укажите версию TLS, необходимую для подключения клиентов к кэше.</span><span class="sxs-lookup"><span data-stu-id="d81d9-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="d81d9-138">-Name</span><span class="sxs-lookup"><span data-stu-id="d81d9-138">-Name</span></span>
<span data-ttu-id="d81d9-139">Имя кэша Redis, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="d81d9-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="d81d9-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="d81d9-140">-RedisConfiguration</span></span>
<span data-ttu-id="d81d9-141">Определяет параметры конфигурации Redis.</span><span class="sxs-lookup"><span data-stu-id="d81d9-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="d81d9-142">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="d81d9-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d81d9-143">RDB-резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="d81d9-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="d81d9-144">Указывает на то, что сохранение данных Redis включено.</span><span class="sxs-lookup"><span data-stu-id="d81d9-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="d81d9-145">Только премиум-уровень.</span><span class="sxs-lookup"><span data-stu-id="d81d9-145">Premium tier only.</span></span>
- <span data-ttu-id="d81d9-146">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="d81d9-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="d81d9-147">Указывает строку подключения к учетной записи хранения для сохранения данных Redis.</span><span class="sxs-lookup"><span data-stu-id="d81d9-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="d81d9-148">Только премиум-уровень.</span><span class="sxs-lookup"><span data-stu-id="d81d9-148">Premium tier only.</span></span>
- <span data-ttu-id="d81d9-149">частота rdb-резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="d81d9-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="d81d9-150">Определяет частоту резервного копирования для сохранения данных Redis.</span><span class="sxs-lookup"><span data-stu-id="d81d9-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="d81d9-151">Только премиум-уровень.</span><span class="sxs-lookup"><span data-stu-id="d81d9-151">Premium tier only.</span></span> 
- <span data-ttu-id="d81d9-152">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="d81d9-152">maxmemory-reserved.</span></span>
<span data-ttu-id="d81d9-153">Настраивает память, зарезервированную для процессов, не кэшируемых.</span><span class="sxs-lookup"><span data-stu-id="d81d9-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="d81d9-154">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="d81d9-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d81d9-155">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="d81d9-155">maxmemory-policy.</span></span>
<span data-ttu-id="d81d9-156">Настраивает политику присоединения к кэшу.</span><span class="sxs-lookup"><span data-stu-id="d81d9-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="d81d9-157">Все уровни цен.</span><span class="sxs-lookup"><span data-stu-id="d81d9-157">All pricing tiers.</span></span> 
- <span data-ttu-id="d81d9-158">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="d81d9-158">notify-keyspace-events.</span></span>
<span data-ttu-id="d81d9-159">Настраивает уведомления в области клавиш.</span><span class="sxs-lookup"><span data-stu-id="d81d9-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="d81d9-160">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="d81d9-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="d81d9-161">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="d81d9-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="d81d9-162">Оптимизация памяти для небольших типов агрегированных данных.</span><span class="sxs-lookup"><span data-stu-id="d81d9-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d81d9-163">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="d81d9-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d81d9-164">hash-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="d81d9-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="d81d9-165">Оптимизация памяти для небольших типов агрегированных данных.</span><span class="sxs-lookup"><span data-stu-id="d81d9-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d81d9-166">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="d81d9-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d81d9-167">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="d81d9-167">set-max-intset-entries.</span></span>
<span data-ttu-id="d81d9-168">Оптимизация памяти для небольших типов агрегированных данных.</span><span class="sxs-lookup"><span data-stu-id="d81d9-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d81d9-169">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="d81d9-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d81d9-170">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="d81d9-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="d81d9-171">Оптимизация памяти для небольших типов агрегированных данных.</span><span class="sxs-lookup"><span data-stu-id="d81d9-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d81d9-172">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="d81d9-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d81d9-173">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="d81d9-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="d81d9-174">Оптимизация памяти для небольших типов агрегированных данных.</span><span class="sxs-lookup"><span data-stu-id="d81d9-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d81d9-175">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="d81d9-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d81d9-176">базы данных.</span><span class="sxs-lookup"><span data-stu-id="d81d9-176">databases.</span></span>
<span data-ttu-id="d81d9-177">Количество баз данных.</span><span class="sxs-lookup"><span data-stu-id="d81d9-177">Configures the number of databases.</span></span>
<span data-ttu-id="d81d9-178">Это свойство можно настроить только при создании кэша.</span><span class="sxs-lookup"><span data-stu-id="d81d9-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="d81d9-179">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="d81d9-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="d81d9-180">Дополнительные сведения см. в кэше Azure Redis cache с помощью Azure http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d81d9-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="d81d9-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d81d9-181">-ResourceGroupName</span></span>
<span data-ttu-id="d81d9-182">Имя группы ресурсов, в которой нужно создать кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="d81d9-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="d81d9-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="d81d9-183">-ShardCount</span></span>
<span data-ttu-id="d81d9-184">Количество шардаев, которые нужно создать в кэше кластера Premium.</span><span class="sxs-lookup"><span data-stu-id="d81d9-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="d81d9-185">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="d81d9-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d81d9-186">1</span><span class="sxs-lookup"><span data-stu-id="d81d9-186">1</span></span>
- <span data-ttu-id="d81d9-187">2</span><span class="sxs-lookup"><span data-stu-id="d81d9-187">2</span></span>
- <span data-ttu-id="d81d9-188">3</span><span class="sxs-lookup"><span data-stu-id="d81d9-188">3</span></span>
- <span data-ttu-id="d81d9-189">4</span><span class="sxs-lookup"><span data-stu-id="d81d9-189">4</span></span>
- <span data-ttu-id="d81d9-190">5</span><span class="sxs-lookup"><span data-stu-id="d81d9-190">5</span></span>
- <span data-ttu-id="d81d9-191">6</span><span class="sxs-lookup"><span data-stu-id="d81d9-191">6</span></span>
- <span data-ttu-id="d81d9-192">7</span><span class="sxs-lookup"><span data-stu-id="d81d9-192">7</span></span>
- <span data-ttu-id="d81d9-193">8</span><span class="sxs-lookup"><span data-stu-id="d81d9-193">8</span></span>
- <span data-ttu-id="d81d9-194">9</span><span class="sxs-lookup"><span data-stu-id="d81d9-194">9</span></span> 
- <span data-ttu-id="d81d9-195">10</span><span class="sxs-lookup"><span data-stu-id="d81d9-195">10</span></span>

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

### <span data-ttu-id="d81d9-196">-Size</span><span class="sxs-lookup"><span data-stu-id="d81d9-196">-Size</span></span>
<span data-ttu-id="d81d9-197">Определяет размер кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="d81d9-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="d81d9-198">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="d81d9-198">Valid values are:</span></span> 
- <span data-ttu-id="d81d9-199">P1</span><span class="sxs-lookup"><span data-stu-id="d81d9-199">P1</span></span>
- <span data-ttu-id="d81d9-200">P2</span><span class="sxs-lookup"><span data-stu-id="d81d9-200">P2</span></span>
- <span data-ttu-id="d81d9-201">P3</span><span class="sxs-lookup"><span data-stu-id="d81d9-201">P3</span></span>
- <span data-ttu-id="d81d9-202">P4</span><span class="sxs-lookup"><span data-stu-id="d81d9-202">P4</span></span>
- <span data-ttu-id="d81d9-203">P5</span><span class="sxs-lookup"><span data-stu-id="d81d9-203">P5</span></span>
- <span data-ttu-id="d81d9-204">C0</span><span class="sxs-lookup"><span data-stu-id="d81d9-204">C0</span></span>
- <span data-ttu-id="d81d9-205">C1</span><span class="sxs-lookup"><span data-stu-id="d81d9-205">C1</span></span>
- <span data-ttu-id="d81d9-206">C2</span><span class="sxs-lookup"><span data-stu-id="d81d9-206">C2</span></span>
- <span data-ttu-id="d81d9-207">C3</span><span class="sxs-lookup"><span data-stu-id="d81d9-207">C3</span></span>
- <span data-ttu-id="d81d9-208">C4</span><span class="sxs-lookup"><span data-stu-id="d81d9-208">C4</span></span>
- <span data-ttu-id="d81d9-209">C5</span><span class="sxs-lookup"><span data-stu-id="d81d9-209">C5</span></span>
- <span data-ttu-id="d81d9-210">C6</span><span class="sxs-lookup"><span data-stu-id="d81d9-210">C6</span></span>
- <span data-ttu-id="d81d9-211">250 МБ</span><span class="sxs-lookup"><span data-stu-id="d81d9-211">250MB</span></span>
- <span data-ttu-id="d81d9-212">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="d81d9-212">1GB</span></span>
- <span data-ttu-id="d81d9-213">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="d81d9-213">2.5GB</span></span>
- <span data-ttu-id="d81d9-214">6 ГБ</span><span class="sxs-lookup"><span data-stu-id="d81d9-214">6GB</span></span>
- <span data-ttu-id="d81d9-215">13 ГБ</span><span class="sxs-lookup"><span data-stu-id="d81d9-215">13GB</span></span>
- <span data-ttu-id="d81d9-216">26 ГБ</span><span class="sxs-lookup"><span data-stu-id="d81d9-216">26GB</span></span>
- <span data-ttu-id="d81d9-217">По умолчанию 53 ГБ — 1 ГБ или C1.</span><span class="sxs-lookup"><span data-stu-id="d81d9-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="d81d9-218">-SKU</span><span class="sxs-lookup"><span data-stu-id="d81d9-218">-Sku</span></span>
<span data-ttu-id="d81d9-219">Определяет SKU кэша Redis, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="d81d9-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="d81d9-220">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="d81d9-220">Valid values are:</span></span> 
- <span data-ttu-id="d81d9-221">Базовая</span><span class="sxs-lookup"><span data-stu-id="d81d9-221">Basic</span></span>
- <span data-ttu-id="d81d9-222">Стандартный</span><span class="sxs-lookup"><span data-stu-id="d81d9-222">Standard</span></span>
- <span data-ttu-id="d81d9-223">Premium Значение по умолчанию — "Стандартная".</span><span class="sxs-lookup"><span data-stu-id="d81d9-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="d81d9-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="d81d9-224">-StaticIP</span></span>
<span data-ttu-id="d81d9-225">Указывает уникальный IP-адрес в подсети для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="d81d9-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="d81d9-226">Если значение для этого параметра не задано, этот cmdlet выбирает IP-адрес из подсети.</span><span class="sxs-lookup"><span data-stu-id="d81d9-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="d81d9-227">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d81d9-227">-SubnetId</span></span>
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

### <span data-ttu-id="d81d9-228">-Tag</span><span class="sxs-lookup"><span data-stu-id="d81d9-228">-Tag</span></span>
<span data-ttu-id="d81d9-229">Hash table which represents tags.</span><span class="sxs-lookup"><span data-stu-id="d81d9-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="d81d9-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="d81d9-230">-TenantSettings</span></span>
<span data-ttu-id="d81d9-231">Этот параметр был неподготовлен.</span><span class="sxs-lookup"><span data-stu-id="d81d9-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="d81d9-232">-Zone</span><span class="sxs-lookup"><span data-stu-id="d81d9-232">-Zone</span></span>
<span data-ttu-id="d81d9-233">Список зон.</span><span class="sxs-lookup"><span data-stu-id="d81d9-233">List of zones.</span></span>

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

### <span data-ttu-id="d81d9-234">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d81d9-234">-Confirm</span></span>
<span data-ttu-id="d81d9-235">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d81d9-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d81d9-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d81d9-236">-WhatIf</span></span>
<span data-ttu-id="d81d9-237">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d81d9-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d81d9-238">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d81d9-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d81d9-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d81d9-239">CommonParameters</span></span>
<span data-ttu-id="d81d9-240">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d81d9-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d81d9-241">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d81d9-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d81d9-242">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d81d9-242">INPUTS</span></span>

### <span data-ttu-id="d81d9-243">System.String</span><span class="sxs-lookup"><span data-stu-id="d81d9-243">System.String</span></span>

### <span data-ttu-id="d81d9-244">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d81d9-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d81d9-245">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d81d9-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d81d9-246">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d81d9-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d81d9-247">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d81d9-247">System.String[]</span></span>

## <span data-ttu-id="d81d9-248">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d81d9-248">OUTPUTS</span></span>

### <span data-ttu-id="d81d9-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d81d9-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="d81d9-250">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d81d9-250">NOTES</span></span>

## <span data-ttu-id="d81d9-251">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d81d9-251">RELATED LINKS</span></span>

[<span data-ttu-id="d81d9-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d81d9-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="d81d9-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d81d9-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="d81d9-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d81d9-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


