---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 951198c93918c08f69f28dc6db3c5fe605e6d3bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563359"
---
# <span data-ttu-id="fef09-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fef09-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="fef09-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fef09-102">SYNOPSIS</span></span>
<span data-ttu-id="fef09-103">Изменяет кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="fef09-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fef09-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fef09-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fef09-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fef09-105">DESCRIPTION</span></span>
<span data-ttu-id="fef09-106">Командлет **Set-AzureRmRedisCache** изменяет кэш Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="fef09-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="fef09-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fef09-107">EXAMPLES</span></span>

### <span data-ttu-id="fef09-108">Пример 1: изменение кэша Redis</span><span class="sxs-lookup"><span data-stu-id="fef09-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

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

<span data-ttu-id="fef09-109">Эта команда обновляет MaxMemory-политику для кэша Redis с именем MyCache.</span><span class="sxs-lookup"><span data-stu-id="fef09-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="fef09-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fef09-110">PARAMETERS</span></span>

### <span data-ttu-id="fef09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef09-111">-DefaultProfile</span></span>
<span data-ttu-id="fef09-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fef09-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef09-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="fef09-113">-EnableNonSslPort</span></span>
<span data-ttu-id="fef09-114">Указывает, включен ли порт без SSL.</span><span class="sxs-lookup"><span data-stu-id="fef09-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="fef09-115">Значение по умолчанию — $False (порт без SSL отключен).</span><span class="sxs-lookup"><span data-stu-id="fef09-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef09-116">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="fef09-116">-MaxMemoryPolicy</span></span>
<span data-ttu-id="fef09-117">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="fef09-117">This parameter has been deprecated.</span></span>
<span data-ttu-id="fef09-118">Для задания MaxMemory-Policy используйте параметр *RedisConfiguration* .</span><span class="sxs-lookup"><span data-stu-id="fef09-118">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="fef09-119">Например:</span><span class="sxs-lookup"><span data-stu-id="fef09-119">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef09-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fef09-120">-Name</span></span>
<span data-ttu-id="fef09-121">Указывает имя кэша Redis, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="fef09-121">Specifies the name of the Redis Cache to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef09-122">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="fef09-122">-RedisConfiguration</span></span>
<span data-ttu-id="fef09-123">Задает параметры конфигурации Redis.</span><span class="sxs-lookup"><span data-stu-id="fef09-123">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="fef09-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fef09-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fef09-125">RDB — включена резервная копия.</span><span class="sxs-lookup"><span data-stu-id="fef09-125">rdb-backup-enabled.</span></span>
<span data-ttu-id="fef09-126">Указывает на то, что сохраняемость данных Redis включена.</span><span class="sxs-lookup"><span data-stu-id="fef09-126">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="fef09-127">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="fef09-127">Premium tier only.</span></span>
- <span data-ttu-id="fef09-128">RDB — строка подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="fef09-128">rdb-storage-connection-string.</span></span>
<span data-ttu-id="fef09-129">Задает строку подключения к учетной записи хранения для Redis сохраняемости данных.</span><span class="sxs-lookup"><span data-stu-id="fef09-129">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="fef09-130">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="fef09-130">Premium tier only.</span></span>
- <span data-ttu-id="fef09-131">RDB — периодичность резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="fef09-131">rdb-backup-frequency.</span></span>
<span data-ttu-id="fef09-132">Указывает периодичность резервного копирования для сохраняемости данных Redis.</span><span class="sxs-lookup"><span data-stu-id="fef09-132">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="fef09-133">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="fef09-133">Premium tier only.</span></span> 
- <span data-ttu-id="fef09-134">MaxMemory — зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="fef09-134">maxmemory-reserved.</span></span>
<span data-ttu-id="fef09-135">Настраивает память, зарезервированную для процессов без кэширования.</span><span class="sxs-lookup"><span data-stu-id="fef09-135">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="fef09-136">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="fef09-136">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="fef09-137">MaxMemory — политика.</span><span class="sxs-lookup"><span data-stu-id="fef09-137">maxmemory-policy.</span></span>
<span data-ttu-id="fef09-138">Настройка политики вытеснения для кэша.</span><span class="sxs-lookup"><span data-stu-id="fef09-138">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="fef09-139">Все ценовые категории.</span><span class="sxs-lookup"><span data-stu-id="fef09-139">All pricing tiers.</span></span> 
- <span data-ttu-id="fef09-140">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="fef09-140">notify-keyspace-events.</span></span>
<span data-ttu-id="fef09-141">Настраивает уведомления keyspace.</span><span class="sxs-lookup"><span data-stu-id="fef09-141">Configures keyspace notifications.</span></span>
<span data-ttu-id="fef09-142">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="fef09-142">Standard and premium tiers.</span></span> 
- <span data-ttu-id="fef09-143">хэш-максимум-ziplist-записи.</span><span class="sxs-lookup"><span data-stu-id="fef09-143">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="fef09-144">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="fef09-144">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="fef09-145">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="fef09-145">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="fef09-146">hash-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="fef09-146">hash-max-ziplist-value.</span></span>
<span data-ttu-id="fef09-147">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="fef09-147">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="fef09-148">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="fef09-148">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="fef09-149">Set-Max-intset-"записи".</span><span class="sxs-lookup"><span data-stu-id="fef09-149">set-max-intset-entries.</span></span>
<span data-ttu-id="fef09-150">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="fef09-150">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="fef09-151">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="fef09-151">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="fef09-152">zset-Max-ziplist-(записи).</span><span class="sxs-lookup"><span data-stu-id="fef09-152">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="fef09-153">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="fef09-153">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="fef09-154">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="fef09-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="fef09-155">zset-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="fef09-155">zset-max-ziplist-value.</span></span>
<span data-ttu-id="fef09-156">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="fef09-156">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="fef09-157">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="fef09-157">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="fef09-158">баз данных.</span><span class="sxs-lookup"><span data-stu-id="fef09-158">databases.</span></span>
<span data-ttu-id="fef09-159">Настраивает количество баз данных.</span><span class="sxs-lookup"><span data-stu-id="fef09-159">Configures the number of databases.</span></span>
<span data-ttu-id="fef09-160">Это свойство можно настроить только при создании кэша.</span><span class="sxs-lookup"><span data-stu-id="fef09-160">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="fef09-161">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="fef09-161">Standard and Premium tiers.</span></span>

