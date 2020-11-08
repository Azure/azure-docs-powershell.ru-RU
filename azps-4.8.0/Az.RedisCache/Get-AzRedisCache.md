---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
ms.openlocfilehash: cc8d6ff7e7fb55c5ee71c82a8eca4cc661b98b07
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242711"
---
# <span data-ttu-id="aba62-101">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="aba62-101">Get-AzRedisCache</span></span>

## <span data-ttu-id="aba62-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aba62-102">SYNOPSIS</span></span>
<span data-ttu-id="aba62-103">Возвращает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="aba62-103">Gets a Redis Cache.</span></span>

## <span data-ttu-id="aba62-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aba62-104">SYNTAX</span></span>

```
Get-AzRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aba62-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aba62-105">DESCRIPTION</span></span>
<span data-ttu-id="aba62-106">Командлет **Get-AzRedisCache** получает указанный кэш Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="aba62-106">The **Get-AzRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="aba62-107">Если вы укажете параметр "нет", эта операция возвращает каждый кэш Redis для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="aba62-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="aba62-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aba62-108">EXAMPLES</span></span>

### <span data-ttu-id="aba62-109">Пример 1: получение кэша Redis по имени</span><span class="sxs-lookup"><span data-stu-id="aba62-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzRedisCache -Name "myexists"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="aba62-110">Эта команда получает кэш Redis с именем myexists.</span><span class="sxs-lookup"><span data-stu-id="aba62-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="aba62-111">Пример 2: получение каждого кэша Redis в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="aba62-111">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzRedisCache -ResourceGroupName "myGroup"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="aba62-112">Эта команда возвращает каждый кэш Redis в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aba62-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="aba62-113">Пример 3: получение всех Redis кэша в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="aba62-113">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzRedisCache

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup2
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup2/providers/Microsoft.Cache/Redis/myearlier2
        Location           : North Central US
        Name               : myearlier2
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier2.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="aba62-114">Эта команда возвращает каждый кэш Redis в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="aba62-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="aba62-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aba62-115">PARAMETERS</span></span>

### <span data-ttu-id="aba62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba62-116">-DefaultProfile</span></span>
<span data-ttu-id="aba62-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aba62-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aba62-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aba62-118">-Name</span></span>
<span data-ttu-id="aba62-119">Указывает имя кэша Redis, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="aba62-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="aba62-120">Использование с параметром *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="aba62-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="aba62-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aba62-121">-ResourceGroupName</span></span>
<span data-ttu-id="aba62-122">Указывает имя группы ресурсов, содержащей кэш Redis, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="aba62-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="aba62-123">Если указан только параметр *ResourceGroupName* , эта операция возвращает каждый кэш Redis в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aba62-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="aba62-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba62-124">CommonParameters</span></span>
<span data-ttu-id="aba62-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aba62-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba62-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aba62-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba62-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aba62-127">INPUTS</span></span>

### <span data-ttu-id="aba62-128">System. String</span><span class="sxs-lookup"><span data-stu-id="aba62-128">System.String</span></span>

## <span data-ttu-id="aba62-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aba62-129">OUTPUTS</span></span>

### <span data-ttu-id="aba62-130">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="aba62-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="aba62-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="aba62-131">NOTES</span></span>

## <span data-ttu-id="aba62-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aba62-132">RELATED LINKS</span></span>

[<span data-ttu-id="aba62-133">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="aba62-133">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="aba62-134">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="aba62-134">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="aba62-135">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="aba62-135">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


