---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: ab0b84578339568e48458de8a89daccd83092e65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904785"
---
# <span data-ttu-id="31f95-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="31f95-101">New-AzRedisCache</span></span>

## <span data-ttu-id="31f95-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31f95-102">SYNOPSIS</span></span>
<span data-ttu-id="31f95-103">Создание кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="31f95-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="31f95-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31f95-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31f95-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31f95-105">DESCRIPTION</span></span>
<span data-ttu-id="31f95-106">Командлет **New-AzRedisCache** создает кэш Redis Azure.</span><span class="sxs-lookup"><span data-stu-id="31f95-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="31f95-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31f95-107">EXAMPLES</span></span>

### <span data-ttu-id="31f95-108">Пример 1: создание кэша Redis</span><span class="sxs-lookup"><span data-stu-id="31f95-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="31f95-109">Эта команда создает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="31f95-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="31f95-110">Пример 2: создание стандартного кэша Redis для SKU</span><span class="sxs-lookup"><span data-stu-id="31f95-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="31f95-111">Эта команда создает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="31f95-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="31f95-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31f95-112">PARAMETERS</span></span>

### <span data-ttu-id="31f95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f95-113">-DefaultProfile</span></span>
<span data-ttu-id="31f95-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31f95-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31f95-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="31f95-115">-EnableNonSslPort</span></span>
<span data-ttu-id="31f95-116">Указывает, включен ли порт без SSL.</span><span class="sxs-lookup"><span data-stu-id="31f95-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="31f95-117">Значение по умолчанию — $False (порт без SSL отключен).</span><span class="sxs-lookup"><span data-stu-id="31f95-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="31f95-118">-Location</span><span class="sxs-lookup"><span data-stu-id="31f95-118">-Location</span></span>
<span data-ttu-id="31f95-119">Указывает место для создания кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="31f95-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="31f95-120">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="31f95-120">Valid values are:</span></span> 
- <span data-ttu-id="31f95-121">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="31f95-121">North Central US</span></span>
- <span data-ttu-id="31f95-122">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="31f95-122">South Central US</span></span>
- <span data-ttu-id="31f95-123">Центральная американская</span><span class="sxs-lookup"><span data-stu-id="31f95-123">Central US</span></span>
- <span data-ttu-id="31f95-124">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="31f95-124">West Europe</span></span>
- <span data-ttu-id="31f95-125">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="31f95-125">North Europe</span></span>
- <span data-ttu-id="31f95-126">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="31f95-126">West US</span></span>
- <span data-ttu-id="31f95-127">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="31f95-127">East US</span></span>
- <span data-ttu-id="31f95-128">Восточная часть 2</span><span class="sxs-lookup"><span data-stu-id="31f95-128">East US 2</span></span>
- <span data-ttu-id="31f95-129">Восточная Япония</span><span class="sxs-lookup"><span data-stu-id="31f95-129">Japan East</span></span>
- <span data-ttu-id="31f95-130">Западная часть Японии</span><span class="sxs-lookup"><span data-stu-id="31f95-130">Japan West</span></span>
- <span data-ttu-id="31f95-131">Южная Бразилия</span><span class="sxs-lookup"><span data-stu-id="31f95-131">Brazil South</span></span>
- <span data-ttu-id="31f95-132">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="31f95-132">Southeast Asia</span></span>
- <span data-ttu-id="31f95-133">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="31f95-133">East Asia</span></span>
- <span data-ttu-id="31f95-134">Восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="31f95-134">Australia East</span></span>
- <span data-ttu-id="31f95-135">Юго-восток Австралии</span><span class="sxs-lookup"><span data-stu-id="31f95-135">Australia Southeast</span></span>

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

