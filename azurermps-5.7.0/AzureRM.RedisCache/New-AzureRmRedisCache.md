---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: bbba6372be7176b8ac1aec553a9abbbf83c7da31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561583"
---
# <span data-ttu-id="d19ef-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d19ef-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="d19ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d19ef-102">SYNOPSIS</span></span>
<span data-ttu-id="d19ef-103">Создание кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="d19ef-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d19ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d19ef-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d19ef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d19ef-105">DESCRIPTION</span></span>
<span data-ttu-id="d19ef-106">Командлет **New-AzureRmRedisCache** создает кэш Redis Azure.</span><span class="sxs-lookup"><span data-stu-id="d19ef-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="d19ef-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d19ef-107">EXAMPLES</span></span>

### <span data-ttu-id="d19ef-108">Пример 1: создание кэша Redis</span><span class="sxs-lookup"><span data-stu-id="d19ef-108">Example 1: Create a Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="d19ef-109">Эта команда создает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="d19ef-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="d19ef-110">Пример 2: создание стандартного кэша Redis для SKU</span><span class="sxs-lookup"><span data-stu-id="d19ef-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="d19ef-111">Эта команда создает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="d19ef-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="d19ef-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d19ef-112">PARAMETERS</span></span>

### <span data-ttu-id="d19ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d19ef-113">-DefaultProfile</span></span>
<span data-ttu-id="d19ef-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d19ef-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d19ef-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="d19ef-115">-EnableNonSslPort</span></span>
<span data-ttu-id="d19ef-116">Указывает, включен ли порт без SSL.</span><span class="sxs-lookup"><span data-stu-id="d19ef-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="d19ef-117">Значение по умолчанию — $False (порт без SSL отключен).</span><span class="sxs-lookup"><span data-stu-id="d19ef-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="d19ef-118">-Location</span><span class="sxs-lookup"><span data-stu-id="d19ef-118">-Location</span></span>
<span data-ttu-id="d19ef-119">Указывает место для создания кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="d19ef-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="d19ef-120">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="d19ef-120">Valid values are:</span></span> 

- <span data-ttu-id="d19ef-121">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="d19ef-121">North Central US</span></span>
- <span data-ttu-id="d19ef-122">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="d19ef-122">South Central US</span></span>
- <span data-ttu-id="d19ef-123">Центральная американская</span><span class="sxs-lookup"><span data-stu-id="d19ef-123">Central US</span></span>
- <span data-ttu-id="d19ef-124">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="d19ef-124">West Europe</span></span>
- <span data-ttu-id="d19ef-125">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="d19ef-125">North Europe</span></span>
- <span data-ttu-id="d19ef-126">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="d19ef-126">West US</span></span>
- <span data-ttu-id="d19ef-127">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="d19ef-127">East US</span></span>
- <span data-ttu-id="d19ef-128">Восточная часть 2</span><span class="sxs-lookup"><span data-stu-id="d19ef-128">East US 2</span></span>
- <span data-ttu-id="d19ef-129">Восточная Япония</span><span class="sxs-lookup"><span data-stu-id="d19ef-129">Japan East</span></span>
- <span data-ttu-id="d19ef-130">Западная часть Японии</span><span class="sxs-lookup"><span data-stu-id="d19ef-130">Japan West</span></span>
- <span data-ttu-id="d19ef-131">Южная Бразилия</span><span class="sxs-lookup"><span data-stu-id="d19ef-131">Brazil South</span></span>
- <span data-ttu-id="d19ef-132">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="d19ef-132">Southeast Asia</span></span>
- <span data-ttu-id="d19ef-133">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="d19ef-133">East Asia</span></span>
- <span data-ttu-id="d19ef-134">Восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="d19ef-134">Australia East</span></span>
- <span data-ttu-id="d19ef-135">Юго-восток Австралии</span><span class="sxs-lookup"><span data-stu-id="d19ef-135">Australia Southeast</span></span>

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

### <span data-ttu-id="d19ef-136">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="d19ef-136">-MaxMemoryPolicy</span></span>
<span data-ttu-id="d19ef-137">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="d19ef-137">This parameter has been deprecated.</span></span>
<span data-ttu-id="d19ef-138">Для задания MaxMemory-Policy используйте параметр *RedisConfiguration* .</span><span class="sxs-lookup"><span data-stu-id="d19ef-138">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="d19ef-139">Например:</span><span class="sxs-lookup"><span data-stu-id="d19ef-139">For example:</span></span> 

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

