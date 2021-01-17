---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 8e28951f826c5a049f345bb3182bda10e7de82fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421215"
---
# <span data-ttu-id="dbdce-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dbdce-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="dbdce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbdce-102">SYNOPSIS</span></span>
<span data-ttu-id="dbdce-103">Установите правила брандмауэра для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="dbdce-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="dbdce-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dbdce-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbdce-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbdce-105">DESCRIPTION</span></span>
<span data-ttu-id="dbdce-106">Если **параметр RuleName** указан, то для **azure RedisCacheFirewallRule** можно получить подробные данные о заданном правиле брандмауэра в кэше Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="dbdce-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="dbdce-107">Если **задано только** имя, в кэше Redis доступны все правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="dbdce-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="dbdce-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dbdce-108">EXAMPLES</span></span>

### <span data-ttu-id="dbdce-109">Пример 1. Получите одно правило брандмауэра</span><span class="sxs-lookup"><span data-stu-id="dbdce-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="dbdce-110">Эта команда получает правило брандмауэра с именем ruleone из кэша Redis с именем mycache.</span><span class="sxs-lookup"><span data-stu-id="dbdce-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="dbdce-111">Пример 2. Получить все правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="dbdce-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruletwo
        RuleName          : ruletwo
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.33
        EndIP             : 10.0.0.64
```

<span data-ttu-id="dbdce-112">Эта команда получает все правила брандмауэра из кэша Redis, который называется mycache.</span><span class="sxs-lookup"><span data-stu-id="dbdce-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="dbdce-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbdce-113">PARAMETERS</span></span>

### <span data-ttu-id="dbdce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbdce-114">-DefaultProfile</span></span>
<span data-ttu-id="dbdce-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dbdce-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbdce-116">-Name</span><span class="sxs-lookup"><span data-stu-id="dbdce-116">-Name</span></span>
<span data-ttu-id="dbdce-117">Имя кэша redis.</span><span class="sxs-lookup"><span data-stu-id="dbdce-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="dbdce-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbdce-118">-ResourceGroupName</span></span>
<span data-ttu-id="dbdce-119">Имя группы ресурсов, в которой есть кэш.</span><span class="sxs-lookup"><span data-stu-id="dbdce-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="dbdce-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="dbdce-120">-RuleName</span></span>
<span data-ttu-id="dbdce-121">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="dbdce-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="dbdce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbdce-122">CommonParameters</span></span>
<span data-ttu-id="dbdce-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbdce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbdce-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbdce-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbdce-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbdce-125">INPUTS</span></span>

### <span data-ttu-id="dbdce-126">System.String</span><span class="sxs-lookup"><span data-stu-id="dbdce-126">System.String</span></span>

## <span data-ttu-id="dbdce-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dbdce-127">OUTPUTS</span></span>

### <span data-ttu-id="dbdce-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dbdce-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="dbdce-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dbdce-129">NOTES</span></span>

## <span data-ttu-id="dbdce-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dbdce-130">RELATED LINKS</span></span>

[<span data-ttu-id="dbdce-131">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dbdce-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="dbdce-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dbdce-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="dbdce-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dbdce-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="dbdce-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dbdce-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="dbdce-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dbdce-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="dbdce-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dbdce-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)