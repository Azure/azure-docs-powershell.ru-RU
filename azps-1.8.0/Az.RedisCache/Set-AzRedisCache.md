---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 637a1e634b0f8b6f890519bf4865378f50774e39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729525"
---
# <span data-ttu-id="6cbd3-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6cbd3-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="6cbd3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6cbd3-102">SYNOPSIS</span></span>
<span data-ttu-id="6cbd3-103">Изменяет кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="6cbd3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6cbd3-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6cbd3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cbd3-105">DESCRIPTION</span></span>
<span data-ttu-id="6cbd3-106">Командлет **Set-AzRedisCache** изменяет кэш Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="6cbd3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6cbd3-107">EXAMPLES</span></span>

### <span data-ttu-id="6cbd3-108">Пример 1: изменение кэша Redis</span><span class="sxs-lookup"><span data-stu-id="6cbd3-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="6cbd3-109">Эта команда обновляет MaxMemory-политику для кэша Redis с именем MyCache.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="6cbd3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6cbd3-110">PARAMETERS</span></span>

### <span data-ttu-id="6cbd3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cbd3-111">-DefaultProfile</span></span>
<span data-ttu-id="6cbd3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cbd3-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="6cbd3-113">-EnableNonSslPort</span></span>
<span data-ttu-id="6cbd3-114">Указывает, включен ли порт без SSL.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="6cbd3-115">Значение по умолчанию — $False (порт без SSL отключен).</span><span class="sxs-lookup"><span data-stu-id="6cbd3-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="6cbd3-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6cbd3-116">-Name</span></span>
<span data-ttu-id="6cbd3-117">Указывает имя кэша Redis, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="6cbd3-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="6cbd3-118">-RedisConfiguration</span></span>
<span data-ttu-id="6cbd3-119">Задает параметры конфигурации Redis.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="6cbd3-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6cbd3-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6cbd3-121">RDB — включена резервная копия.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="6cbd3-122">Указывает на то, что сохраняемость данных Redis включена.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="6cbd3-123">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-123">Premium tier only.</span></span>
- <span data-ttu-id="6cbd3-124">RDB — строка подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="6cbd3-125">Задает строку подключения к учетной записи хранения для Redis сохраняемости данных.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="6cbd3-126">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-126">Premium tier only.</span></span>
- <span data-ttu-id="6cbd3-127">RDB — периодичность резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="6cbd3-128">Указывает периодичность резервного копирования для сохраняемости данных Redis.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="6cbd3-129">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-129">Premium tier only.</span></span> 
- <span data-ttu-id="6cbd3-130">MaxMemory — зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-130">maxmemory-reserved.</span></span>
<span data-ttu-id="6cbd3-131">Настраивает память, зарезервированную для процессов без кэширования.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="6cbd3-132">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cbd3-133">MaxMemory — политика.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-133">maxmemory-policy.</span></span>
<span data-ttu-id="6cbd3-134">Настройка политики вытеснения для кэша.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="6cbd3-135">Все ценовые категории.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-135">All pricing tiers.</span></span> 
- <span data-ttu-id="6cbd3-136">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-136">notify-keyspace-events.</span></span>
<span data-ttu-id="6cbd3-137">Настраивает уведомления keyspace.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="6cbd3-138">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="6cbd3-139">хэш-максимум-ziplist-записи.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="6cbd3-140">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6cbd3-141">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cbd3-142">hash-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="6cbd3-143">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6cbd3-144">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cbd3-145">Set-Max-intset-"записи".</span><span class="sxs-lookup"><span data-stu-id="6cbd3-145">set-max-intset-entries.</span></span>
<span data-ttu-id="6cbd3-146">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6cbd3-147">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cbd3-148">zset-Max-ziplist-(записи).</span><span class="sxs-lookup"><span data-stu-id="6cbd3-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="6cbd3-149">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6cbd3-150">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cbd3-151">zset-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="6cbd3-152">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6cbd3-153">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cbd3-154">баз данных.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-154">databases.</span></span>
<span data-ttu-id="6cbd3-155">Настраивает количество баз данных.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-155">Configures the number of databases.</span></span>
<span data-ttu-id="6cbd3-156">Это свойство можно настроить только при создании кэша.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="6cbd3-157">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="6cbd3-158">Дополнительные сведения можно найти в разделе Управление кэшем Redis Azure с помощью Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="6cbd3-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="6cbd3-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cbd3-159">-ResourceGroupName</span></span>
<span data-ttu-id="6cbd3-160">Указывает имя группы ресурсов, которая содержит кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="6cbd3-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="6cbd3-161">-ShardCount</span></span>
<span data-ttu-id="6cbd3-162">Задает количество сегментов для создания в кэше высококачественных кластеров.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="6cbd3-163">-Size</span><span class="sxs-lookup"><span data-stu-id="6cbd3-163">-Size</span></span>
<span data-ttu-id="6cbd3-164">Задает размер кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="6cbd3-165">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="6cbd3-165">Valid values are:</span></span> 
- <span data-ttu-id="6cbd3-166">P1</span><span class="sxs-lookup"><span data-stu-id="6cbd3-166">P1</span></span>
- <span data-ttu-id="6cbd3-167">–</span><span class="sxs-lookup"><span data-stu-id="6cbd3-167">P2</span></span>
- <span data-ttu-id="6cbd3-168">–</span><span class="sxs-lookup"><span data-stu-id="6cbd3-168">P3</span></span>
- <span data-ttu-id="6cbd3-169">P4</span><span class="sxs-lookup"><span data-stu-id="6cbd3-169">P4</span></span>
- <span data-ttu-id="6cbd3-170">C0</span><span class="sxs-lookup"><span data-stu-id="6cbd3-170">C0</span></span>
- <span data-ttu-id="6cbd3-171">C1</span><span class="sxs-lookup"><span data-stu-id="6cbd3-171">C1</span></span>
- <span data-ttu-id="6cbd3-172">Режим</span><span class="sxs-lookup"><span data-stu-id="6cbd3-172">C2</span></span>
- <span data-ttu-id="6cbd3-173">Ячейку</span><span class="sxs-lookup"><span data-stu-id="6cbd3-173">C3</span></span>
- <span data-ttu-id="6cbd3-174">C4</span><span class="sxs-lookup"><span data-stu-id="6cbd3-174">C4</span></span>
- <span data-ttu-id="6cbd3-175">C5</span><span class="sxs-lookup"><span data-stu-id="6cbd3-175">C5</span></span>
- <span data-ttu-id="6cbd3-176">C6</span><span class="sxs-lookup"><span data-stu-id="6cbd3-176">C6</span></span>
- <span data-ttu-id="6cbd3-177">250MB</span><span class="sxs-lookup"><span data-stu-id="6cbd3-177">250MB</span></span>
- <span data-ttu-id="6cbd3-178">Гбайт</span><span class="sxs-lookup"><span data-stu-id="6cbd3-178">1GB</span></span>
- <span data-ttu-id="6cbd3-179">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="6cbd3-179">2.5GB</span></span>
- <span data-ttu-id="6cbd3-180">6GB</span><span class="sxs-lookup"><span data-stu-id="6cbd3-180">6GB</span></span>
- <span data-ttu-id="6cbd3-181">13GB</span><span class="sxs-lookup"><span data-stu-id="6cbd3-181">13GB</span></span>
- <span data-ttu-id="6cbd3-182">26GB</span><span class="sxs-lookup"><span data-stu-id="6cbd3-182">26GB</span></span>
- <span data-ttu-id="6cbd3-183">53GB значение по умолчанию — 1 ГБ или C1.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-183">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="6cbd3-184">-SKU</span><span class="sxs-lookup"><span data-stu-id="6cbd3-184">-Sku</span></span>
<span data-ttu-id="6cbd3-185">Указывает SKU кэша Redis для создания.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-185">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="6cbd3-186">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="6cbd3-186">Valid values are:</span></span> 
- <span data-ttu-id="6cbd3-187">Базового</span><span class="sxs-lookup"><span data-stu-id="6cbd3-187">Basic</span></span>
- <span data-ttu-id="6cbd3-188">Стандартная</span><span class="sxs-lookup"><span data-stu-id="6cbd3-188">Standard</span></span>
- <span data-ttu-id="6cbd3-189">Premium по умолчанию используется значение Standard.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-189">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="6cbd3-190">-Тег</span><span class="sxs-lookup"><span data-stu-id="6cbd3-190">-Tag</span></span>
<span data-ttu-id="6cbd3-191">Хэш-таблица, представляющая Теги.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-191">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="6cbd3-192">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="6cbd3-192">-TenantSettings</span></span>
<span data-ttu-id="6cbd3-193">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-193">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="6cbd3-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cbd3-194">-Confirm</span></span>
<span data-ttu-id="6cbd3-195">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cbd3-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cbd3-196">-WhatIf</span></span>
<span data-ttu-id="6cbd3-197">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-197">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6cbd3-198">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cbd3-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cbd3-199">CommonParameters</span></span>
<span data-ttu-id="6cbd3-200">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6cbd3-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cbd3-201">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cbd3-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cbd3-202">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6cbd3-202">INPUTS</span></span>

### <span data-ttu-id="6cbd3-203">System. String</span><span class="sxs-lookup"><span data-stu-id="6cbd3-203">System.String</span></span>

### <span data-ttu-id="6cbd3-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6cbd3-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6cbd3-205">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6cbd3-205">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6cbd3-206">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6cbd3-206">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6cbd3-207">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cbd3-207">OUTPUTS</span></span>

### <span data-ttu-id="6cbd3-208">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="6cbd3-208">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="6cbd3-209">Пуск</span><span class="sxs-lookup"><span data-stu-id="6cbd3-209">NOTES</span></span>

## <span data-ttu-id="6cbd3-210">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cbd3-210">RELATED LINKS</span></span>

[<span data-ttu-id="6cbd3-211">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6cbd3-211">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="6cbd3-212">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6cbd3-212">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="6cbd3-213">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6cbd3-213">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