### <span data-ttu-id="d19ef-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d19ef-140">-Name</span></span>
<span data-ttu-id="d19ef-141">Указывает имя создаваемого кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="d19ef-141">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="d19ef-142">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="d19ef-142">-RedisConfiguration</span></span>
<span data-ttu-id="d19ef-143">Задает параметры конфигурации Redis.</span><span class="sxs-lookup"><span data-stu-id="d19ef-143">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="d19ef-144">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d19ef-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d19ef-145">RDB — включена резервная копия.</span><span class="sxs-lookup"><span data-stu-id="d19ef-145">rdb-backup-enabled.</span></span>
<span data-ttu-id="d19ef-146">Указывает на то, что сохраняемость данных Redis включена.</span><span class="sxs-lookup"><span data-stu-id="d19ef-146">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="d19ef-147">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="d19ef-147">Premium tier only.</span></span>
- <span data-ttu-id="d19ef-148">RDB — строка подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="d19ef-148">rdb-storage-connection-string.</span></span>
<span data-ttu-id="d19ef-149">Задает строку подключения к учетной записи хранения для Redis сохраняемости данных.</span><span class="sxs-lookup"><span data-stu-id="d19ef-149">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="d19ef-150">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="d19ef-150">Premium tier only.</span></span>
- <span data-ttu-id="d19ef-151">RDB — периодичность резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="d19ef-151">rdb-backup-frequency.</span></span>
<span data-ttu-id="d19ef-152">Указывает периодичность резервного копирования для сохраняемости данных Redis.</span><span class="sxs-lookup"><span data-stu-id="d19ef-152">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="d19ef-153">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="d19ef-153">Premium tier only.</span></span> 
- <span data-ttu-id="d19ef-154">MaxMemory — зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="d19ef-154">maxmemory-reserved.</span></span>
<span data-ttu-id="d19ef-155">Настраивает память, зарезервированную для процессов без кэширования.</span><span class="sxs-lookup"><span data-stu-id="d19ef-155">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="d19ef-156">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="d19ef-156">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d19ef-157">MaxMemory — политика.</span><span class="sxs-lookup"><span data-stu-id="d19ef-157">maxmemory-policy.</span></span>
<span data-ttu-id="d19ef-158">Настройка политики вытеснения для кэша.</span><span class="sxs-lookup"><span data-stu-id="d19ef-158">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="d19ef-159">Все ценовые категории.</span><span class="sxs-lookup"><span data-stu-id="d19ef-159">All pricing tiers.</span></span> 
- <span data-ttu-id="d19ef-160">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="d19ef-160">notify-keyspace-events.</span></span>
<span data-ttu-id="d19ef-161">Настраивает уведомления keyspace.</span><span class="sxs-lookup"><span data-stu-id="d19ef-161">Configures keyspace notifications.</span></span>
<span data-ttu-id="d19ef-162">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="d19ef-162">Standard and premium tiers.</span></span> 
- <span data-ttu-id="d19ef-163">хэш-максимум-ziplist-записи.</span><span class="sxs-lookup"><span data-stu-id="d19ef-163">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="d19ef-164">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="d19ef-164">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d19ef-165">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="d19ef-165">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d19ef-166">hash-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="d19ef-166">hash-max-ziplist-value.</span></span>
<span data-ttu-id="d19ef-167">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="d19ef-167">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d19ef-168">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="d19ef-168">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d19ef-169">Set-Max-intset-"записи".</span><span class="sxs-lookup"><span data-stu-id="d19ef-169">set-max-intset-entries.</span></span>
<span data-ttu-id="d19ef-170">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="d19ef-170">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d19ef-171">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="d19ef-171">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d19ef-172">zset-Max-ziplist-(записи).</span><span class="sxs-lookup"><span data-stu-id="d19ef-172">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="d19ef-173">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="d19ef-173">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d19ef-174">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="d19ef-174">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d19ef-175">zset-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="d19ef-175">zset-max-ziplist-value.</span></span>
<span data-ttu-id="d19ef-176">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="d19ef-176">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="d19ef-177">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="d19ef-177">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="d19ef-178">баз данных.</span><span class="sxs-lookup"><span data-stu-id="d19ef-178">databases.</span></span>
<span data-ttu-id="d19ef-179">Настраивает количество баз данных.</span><span class="sxs-lookup"><span data-stu-id="d19ef-179">Configures the number of databases.</span></span>
<span data-ttu-id="d19ef-180">Это свойство можно настроить только при создании кэша.</span><span class="sxs-lookup"><span data-stu-id="d19ef-180">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="d19ef-181">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="d19ef-181">Standard and Premium tiers.</span></span>

