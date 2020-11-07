---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 493a8e7a4e356284b2ae14241715a7631d99839c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732420"
---
# <span data-ttu-id="f711e-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f711e-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="f711e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f711e-102">SYNOPSIS</span></span>
<span data-ttu-id="f711e-103">Создание кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="f711e-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f711e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f711e-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f711e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f711e-105">DESCRIPTION</span></span>
<span data-ttu-id="f711e-106">Командлет **New-AzureRmRedisCache** создает кэш Redis Azure.</span><span class="sxs-lookup"><span data-stu-id="f711e-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="f711e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f711e-107">EXAMPLES</span></span>

### <span data-ttu-id="f711e-108">Пример 1: создание кэша Redis</span><span class="sxs-lookup"><span data-stu-id="f711e-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"


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
```

<span data-ttu-id="f711e-109">Эта команда создает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="f711e-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="f711e-110">Пример 2: создание стандартного кэша Redis для SKU</span><span class="sxs-lookup"><span data-stu-id="f711e-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force


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
```

<span data-ttu-id="f711e-111">Эта команда создает кэш Redis или обновляет кэш Redis, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="f711e-111">This command creates a Redis Cache or updates the Redis Cache if it already exists.</span></span>

## <span data-ttu-id="f711e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f711e-112">PARAMETERS</span></span>

### <span data-ttu-id="f711e-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="f711e-113">-EnableNonSslPort</span></span>
<span data-ttu-id="f711e-114">Указывает, включен ли порт без SSL.</span><span class="sxs-lookup"><span data-stu-id="f711e-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="f711e-115">Значение по умолчанию — $False (порт без SSL отключен).</span><span class="sxs-lookup"><span data-stu-id="f711e-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="f711e-116">-Location</span><span class="sxs-lookup"><span data-stu-id="f711e-116">-Location</span></span>
<span data-ttu-id="f711e-117">Указывает место для создания кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="f711e-117">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="f711e-118">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="f711e-118">Valid values are:</span></span> 

- <span data-ttu-id="f711e-119">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="f711e-119">North Central US</span></span>
- <span data-ttu-id="f711e-120">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="f711e-120">South Central US</span></span>
- <span data-ttu-id="f711e-121">Центральная американская</span><span class="sxs-lookup"><span data-stu-id="f711e-121">Central US</span></span>
- <span data-ttu-id="f711e-122">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="f711e-122">West Europe</span></span>
- <span data-ttu-id="f711e-123">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="f711e-123">North Europe</span></span>
- <span data-ttu-id="f711e-124">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="f711e-124">West US</span></span>
- <span data-ttu-id="f711e-125">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="f711e-125">East US</span></span>
- <span data-ttu-id="f711e-126">Восточная часть 2</span><span class="sxs-lookup"><span data-stu-id="f711e-126">East US 2</span></span>
- <span data-ttu-id="f711e-127">Восточная Япония</span><span class="sxs-lookup"><span data-stu-id="f711e-127">Japan East</span></span>
- <span data-ttu-id="f711e-128">Западная часть Японии</span><span class="sxs-lookup"><span data-stu-id="f711e-128">Japan West</span></span>
- <span data-ttu-id="f711e-129">Южная Бразилия</span><span class="sxs-lookup"><span data-stu-id="f711e-129">Brazil South</span></span>
- <span data-ttu-id="f711e-130">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="f711e-130">Southeast Asia</span></span>
- <span data-ttu-id="f711e-131">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="f711e-131">East Asia</span></span>
- <span data-ttu-id="f711e-132">Восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="f711e-132">Australia East</span></span>
- <span data-ttu-id="f711e-133">Юго-восток Австралии</span><span class="sxs-lookup"><span data-stu-id="f711e-133">Australia Southeast</span></span>

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

### <span data-ttu-id="f711e-134">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="f711e-134">-MaxMemoryPolicy</span></span>
<span data-ttu-id="f711e-135">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="f711e-135">This parameter has been deprecated.</span></span>
<span data-ttu-id="f711e-136">Для задания MaxMemory-Policy используйте параметр *RedisConfiguration* .</span><span class="sxs-lookup"><span data-stu-id="f711e-136">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="f711e-137">Например:</span><span class="sxs-lookup"><span data-stu-id="f711e-137">For example:</span></span> 

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

