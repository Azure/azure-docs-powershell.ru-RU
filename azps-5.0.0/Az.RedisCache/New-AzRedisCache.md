---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248477"
---
# <span data-ttu-id="26851-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="26851-101">New-AzRedisCache</span></span>

## <span data-ttu-id="26851-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26851-102">SYNOPSIS</span></span>
<span data-ttu-id="26851-103">Создание кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="26851-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="26851-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26851-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26851-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26851-105">DESCRIPTION</span></span>
<span data-ttu-id="26851-106">Командлет **New-AzRedisCache** создает кэш Redis Azure.</span><span class="sxs-lookup"><span data-stu-id="26851-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="26851-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26851-107">EXAMPLES</span></span>

### <span data-ttu-id="26851-108">Пример 1: создание кэша Redis</span><span class="sxs-lookup"><span data-stu-id="26851-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

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

<span data-ttu-id="26851-109">Эта команда создает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="26851-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="26851-110">Пример 2: создание стандартного кэша Redis для SKU</span><span class="sxs-lookup"><span data-stu-id="26851-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

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

<span data-ttu-id="26851-111">Эта команда создает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="26851-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="26851-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26851-112">PARAMETERS</span></span>

### <span data-ttu-id="26851-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26851-113">-DefaultProfile</span></span>
<span data-ttu-id="26851-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26851-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26851-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="26851-115">-EnableNonSslPort</span></span>
<span data-ttu-id="26851-116">Указывает, включен ли порт без SSL.</span><span class="sxs-lookup"><span data-stu-id="26851-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="26851-117">Значение по умолчанию — $False (порт без SSL отключен).</span><span class="sxs-lookup"><span data-stu-id="26851-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="26851-118">-Location</span><span class="sxs-lookup"><span data-stu-id="26851-118">-Location</span></span>
<span data-ttu-id="26851-119">Указывает место для создания кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="26851-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="26851-120">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="26851-120">Valid values are:</span></span> 
- <span data-ttu-id="26851-121">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="26851-121">North Central US</span></span>
- <span data-ttu-id="26851-122">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="26851-122">South Central US</span></span>
- <span data-ttu-id="26851-123">Центральная американская</span><span class="sxs-lookup"><span data-stu-id="26851-123">Central US</span></span>
- <span data-ttu-id="26851-124">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="26851-124">West Europe</span></span>
- <span data-ttu-id="26851-125">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="26851-125">North Europe</span></span>
- <span data-ttu-id="26851-126">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="26851-126">West US</span></span>
- <span data-ttu-id="26851-127">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="26851-127">East US</span></span>
- <span data-ttu-id="26851-128">Восточная часть 2</span><span class="sxs-lookup"><span data-stu-id="26851-128">East US 2</span></span>
- <span data-ttu-id="26851-129">Восточная Япония</span><span class="sxs-lookup"><span data-stu-id="26851-129">Japan East</span></span>
- <span data-ttu-id="26851-130">Западная часть Японии</span><span class="sxs-lookup"><span data-stu-id="26851-130">Japan West</span></span>
- <span data-ttu-id="26851-131">Южная Бразилия</span><span class="sxs-lookup"><span data-stu-id="26851-131">Brazil South</span></span>
- <span data-ttu-id="26851-132">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="26851-132">Southeast Asia</span></span>
- <span data-ttu-id="26851-133">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="26851-133">East Asia</span></span>
- <span data-ttu-id="26851-134">Восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="26851-134">Australia East</span></span>
- <span data-ttu-id="26851-135">Юго-восток Австралии</span><span class="sxs-lookup"><span data-stu-id="26851-135">Australia Southeast</span></span>

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