<span data-ttu-id="fef09-162">Дополнительные сведения можно найти в разделе Управление кэшем Redis Azure с помощью Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="fef09-162">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef09-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fef09-163">-ResourceGroupName</span></span>
<span data-ttu-id="fef09-164">Указывает имя группы ресурсов, которая содержит кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="fef09-164">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef09-165">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="fef09-165">-ShardCount</span></span>
<span data-ttu-id="fef09-166">Задает количество сегментов для создания в кэше высококачественных кластеров.</span><span class="sxs-lookup"><span data-stu-id="fef09-166">Specifies the number of shards to create on a Premium cluster cache.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef09-167">-Size</span><span class="sxs-lookup"><span data-stu-id="fef09-167">-Size</span></span>
<span data-ttu-id="fef09-168">Задает размер кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="fef09-168">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="fef09-169">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="fef09-169">Valid values are:</span></span> 

- <span data-ttu-id="fef09-170">P1</span><span class="sxs-lookup"><span data-stu-id="fef09-170">P1</span></span>
- <span data-ttu-id="fef09-171">–</span><span class="sxs-lookup"><span data-stu-id="fef09-171">P2</span></span>
- <span data-ttu-id="fef09-172">–</span><span class="sxs-lookup"><span data-stu-id="fef09-172">P3</span></span>
- <span data-ttu-id="fef09-173">P4</span><span class="sxs-lookup"><span data-stu-id="fef09-173">P4</span></span>
- <span data-ttu-id="fef09-174">C0</span><span class="sxs-lookup"><span data-stu-id="fef09-174">C0</span></span>
- <span data-ttu-id="fef09-175">C1</span><span class="sxs-lookup"><span data-stu-id="fef09-175">C1</span></span>
- <span data-ttu-id="fef09-176">Режим</span><span class="sxs-lookup"><span data-stu-id="fef09-176">C2</span></span>
- <span data-ttu-id="fef09-177">Ячейку</span><span class="sxs-lookup"><span data-stu-id="fef09-177">C3</span></span>
- <span data-ttu-id="fef09-178">C4</span><span class="sxs-lookup"><span data-stu-id="fef09-178">C4</span></span>
- <span data-ttu-id="fef09-179">C5</span><span class="sxs-lookup"><span data-stu-id="fef09-179">C5</span></span>
- <span data-ttu-id="fef09-180">C6</span><span class="sxs-lookup"><span data-stu-id="fef09-180">C6</span></span>
- <span data-ttu-id="fef09-181">250MB</span><span class="sxs-lookup"><span data-stu-id="fef09-181">250MB</span></span>
- <span data-ttu-id="fef09-182">Гбайт</span><span class="sxs-lookup"><span data-stu-id="fef09-182">1GB</span></span>
- <span data-ttu-id="fef09-183">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="fef09-183">2.5GB</span></span>
- <span data-ttu-id="fef09-184">6GB</span><span class="sxs-lookup"><span data-stu-id="fef09-184">6GB</span></span>
- <span data-ttu-id="fef09-185">13GB</span><span class="sxs-lookup"><span data-stu-id="fef09-185">13GB</span></span>
- <span data-ttu-id="fef09-186">26GB</span><span class="sxs-lookup"><span data-stu-id="fef09-186">26GB</span></span>
- <span data-ttu-id="fef09-187">53GB</span><span class="sxs-lookup"><span data-stu-id="fef09-187">53GB</span></span>