### <span data-ttu-id="f711e-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f711e-138">-Name</span></span>
<span data-ttu-id="f711e-139">Указывает имя создаваемого кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="f711e-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="f711e-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="f711e-140">-RedisConfiguration</span></span>
<span data-ttu-id="f711e-141">Задает параметры конфигурации Redis.</span><span class="sxs-lookup"><span data-stu-id="f711e-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="f711e-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f711e-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f711e-143">RDB — включена резервная копия.</span><span class="sxs-lookup"><span data-stu-id="f711e-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="f711e-144">Указывает на то, что сохраняемость данных Redis включена.</span><span class="sxs-lookup"><span data-stu-id="f711e-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="f711e-145">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="f711e-145">Premium tier only.</span></span>
- <span data-ttu-id="f711e-146">RDB — строка подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="f711e-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="f711e-147">Задает строку подключения к учетной записи хранения для Redis сохраняемости данных.</span><span class="sxs-lookup"><span data-stu-id="f711e-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="f711e-148">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="f711e-148">Premium tier only.</span></span>
- <span data-ttu-id="f711e-149">RDB — периодичность резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="f711e-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="f711e-150">Указывает периодичность резервного копирования для сохраняемости данных Redis.</span><span class="sxs-lookup"><span data-stu-id="f711e-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="f711e-151">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="f711e-151">Premium tier only.</span></span> 
- <span data-ttu-id="f711e-152">MaxMemory — зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="f711e-152">maxmemory-reserved.</span></span>
<span data-ttu-id="f711e-153">Настраивает память, зарезервированную для процессов без кэширования.</span><span class="sxs-lookup"><span data-stu-id="f711e-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="f711e-154">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="f711e-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f711e-155">MaxMemory — политика.</span><span class="sxs-lookup"><span data-stu-id="f711e-155">maxmemory-policy.</span></span>
<span data-ttu-id="f711e-156">Настройка политики вытеснения для кэша.</span><span class="sxs-lookup"><span data-stu-id="f711e-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="f711e-157">Все ценовые категории.</span><span class="sxs-lookup"><span data-stu-id="f711e-157">All pricing tiers.</span></span> 
- <span data-ttu-id="f711e-158">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="f711e-158">notify-keyspace-events.</span></span>
<span data-ttu-id="f711e-159">Настраивает уведомления keyspace.</span><span class="sxs-lookup"><span data-stu-id="f711e-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="f711e-160">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="f711e-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="f711e-161">хэш-максимум-ziplist-записи.</span><span class="sxs-lookup"><span data-stu-id="f711e-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="f711e-162">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="f711e-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f711e-163">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="f711e-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f711e-164">hash-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="f711e-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="f711e-165">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="f711e-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f711e-166">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="f711e-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f711e-167">Set-Max-intset-"записи".</span><span class="sxs-lookup"><span data-stu-id="f711e-167">set-max-intset-entries.</span></span>
<span data-ttu-id="f711e-168">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="f711e-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f711e-169">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="f711e-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f711e-170">zset-Max-ziplist-(записи).</span><span class="sxs-lookup"><span data-stu-id="f711e-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="f711e-171">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="f711e-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f711e-172">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="f711e-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f711e-173">zset-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="f711e-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="f711e-174">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="f711e-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f711e-175">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="f711e-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f711e-176">баз данных.</span><span class="sxs-lookup"><span data-stu-id="f711e-176">databases.</span></span>
<span data-ttu-id="f711e-177">Настраивает количество баз данных.</span><span class="sxs-lookup"><span data-stu-id="f711e-177">Configures the number of databases.</span></span>
<span data-ttu-id="f711e-178">Это свойство можно настроить только при создании кэша.</span><span class="sxs-lookup"><span data-stu-id="f711e-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="f711e-179">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="f711e-179">Standard and Premium tiers.</span></span>