### <span data-ttu-id="31f95-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31f95-136">-Name</span></span>
<span data-ttu-id="31f95-137">Указывает имя создаваемого кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="31f95-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="31f95-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="31f95-138">-RedisConfiguration</span></span>
<span data-ttu-id="31f95-139">Задает параметры конфигурации Redis.</span><span class="sxs-lookup"><span data-stu-id="31f95-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="31f95-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="31f95-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="31f95-141">RDB — включена резервная копия.</span><span class="sxs-lookup"><span data-stu-id="31f95-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="31f95-142">Указывает на то, что сохраняемость данных Redis включена.</span><span class="sxs-lookup"><span data-stu-id="31f95-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="31f95-143">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="31f95-143">Premium tier only.</span></span>
- <span data-ttu-id="31f95-144">RDB — строка подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="31f95-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="31f95-145">Задает строку подключения к учетной записи хранения для Redis сохраняемости данных.</span><span class="sxs-lookup"><span data-stu-id="31f95-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="31f95-146">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="31f95-146">Premium tier only.</span></span>
- <span data-ttu-id="31f95-147">RDB — периодичность резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="31f95-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="31f95-148">Указывает периодичность резервного копирования для сохраняемости данных Redis.</span><span class="sxs-lookup"><span data-stu-id="31f95-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="31f95-149">Только уровень Premium.</span><span class="sxs-lookup"><span data-stu-id="31f95-149">Premium tier only.</span></span> 
- <span data-ttu-id="31f95-150">MaxMemory — зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="31f95-150">maxmemory-reserved.</span></span>
<span data-ttu-id="31f95-151">Настраивает память, зарезервированную для процессов без кэширования.</span><span class="sxs-lookup"><span data-stu-id="31f95-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="31f95-152">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="31f95-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="31f95-153">MaxMemory — политика.</span><span class="sxs-lookup"><span data-stu-id="31f95-153">maxmemory-policy.</span></span>
<span data-ttu-id="31f95-154">Настройка политики вытеснения для кэша.</span><span class="sxs-lookup"><span data-stu-id="31f95-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="31f95-155">Все ценовые категории.</span><span class="sxs-lookup"><span data-stu-id="31f95-155">All pricing tiers.</span></span> 
- <span data-ttu-id="31f95-156">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="31f95-156">notify-keyspace-events.</span></span>
<span data-ttu-id="31f95-157">Настраивает уведомления keyspace.</span><span class="sxs-lookup"><span data-stu-id="31f95-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="31f95-158">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="31f95-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="31f95-159">хэш-максимум-ziplist-записи.</span><span class="sxs-lookup"><span data-stu-id="31f95-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="31f95-160">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="31f95-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="31f95-161">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="31f95-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="31f95-162">hash-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="31f95-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="31f95-163">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="31f95-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="31f95-164">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="31f95-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="31f95-165">Set-Max-intset-"записи".</span><span class="sxs-lookup"><span data-stu-id="31f95-165">set-max-intset-entries.</span></span>
<span data-ttu-id="31f95-166">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="31f95-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="31f95-167">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="31f95-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="31f95-168">zset-Max-ziplist-(записи).</span><span class="sxs-lookup"><span data-stu-id="31f95-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="31f95-169">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="31f95-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="31f95-170">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="31f95-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="31f95-171">zset-Max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="31f95-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="31f95-172">Настройка оптимизации памяти для небольших типов данных агрегатов.</span><span class="sxs-lookup"><span data-stu-id="31f95-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="31f95-173">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="31f95-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="31f95-174">баз данных.</span><span class="sxs-lookup"><span data-stu-id="31f95-174">databases.</span></span>
<span data-ttu-id="31f95-175">Настраивает количество баз данных.</span><span class="sxs-lookup"><span data-stu-id="31f95-175">Configures the number of databases.</span></span>
<span data-ttu-id="31f95-176">Это свойство можно настроить только при создании кэша.</span><span class="sxs-lookup"><span data-stu-id="31f95-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="31f95-177">Уровни Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="31f95-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="31f95-178">Дополнительные сведения можно найти в разделе Управление кэшем Redis Azure с помощью Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="31f95-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="31f95-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f95-179">-ResourceGroupName</span></span>
<span data-ttu-id="31f95-180">Указывает имя группы ресурсов, в которой нужно создать кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="31f95-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="31f95-181">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="31f95-181">-ShardCount</span></span>
<span data-ttu-id="31f95-182">Задает количество сегментов для создания в кэше высококачественных кластеров.</span><span class="sxs-lookup"><span data-stu-id="31f95-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="31f95-183">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="31f95-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="31f95-184">1,1</span><span class="sxs-lookup"><span data-stu-id="31f95-184">1</span></span>
- <span data-ttu-id="31f95-185">2</span><span class="sxs-lookup"><span data-stu-id="31f95-185">2</span></span>
- <span data-ttu-id="31f95-186">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="31f95-186">3</span></span>
- <span data-ttu-id="31f95-187">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="31f95-187">4</span></span>
- <span data-ttu-id="31f95-188">5</span><span class="sxs-lookup"><span data-stu-id="31f95-188">5</span></span>
- <span data-ttu-id="31f95-189">152</span><span class="sxs-lookup"><span data-stu-id="31f95-189">6</span></span>
- <span data-ttu-id="31f95-190">5-7</span><span class="sxs-lookup"><span data-stu-id="31f95-190">7</span></span>
- <span data-ttu-id="31f95-191">No8</span><span class="sxs-lookup"><span data-stu-id="31f95-191">8</span></span>
- <span data-ttu-id="31f95-192">@</span><span class="sxs-lookup"><span data-stu-id="31f95-192">9</span></span> 
- <span data-ttu-id="31f95-193">5-10</span><span class="sxs-lookup"><span data-stu-id="31f95-193">10</span></span>

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

