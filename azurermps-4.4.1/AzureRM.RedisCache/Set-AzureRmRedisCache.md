---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: bac4176671f5583072142b5973d12bc62205a0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562235"
---
# <span data-ttu-id="edd87-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="edd87-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="edd87-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="edd87-102">SYNOPSIS</span></span>
<span data-ttu-id="edd87-103">Изменяет кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="edd87-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edd87-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="edd87-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="edd87-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="edd87-105">DESCRIPTION</span></span>
<span data-ttu-id="edd87-106">Командлет **Set-AzureRmRedisCache** изменяет кэш Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="edd87-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="edd87-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="edd87-107">EXAMPLES</span></span>

### <span data-ttu-id="edd87-108">Пример 1: изменение кэша Redis</span><span class="sxs-lookup"><span data-stu-id="edd87-108">Example 1: Modify a Redis Cache</span></span>
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
```

<span data-ttu-id="edd87-109">Эта команда обновляет MaxMemory-политику для кэша Redis с именем MyCache.</span><span class="sxs-lookup"><span data-stu-id="edd87-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="edd87-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="edd87-110">PARAMETERS</span></span>

### <span data-ttu-id="edd87-111">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="edd87-111">-EnableNonSslPort</span></span>
<span data-ttu-id="edd87-112">Указывает, включен ли порт без SSL.</span><span class="sxs-lookup"><span data-stu-id="edd87-112">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="edd87-113">Значение по умолчанию — $False (порт без SSL отключен).</span><span class="sxs-lookup"><span data-stu-id="edd87-113">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="edd87-114">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="edd87-114">-MaxMemoryPolicy</span></span>
<span data-ttu-id="edd87-115">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="edd87-115">This parameter has been deprecated.</span></span>
<span data-ttu-id="edd87-116">Для задания MaxMemory-Policy используйте параметр *RedisConfiguration* .</span><span class="sxs-lookup"><span data-stu-id="edd87-116">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="edd87-117">Например:</span><span class="sxs-lookup"><span data-stu-id="edd87-117">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

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

### <span data-ttu-id="edd87-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="edd87-118">-Name</span></span>
<span data-ttu-id="edd87-119">Указывает имя кэша Redis, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="edd87-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="edd87-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="edd87-120">-RedisConfiguration</span></span>
<span data-ttu-id="edd87-121">Задает параметры конфигурации Redis.</span><span class="sxs-lookup"><span data-stu-id="edd87-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="edd87-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="edd87-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="edd87-123">RDB — включена резервная копия.</span><span class="sxs-lookup"><span data-stu-id="edd87-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="edd87-124">Указывает на то, что сохраняемость данных Redis включена.</span><span class="sxs-lookup"><span data-stu-id="edd87-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="edd87-125">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="edd87-125">Premium tier only.</span></span>
- <span data-ttu-id="edd87-126">RDB — строка подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="edd87-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="edd87-127">Задает строку подключения к учетной записи хранения для Redis сохраняемости данных.</span><span class="sxs-lookup"><span data-stu-id="edd87-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="edd87-128">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="edd87-128">Premium tier only.</span></span>
- <span data-ttu-id="edd87-129">RDB — периодичность резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="edd87-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="edd87-130">Указывает периодичность резервного копирования для сохраняемости данных Redis.</span><span class="sxs-lookup"><span data-stu-id="edd87-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="edd87-131">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="edd87-131">Premium tier only.</span></span> 
- <span data-ttu-id="edd87-132">MaxMemory — зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="edd87-132">maxmemory-reserved.</span></span>
<span data-ttu-id="edd87-133">Настраивает память, зарезервированную для процессов без кэширования.</span><span class="sxs-lookup"><span data-stu-id="edd87-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="edd87-134">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="edd87-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="edd87-135">MaxMemory — политика.</span><span class="sxs-lookup"><span data-stu-id="edd87-135">maxmemory-policy.</span></span>
<span data-ttu-id="edd87-136">Настройка политики вытеснения для кэша.</span><span class="sxs-lookup"><span data-stu-id="edd87-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="edd87-137">Все ценовые категории.</span><span class="sxs-lookup"><span data-stu-id="edd87-137">All pricing tiers.</span></span> 
- <span data-ttu-id="edd87-138">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="edd87-138">notify-keyspace-events.</span></span>
<span data-ttu-id="edd87-139">Настраивает уведомления keyspace.</span><span class="sxs-lookup"><span data-stu-id="edd87-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="edd87-140">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="edd87-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="edd87-141">хэш-максимум-ziplist-записи.</span><span class="sxs-lookup"><span data-stu-id="edd87-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="edd87-142">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="edd87-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="edd87-143">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="edd87-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="edd87-144">hash-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="edd87-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="edd87-145">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="edd87-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="edd87-146">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="edd87-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="edd87-147">Set-Max-intset-"записи".</span><span class="sxs-lookup"><span data-stu-id="edd87-147">set-max-intset-entries.</span></span>
<span data-ttu-id="edd87-148">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="edd87-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="edd87-149">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="edd87-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="edd87-150">zset-Max-ziplist-(записи).</span><span class="sxs-lookup"><span data-stu-id="edd87-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="edd87-151">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="edd87-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="edd87-152">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="edd87-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="edd87-153">zset-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="edd87-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="edd87-154">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="edd87-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="edd87-155">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="edd87-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="edd87-156">баз данных.</span><span class="sxs-lookup"><span data-stu-id="edd87-156">databases.</span></span>
<span data-ttu-id="edd87-157">Настраивает количество баз данных.</span><span class="sxs-lookup"><span data-stu-id="edd87-157">Configures the number of databases.</span></span>
<span data-ttu-id="edd87-158">Это свойство можно настроить только при создании кэша.</span><span class="sxs-lookup"><span data-stu-id="edd87-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="edd87-159">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="edd87-159">Standard and Premium tiers.</span></span>

<span data-ttu-id="edd87-160">Дополнительные сведения можно найти в разделе Управление кэшем Redis Azure с помощью Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="edd87-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="edd87-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edd87-161">-ResourceGroupName</span></span>
<span data-ttu-id="edd87-162">Указывает имя группы ресурсов, которая содержит кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="edd87-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="edd87-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="edd87-163">-ShardCount</span></span>
<span data-ttu-id="edd87-164">Задает количество сегментов для создания в кэше высококачественных кластеров.</span><span class="sxs-lookup"><span data-stu-id="edd87-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="edd87-165">-Size</span><span class="sxs-lookup"><span data-stu-id="edd87-165">-Size</span></span>
<span data-ttu-id="edd87-166">Задает размер кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="edd87-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="edd87-167">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="edd87-167">Valid values are:</span></span> 

- <span data-ttu-id="edd87-168">P1</span><span class="sxs-lookup"><span data-stu-id="edd87-168">P1</span></span>
- <span data-ttu-id="edd87-169">–</span><span class="sxs-lookup"><span data-stu-id="edd87-169">P2</span></span>
- <span data-ttu-id="edd87-170">–</span><span class="sxs-lookup"><span data-stu-id="edd87-170">P3</span></span>
- <span data-ttu-id="edd87-171">P4</span><span class="sxs-lookup"><span data-stu-id="edd87-171">P4</span></span>
- <span data-ttu-id="edd87-172">C0</span><span class="sxs-lookup"><span data-stu-id="edd87-172">C0</span></span>
- <span data-ttu-id="edd87-173">C1</span><span class="sxs-lookup"><span data-stu-id="edd87-173">C1</span></span>
- <span data-ttu-id="edd87-174">Режим</span><span class="sxs-lookup"><span data-stu-id="edd87-174">C2</span></span>
- <span data-ttu-id="edd87-175">Ячейку</span><span class="sxs-lookup"><span data-stu-id="edd87-175">C3</span></span>
- <span data-ttu-id="edd87-176">C4</span><span class="sxs-lookup"><span data-stu-id="edd87-176">C4</span></span>
- <span data-ttu-id="edd87-177">C5</span><span class="sxs-lookup"><span data-stu-id="edd87-177">C5</span></span>
- <span data-ttu-id="edd87-178">C6</span><span class="sxs-lookup"><span data-stu-id="edd87-178">C6</span></span>
- <span data-ttu-id="edd87-179">250MB</span><span class="sxs-lookup"><span data-stu-id="edd87-179">250MB</span></span>
- <span data-ttu-id="edd87-180">Гбайт</span><span class="sxs-lookup"><span data-stu-id="edd87-180">1GB</span></span>
- <span data-ttu-id="edd87-181">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="edd87-181">2.5GB</span></span>
- <span data-ttu-id="edd87-182">6GB</span><span class="sxs-lookup"><span data-stu-id="edd87-182">6GB</span></span>
- <span data-ttu-id="edd87-183">13GB</span><span class="sxs-lookup"><span data-stu-id="edd87-183">13GB</span></span>
- <span data-ttu-id="edd87-184">26GB</span><span class="sxs-lookup"><span data-stu-id="edd87-184">26GB</span></span>
- <span data-ttu-id="edd87-185">53GB</span><span class="sxs-lookup"><span data-stu-id="edd87-185">53GB</span></span>

<span data-ttu-id="edd87-186">Значение по умолчанию — 1 ГБ или C1.</span><span class="sxs-lookup"><span data-stu-id="edd87-186">The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edd87-187">-SKU</span><span class="sxs-lookup"><span data-stu-id="edd87-187">-Sku</span></span>
<span data-ttu-id="edd87-188">Указывает SKU кэша Redis для создания.</span><span class="sxs-lookup"><span data-stu-id="edd87-188">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="edd87-189">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="edd87-189">Valid values are:</span></span> 

- <span data-ttu-id="edd87-190">Базового</span><span class="sxs-lookup"><span data-stu-id="edd87-190">Basic</span></span>
- <span data-ttu-id="edd87-191">Стандартная</span><span class="sxs-lookup"><span data-stu-id="edd87-191">Standard</span></span>
- <span data-ttu-id="edd87-192">Версию</span><span class="sxs-lookup"><span data-stu-id="edd87-192">Premium</span></span>

<span data-ttu-id="edd87-193">По умолчанию используется значение Standard.</span><span class="sxs-lookup"><span data-stu-id="edd87-193">The default value is Standard.</span></span>

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

### <span data-ttu-id="edd87-194">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="edd87-194">-TenantSettings</span></span>
<span data-ttu-id="edd87-195">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="edd87-195">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="edd87-196">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd87-196">-DefaultProfile</span></span>
<span data-ttu-id="edd87-197">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="edd87-197">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edd87-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd87-198">CommonParameters</span></span>
<span data-ttu-id="edd87-199">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="edd87-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd87-200">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edd87-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd87-201">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="edd87-201">INPUTS</span></span>

### <span data-ttu-id="edd87-202">Ничего</span><span class="sxs-lookup"><span data-stu-id="edd87-202">None</span></span>
<span data-ttu-id="edd87-203">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="edd87-203">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="edd87-204">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="edd87-204">OUTPUTS</span></span>

### <span data-ttu-id="edd87-205">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="edd87-205">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="edd87-206">Возвращает все атрибуты кэша Redis, включая первичные и вторичные ключи доступа.</span><span class="sxs-lookup"><span data-stu-id="edd87-206">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="edd87-207">Пуск</span><span class="sxs-lookup"><span data-stu-id="edd87-207">NOTES</span></span>

## <span data-ttu-id="edd87-208">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="edd87-208">RELATED LINKS</span></span>

[<span data-ttu-id="edd87-209">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="edd87-209">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="edd87-210">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="edd87-210">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="edd87-211">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="edd87-211">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