<span data-ttu-id="f711e-180">Дополнительные сведения можно найти в разделе Управление кэшем Redis Azure с помощью Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="f711e-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="f711e-181">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="f711e-181">-RedisVersion</span></span>
<span data-ttu-id="f711e-182">Этот параметр устарел и будет удален из будущих выпусков.</span><span class="sxs-lookup"><span data-stu-id="f711e-182">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="f711e-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f711e-183">-ResourceGroupName</span></span>
<span data-ttu-id="f711e-184">Указывает имя группы ресурсов, в которой нужно создать кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="f711e-184">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="f711e-185">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="f711e-185">-ShardCount</span></span>
<span data-ttu-id="f711e-186">Задает количество сегментов для создания в кэше высококачественных кластеров.</span><span class="sxs-lookup"><span data-stu-id="f711e-186">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="f711e-187">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f711e-187">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f711e-188">1,1</span><span class="sxs-lookup"><span data-stu-id="f711e-188">1</span></span>
- <span data-ttu-id="f711e-189">2</span><span class="sxs-lookup"><span data-stu-id="f711e-189">2</span></span>
- <span data-ttu-id="f711e-190">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="f711e-190">3</span></span>
- <span data-ttu-id="f711e-191">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="f711e-191">4</span></span>
- <span data-ttu-id="f711e-192">5</span><span class="sxs-lookup"><span data-stu-id="f711e-192">5</span></span>
- <span data-ttu-id="f711e-193">152</span><span class="sxs-lookup"><span data-stu-id="f711e-193">6</span></span>
- <span data-ttu-id="f711e-194">5-7</span><span class="sxs-lookup"><span data-stu-id="f711e-194">7</span></span>
- <span data-ttu-id="f711e-195">No8</span><span class="sxs-lookup"><span data-stu-id="f711e-195">8</span></span>
- <span data-ttu-id="f711e-196">@</span><span class="sxs-lookup"><span data-stu-id="f711e-196">9</span></span> 
- <span data-ttu-id="f711e-197">5-10</span><span class="sxs-lookup"><span data-stu-id="f711e-197">10</span></span>

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

### <span data-ttu-id="f711e-198">-Size</span><span class="sxs-lookup"><span data-stu-id="f711e-198">-Size</span></span>
<span data-ttu-id="f711e-199">Задает размер кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="f711e-199">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="f711e-200">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="f711e-200">Valid values are:</span></span> 

- <span data-ttu-id="f711e-201">P1</span><span class="sxs-lookup"><span data-stu-id="f711e-201">P1</span></span>
- <span data-ttu-id="f711e-202">–</span><span class="sxs-lookup"><span data-stu-id="f711e-202">P2</span></span>
- <span data-ttu-id="f711e-203">–</span><span class="sxs-lookup"><span data-stu-id="f711e-203">P3</span></span>
- <span data-ttu-id="f711e-204">P4</span><span class="sxs-lookup"><span data-stu-id="f711e-204">P4</span></span>
- <span data-ttu-id="f711e-205">C0</span><span class="sxs-lookup"><span data-stu-id="f711e-205">C0</span></span>
- <span data-ttu-id="f711e-206">C1</span><span class="sxs-lookup"><span data-stu-id="f711e-206">C1</span></span>
- <span data-ttu-id="f711e-207">Режим</span><span class="sxs-lookup"><span data-stu-id="f711e-207">C2</span></span>
- <span data-ttu-id="f711e-208">Ячейку</span><span class="sxs-lookup"><span data-stu-id="f711e-208">C3</span></span>
- <span data-ttu-id="f711e-209">C4</span><span class="sxs-lookup"><span data-stu-id="f711e-209">C4</span></span>
- <span data-ttu-id="f711e-210">C5</span><span class="sxs-lookup"><span data-stu-id="f711e-210">C5</span></span>
- <span data-ttu-id="f711e-211">C6</span><span class="sxs-lookup"><span data-stu-id="f711e-211">C6</span></span>
- <span data-ttu-id="f711e-212">250MB</span><span class="sxs-lookup"><span data-stu-id="f711e-212">250MB</span></span>
- <span data-ttu-id="f711e-213">Гбайт</span><span class="sxs-lookup"><span data-stu-id="f711e-213">1GB</span></span>
- <span data-ttu-id="f711e-214">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="f711e-214">2.5GB</span></span>
- <span data-ttu-id="f711e-215">6GB</span><span class="sxs-lookup"><span data-stu-id="f711e-215">6GB</span></span>
- <span data-ttu-id="f711e-216">13GB</span><span class="sxs-lookup"><span data-stu-id="f711e-216">13GB</span></span>
- <span data-ttu-id="f711e-217">26GB</span><span class="sxs-lookup"><span data-stu-id="f711e-217">26GB</span></span>
- <span data-ttu-id="f711e-218">53GB</span><span class="sxs-lookup"><span data-stu-id="f711e-218">53GB</span></span>

