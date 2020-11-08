---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 5cb3723e95acbc05b5fffce55a1f768c8a3b7fba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235926"
---
# <span data-ttu-id="540bb-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="540bb-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="540bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="540bb-102">SYNOPSIS</span></span>
<span data-ttu-id="540bb-103">Изменяет кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="540bb-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="540bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="540bb-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="540bb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="540bb-105">DESCRIPTION</span></span>
<span data-ttu-id="540bb-106">Командлет **Set-AzRedisCache** изменяет кэш Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="540bb-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="540bb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="540bb-107">EXAMPLES</span></span>

### <span data-ttu-id="540bb-108">Пример 1: изменение кэша Redis</span><span class="sxs-lookup"><span data-stu-id="540bb-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="540bb-109">Эта команда обновляет MaxMemory-политику для кэша Redis с именем MyCache.</span><span class="sxs-lookup"><span data-stu-id="540bb-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="540bb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="540bb-110">PARAMETERS</span></span>

### <span data-ttu-id="540bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="540bb-111">-DefaultProfile</span></span>
<span data-ttu-id="540bb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="540bb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="540bb-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="540bb-113">-EnableNonSslPort</span></span>
<span data-ttu-id="540bb-114">Указывает, включен ли порт без SSL.</span><span class="sxs-lookup"><span data-stu-id="540bb-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="540bb-115">Значение по умолчанию — $False (порт без SSL отключен).</span><span class="sxs-lookup"><span data-stu-id="540bb-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="540bb-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="540bb-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="540bb-117">Укажите версию TLS, необходимую клиентам для подключения к кэшу.</span><span class="sxs-lookup"><span data-stu-id="540bb-117">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="540bb-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="540bb-118">-Name</span></span>
<span data-ttu-id="540bb-119">Указывает имя кэша Redis, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="540bb-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="540bb-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="540bb-120">-RedisConfiguration</span></span>
<span data-ttu-id="540bb-121">Задает параметры конфигурации Redis.</span><span class="sxs-lookup"><span data-stu-id="540bb-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="540bb-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="540bb-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="540bb-123">RDB — включена резервная копия.</span><span class="sxs-lookup"><span data-stu-id="540bb-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="540bb-124">Указывает на то, что сохраняемость данных Redis включена.</span><span class="sxs-lookup"><span data-stu-id="540bb-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="540bb-125">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="540bb-125">Premium tier only.</span></span>
- <span data-ttu-id="540bb-126">RDB — строка подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="540bb-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="540bb-127">Задает строку подключения к учетной записи хранения для Redis сохраняемости данных.</span><span class="sxs-lookup"><span data-stu-id="540bb-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="540bb-128">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="540bb-128">Premium tier only.</span></span>
- <span data-ttu-id="540bb-129">RDB — периодичность резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="540bb-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="540bb-130">Указывает периодичность резервного копирования для сохраняемости данных Redis.</span><span class="sxs-lookup"><span data-stu-id="540bb-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="540bb-131">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="540bb-131">Premium tier only.</span></span> 
- <span data-ttu-id="540bb-132">MaxMemory — зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="540bb-132">maxmemory-reserved.</span></span>
<span data-ttu-id="540bb-133">Настраивает память, зарезервированную для процессов без кэширования.</span><span class="sxs-lookup"><span data-stu-id="540bb-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="540bb-134">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="540bb-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="540bb-135">MaxMemory — политика.</span><span class="sxs-lookup"><span data-stu-id="540bb-135">maxmemory-policy.</span></span>
<span data-ttu-id="540bb-136">Настройка политики вытеснения для кэша.</span><span class="sxs-lookup"><span data-stu-id="540bb-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="540bb-137">Все ценовые категории.</span><span class="sxs-lookup"><span data-stu-id="540bb-137">All pricing tiers.</span></span> 
- <span data-ttu-id="540bb-138">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="540bb-138">notify-keyspace-events.</span></span>
<span data-ttu-id="540bb-139">Настраивает уведомления keyspace.</span><span class="sxs-lookup"><span data-stu-id="540bb-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="540bb-140">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="540bb-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="540bb-141">хэш-максимум-ziplist-записи.</span><span class="sxs-lookup"><span data-stu-id="540bb-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="540bb-142">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="540bb-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="540bb-143">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="540bb-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="540bb-144">hash-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="540bb-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="540bb-145">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="540bb-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="540bb-146">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="540bb-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="540bb-147">Set-Max-intset-"записи".</span><span class="sxs-lookup"><span data-stu-id="540bb-147">set-max-intset-entries.</span></span>
<span data-ttu-id="540bb-148">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="540bb-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="540bb-149">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="540bb-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="540bb-150">zset-Max-ziplist-(записи).</span><span class="sxs-lookup"><span data-stu-id="540bb-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="540bb-151">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="540bb-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="540bb-152">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="540bb-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="540bb-153">zset-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="540bb-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="540bb-154">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="540bb-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="540bb-155">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="540bb-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="540bb-156">баз данных.</span><span class="sxs-lookup"><span data-stu-id="540bb-156">databases.</span></span>
<span data-ttu-id="540bb-157">Настраивает количество баз данных.</span><span class="sxs-lookup"><span data-stu-id="540bb-157">Configures the number of databases.</span></span>
<span data-ttu-id="540bb-158">Это свойство можно настроить только при создании кэша.</span><span class="sxs-lookup"><span data-stu-id="540bb-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="540bb-159">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="540bb-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="540bb-160">Дополнительные сведения можно найти в разделе Управление кэшем Redis Azure с помощью Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="540bb-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="540bb-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="540bb-161">-ResourceGroupName</span></span>
<span data-ttu-id="540bb-162">Указывает имя группы ресурсов, которая содержит кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="540bb-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="540bb-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="540bb-163">-ShardCount</span></span>
<span data-ttu-id="540bb-164">Задает количество сегментов для создания в кэше высококачественных кластеров.</span><span class="sxs-lookup"><span data-stu-id="540bb-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="540bb-165">-Size</span><span class="sxs-lookup"><span data-stu-id="540bb-165">-Size</span></span>
<span data-ttu-id="540bb-166">Задает размер кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="540bb-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="540bb-167">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="540bb-167">Valid values are:</span></span> 
- <span data-ttu-id="540bb-168">P1</span><span class="sxs-lookup"><span data-stu-id="540bb-168">P1</span></span>
- <span data-ttu-id="540bb-169">–</span><span class="sxs-lookup"><span data-stu-id="540bb-169">P2</span></span>
- <span data-ttu-id="540bb-170">–</span><span class="sxs-lookup"><span data-stu-id="540bb-170">P3</span></span>
- <span data-ttu-id="540bb-171">P4</span><span class="sxs-lookup"><span data-stu-id="540bb-171">P4</span></span>
- <span data-ttu-id="540bb-172">P5</span><span class="sxs-lookup"><span data-stu-id="540bb-172">P5</span></span>
- <span data-ttu-id="540bb-173">C0</span><span class="sxs-lookup"><span data-stu-id="540bb-173">C0</span></span>
- <span data-ttu-id="540bb-174">C1</span><span class="sxs-lookup"><span data-stu-id="540bb-174">C1</span></span>
- <span data-ttu-id="540bb-175">Режим</span><span class="sxs-lookup"><span data-stu-id="540bb-175">C2</span></span>
- <span data-ttu-id="540bb-176">Ячейку</span><span class="sxs-lookup"><span data-stu-id="540bb-176">C3</span></span>
- <span data-ttu-id="540bb-177">C4</span><span class="sxs-lookup"><span data-stu-id="540bb-177">C4</span></span>
- <span data-ttu-id="540bb-178">C5</span><span class="sxs-lookup"><span data-stu-id="540bb-178">C5</span></span>
- <span data-ttu-id="540bb-179">C6</span><span class="sxs-lookup"><span data-stu-id="540bb-179">C6</span></span>
- <span data-ttu-id="540bb-180">250MB</span><span class="sxs-lookup"><span data-stu-id="540bb-180">250MB</span></span>
- <span data-ttu-id="540bb-181">Гбайт</span><span class="sxs-lookup"><span data-stu-id="540bb-181">1GB</span></span>
- <span data-ttu-id="540bb-182">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="540bb-182">2.5GB</span></span>
- <span data-ttu-id="540bb-183">6GB</span><span class="sxs-lookup"><span data-stu-id="540bb-183">6GB</span></span>
- <span data-ttu-id="540bb-184">13GB</span><span class="sxs-lookup"><span data-stu-id="540bb-184">13GB</span></span>
- <span data-ttu-id="540bb-185">26GB</span><span class="sxs-lookup"><span data-stu-id="540bb-185">26GB</span></span>
- <span data-ttu-id="540bb-186">53GB</span><span class="sxs-lookup"><span data-stu-id="540bb-186">53GB</span></span>
- <span data-ttu-id="540bb-187">120 ГБ значение по умолчанию — 1 ГБ или C1.</span><span class="sxs-lookup"><span data-stu-id="540bb-187">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="540bb-188">-SKU</span><span class="sxs-lookup"><span data-stu-id="540bb-188">-Sku</span></span>
<span data-ttu-id="540bb-189">Указывает SKU кэша Redis для создания.</span><span class="sxs-lookup"><span data-stu-id="540bb-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="540bb-190">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="540bb-190">Valid values are:</span></span> 
- <span data-ttu-id="540bb-191">Базового</span><span class="sxs-lookup"><span data-stu-id="540bb-191">Basic</span></span>
- <span data-ttu-id="540bb-192">Стандартная</span><span class="sxs-lookup"><span data-stu-id="540bb-192">Standard</span></span>
- <span data-ttu-id="540bb-193">Premium по умолчанию используется значение Standard.</span><span class="sxs-lookup"><span data-stu-id="540bb-193">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="540bb-194">-Тег</span><span class="sxs-lookup"><span data-stu-id="540bb-194">-Tag</span></span>
<span data-ttu-id="540bb-195">Хэш-таблица, представляющая Теги.</span><span class="sxs-lookup"><span data-stu-id="540bb-195">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="540bb-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="540bb-196">-TenantSettings</span></span>
<span data-ttu-id="540bb-197">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="540bb-197">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="540bb-198">-Confirm</span><span class="sxs-lookup"><span data-stu-id="540bb-198">-Confirm</span></span>
<span data-ttu-id="540bb-199">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="540bb-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="540bb-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="540bb-200">-WhatIf</span></span>
<span data-ttu-id="540bb-201">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="540bb-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="540bb-202">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="540bb-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="540bb-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="540bb-203">CommonParameters</span></span>
<span data-ttu-id="540bb-204">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="540bb-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="540bb-205">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="540bb-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="540bb-206">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="540bb-206">INPUTS</span></span>

### <span data-ttu-id="540bb-207">System. String</span><span class="sxs-lookup"><span data-stu-id="540bb-207">System.String</span></span>

### <span data-ttu-id="540bb-208">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="540bb-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="540bb-209">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="540bb-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="540bb-210">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="540bb-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="540bb-211">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="540bb-211">OUTPUTS</span></span>

### <span data-ttu-id="540bb-212">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="540bb-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="540bb-213">Пуск</span><span class="sxs-lookup"><span data-stu-id="540bb-213">NOTES</span></span>

## <span data-ttu-id="540bb-214">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="540bb-214">RELATED LINKS</span></span>

[<span data-ttu-id="540bb-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="540bb-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="540bb-216">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="540bb-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="540bb-217">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="540bb-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

