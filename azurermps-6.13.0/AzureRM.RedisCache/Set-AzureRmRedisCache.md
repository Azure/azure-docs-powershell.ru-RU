---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 484c72dd77ada862536b064cb2bcaec07ef51bb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568415"
---
# <span data-ttu-id="518e1-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="518e1-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="518e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="518e1-102">SYNOPSIS</span></span>
<span data-ttu-id="518e1-103">Изменяет кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="518e1-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="518e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="518e1-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="518e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="518e1-105">DESCRIPTION</span></span>
<span data-ttu-id="518e1-106">Командлет **Set-AzureRmRedisCache** изменяет кэш Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="518e1-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="518e1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="518e1-107">EXAMPLES</span></span>

### <span data-ttu-id="518e1-108">Пример 1: изменение кэша Redis</span><span class="sxs-lookup"><span data-stu-id="518e1-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="518e1-109">Эта команда обновляет MaxMemory-политику для кэша Redis с именем MyCache.</span><span class="sxs-lookup"><span data-stu-id="518e1-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="518e1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="518e1-110">PARAMETERS</span></span>

### <span data-ttu-id="518e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="518e1-111">-DefaultProfile</span></span>
<span data-ttu-id="518e1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="518e1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="518e1-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="518e1-113">-EnableNonSslPort</span></span>
<span data-ttu-id="518e1-114">Указывает, включен ли порт без SSL.</span><span class="sxs-lookup"><span data-stu-id="518e1-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="518e1-115">Значение по умолчанию — $False (порт без SSL отключен).</span><span class="sxs-lookup"><span data-stu-id="518e1-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="518e1-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="518e1-116">-Name</span></span>
<span data-ttu-id="518e1-117">Указывает имя кэша Redis, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="518e1-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="518e1-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="518e1-118">-RedisConfiguration</span></span>
<span data-ttu-id="518e1-119">Задает параметры конфигурации Redis.</span><span class="sxs-lookup"><span data-stu-id="518e1-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="518e1-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="518e1-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="518e1-121">RDB — включена резервная копия.</span><span class="sxs-lookup"><span data-stu-id="518e1-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="518e1-122">Указывает на то, что сохраняемость данных Redis включена.</span><span class="sxs-lookup"><span data-stu-id="518e1-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="518e1-123">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="518e1-123">Premium tier only.</span></span>
- <span data-ttu-id="518e1-124">RDB — строка подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="518e1-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="518e1-125">Задает строку подключения к учетной записи хранения для Redis сохраняемости данных.</span><span class="sxs-lookup"><span data-stu-id="518e1-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="518e1-126">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="518e1-126">Premium tier only.</span></span>
- <span data-ttu-id="518e1-127">RDB — периодичность резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="518e1-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="518e1-128">Указывает периодичность резервного копирования для сохраняемости данных Redis.</span><span class="sxs-lookup"><span data-stu-id="518e1-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="518e1-129">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="518e1-129">Premium tier only.</span></span> 
- <span data-ttu-id="518e1-130">MaxMemory — зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="518e1-130">maxmemory-reserved.</span></span>
<span data-ttu-id="518e1-131">Настраивает память, зарезервированную для процессов без кэширования.</span><span class="sxs-lookup"><span data-stu-id="518e1-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="518e1-132">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="518e1-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="518e1-133">MaxMemory — политика.</span><span class="sxs-lookup"><span data-stu-id="518e1-133">maxmemory-policy.</span></span>
<span data-ttu-id="518e1-134">Настройка политики вытеснения для кэша.</span><span class="sxs-lookup"><span data-stu-id="518e1-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="518e1-135">Все ценовые категории.</span><span class="sxs-lookup"><span data-stu-id="518e1-135">All pricing tiers.</span></span> 
- <span data-ttu-id="518e1-136">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="518e1-136">notify-keyspace-events.</span></span>
<span data-ttu-id="518e1-137">Настраивает уведомления keyspace.</span><span class="sxs-lookup"><span data-stu-id="518e1-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="518e1-138">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="518e1-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="518e1-139">хэш-максимум-ziplist-записи.</span><span class="sxs-lookup"><span data-stu-id="518e1-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="518e1-140">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="518e1-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="518e1-141">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="518e1-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="518e1-142">hash-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="518e1-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="518e1-143">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="518e1-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="518e1-144">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="518e1-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="518e1-145">Set-Max-intset-"записи".</span><span class="sxs-lookup"><span data-stu-id="518e1-145">set-max-intset-entries.</span></span>
<span data-ttu-id="518e1-146">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="518e1-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="518e1-147">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="518e1-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="518e1-148">zset-Max-ziplist-(записи).</span><span class="sxs-lookup"><span data-stu-id="518e1-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="518e1-149">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="518e1-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="518e1-150">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="518e1-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="518e1-151">zset-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="518e1-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="518e1-152">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="518e1-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="518e1-153">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="518e1-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="518e1-154">баз данных.</span><span class="sxs-lookup"><span data-stu-id="518e1-154">databases.</span></span>
<span data-ttu-id="518e1-155">Настраивает количество баз данных.</span><span class="sxs-lookup"><span data-stu-id="518e1-155">Configures the number of databases.</span></span>
<span data-ttu-id="518e1-156">Это свойство можно настроить только при создании кэша.</span><span class="sxs-lookup"><span data-stu-id="518e1-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="518e1-157">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="518e1-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="518e1-158">Дополнительные сведения можно найти в разделе Управление кэшем Redis Azure с помощью Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="518e1-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="518e1-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="518e1-159">-ResourceGroupName</span></span>
<span data-ttu-id="518e1-160">Указывает имя группы ресурсов, которая содержит кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="518e1-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="518e1-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="518e1-161">-ShardCount</span></span>
<span data-ttu-id="518e1-162">Задает количество сегментов для создания в кэше высококачественных кластеров.</span><span class="sxs-lookup"><span data-stu-id="518e1-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="518e1-163">-Size</span><span class="sxs-lookup"><span data-stu-id="518e1-163">-Size</span></span>
<span data-ttu-id="518e1-164">Задает размер кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="518e1-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="518e1-165">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="518e1-165">Valid values are:</span></span> 
- <span data-ttu-id="518e1-166">P1</span><span class="sxs-lookup"><span data-stu-id="518e1-166">P1</span></span>
- <span data-ttu-id="518e1-167">–</span><span class="sxs-lookup"><span data-stu-id="518e1-167">P2</span></span>
- <span data-ttu-id="518e1-168">–</span><span class="sxs-lookup"><span data-stu-id="518e1-168">P3</span></span>
- <span data-ttu-id="518e1-169">P4</span><span class="sxs-lookup"><span data-stu-id="518e1-169">P4</span></span>
- <span data-ttu-id="518e1-170">C0</span><span class="sxs-lookup"><span data-stu-id="518e1-170">C0</span></span>
- <span data-ttu-id="518e1-171">C1</span><span class="sxs-lookup"><span data-stu-id="518e1-171">C1</span></span>
- <span data-ttu-id="518e1-172">Режим</span><span class="sxs-lookup"><span data-stu-id="518e1-172">C2</span></span>
- <span data-ttu-id="518e1-173">Ячейку</span><span class="sxs-lookup"><span data-stu-id="518e1-173">C3</span></span>
- <span data-ttu-id="518e1-174">C4</span><span class="sxs-lookup"><span data-stu-id="518e1-174">C4</span></span>
- <span data-ttu-id="518e1-175">C5</span><span class="sxs-lookup"><span data-stu-id="518e1-175">C5</span></span>
- <span data-ttu-id="518e1-176">C6</span><span class="sxs-lookup"><span data-stu-id="518e1-176">C6</span></span>
- <span data-ttu-id="518e1-177">250MB</span><span class="sxs-lookup"><span data-stu-id="518e1-177">250MB</span></span>
- <span data-ttu-id="518e1-178">Гбайт</span><span class="sxs-lookup"><span data-stu-id="518e1-178">1GB</span></span>
- <span data-ttu-id="518e1-179">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="518e1-179">2.5GB</span></span>
- <span data-ttu-id="518e1-180">6GB</span><span class="sxs-lookup"><span data-stu-id="518e1-180">6GB</span></span>
- <span data-ttu-id="518e1-181">13GB</span><span class="sxs-lookup"><span data-stu-id="518e1-181">13GB</span></span>
- <span data-ttu-id="518e1-182">26GB</span><span class="sxs-lookup"><span data-stu-id="518e1-182">26GB</span></span>
- <span data-ttu-id="518e1-183">53GB значение по умолчанию — 1 ГБ или C1.</span><span class="sxs-lookup"><span data-stu-id="518e1-183">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="518e1-184">-SKU</span><span class="sxs-lookup"><span data-stu-id="518e1-184">-Sku</span></span>
<span data-ttu-id="518e1-185">Указывает SKU кэша Redis для создания.</span><span class="sxs-lookup"><span data-stu-id="518e1-185">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="518e1-186">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="518e1-186">Valid values are:</span></span> 
- <span data-ttu-id="518e1-187">Базового</span><span class="sxs-lookup"><span data-stu-id="518e1-187">Basic</span></span>
- <span data-ttu-id="518e1-188">Стандартная</span><span class="sxs-lookup"><span data-stu-id="518e1-188">Standard</span></span>
- <span data-ttu-id="518e1-189">Premium по умолчанию используется значение Standard.</span><span class="sxs-lookup"><span data-stu-id="518e1-189">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="518e1-190">-Тег</span><span class="sxs-lookup"><span data-stu-id="518e1-190">-Tag</span></span>
<span data-ttu-id="518e1-191">Хэш-таблица, представляющая Теги.</span><span class="sxs-lookup"><span data-stu-id="518e1-191">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="518e1-192">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="518e1-192">-TenantSettings</span></span>
<span data-ttu-id="518e1-193">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="518e1-193">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="518e1-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="518e1-194">-Confirm</span></span>
<span data-ttu-id="518e1-195">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="518e1-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="518e1-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="518e1-196">-WhatIf</span></span>
<span data-ttu-id="518e1-197">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="518e1-197">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="518e1-198">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="518e1-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="518e1-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="518e1-199">CommonParameters</span></span>
<span data-ttu-id="518e1-200">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="518e1-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="518e1-201">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="518e1-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="518e1-202">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="518e1-202">INPUTS</span></span>

### <span data-ttu-id="518e1-203">System. String</span><span class="sxs-lookup"><span data-stu-id="518e1-203">System.String</span></span>

### <span data-ttu-id="518e1-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="518e1-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="518e1-205">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="518e1-205">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="518e1-206">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="518e1-206">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="518e1-207">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="518e1-207">OUTPUTS</span></span>

### <span data-ttu-id="518e1-208">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="518e1-208">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="518e1-209">Пуск</span><span class="sxs-lookup"><span data-stu-id="518e1-209">NOTES</span></span>

## <span data-ttu-id="518e1-210">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="518e1-210">RELATED LINKS</span></span>

[<span data-ttu-id="518e1-211">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="518e1-211">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="518e1-212">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="518e1-212">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="518e1-213">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="518e1-213">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