<span data-ttu-id="d19ef-182">Дополнительные сведения можно найти в разделе Управление кэшем Redis Azure с помощью Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="d19ef-182">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="d19ef-183">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="d19ef-183">-RedisVersion</span></span>
<span data-ttu-id="d19ef-184">Этот параметр устарел и будет удален из будущих выпусков.</span><span class="sxs-lookup"><span data-stu-id="d19ef-184">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="d19ef-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d19ef-185">-ResourceGroupName</span></span>
<span data-ttu-id="d19ef-186">Указывает имя группы ресурсов, в которой нужно создать кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="d19ef-186">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="d19ef-187">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="d19ef-187">-ShardCount</span></span>
<span data-ttu-id="d19ef-188">Задает количество сегментов для создания в кэше высококачественных кластеров.</span><span class="sxs-lookup"><span data-stu-id="d19ef-188">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="d19ef-189">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d19ef-189">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d19ef-190">1,1</span><span class="sxs-lookup"><span data-stu-id="d19ef-190">1</span></span>
- <span data-ttu-id="d19ef-191">2</span><span class="sxs-lookup"><span data-stu-id="d19ef-191">2</span></span>
- <span data-ttu-id="d19ef-192">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="d19ef-192">3</span></span>
- <span data-ttu-id="d19ef-193">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="d19ef-193">4</span></span>
- <span data-ttu-id="d19ef-194">5</span><span class="sxs-lookup"><span data-stu-id="d19ef-194">5</span></span>
- <span data-ttu-id="d19ef-195">152</span><span class="sxs-lookup"><span data-stu-id="d19ef-195">6</span></span>
- <span data-ttu-id="d19ef-196">5-7</span><span class="sxs-lookup"><span data-stu-id="d19ef-196">7</span></span>
- <span data-ttu-id="d19ef-197">No8</span><span class="sxs-lookup"><span data-stu-id="d19ef-197">8</span></span>
- <span data-ttu-id="d19ef-198">@</span><span class="sxs-lookup"><span data-stu-id="d19ef-198">9</span></span> 
- <span data-ttu-id="d19ef-199">5-10</span><span class="sxs-lookup"><span data-stu-id="d19ef-199">10</span></span>

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

### <span data-ttu-id="d19ef-200">-Size</span><span class="sxs-lookup"><span data-stu-id="d19ef-200">-Size</span></span>
<span data-ttu-id="d19ef-201">Задает размер кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="d19ef-201">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="d19ef-202">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="d19ef-202">Valid values are:</span></span> 

- <span data-ttu-id="d19ef-203">P1</span><span class="sxs-lookup"><span data-stu-id="d19ef-203">P1</span></span>
- <span data-ttu-id="d19ef-204">–</span><span class="sxs-lookup"><span data-stu-id="d19ef-204">P2</span></span>
- <span data-ttu-id="d19ef-205">–</span><span class="sxs-lookup"><span data-stu-id="d19ef-205">P3</span></span>
- <span data-ttu-id="d19ef-206">P4</span><span class="sxs-lookup"><span data-stu-id="d19ef-206">P4</span></span>
- <span data-ttu-id="d19ef-207">C0</span><span class="sxs-lookup"><span data-stu-id="d19ef-207">C0</span></span>
- <span data-ttu-id="d19ef-208">C1</span><span class="sxs-lookup"><span data-stu-id="d19ef-208">C1</span></span>
- <span data-ttu-id="d19ef-209">Режим</span><span class="sxs-lookup"><span data-stu-id="d19ef-209">C2</span></span>
- <span data-ttu-id="d19ef-210">Ячейку</span><span class="sxs-lookup"><span data-stu-id="d19ef-210">C3</span></span>
- <span data-ttu-id="d19ef-211">C4</span><span class="sxs-lookup"><span data-stu-id="d19ef-211">C4</span></span>
- <span data-ttu-id="d19ef-212">C5</span><span class="sxs-lookup"><span data-stu-id="d19ef-212">C5</span></span>
- <span data-ttu-id="d19ef-213">C6</span><span class="sxs-lookup"><span data-stu-id="d19ef-213">C6</span></span>
- <span data-ttu-id="d19ef-214">250MB</span><span class="sxs-lookup"><span data-stu-id="d19ef-214">250MB</span></span>
- <span data-ttu-id="d19ef-215">Гбайт</span><span class="sxs-lookup"><span data-stu-id="d19ef-215">1GB</span></span>
- <span data-ttu-id="d19ef-216">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="d19ef-216">2.5GB</span></span>
- <span data-ttu-id="d19ef-217">6GB</span><span class="sxs-lookup"><span data-stu-id="d19ef-217">6GB</span></span>
- <span data-ttu-id="d19ef-218">13GB</span><span class="sxs-lookup"><span data-stu-id="d19ef-218">13GB</span></span>
- <span data-ttu-id="d19ef-219">26GB</span><span class="sxs-lookup"><span data-stu-id="d19ef-219">26GB</span></span>
- <span data-ttu-id="d19ef-220">53GB</span><span class="sxs-lookup"><span data-stu-id="d19ef-220">53GB</span></span>