### <span data-ttu-id="26851-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="26851-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="26851-137">Укажите версию TLS, необходимую клиентам для подключения к кэшу.</span><span class="sxs-lookup"><span data-stu-id="26851-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="26851-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="26851-138">-Name</span></span>
<span data-ttu-id="26851-139">Указывает имя создаваемого кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="26851-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="26851-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="26851-140">-RedisConfiguration</span></span>
<span data-ttu-id="26851-141">Задает параметры конфигурации Redis.</span><span class="sxs-lookup"><span data-stu-id="26851-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="26851-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="26851-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26851-143">RDB — включена резервная копия.</span><span class="sxs-lookup"><span data-stu-id="26851-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="26851-144">Указывает на то, что сохраняемость данных Redis включена.</span><span class="sxs-lookup"><span data-stu-id="26851-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="26851-145">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="26851-145">Premium tier only.</span></span>
- <span data-ttu-id="26851-146">RDB — строка подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="26851-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="26851-147">Задает строку подключения к учетной записи хранения для Redis сохраняемости данных.</span><span class="sxs-lookup"><span data-stu-id="26851-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="26851-148">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="26851-148">Premium tier only.</span></span>
- <span data-ttu-id="26851-149">RDB — периодичность резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="26851-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="26851-150">Указывает периодичность резервного копирования для сохраняемости данных Redis.</span><span class="sxs-lookup"><span data-stu-id="26851-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="26851-151">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="26851-151">Premium tier only.</span></span> 
- <span data-ttu-id="26851-152">MaxMemory — зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="26851-152">maxmemory-reserved.</span></span>
<span data-ttu-id="26851-153">Настраивает память, зарезервированную для процессов без кэширования.</span><span class="sxs-lookup"><span data-stu-id="26851-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="26851-154">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="26851-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="26851-155">MaxMemory — политика.</span><span class="sxs-lookup"><span data-stu-id="26851-155">maxmemory-policy.</span></span>
<span data-ttu-id="26851-156">Настройка политики вытеснения для кэша.</span><span class="sxs-lookup"><span data-stu-id="26851-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="26851-157">Все ценовые категории.</span><span class="sxs-lookup"><span data-stu-id="26851-157">All pricing tiers.</span></span> 
- <span data-ttu-id="26851-158">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="26851-158">notify-keyspace-events.</span></span>
<span data-ttu-id="26851-159">Настраивает уведомления keyspace.</span><span class="sxs-lookup"><span data-stu-id="26851-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="26851-160">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="26851-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="26851-161">хэш-максимум-ziplist-записи.</span><span class="sxs-lookup"><span data-stu-id="26851-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="26851-162">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="26851-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="26851-163">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="26851-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="26851-164">hash-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="26851-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="26851-165">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="26851-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="26851-166">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="26851-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="26851-167">Set-Max-intset-"записи".</span><span class="sxs-lookup"><span data-stu-id="26851-167">set-max-intset-entries.</span></span>
<span data-ttu-id="26851-168">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="26851-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="26851-169">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="26851-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="26851-170">zset-Max-ziplist-(записи).</span><span class="sxs-lookup"><span data-stu-id="26851-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="26851-171">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="26851-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="26851-172">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="26851-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="26851-173">zset-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="26851-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="26851-174">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="26851-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="26851-175">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="26851-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="26851-176">баз данных.</span><span class="sxs-lookup"><span data-stu-id="26851-176">databases.</span></span>
<span data-ttu-id="26851-177">Настраивает количество баз данных.</span><span class="sxs-lookup"><span data-stu-id="26851-177">Configures the number of databases.</span></span>
<span data-ttu-id="26851-178">Это свойство можно настроить только при создании кэша.</span><span class="sxs-lookup"><span data-stu-id="26851-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="26851-179">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="26851-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="26851-180">Дополнительные сведения можно найти в разделе Управление кэшем Redis Azure с помощью Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="26851-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="26851-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26851-181">-ResourceGroupName</span></span>
<span data-ttu-id="26851-182">Указывает имя группы ресурсов, в которой нужно создать кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="26851-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="26851-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="26851-183">-ShardCount</span></span>
<span data-ttu-id="26851-184">Задает количество сегментов для создания в кэше высококачественных кластеров.</span><span class="sxs-lookup"><span data-stu-id="26851-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="26851-185">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="26851-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26851-186">1,1</span><span class="sxs-lookup"><span data-stu-id="26851-186">1</span></span>
- <span data-ttu-id="26851-187">2</span><span class="sxs-lookup"><span data-stu-id="26851-187">2</span></span>
- <span data-ttu-id="26851-188">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="26851-188">3</span></span>
- <span data-ttu-id="26851-189">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="26851-189">4</span></span>
- <span data-ttu-id="26851-190">5</span><span class="sxs-lookup"><span data-stu-id="26851-190">5</span></span>
- <span data-ttu-id="26851-191">152</span><span class="sxs-lookup"><span data-stu-id="26851-191">6</span></span>
- <span data-ttu-id="26851-192">5-7</span><span class="sxs-lookup"><span data-stu-id="26851-192">7</span></span>
- <span data-ttu-id="26851-193">No8</span><span class="sxs-lookup"><span data-stu-id="26851-193">8</span></span>
- <span data-ttu-id="26851-194">@</span><span class="sxs-lookup"><span data-stu-id="26851-194">9</span></span> 
- <span data-ttu-id="26851-195">5-10</span><span class="sxs-lookup"><span data-stu-id="26851-195">10</span></span>

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

