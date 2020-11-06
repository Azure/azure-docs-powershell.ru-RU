---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 231787f57061ff4e118510c3dc166915b39da436
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563380"
---
# <span data-ttu-id="02a0b-101">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="02a0b-101">Get-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="02a0b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="02a0b-103">Получение правил брандмауэра, заданных для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="02a0b-103">Get firewall rules set on Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02a0b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02a0b-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02a0b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02a0b-105">DESCRIPTION</span></span>
<span data-ttu-id="02a0b-106">Если параметр **RuleName** задан, командлет **Get-AzureRmRedisCacheFirewallRule** получает подробные сведения о указанном правиле брандмауэра для кэша Redis Azure.</span><span class="sxs-lookup"><span data-stu-id="02a0b-106">If **RuleName** parameter if provided, **Get-AzureRmRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="02a0b-107">Если задано только **имя** , эта операция получает все правила брандмауэра, доступные в этом кэше Redis.</span><span class="sxs-lookup"><span data-stu-id="02a0b-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="02a0b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02a0b-108">EXAMPLES</span></span>

### <span data-ttu-id="02a0b-109">Пример 1: получение отдельного правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="02a0b-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="02a0b-110">Эта команда получает правило брандмауэра с именем ruleone из кэша Redis с именем mycache.</span><span class="sxs-lookup"><span data-stu-id="02a0b-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="02a0b-111">Пример 2: получение всех правил брандмауэра</span><span class="sxs-lookup"><span data-stu-id="02a0b-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache"

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

<span data-ttu-id="02a0b-112">Эта команда получает все правила брандмауэра из кэша Redis с именем mycache.</span><span class="sxs-lookup"><span data-stu-id="02a0b-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="02a0b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02a0b-113">PARAMETERS</span></span>

### <span data-ttu-id="02a0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a0b-114">-DefaultProfile</span></span>
<span data-ttu-id="02a0b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02a0b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02a0b-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="02a0b-116">-Name</span></span>
<span data-ttu-id="02a0b-117">Имя кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="02a0b-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="02a0b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a0b-118">-ResourceGroupName</span></span>
<span data-ttu-id="02a0b-119">Имя группы ресурсов, в которой находится кэш.</span><span class="sxs-lookup"><span data-stu-id="02a0b-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="02a0b-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="02a0b-120">-RuleName</span></span>
<span data-ttu-id="02a0b-121">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="02a0b-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="02a0b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a0b-122">CommonParameters</span></span>
<span data-ttu-id="02a0b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02a0b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a0b-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a0b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a0b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02a0b-125">INPUTS</span></span>

### <span data-ttu-id="02a0b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="02a0b-126">System.String</span></span>
<span data-ttu-id="02a0b-127">Вы можете передавать входные данные командлету по имени, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="02a0b-127">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="02a0b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02a0b-128">OUTPUTS</span></span>

### <span data-ttu-id="02a0b-129">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule, Microsoft. Azure. Commands. RedisCache, Version = 4.0.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="02a0b-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule, Microsoft.Azure.Commands.RedisCache, Version=4.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="02a0b-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="02a0b-130">NOTES</span></span>

## <span data-ttu-id="02a0b-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02a0b-131">RELATED LINKS</span></span>

[<span data-ttu-id="02a0b-132">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="02a0b-132">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="02a0b-133">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="02a0b-133">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="02a0b-134">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="02a0b-134">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="02a0b-135">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="02a0b-135">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="02a0b-136">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="02a0b-136">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="02a0b-137">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="02a0b-137">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