<span data-ttu-id="d19ef-221">Значение по умолчанию — 1 ГБ или C1.</span><span class="sxs-lookup"><span data-stu-id="d19ef-221">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="d19ef-222">-SKU</span><span class="sxs-lookup"><span data-stu-id="d19ef-222">-Sku</span></span>
<span data-ttu-id="d19ef-223">Указывает SKU кэша Redis для создания.</span><span class="sxs-lookup"><span data-stu-id="d19ef-223">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="d19ef-224">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="d19ef-224">Valid values are:</span></span> 

- <span data-ttu-id="d19ef-225">Базового</span><span class="sxs-lookup"><span data-stu-id="d19ef-225">Basic</span></span>
- <span data-ttu-id="d19ef-226">Стандартная</span><span class="sxs-lookup"><span data-stu-id="d19ef-226">Standard</span></span>
- <span data-ttu-id="d19ef-227">Версию</span><span class="sxs-lookup"><span data-stu-id="d19ef-227">Premium</span></span>

<span data-ttu-id="d19ef-228">По умолчанию используется значение Standard.</span><span class="sxs-lookup"><span data-stu-id="d19ef-228">The default value is Standard.</span></span>

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

### <span data-ttu-id="d19ef-229">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="d19ef-229">-StaticIP</span></span>
<span data-ttu-id="d19ef-230">Задает уникальный IP-адрес в подсети для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="d19ef-230">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="d19ef-231">Если вы не укажете значение для этого параметра, этот командлет выберет IP-адрес из подсети.</span><span class="sxs-lookup"><span data-stu-id="d19ef-231">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="d19ef-232">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="d19ef-232">-Subnet</span></span>
<span data-ttu-id="d19ef-233">Указывает имя подсети для развертывания кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="d19ef-233">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="d19ef-234">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d19ef-234">-SubnetId</span></span>
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

### <span data-ttu-id="d19ef-235">-Тег</span><span class="sxs-lookup"><span data-stu-id="d19ef-235">-Tag</span></span>
<span data-ttu-id="d19ef-236">Хэш-таблица, представляющая Теги.</span><span class="sxs-lookup"><span data-stu-id="d19ef-236">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="d19ef-237">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="d19ef-237">-TenantSettings</span></span>
<span data-ttu-id="d19ef-238">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="d19ef-238">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="d19ef-239">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d19ef-239">-VirtualNetwork</span></span>
<span data-ttu-id="d19ef-240">Указывает ИД виртуальной сети, в которой развертывается кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="d19ef-240">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="d19ef-241">-Zone</span><span class="sxs-lookup"><span data-stu-id="d19ef-241">-Zone</span></span>
<span data-ttu-id="d19ef-242">Список зон.</span><span class="sxs-lookup"><span data-stu-id="d19ef-242">List of zones.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d19ef-243">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d19ef-243">-Confirm</span></span>
<span data-ttu-id="d19ef-244">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d19ef-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d19ef-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d19ef-245">-WhatIf</span></span>
<span data-ttu-id="d19ef-246">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d19ef-246">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d19ef-247">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d19ef-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d19ef-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d19ef-248">CommonParameters</span></span>
<span data-ttu-id="d19ef-249">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d19ef-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d19ef-250">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d19ef-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d19ef-251">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d19ef-251">INPUTS</span></span>

### <span data-ttu-id="d19ef-252">Ничего</span><span class="sxs-lookup"><span data-stu-id="d19ef-252">None</span></span>
<span data-ttu-id="d19ef-253">Вы можете передавать входные данные командлету по имени, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="d19ef-253">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="d19ef-254">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d19ef-254">OUTPUTS</span></span>

### <span data-ttu-id="d19ef-255">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d19ef-255">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="d19ef-256">Этот командлет возвращает все атрибуты кэша Redis, включая первичные и вторичные ключи доступа.</span><span class="sxs-lookup"><span data-stu-id="d19ef-256">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="d19ef-257">Пуск</span><span class="sxs-lookup"><span data-stu-id="d19ef-257">NOTES</span></span>

## <span data-ttu-id="d19ef-258">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d19ef-258">RELATED LINKS</span></span>

[<span data-ttu-id="d19ef-259">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d19ef-259">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="d19ef-260">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d19ef-260">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="d19ef-261">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d19ef-261">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