### <span data-ttu-id="26851-196">-Size</span><span class="sxs-lookup"><span data-stu-id="26851-196">-Size</span></span>
<span data-ttu-id="26851-197">Задает размер кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="26851-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="26851-198">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="26851-198">Valid values are:</span></span> 
- <span data-ttu-id="26851-199">P1</span><span class="sxs-lookup"><span data-stu-id="26851-199">P1</span></span>
- <span data-ttu-id="26851-200">–</span><span class="sxs-lookup"><span data-stu-id="26851-200">P2</span></span>
- <span data-ttu-id="26851-201">–</span><span class="sxs-lookup"><span data-stu-id="26851-201">P3</span></span>
- <span data-ttu-id="26851-202">P4</span><span class="sxs-lookup"><span data-stu-id="26851-202">P4</span></span>
- <span data-ttu-id="26851-203">P5</span><span class="sxs-lookup"><span data-stu-id="26851-203">P5</span></span>
- <span data-ttu-id="26851-204">C0</span><span class="sxs-lookup"><span data-stu-id="26851-204">C0</span></span>
- <span data-ttu-id="26851-205">C1</span><span class="sxs-lookup"><span data-stu-id="26851-205">C1</span></span>
- <span data-ttu-id="26851-206">Режим</span><span class="sxs-lookup"><span data-stu-id="26851-206">C2</span></span>
- <span data-ttu-id="26851-207">Ячейку</span><span class="sxs-lookup"><span data-stu-id="26851-207">C3</span></span>
- <span data-ttu-id="26851-208">C4</span><span class="sxs-lookup"><span data-stu-id="26851-208">C4</span></span>
- <span data-ttu-id="26851-209">C5</span><span class="sxs-lookup"><span data-stu-id="26851-209">C5</span></span>
- <span data-ttu-id="26851-210">C6</span><span class="sxs-lookup"><span data-stu-id="26851-210">C6</span></span>
- <span data-ttu-id="26851-211">250MB</span><span class="sxs-lookup"><span data-stu-id="26851-211">250MB</span></span>
- <span data-ttu-id="26851-212">Гбайт</span><span class="sxs-lookup"><span data-stu-id="26851-212">1GB</span></span>
- <span data-ttu-id="26851-213">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="26851-213">2.5GB</span></span>
- <span data-ttu-id="26851-214">6GB</span><span class="sxs-lookup"><span data-stu-id="26851-214">6GB</span></span>
- <span data-ttu-id="26851-215">13GB</span><span class="sxs-lookup"><span data-stu-id="26851-215">13GB</span></span>
- <span data-ttu-id="26851-216">26GB</span><span class="sxs-lookup"><span data-stu-id="26851-216">26GB</span></span>
- <span data-ttu-id="26851-217">53GB значение по умолчанию — 1 ГБ или C1.</span><span class="sxs-lookup"><span data-stu-id="26851-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="26851-218">-SKU</span><span class="sxs-lookup"><span data-stu-id="26851-218">-Sku</span></span>
<span data-ttu-id="26851-219">Указывает SKU кэша Redis для создания.</span><span class="sxs-lookup"><span data-stu-id="26851-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="26851-220">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="26851-220">Valid values are:</span></span> 
- <span data-ttu-id="26851-221">Базового</span><span class="sxs-lookup"><span data-stu-id="26851-221">Basic</span></span>
- <span data-ttu-id="26851-222">Стандартная</span><span class="sxs-lookup"><span data-stu-id="26851-222">Standard</span></span>
- <span data-ttu-id="26851-223">Premium по умолчанию используется значение Standard.</span><span class="sxs-lookup"><span data-stu-id="26851-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="26851-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="26851-224">-StaticIP</span></span>
<span data-ttu-id="26851-225">Задает уникальный IP-адрес в подсети для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="26851-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="26851-226">Если вы не укажете значение для этого параметра, этот командлет выберет IP-адрес из подсети.</span><span class="sxs-lookup"><span data-stu-id="26851-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="26851-227">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="26851-227">-SubnetId</span></span>
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

### <span data-ttu-id="26851-228">-Тег</span><span class="sxs-lookup"><span data-stu-id="26851-228">-Tag</span></span>
<span data-ttu-id="26851-229">Хэш-таблица, представляющая Теги.</span><span class="sxs-lookup"><span data-stu-id="26851-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="26851-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="26851-230">-TenantSettings</span></span>
<span data-ttu-id="26851-231">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="26851-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="26851-232">-Zone</span><span class="sxs-lookup"><span data-stu-id="26851-232">-Zone</span></span>
<span data-ttu-id="26851-233">Список зон.</span><span class="sxs-lookup"><span data-stu-id="26851-233">List of zones.</span></span>

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

### <span data-ttu-id="26851-234">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26851-234">-Confirm</span></span>
<span data-ttu-id="26851-235">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="26851-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26851-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26851-236">-WhatIf</span></span>
<span data-ttu-id="26851-237">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="26851-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26851-238">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="26851-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26851-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26851-239">CommonParameters</span></span>
<span data-ttu-id="26851-240">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26851-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26851-241">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26851-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26851-242">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26851-242">INPUTS</span></span>

### <span data-ttu-id="26851-243">System. String</span><span class="sxs-lookup"><span data-stu-id="26851-243">System.String</span></span>

### <span data-ttu-id="26851-244">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="26851-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="26851-245">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="26851-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="26851-246">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="26851-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="26851-247">System. String []</span><span class="sxs-lookup"><span data-stu-id="26851-247">System.String[]</span></span>

## <span data-ttu-id="26851-248">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26851-248">OUTPUTS</span></span>

### <span data-ttu-id="26851-249">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="26851-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="26851-250">Пуск</span><span class="sxs-lookup"><span data-stu-id="26851-250">NOTES</span></span>

## <span data-ttu-id="26851-251">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26851-251">RELATED LINKS</span></span>

[<span data-ttu-id="26851-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="26851-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="26851-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="26851-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="26851-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="26851-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


