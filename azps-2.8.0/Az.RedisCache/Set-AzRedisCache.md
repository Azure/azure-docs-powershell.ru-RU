---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: aaec1ed3f165338c0aea6bf93e38dfaa8460cdf3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904194"
---
# <span data-ttu-id="19579-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="19579-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="19579-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19579-102">SYNOPSIS</span></span>
<span data-ttu-id="19579-103">Изменяет кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="19579-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="19579-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19579-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19579-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19579-105">DESCRIPTION</span></span>
<span data-ttu-id="19579-106">Командлет **Set-AzRedisCache** изменяет кэш Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="19579-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="19579-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19579-107">EXAMPLES</span></span>

### <span data-ttu-id="19579-108">Пример 1: изменение кэша Redis</span><span class="sxs-lookup"><span data-stu-id="19579-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="19579-109">Эта команда обновляет MaxMemory-политику для кэша Redis с именем MyCache.</span><span class="sxs-lookup"><span data-stu-id="19579-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="19579-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19579-110">PARAMETERS</span></span>

### <span data-ttu-id="19579-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19579-111">-DefaultProfile</span></span>
<span data-ttu-id="19579-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19579-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19579-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="19579-113">-EnableNonSslPort</span></span>
<span data-ttu-id="19579-114">Указывает, включен ли порт без SSL.</span><span class="sxs-lookup"><span data-stu-id="19579-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="19579-115">Значение по умолчанию — $False (порт без SSL отключен).</span><span class="sxs-lookup"><span data-stu-id="19579-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="19579-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="19579-116">-Name</span></span>
<span data-ttu-id="19579-117">Указывает имя кэша Redis, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="19579-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="19579-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="19579-118">-RedisConfiguration</span></span>
<span data-ttu-id="19579-119">Задает параметры конфигурации Redis.</span><span class="sxs-lookup"><span data-stu-id="19579-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="19579-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="19579-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19579-121">RDB — включена резервная копия.</span><span class="sxs-lookup"><span data-stu-id="19579-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="19579-122">Указывает на то, что сохраняемость данных Redis включена.</span><span class="sxs-lookup"><span data-stu-id="19579-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="19579-123">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="19579-123">Premium tier only.</span></span>
- <span data-ttu-id="19579-124">RDB — строка подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="19579-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="19579-125">Задает строку подключения к учетной записи хранения для Redis сохраняемости данных.</span><span class="sxs-lookup"><span data-stu-id="19579-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="19579-126">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="19579-126">Premium tier only.</span></span>
- <span data-ttu-id="19579-127">RDB — периодичность резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="19579-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="19579-128">Указывает периодичность резервного копирования для сохраняемости данных Redis.</span><span class="sxs-lookup"><span data-stu-id="19579-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="19579-129">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="19579-129">Premium tier only.</span></span> 
- <span data-ttu-id="19579-130">MaxMemory — зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="19579-130">maxmemory-reserved.</span></span>
<span data-ttu-id="19579-131">Настраивает память, зарезервированную для процессов без кэширования.</span><span class="sxs-lookup"><span data-stu-id="19579-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="19579-132">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="19579-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="19579-133">MaxMemory — политика.</span><span class="sxs-lookup"><span data-stu-id="19579-133">maxmemory-policy.</span></span>
<span data-ttu-id="19579-134">Настройка политики вытеснения для кэша.</span><span class="sxs-lookup"><span data-stu-id="19579-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="19579-135">Все ценовые категории.</span><span class="sxs-lookup"><span data-stu-id="19579-135">All pricing tiers.</span></span> 
- <span data-ttu-id="19579-136">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="19579-136">notify-keyspace-events.</span></span>
<span data-ttu-id="19579-137">Настраивает уведомления keyspace.</span><span class="sxs-lookup"><span data-stu-id="19579-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="19579-138">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="19579-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="19579-139">хэш-максимум-ziplist-записи.</span><span class="sxs-lookup"><span data-stu-id="19579-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="19579-140">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="19579-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="19579-141">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="19579-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="19579-142">hash-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="19579-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="19579-143">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="19579-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="19579-144">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="19579-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="19579-145">Set-Max-intset-"записи".</span><span class="sxs-lookup"><span data-stu-id="19579-145">set-max-intset-entries.</span></span>
<span data-ttu-id="19579-146">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="19579-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="19579-147">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="19579-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="19579-148">zset-Max-ziplist-(записи).</span><span class="sxs-lookup"><span data-stu-id="19579-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="19579-149">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="19579-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="19579-150">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="19579-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="19579-151">zset-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="19579-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="19579-152">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="19579-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="19579-153">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="19579-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="19579-154">баз данных.</span><span class="sxs-lookup"><span data-stu-id="19579-154">databases.</span></span>
<span data-ttu-id="19579-155">Настраивает количество баз данных.</span><span class="sxs-lookup"><span data-stu-id="19579-155">Configures the number of databases.</span></span>
<span data-ttu-id="19579-156">Это свойство можно настроить только при создании кэша.</span><span class="sxs-lookup"><span data-stu-id="19579-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="19579-157">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="19579-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="19579-158">Дополнительные сведения можно найти в разделе Управление кэшем Redis Azure с помощью Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="19579-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="19579-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19579-159">-ResourceGroupName</span></span>
<span data-ttu-id="19579-160">Указывает имя группы ресурсов, которая содержит кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="19579-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="19579-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="19579-161">-ShardCount</span></span>
<span data-ttu-id="19579-162">Задает количество сегментов для создания в кэше высококачественных кластеров.</span><span class="sxs-lookup"><span data-stu-id="19579-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="19579-163">-Size</span><span class="sxs-lookup"><span data-stu-id="19579-163">-Size</span></span>
<span data-ttu-id="19579-164">Задает размер кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="19579-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="19579-165">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="19579-165">Valid values are:</span></span> 
- <span data-ttu-id="19579-166">P1</span><span class="sxs-lookup"><span data-stu-id="19579-166">P1</span></span>
- <span data-ttu-id="19579-167">–</span><span class="sxs-lookup"><span data-stu-id="19579-167">P2</span></span>
- <span data-ttu-id="19579-168">–</span><span class="sxs-lookup"><span data-stu-id="19579-168">P3</span></span>
- <span data-ttu-id="19579-169">P4</span><span class="sxs-lookup"><span data-stu-id="19579-169">P4</span></span>
- <span data-ttu-id="19579-170">P5</span><span class="sxs-lookup"><span data-stu-id="19579-170">P5</span></span>
- <span data-ttu-id="19579-171">C0</span><span class="sxs-lookup"><span data-stu-id="19579-171">C0</span></span>
- <span data-ttu-id="19579-172">C1</span><span class="sxs-lookup"><span data-stu-id="19579-172">C1</span></span>
- <span data-ttu-id="19579-173">Режим</span><span class="sxs-lookup"><span data-stu-id="19579-173">C2</span></span>
- <span data-ttu-id="19579-174">Ячейку</span><span class="sxs-lookup"><span data-stu-id="19579-174">C3</span></span>
- <span data-ttu-id="19579-175">C4</span><span class="sxs-lookup"><span data-stu-id="19579-175">C4</span></span>
- <span data-ttu-id="19579-176">C5</span><span class="sxs-lookup"><span data-stu-id="19579-176">C5</span></span>
- <span data-ttu-id="19579-177">C6</span><span class="sxs-lookup"><span data-stu-id="19579-177">C6</span></span>
- <span data-ttu-id="19579-178">250MB</span><span class="sxs-lookup"><span data-stu-id="19579-178">250MB</span></span>
- <span data-ttu-id="19579-179">Гбайт</span><span class="sxs-lookup"><span data-stu-id="19579-179">1GB</span></span>
- <span data-ttu-id="19579-180">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="19579-180">2.5GB</span></span>
- <span data-ttu-id="19579-181">6GB</span><span class="sxs-lookup"><span data-stu-id="19579-181">6GB</span></span>
- <span data-ttu-id="19579-182">13GB</span><span class="sxs-lookup"><span data-stu-id="19579-182">13GB</span></span>
- <span data-ttu-id="19579-183">26GB</span><span class="sxs-lookup"><span data-stu-id="19579-183">26GB</span></span>
- <span data-ttu-id="19579-184">53GB</span><span class="sxs-lookup"><span data-stu-id="19579-184">53GB</span></span>
- <span data-ttu-id="19579-185">120 ГБ значение по умолчанию — 1 ГБ или C1.</span><span class="sxs-lookup"><span data-stu-id="19579-185">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="19579-186">-SKU</span><span class="sxs-lookup"><span data-stu-id="19579-186">-Sku</span></span>
<span data-ttu-id="19579-187">Указывает SKU кэша Redis для создания.</span><span class="sxs-lookup"><span data-stu-id="19579-187">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="19579-188">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="19579-188">Valid values are:</span></span> 
- <span data-ttu-id="19579-189">Базового</span><span class="sxs-lookup"><span data-stu-id="19579-189">Basic</span></span>
- <span data-ttu-id="19579-190">Стандартная</span><span class="sxs-lookup"><span data-stu-id="19579-190">Standard</span></span>
- <span data-ttu-id="19579-191">Premium по умолчанию используется значение Standard.</span><span class="sxs-lookup"><span data-stu-id="19579-191">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="19579-192">-Тег</span><span class="sxs-lookup"><span data-stu-id="19579-192">-Tag</span></span>
<span data-ttu-id="19579-193">Хэш-таблица, представляющая Теги.</span><span class="sxs-lookup"><span data-stu-id="19579-193">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="19579-194">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="19579-194">-TenantSettings</span></span>
<span data-ttu-id="19579-195">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="19579-195">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="19579-196">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19579-196">-Confirm</span></span>
<span data-ttu-id="19579-197">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="19579-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19579-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19579-198">-WhatIf</span></span>
<span data-ttu-id="19579-199">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="19579-199">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19579-200">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="19579-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19579-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19579-201">CommonParameters</span></span>
<span data-ttu-id="19579-202">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19579-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19579-203">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19579-203">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19579-204">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19579-204">INPUTS</span></span>

### <span data-ttu-id="19579-205">System. String</span><span class="sxs-lookup"><span data-stu-id="19579-205">System.String</span></span>

### <span data-ttu-id="19579-206">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="19579-206">System.Collections.Hashtable</span></span>

### <span data-ttu-id="19579-207">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="19579-207">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="19579-208">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="19579-208">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="19579-209">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19579-209">OUTPUTS</span></span>

### <span data-ttu-id="19579-210">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="19579-210">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="19579-211">Пуск</span><span class="sxs-lookup"><span data-stu-id="19579-211">NOTES</span></span>

## <span data-ttu-id="19579-212">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19579-212">RELATED LINKS</span></span>

[<span data-ttu-id="19579-213">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="19579-213">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="19579-214">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="19579-214">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="19579-215">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="19579-215">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


