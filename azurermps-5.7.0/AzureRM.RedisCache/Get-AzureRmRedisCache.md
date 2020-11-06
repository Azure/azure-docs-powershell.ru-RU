---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: 1e91aa946e89b8231ea2c58b28c686d603855ada
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563384"
---
# <span data-ttu-id="c6834-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c6834-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="c6834-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6834-102">SYNOPSIS</span></span>
<span data-ttu-id="c6834-103">Возвращает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="c6834-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6834-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6834-104">SYNTAX</span></span>

```
Get-AzureRmRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6834-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6834-105">DESCRIPTION</span></span>
<span data-ttu-id="c6834-106">Командлет **Get-AzureRmRedisCache** получает указанный кэш Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="c6834-106">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="c6834-107">Если вы укажете параметр "нет", эта операция возвращает каждый кэш Redis для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="c6834-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="c6834-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6834-108">EXAMPLES</span></span>

### <span data-ttu-id="c6834-109">Пример 1: получение кэша Redis по имени</span><span class="sxs-lookup"><span data-stu-id="c6834-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzureRmRedisCache -Name "myexists"

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

<span data-ttu-id="c6834-110">Эта команда получает кэш Redis с именем myexists.</span><span class="sxs-lookup"><span data-stu-id="c6834-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="c6834-111">Пример 2: получение каждого кэша Redis в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="c6834-111">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup"

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

<span data-ttu-id="c6834-112">Эта команда возвращает каждый кэш Redis в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c6834-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="c6834-113">Пример 3: получение всех Redis кэша в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="c6834-113">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzureRmRedisCache

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

<span data-ttu-id="c6834-114">Эта команда возвращает каждый кэш Redis в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="c6834-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="c6834-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6834-115">PARAMETERS</span></span>

### <span data-ttu-id="c6834-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6834-116">-DefaultProfile</span></span>
<span data-ttu-id="c6834-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6834-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6834-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c6834-118">-Name</span></span>
<span data-ttu-id="c6834-119">Указывает имя кэша Redis, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="c6834-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="c6834-120">Использование с параметром *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="c6834-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="c6834-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6834-121">-ResourceGroupName</span></span>
<span data-ttu-id="c6834-122">Указывает имя группы ресурсов, содержащей кэш Redis, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="c6834-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>

<span data-ttu-id="c6834-123">Если указан только параметр *ResourceGroupName* , эта операция возвращает каждый кэш Redis в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c6834-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="c6834-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6834-124">CommonParameters</span></span>
<span data-ttu-id="c6834-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6834-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6834-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6834-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6834-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6834-127">INPUTS</span></span>

### <span data-ttu-id="c6834-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="c6834-128">None</span></span>
<span data-ttu-id="c6834-129">Вы можете передавать входные данные командлету по имени, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="c6834-129">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="c6834-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6834-130">OUTPUTS</span></span>

### <span data-ttu-id="c6834-131">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="c6834-131">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="c6834-132">Возвращает массив объектов **RedisCacheAttributes** .</span><span class="sxs-lookup"><span data-stu-id="c6834-132">Returns an array of **RedisCacheAttributes** objects.</span></span>

## <span data-ttu-id="c6834-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6834-133">NOTES</span></span>

## <span data-ttu-id="c6834-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6834-134">RELATED LINKS</span></span>

[<span data-ttu-id="c6834-135">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c6834-135">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="c6834-136">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c6834-136">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="c6834-137">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c6834-137">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


