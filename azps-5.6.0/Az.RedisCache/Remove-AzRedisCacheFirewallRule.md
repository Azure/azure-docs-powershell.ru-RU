---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 9c68e89d09d386d6071cb639fa77ba740a6da53f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972664"
---
# <span data-ttu-id="c8e12-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c8e12-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="c8e12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8e12-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e12-103">Удаление правила брандмауэра из кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="c8e12-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="c8e12-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c8e12-104">SYNTAX</span></span>

### <span data-ttu-id="c8e12-105">NormalParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8e12-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8e12-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="c8e12-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8e12-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8e12-107">DESCRIPTION</span></span>
<span data-ttu-id="c8e12-108">Удаление правила брандмауэра из кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="c8e12-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="c8e12-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c8e12-109">EXAMPLES</span></span>

### <span data-ttu-id="c8e12-110">Пример 1. Удаление одного правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="c8e12-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="c8e12-111">Эта команда удаляет правило брандмауэра с именем ruleone из кэша Redis с именем mycache.</span><span class="sxs-lookup"><span data-stu-id="c8e12-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="c8e12-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8e12-112">PARAMETERS</span></span>

### <span data-ttu-id="c8e12-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8e12-113">-DefaultProfile</span></span>
<span data-ttu-id="c8e12-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e12-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8e12-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8e12-115">-InputObject</span></span>
<span data-ttu-id="c8e12-116">объект типа PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c8e12-116">object of type PSRedisFirewallRule</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule
Parameter Sets: PSRedisFirewallRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e12-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c8e12-117">-Name</span></span>
<span data-ttu-id="c8e12-118">Имя кэша redis.</span><span class="sxs-lookup"><span data-stu-id="c8e12-118">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e12-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8e12-119">-PassThru</span></span>
<span data-ttu-id="c8e12-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c8e12-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8e12-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8e12-121">-ResourceGroupName</span></span>
<span data-ttu-id="c8e12-122">Имя группы ресурсов, в которой есть кэш.</span><span class="sxs-lookup"><span data-stu-id="c8e12-122">Name of resource group in which cache exists.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e12-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="c8e12-123">-RuleName</span></span>
<span data-ttu-id="c8e12-124">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="c8e12-124">Name of firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e12-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8e12-125">-Confirm</span></span>
<span data-ttu-id="c8e12-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8e12-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8e12-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8e12-127">-WhatIf</span></span>
<span data-ttu-id="c8e12-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8e12-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8e12-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c8e12-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8e12-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e12-130">CommonParameters</span></span>
<span data-ttu-id="c8e12-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8e12-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e12-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8e12-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e12-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8e12-133">INPUTS</span></span>

### <span data-ttu-id="c8e12-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c8e12-134">System.String</span></span>

### <span data-ttu-id="c8e12-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c8e12-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="c8e12-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c8e12-136">OUTPUTS</span></span>

### <span data-ttu-id="c8e12-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c8e12-137">System.Boolean</span></span>

## <span data-ttu-id="c8e12-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c8e12-138">NOTES</span></span>

## <span data-ttu-id="c8e12-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8e12-139">RELATED LINKS</span></span>

[<span data-ttu-id="c8e12-140">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c8e12-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="c8e12-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c8e12-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="c8e12-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c8e12-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="c8e12-143">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c8e12-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="c8e12-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c8e12-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="c8e12-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c8e12-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)