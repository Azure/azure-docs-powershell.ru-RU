---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
ms.openlocfilehash: cc8d6ff7e7fb55c5ee71c82a8eca4cc661b98b07
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417527"
---
# <span data-ttu-id="ebfab-101">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ebfab-101">Get-AzRedisCache</span></span>

## <span data-ttu-id="ebfab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebfab-102">SYNOPSIS</span></span>
<span data-ttu-id="ebfab-103">Возвращает кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="ebfab-103">Gets a Redis Cache.</span></span>

## <span data-ttu-id="ebfab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ebfab-104">SYNTAX</span></span>

```
Get-AzRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebfab-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebfab-105">DESCRIPTION</span></span>
<span data-ttu-id="ebfab-106">Для **указанного кэша Azure Redis Cache** возвращается указанный cmdlet Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="ebfab-106">The **Get-AzRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="ebfab-107">Если параметры не указаны, эта операция возвращает каждый кэш Redis для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="ebfab-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="ebfab-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ebfab-108">EXAMPLES</span></span>

### <span data-ttu-id="ebfab-109">Пример 1. Получить кэш Redis по имени</span><span class="sxs-lookup"><span data-stu-id="ebfab-109">Example 1: Get a Redis Cache by name</span></span>
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

<span data-ttu-id="ebfab-110">Эта команда получает кэш Redis с именами myexists.</span><span class="sxs-lookup"><span data-stu-id="ebfab-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="ebfab-111">Пример 2. Все кэш Redis в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="ebfab-111">Example 2: Get every Redis Cache in a resource group</span></span>
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

<span data-ttu-id="ebfab-112">Эта команда возвращает каждый кэш Redis в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ebfab-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="ebfab-113">Пример 3. Получите все кэш Redis в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="ebfab-113">Example 3: Get every Redis Cache in the current subscription</span></span>
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

<span data-ttu-id="ebfab-114">Эта команда возвращает каждый кэш Redis в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="ebfab-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="ebfab-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebfab-115">PARAMETERS</span></span>

### <span data-ttu-id="ebfab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebfab-116">-DefaultProfile</span></span>
<span data-ttu-id="ebfab-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebfab-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebfab-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ebfab-118">-Name</span></span>
<span data-ttu-id="ebfab-119">Имя кэша Redis, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="ebfab-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="ebfab-120">Используется с *параметром ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="ebfab-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="ebfab-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebfab-121">-ResourceGroupName</span></span>
<span data-ttu-id="ebfab-122">Имя группы ресурсов, которая содержит кэш Redis, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="ebfab-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="ebfab-123">Если указать только параметр *ResourceGroupName,* эта операция возвращает каждый кэш Redis в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ebfab-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="ebfab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebfab-124">CommonParameters</span></span>
<span data-ttu-id="ebfab-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebfab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebfab-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebfab-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebfab-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebfab-127">INPUTS</span></span>

### <span data-ttu-id="ebfab-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ebfab-128">System.String</span></span>

## <span data-ttu-id="ebfab-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ebfab-129">OUTPUTS</span></span>

### <span data-ttu-id="ebfab-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="ebfab-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="ebfab-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ebfab-131">NOTES</span></span>

## <span data-ttu-id="ebfab-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebfab-132">RELATED LINKS</span></span>

[<span data-ttu-id="ebfab-133">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ebfab-133">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="ebfab-134">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ebfab-134">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="ebfab-135">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ebfab-135">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


