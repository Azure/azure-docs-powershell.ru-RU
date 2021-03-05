---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 809939a4e218005c9b4c41846e0885dfca553964
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000915"
---
# <span data-ttu-id="7c708-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7c708-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="7c708-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c708-102">SYNOPSIS</span></span>
<span data-ttu-id="7c708-103">Изменяет кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="7c708-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="7c708-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7c708-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c708-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c708-105">DESCRIPTION</span></span>
<span data-ttu-id="7c708-106">**Cmdlet Set-AzRedisCache** изменяет кэш Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="7c708-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="7c708-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7c708-107">EXAMPLES</span></span>

### <span data-ttu-id="7c708-108">Пример 1. Изменение кэша Redis</span><span class="sxs-lookup"><span data-stu-id="7c708-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : mygroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/myCache
          Location           : North Central US
          Name               : MyCache
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

<span data-ttu-id="7c708-109">Эта команда обновляет политику maxmemory для кэша Redis с именем MyCache.</span><span class="sxs-lookup"><span data-stu-id="7c708-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="7c708-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c708-110">PARAMETERS</span></span>

### <span data-ttu-id="7c708-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c708-111">-DefaultProfile</span></span>
<span data-ttu-id="7c708-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c708-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c708-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="7c708-113">-EnableNonSslPort</span></span>
<span data-ttu-id="7c708-114">Указывает на то, включен ли порт, не ключаный SSL.</span><span class="sxs-lookup"><span data-stu-id="7c708-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="7c708-115">Значение по умолчанию — $False (не SSL-порт отключен).</span><span class="sxs-lookup"><span data-stu-id="7c708-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="7c708-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="7c708-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="7c708-117">Укажите версию TLS, необходимую для подключения клиентов к кэше.</span><span class="sxs-lookup"><span data-stu-id="7c708-117">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="7c708-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7c708-118">-Name</span></span>
<span data-ttu-id="7c708-119">Имя кэша Redis, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="7c708-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="7c708-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c708-120">-RedisConfiguration</span></span>
<span data-ttu-id="7c708-121">Определяет параметры конфигурации Redis.</span><span class="sxs-lookup"><span data-stu-id="7c708-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="7c708-122">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="7c708-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7c708-123">RDB-резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="7c708-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="7c708-124">Указывает на то, что сохранение данных Redis включено.</span><span class="sxs-lookup"><span data-stu-id="7c708-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="7c708-125">Только премиум-уровень.</span><span class="sxs-lookup"><span data-stu-id="7c708-125">Premium tier only.</span></span>
- <span data-ttu-id="7c708-126">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="7c708-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="7c708-127">Указывает строку подключения к учетной записи хранения для сохранения данных Redis.</span><span class="sxs-lookup"><span data-stu-id="7c708-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="7c708-128">Только премиум-уровень.</span><span class="sxs-lookup"><span data-stu-id="7c708-128">Premium tier only.</span></span>
- <span data-ttu-id="7c708-129">RDB-частота резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7c708-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="7c708-130">Определяет частоту резервного копирования для сохранения данных Redis.</span><span class="sxs-lookup"><span data-stu-id="7c708-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="7c708-131">Только премиум-уровень.</span><span class="sxs-lookup"><span data-stu-id="7c708-131">Premium tier only.</span></span> 
- <span data-ttu-id="7c708-132">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="7c708-132">maxmemory-reserved.</span></span>
<span data-ttu-id="7c708-133">Настраивает память, зарезервированную для процессов, не кэшируемых.</span><span class="sxs-lookup"><span data-stu-id="7c708-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="7c708-134">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="7c708-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="7c708-135">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="7c708-135">maxmemory-policy.</span></span>
<span data-ttu-id="7c708-136">Настраивает политику присоединения к кэшу.</span><span class="sxs-lookup"><span data-stu-id="7c708-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="7c708-137">Все уровни цен.</span><span class="sxs-lookup"><span data-stu-id="7c708-137">All pricing tiers.</span></span> 
- <span data-ttu-id="7c708-138">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="7c708-138">notify-keyspace-events.</span></span>
<span data-ttu-id="7c708-139">Настраивает уведомления в области клавиш.</span><span class="sxs-lookup"><span data-stu-id="7c708-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="7c708-140">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="7c708-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="7c708-141">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="7c708-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="7c708-142">Оптимизация памяти для небольших типов агрегированных данных.</span><span class="sxs-lookup"><span data-stu-id="7c708-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="7c708-143">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="7c708-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="7c708-144">hash-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="7c708-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="7c708-145">Оптимизация памяти для небольших типов агрегированных данных.</span><span class="sxs-lookup"><span data-stu-id="7c708-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="7c708-146">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="7c708-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="7c708-147">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="7c708-147">set-max-intset-entries.</span></span>
<span data-ttu-id="7c708-148">Оптимизация памяти для небольших типов агрегированных данных.</span><span class="sxs-lookup"><span data-stu-id="7c708-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="7c708-149">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="7c708-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="7c708-150">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="7c708-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="7c708-151">Оптимизация памяти для небольших типов агрегированных данных.</span><span class="sxs-lookup"><span data-stu-id="7c708-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="7c708-152">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="7c708-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="7c708-153">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="7c708-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="7c708-154">Оптимизация памяти для небольших типов агрегированных данных.</span><span class="sxs-lookup"><span data-stu-id="7c708-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="7c708-155">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="7c708-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="7c708-156">базы данных.</span><span class="sxs-lookup"><span data-stu-id="7c708-156">databases.</span></span>
<span data-ttu-id="7c708-157">Количество баз данных.</span><span class="sxs-lookup"><span data-stu-id="7c708-157">Configures the number of databases.</span></span>
<span data-ttu-id="7c708-158">Это свойство можно настроить только при создании кэша.</span><span class="sxs-lookup"><span data-stu-id="7c708-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="7c708-159">Стандартные и премиум-уровни.</span><span class="sxs-lookup"><span data-stu-id="7c708-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="7c708-160">Дополнительные сведения см. в кэше Azure Redis с помощью Azure http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7c708-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="7c708-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c708-161">-ResourceGroupName</span></span>
<span data-ttu-id="7c708-162">Имя группы ресурсов, которая содержит кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="7c708-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="7c708-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="7c708-163">-ShardCount</span></span>
<span data-ttu-id="7c708-164">Определяет количество шардаков, которые нужно создать в кэше кластера Premium.</span><span class="sxs-lookup"><span data-stu-id="7c708-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="7c708-165">-Size</span><span class="sxs-lookup"><span data-stu-id="7c708-165">-Size</span></span>
<span data-ttu-id="7c708-166">Определяет размер кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="7c708-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="7c708-167">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="7c708-167">Valid values are:</span></span> 
- <span data-ttu-id="7c708-168">P1</span><span class="sxs-lookup"><span data-stu-id="7c708-168">P1</span></span>
- <span data-ttu-id="7c708-169">P2</span><span class="sxs-lookup"><span data-stu-id="7c708-169">P2</span></span>
- <span data-ttu-id="7c708-170">P3</span><span class="sxs-lookup"><span data-stu-id="7c708-170">P3</span></span>
- <span data-ttu-id="7c708-171">P4</span><span class="sxs-lookup"><span data-stu-id="7c708-171">P4</span></span>
- <span data-ttu-id="7c708-172">P5</span><span class="sxs-lookup"><span data-stu-id="7c708-172">P5</span></span>
- <span data-ttu-id="7c708-173">C0</span><span class="sxs-lookup"><span data-stu-id="7c708-173">C0</span></span>
- <span data-ttu-id="7c708-174">C1</span><span class="sxs-lookup"><span data-stu-id="7c708-174">C1</span></span>
- <span data-ttu-id="7c708-175">C2</span><span class="sxs-lookup"><span data-stu-id="7c708-175">C2</span></span>
- <span data-ttu-id="7c708-176">C3</span><span class="sxs-lookup"><span data-stu-id="7c708-176">C3</span></span>
- <span data-ttu-id="7c708-177">C4</span><span class="sxs-lookup"><span data-stu-id="7c708-177">C4</span></span>
- <span data-ttu-id="7c708-178">C5</span><span class="sxs-lookup"><span data-stu-id="7c708-178">C5</span></span>
- <span data-ttu-id="7c708-179">C6</span><span class="sxs-lookup"><span data-stu-id="7c708-179">C6</span></span>
- <span data-ttu-id="7c708-180">250 МБ</span><span class="sxs-lookup"><span data-stu-id="7c708-180">250MB</span></span>
- <span data-ttu-id="7c708-181">1 ГБ</span><span class="sxs-lookup"><span data-stu-id="7c708-181">1GB</span></span>
- <span data-ttu-id="7c708-182">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="7c708-182">2.5GB</span></span>
- <span data-ttu-id="7c708-183">6 ГБ</span><span class="sxs-lookup"><span data-stu-id="7c708-183">6GB</span></span>
- <span data-ttu-id="7c708-184">13 ГБ</span><span class="sxs-lookup"><span data-stu-id="7c708-184">13GB</span></span>
- <span data-ttu-id="7c708-185">26 ГБ</span><span class="sxs-lookup"><span data-stu-id="7c708-185">26GB</span></span>
- <span data-ttu-id="7c708-186">53 ГБ</span><span class="sxs-lookup"><span data-stu-id="7c708-186">53GB</span></span>
- <span data-ttu-id="7c708-187">По умолчанию 120 ГБ — 1 ГБ или C1.</span><span class="sxs-lookup"><span data-stu-id="7c708-187">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="7c708-188">-SKU</span><span class="sxs-lookup"><span data-stu-id="7c708-188">-Sku</span></span>
<span data-ttu-id="7c708-189">Определяет SKU кэша Redis, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="7c708-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="7c708-190">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="7c708-190">Valid values are:</span></span> 
- <span data-ttu-id="7c708-191">Базовая</span><span class="sxs-lookup"><span data-stu-id="7c708-191">Basic</span></span>
- <span data-ttu-id="7c708-192">Стандартный</span><span class="sxs-lookup"><span data-stu-id="7c708-192">Standard</span></span>
- <span data-ttu-id="7c708-193">Premium Значение по умолчанию — "Стандартная".</span><span class="sxs-lookup"><span data-stu-id="7c708-193">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="7c708-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="7c708-194">-Tag</span></span>
<span data-ttu-id="7c708-195">Hash table which represents tags.</span><span class="sxs-lookup"><span data-stu-id="7c708-195">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="7c708-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="7c708-196">-TenantSettings</span></span>
<span data-ttu-id="7c708-197">Этот параметр был неподготовлен.</span><span class="sxs-lookup"><span data-stu-id="7c708-197">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="7c708-198">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c708-198">-Confirm</span></span>
<span data-ttu-id="7c708-199">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c708-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c708-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c708-200">-WhatIf</span></span>
<span data-ttu-id="7c708-201">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c708-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c708-202">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7c708-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c708-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c708-203">CommonParameters</span></span>
<span data-ttu-id="7c708-204">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c708-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c708-205">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c708-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c708-206">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c708-206">INPUTS</span></span>

### <span data-ttu-id="7c708-207">System.String</span><span class="sxs-lookup"><span data-stu-id="7c708-207">System.String</span></span>

### <span data-ttu-id="7c708-208">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7c708-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7c708-209">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7c708-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7c708-210">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7c708-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7c708-211">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7c708-211">OUTPUTS</span></span>

### <span data-ttu-id="7c708-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="7c708-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="7c708-213">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7c708-213">NOTES</span></span>

## <span data-ttu-id="7c708-214">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c708-214">RELATED LINKS</span></span>

[<span data-ttu-id="7c708-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7c708-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="7c708-216">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7c708-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="7c708-217">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7c708-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


