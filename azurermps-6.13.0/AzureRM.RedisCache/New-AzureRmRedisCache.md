---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 6b2239e09a35ada6b756e58cf2c3a09ed891e730
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733441"
---
# <span data-ttu-id="35751-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="35751-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="35751-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35751-102">SYNOPSIS</span></span>
<span data-ttu-id="35751-103">Создание кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="35751-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35751-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35751-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>]
 [-Sku <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35751-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35751-105">DESCRIPTION</span></span>
<span data-ttu-id="35751-106">Командлет **New-AzureRmRedisCache** создает кэш Redis Azure.</span><span class="sxs-lookup"><span data-stu-id="35751-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="35751-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35751-107">EXAMPLES</span></span>

### <span data-ttu-id="35751-108">Пример 1: создание кэша Redis</span><span class="sxs-lookup"><span data-stu-id="35751-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="35751-109">Эта команда создает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="35751-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="35751-110">Пример 2: создание стандартного кэша Redis для SKU</span><span class="sxs-lookup"><span data-stu-id="35751-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="35751-111">Эта команда создает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="35751-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="35751-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35751-112">PARAMETERS</span></span>

### <span data-ttu-id="35751-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35751-113">-DefaultProfile</span></span>
<span data-ttu-id="35751-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35751-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35751-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="35751-115">-EnableNonSslPort</span></span>
<span data-ttu-id="35751-116">Указывает, включен ли порт без SSL.</span><span class="sxs-lookup"><span data-stu-id="35751-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="35751-117">Значение по умолчанию — $False (порт без SSL отключен).</span><span class="sxs-lookup"><span data-stu-id="35751-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="35751-118">-Location</span><span class="sxs-lookup"><span data-stu-id="35751-118">-Location</span></span>
<span data-ttu-id="35751-119">Указывает место для создания кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="35751-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="35751-120">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="35751-120">Valid values are:</span></span> 
- <span data-ttu-id="35751-121">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="35751-121">North Central US</span></span>
- <span data-ttu-id="35751-122">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="35751-122">South Central US</span></span>
- <span data-ttu-id="35751-123">Центральная американская</span><span class="sxs-lookup"><span data-stu-id="35751-123">Central US</span></span>
- <span data-ttu-id="35751-124">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="35751-124">West Europe</span></span>
- <span data-ttu-id="35751-125">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="35751-125">North Europe</span></span>
- <span data-ttu-id="35751-126">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="35751-126">West US</span></span>
- <span data-ttu-id="35751-127">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="35751-127">East US</span></span>
- <span data-ttu-id="35751-128">Восточная часть 2</span><span class="sxs-lookup"><span data-stu-id="35751-128">East US 2</span></span>
- <span data-ttu-id="35751-129">Восточная Япония</span><span class="sxs-lookup"><span data-stu-id="35751-129">Japan East</span></span>
- <span data-ttu-id="35751-130">Западная часть Японии</span><span class="sxs-lookup"><span data-stu-id="35751-130">Japan West</span></span>
- <span data-ttu-id="35751-131">Южная Бразилия</span><span class="sxs-lookup"><span data-stu-id="35751-131">Brazil South</span></span>
- <span data-ttu-id="35751-132">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="35751-132">Southeast Asia</span></span>
- <span data-ttu-id="35751-133">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="35751-133">East Asia</span></span>
- <span data-ttu-id="35751-134">Восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="35751-134">Australia East</span></span>
- <span data-ttu-id="35751-135">Юго-восток Австралии</span><span class="sxs-lookup"><span data-stu-id="35751-135">Australia Southeast</span></span>

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

### <span data-ttu-id="35751-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="35751-136">-Name</span></span>
<span data-ttu-id="35751-137">Указывает имя создаваемого кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="35751-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="35751-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="35751-138">-RedisConfiguration</span></span>
<span data-ttu-id="35751-139">Задает параметры конфигурации Redis.</span><span class="sxs-lookup"><span data-stu-id="35751-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="35751-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="35751-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="35751-141">RDB — включена резервная копия.</span><span class="sxs-lookup"><span data-stu-id="35751-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="35751-142">Указывает на то, что сохраняемость данных Redis включена.</span><span class="sxs-lookup"><span data-stu-id="35751-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="35751-143">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="35751-143">Premium tier only.</span></span>
- <span data-ttu-id="35751-144">RDB — строка подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="35751-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="35751-145">Задает строку подключения к учетной записи хранения для Redis сохраняемости данных.</span><span class="sxs-lookup"><span data-stu-id="35751-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="35751-146">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="35751-146">Premium tier only.</span></span>
- <span data-ttu-id="35751-147">RDB — периодичность резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="35751-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="35751-148">Указывает периодичность резервного копирования для сохраняемости данных Redis.</span><span class="sxs-lookup"><span data-stu-id="35751-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="35751-149">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="35751-149">Premium tier only.</span></span> 
- <span data-ttu-id="35751-150">MaxMemory — зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="35751-150">maxmemory-reserved.</span></span>
<span data-ttu-id="35751-151">Настраивает память, зарезервированную для процессов без кэширования.</span><span class="sxs-lookup"><span data-stu-id="35751-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="35751-152">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="35751-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="35751-153">MaxMemory — политика.</span><span class="sxs-lookup"><span data-stu-id="35751-153">maxmemory-policy.</span></span>
<span data-ttu-id="35751-154">Настройка политики вытеснения для кэша.</span><span class="sxs-lookup"><span data-stu-id="35751-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="35751-155">Все ценовые категории.</span><span class="sxs-lookup"><span data-stu-id="35751-155">All pricing tiers.</span></span> 
- <span data-ttu-id="35751-156">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="35751-156">notify-keyspace-events.</span></span>
<span data-ttu-id="35751-157">Настраивает уведомления keyspace.</span><span class="sxs-lookup"><span data-stu-id="35751-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="35751-158">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="35751-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="35751-159">хэш-максимум-ziplist-записи.</span><span class="sxs-lookup"><span data-stu-id="35751-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="35751-160">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="35751-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="35751-161">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="35751-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="35751-162">hash-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="35751-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="35751-163">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="35751-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="35751-164">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="35751-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="35751-165">Set-Max-intset-"записи".</span><span class="sxs-lookup"><span data-stu-id="35751-165">set-max-intset-entries.</span></span>
<span data-ttu-id="35751-166">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="35751-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="35751-167">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="35751-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="35751-168">zset-Max-ziplist-(записи).</span><span class="sxs-lookup"><span data-stu-id="35751-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="35751-169">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="35751-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="35751-170">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="35751-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="35751-171">zset-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="35751-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="35751-172">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="35751-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="35751-173">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="35751-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="35751-174">баз данных.</span><span class="sxs-lookup"><span data-stu-id="35751-174">databases.</span></span>
<span data-ttu-id="35751-175">Настраивает количество баз данных.</span><span class="sxs-lookup"><span data-stu-id="35751-175">Configures the number of databases.</span></span>
<span data-ttu-id="35751-176">Это свойство можно настроить только при создании кэша.</span><span class="sxs-lookup"><span data-stu-id="35751-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="35751-177">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="35751-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="35751-178">Дополнительные сведения можно найти в разделе Управление кэшем Redis Azure с помощью Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="35751-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="35751-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35751-179">-ResourceGroupName</span></span>
<span data-ttu-id="35751-180">Указывает имя группы ресурсов, в которой нужно создать кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="35751-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="35751-181">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="35751-181">-ShardCount</span></span>
<span data-ttu-id="35751-182">Задает количество сегментов для создания в кэше высококачественных кластеров.</span><span class="sxs-lookup"><span data-stu-id="35751-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="35751-183">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="35751-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="35751-184">1,1</span><span class="sxs-lookup"><span data-stu-id="35751-184">1</span></span>
- <span data-ttu-id="35751-185">2</span><span class="sxs-lookup"><span data-stu-id="35751-185">2</span></span>
- <span data-ttu-id="35751-186">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="35751-186">3</span></span>
- <span data-ttu-id="35751-187">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="35751-187">4</span></span>
- <span data-ttu-id="35751-188">5</span><span class="sxs-lookup"><span data-stu-id="35751-188">5</span></span>
- <span data-ttu-id="35751-189">152</span><span class="sxs-lookup"><span data-stu-id="35751-189">6</span></span>
- <span data-ttu-id="35751-190">5-7</span><span class="sxs-lookup"><span data-stu-id="35751-190">7</span></span>
- <span data-ttu-id="35751-191">No8</span><span class="sxs-lookup"><span data-stu-id="35751-191">8</span></span>
- <span data-ttu-id="35751-192">@</span><span class="sxs-lookup"><span data-stu-id="35751-192">9</span></span> 
- <span data-ttu-id="35751-193">5-10</span><span class="sxs-lookup"><span data-stu-id="35751-193">10</span></span>

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

### <span data-ttu-id="35751-194">-Size</span><span class="sxs-lookup"><span data-stu-id="35751-194">-Size</span></span>
<span data-ttu-id="35751-195">Задает размер кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="35751-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="35751-196">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="35751-196">Valid values are:</span></span> 
- <span data-ttu-id="35751-197">P1</span><span class="sxs-lookup"><span data-stu-id="35751-197">P1</span></span>
- <span data-ttu-id="35751-198">–</span><span class="sxs-lookup"><span data-stu-id="35751-198">P2</span></span>
- <span data-ttu-id="35751-199">–</span><span class="sxs-lookup"><span data-stu-id="35751-199">P3</span></span>
- <span data-ttu-id="35751-200">P4</span><span class="sxs-lookup"><span data-stu-id="35751-200">P4</span></span>
- <span data-ttu-id="35751-201">C0</span><span class="sxs-lookup"><span data-stu-id="35751-201">C0</span></span>
- <span data-ttu-id="35751-202">C1</span><span class="sxs-lookup"><span data-stu-id="35751-202">C1</span></span>
- <span data-ttu-id="35751-203">Режим</span><span class="sxs-lookup"><span data-stu-id="35751-203">C2</span></span>
- <span data-ttu-id="35751-204">Ячейку</span><span class="sxs-lookup"><span data-stu-id="35751-204">C3</span></span>
- <span data-ttu-id="35751-205">C4</span><span class="sxs-lookup"><span data-stu-id="35751-205">C4</span></span>
- <span data-ttu-id="35751-206">C5</span><span class="sxs-lookup"><span data-stu-id="35751-206">C5</span></span>
- <span data-ttu-id="35751-207">C6</span><span class="sxs-lookup"><span data-stu-id="35751-207">C6</span></span>
- <span data-ttu-id="35751-208">250MB</span><span class="sxs-lookup"><span data-stu-id="35751-208">250MB</span></span>
- <span data-ttu-id="35751-209">Гбайт</span><span class="sxs-lookup"><span data-stu-id="35751-209">1GB</span></span>
- <span data-ttu-id="35751-210">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="35751-210">2.5GB</span></span>
- <span data-ttu-id="35751-211">6GB</span><span class="sxs-lookup"><span data-stu-id="35751-211">6GB</span></span>
- <span data-ttu-id="35751-212">13GB</span><span class="sxs-lookup"><span data-stu-id="35751-212">13GB</span></span>
- <span data-ttu-id="35751-213">26GB</span><span class="sxs-lookup"><span data-stu-id="35751-213">26GB</span></span>
- <span data-ttu-id="35751-214">53GB значение по умолчанию — 1 ГБ или C1.</span><span class="sxs-lookup"><span data-stu-id="35751-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="35751-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="35751-215">-Sku</span></span>
<span data-ttu-id="35751-216">Указывает SKU кэша Redis для создания.</span><span class="sxs-lookup"><span data-stu-id="35751-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="35751-217">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="35751-217">Valid values are:</span></span> 
- <span data-ttu-id="35751-218">Базового</span><span class="sxs-lookup"><span data-stu-id="35751-218">Basic</span></span>
- <span data-ttu-id="35751-219">Стандартная</span><span class="sxs-lookup"><span data-stu-id="35751-219">Standard</span></span>
- <span data-ttu-id="35751-220">Premium по умолчанию используется значение Standard.</span><span class="sxs-lookup"><span data-stu-id="35751-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="35751-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="35751-221">-StaticIP</span></span>
<span data-ttu-id="35751-222">Задает уникальный IP-адрес в подсети для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="35751-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="35751-223">Если вы не укажете значение для этого параметра, этот командлет выберет IP-адрес из подсети.</span><span class="sxs-lookup"><span data-stu-id="35751-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="35751-224">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="35751-224">-SubnetId</span></span>
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

### <span data-ttu-id="35751-225">-Тег</span><span class="sxs-lookup"><span data-stu-id="35751-225">-Tag</span></span>
<span data-ttu-id="35751-226">Хэш-таблица, представляющая Теги.</span><span class="sxs-lookup"><span data-stu-id="35751-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="35751-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="35751-227">-TenantSettings</span></span>
<span data-ttu-id="35751-228">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="35751-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="35751-229">-Zone</span><span class="sxs-lookup"><span data-stu-id="35751-229">-Zone</span></span>
<span data-ttu-id="35751-230">Список зон.</span><span class="sxs-lookup"><span data-stu-id="35751-230">List of zones.</span></span>

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

### <span data-ttu-id="35751-231">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35751-231">-Confirm</span></span>
<span data-ttu-id="35751-232">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="35751-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35751-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35751-233">-WhatIf</span></span>
<span data-ttu-id="35751-234">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="35751-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35751-235">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="35751-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35751-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35751-236">CommonParameters</span></span>
<span data-ttu-id="35751-237">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35751-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35751-238">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35751-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35751-239">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35751-239">INPUTS</span></span>

### <span data-ttu-id="35751-240">System. String</span><span class="sxs-lookup"><span data-stu-id="35751-240">System.String</span></span>

### <span data-ttu-id="35751-241">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="35751-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="35751-242">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="35751-242">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="35751-243">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="35751-243">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="35751-244">System. String []</span><span class="sxs-lookup"><span data-stu-id="35751-244">System.String[]</span></span>

## <span data-ttu-id="35751-245">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35751-245">OUTPUTS</span></span>

### <span data-ttu-id="35751-246">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="35751-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="35751-247">Пуск</span><span class="sxs-lookup"><span data-stu-id="35751-247">NOTES</span></span>

## <span data-ttu-id="35751-248">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35751-248">RELATED LINKS</span></span>

[<span data-ttu-id="35751-249">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="35751-249">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="35751-250">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="35751-250">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="35751-251">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="35751-251">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