<span data-ttu-id="fef09-188">Значение по умолчанию — 1 ГБ или C1.</span><span class="sxs-lookup"><span data-stu-id="fef09-188">The default value is 1GB or C1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef09-189">-SKU</span><span class="sxs-lookup"><span data-stu-id="fef09-189">-Sku</span></span>
<span data-ttu-id="fef09-190">Указывает SKU кэша Redis для создания.</span><span class="sxs-lookup"><span data-stu-id="fef09-190">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="fef09-191">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="fef09-191">Valid values are:</span></span> 

- <span data-ttu-id="fef09-192">Базового</span><span class="sxs-lookup"><span data-stu-id="fef09-192">Basic</span></span>
- <span data-ttu-id="fef09-193">Стандартная</span><span class="sxs-lookup"><span data-stu-id="fef09-193">Standard</span></span>
- <span data-ttu-id="fef09-194">Версию</span><span class="sxs-lookup"><span data-stu-id="fef09-194">Premium</span></span>

<span data-ttu-id="fef09-195">По умолчанию используется значение Standard.</span><span class="sxs-lookup"><span data-stu-id="fef09-195">The default value is Standard.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef09-196">-Тег</span><span class="sxs-lookup"><span data-stu-id="fef09-196">-Tag</span></span>
<span data-ttu-id="fef09-197">Хэш-таблица, представляющая Теги.</span><span class="sxs-lookup"><span data-stu-id="fef09-197">A hash table which represents tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef09-198">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="fef09-198">-TenantSettings</span></span>
<span data-ttu-id="fef09-199">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="fef09-199">This parameter has been deprecated.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef09-200">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fef09-200">-Confirm</span></span>
<span data-ttu-id="fef09-201">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fef09-201">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef09-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fef09-202">-WhatIf</span></span>
<span data-ttu-id="fef09-203">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fef09-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fef09-204">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fef09-204">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef09-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef09-205">CommonParameters</span></span>
<span data-ttu-id="fef09-206">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fef09-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef09-207">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fef09-207">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef09-208">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fef09-208">INPUTS</span></span>

### <span data-ttu-id="fef09-209">Ничего</span><span class="sxs-lookup"><span data-stu-id="fef09-209">None</span></span>
<span data-ttu-id="fef09-210">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="fef09-210">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="fef09-211">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fef09-211">OUTPUTS</span></span>

### <span data-ttu-id="fef09-212">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="fef09-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="fef09-213">Возвращает все атрибуты кэша Redis, включая первичные и вторичные ключи доступа.</span><span class="sxs-lookup"><span data-stu-id="fef09-213">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="fef09-214">Пуск</span><span class="sxs-lookup"><span data-stu-id="fef09-214">NOTES</span></span>

## <span data-ttu-id="fef09-215">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fef09-215">RELATED LINKS</span></span>

[<span data-ttu-id="fef09-216">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fef09-216">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="fef09-217">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fef09-217">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="fef09-218">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fef09-218">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