### <span data-ttu-id="31f95-194">-Size</span><span class="sxs-lookup"><span data-stu-id="31f95-194">-Size</span></span>
<span data-ttu-id="31f95-195">Задает размер кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="31f95-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="31f95-196">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="31f95-196">Valid values are:</span></span> 
- <span data-ttu-id="31f95-197">P1</span><span class="sxs-lookup"><span data-stu-id="31f95-197">P1</span></span>
- <span data-ttu-id="31f95-198">–</span><span class="sxs-lookup"><span data-stu-id="31f95-198">P2</span></span>
- <span data-ttu-id="31f95-199">–</span><span class="sxs-lookup"><span data-stu-id="31f95-199">P3</span></span>
- <span data-ttu-id="31f95-200">P4</span><span class="sxs-lookup"><span data-stu-id="31f95-200">P4</span></span>
- <span data-ttu-id="31f95-201">C0</span><span class="sxs-lookup"><span data-stu-id="31f95-201">C0</span></span>
- <span data-ttu-id="31f95-202">C1</span><span class="sxs-lookup"><span data-stu-id="31f95-202">C1</span></span>
- <span data-ttu-id="31f95-203">Режим</span><span class="sxs-lookup"><span data-stu-id="31f95-203">C2</span></span>
- <span data-ttu-id="31f95-204">Ячейку</span><span class="sxs-lookup"><span data-stu-id="31f95-204">C3</span></span>
- <span data-ttu-id="31f95-205">C4</span><span class="sxs-lookup"><span data-stu-id="31f95-205">C4</span></span>
- <span data-ttu-id="31f95-206">C5</span><span class="sxs-lookup"><span data-stu-id="31f95-206">C5</span></span>
- <span data-ttu-id="31f95-207">C6</span><span class="sxs-lookup"><span data-stu-id="31f95-207">C6</span></span>
- <span data-ttu-id="31f95-208">250MB</span><span class="sxs-lookup"><span data-stu-id="31f95-208">250MB</span></span>
- <span data-ttu-id="31f95-209">Гбайт</span><span class="sxs-lookup"><span data-stu-id="31f95-209">1GB</span></span>
- <span data-ttu-id="31f95-210">2,5 ГБ</span><span class="sxs-lookup"><span data-stu-id="31f95-210">2.5GB</span></span>
- <span data-ttu-id="31f95-211">6GB</span><span class="sxs-lookup"><span data-stu-id="31f95-211">6GB</span></span>
- <span data-ttu-id="31f95-212">13GB</span><span class="sxs-lookup"><span data-stu-id="31f95-212">13GB</span></span>
- <span data-ttu-id="31f95-213">26GB</span><span class="sxs-lookup"><span data-stu-id="31f95-213">26GB</span></span>
- <span data-ttu-id="31f95-214">53GB значение по умолчанию — 1 ГБ или C1.</span><span class="sxs-lookup"><span data-stu-id="31f95-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="31f95-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="31f95-215">-Sku</span></span>
<span data-ttu-id="31f95-216">Указывает SKU кэша Redis для создания.</span><span class="sxs-lookup"><span data-stu-id="31f95-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="31f95-217">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="31f95-217">Valid values are:</span></span> 
- <span data-ttu-id="31f95-218">Базового</span><span class="sxs-lookup"><span data-stu-id="31f95-218">Basic</span></span>
- <span data-ttu-id="31f95-219">Стандартная</span><span class="sxs-lookup"><span data-stu-id="31f95-219">Standard</span></span>
- <span data-ttu-id="31f95-220">Premium по умолчанию используется значение Standard.</span><span class="sxs-lookup"><span data-stu-id="31f95-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="31f95-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="31f95-221">-StaticIP</span></span>
<span data-ttu-id="31f95-222">Задает уникальный IP-адрес в подсети для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="31f95-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="31f95-223">Если вы не укажете значение для этого параметра, этот командлет выберет IP-адрес из подсети.</span><span class="sxs-lookup"><span data-stu-id="31f95-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="31f95-224">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="31f95-224">-SubnetId</span></span>
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