<span data-ttu-id="f711e-219">Значение по умолчанию — 1 ГБ или C1.</span><span class="sxs-lookup"><span data-stu-id="f711e-219">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="f711e-220">-SKU</span><span class="sxs-lookup"><span data-stu-id="f711e-220">-Sku</span></span>
<span data-ttu-id="f711e-221">Указывает SKU кэша Redis для создания.</span><span class="sxs-lookup"><span data-stu-id="f711e-221">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="f711e-222">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="f711e-222">Valid values are:</span></span> 

- <span data-ttu-id="f711e-223">Базового</span><span class="sxs-lookup"><span data-stu-id="f711e-223">Basic</span></span>
- <span data-ttu-id="f711e-224">Стандартная</span><span class="sxs-lookup"><span data-stu-id="f711e-224">Standard</span></span>
- <span data-ttu-id="f711e-225">Версию</span><span class="sxs-lookup"><span data-stu-id="f711e-225">Premium</span></span>

<span data-ttu-id="f711e-226">По умолчанию используется значение Standard.</span><span class="sxs-lookup"><span data-stu-id="f711e-226">The default value is Standard.</span></span>

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

### <span data-ttu-id="f711e-227">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="f711e-227">-StaticIP</span></span>
<span data-ttu-id="f711e-228">Задает уникальный IP-адрес в подсети для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="f711e-228">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="f711e-229">Если вы не укажете значение для этого параметра, этот командлет выберет IP-адрес из подсети.</span><span class="sxs-lookup"><span data-stu-id="f711e-229">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="f711e-230">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="f711e-230">-Subnet</span></span>
<span data-ttu-id="f711e-231">Указывает имя подсети для развертывания кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="f711e-231">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="f711e-232">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f711e-232">-SubnetId</span></span>
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

### <span data-ttu-id="f711e-233">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="f711e-233">-TenantSettings</span></span>
<span data-ttu-id="f711e-234">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="f711e-234">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="f711e-235">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f711e-235">-VirtualNetwork</span></span>
<span data-ttu-id="f711e-236">Указывает ИД виртуальной сети, в которой развертывается кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="f711e-236">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="f711e-237">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f711e-237">-DefaultProfile</span></span>
<span data-ttu-id="f711e-238">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f711e-238">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f711e-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f711e-239">CommonParameters</span></span>
<span data-ttu-id="f711e-240">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f711e-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f711e-241">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f711e-241">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f711e-242">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f711e-242">INPUTS</span></span>

### <span data-ttu-id="f711e-243">Ничего</span><span class="sxs-lookup"><span data-stu-id="f711e-243">None</span></span>
<span data-ttu-id="f711e-244">Вы можете передавать входные данные командлету по имени, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="f711e-244">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="f711e-245">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f711e-245">OUTPUTS</span></span>

### <span data-ttu-id="f711e-246">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="f711e-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="f711e-247">Этот командлет возвращает все атрибуты кэша Redis, включая первичные и вторичные ключи доступа.</span><span class="sxs-lookup"><span data-stu-id="f711e-247">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="f711e-248">Пуск</span><span class="sxs-lookup"><span data-stu-id="f711e-248">NOTES</span></span>

## <span data-ttu-id="f711e-249">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f711e-249">RELATED LINKS</span></span>

[<span data-ttu-id="f711e-250">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f711e-250">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="f711e-251">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f711e-251">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="f711e-252">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f711e-252">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