### <span data-ttu-id="31f95-225">-Тег</span><span class="sxs-lookup"><span data-stu-id="31f95-225">-Tag</span></span>
<span data-ttu-id="31f95-226">Хэш-таблица, представляющая Теги.</span><span class="sxs-lookup"><span data-stu-id="31f95-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="31f95-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="31f95-227">-TenantSettings</span></span>
<span data-ttu-id="31f95-228">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="31f95-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="31f95-229">-Zone</span><span class="sxs-lookup"><span data-stu-id="31f95-229">-Zone</span></span>
<span data-ttu-id="31f95-230">Список зон.</span><span class="sxs-lookup"><span data-stu-id="31f95-230">List of zones.</span></span>

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

### <span data-ttu-id="31f95-231">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31f95-231">-Confirm</span></span>
<span data-ttu-id="31f95-232">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="31f95-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31f95-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31f95-233">-WhatIf</span></span>
<span data-ttu-id="31f95-234">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="31f95-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31f95-235">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="31f95-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31f95-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f95-236">CommonParameters</span></span>
<span data-ttu-id="31f95-237">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31f95-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f95-238">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31f95-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f95-239">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31f95-239">INPUTS</span></span>

### <span data-ttu-id="31f95-240">System. String</span><span class="sxs-lookup"><span data-stu-id="31f95-240">System.String</span></span>

### <span data-ttu-id="31f95-241">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="31f95-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="31f95-242">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="31f95-242">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="31f95-243">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="31f95-243">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="31f95-244">System. String []</span><span class="sxs-lookup"><span data-stu-id="31f95-244">System.String[]</span></span>

## <span data-ttu-id="31f95-245">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31f95-245">OUTPUTS</span></span>

### <span data-ttu-id="31f95-246">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="31f95-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="31f95-247">Пуск</span><span class="sxs-lookup"><span data-stu-id="31f95-247">NOTES</span></span>

## <span data-ttu-id="31f95-248">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31f95-248">RELATED LINKS</span></span>

[<span data-ttu-id="31f95-249">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="31f95-249">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="31f95-250">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="31f95-250">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="31f95-251">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="31f95-251">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


