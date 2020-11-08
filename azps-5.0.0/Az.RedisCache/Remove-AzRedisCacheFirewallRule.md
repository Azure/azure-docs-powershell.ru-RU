---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: c19be1f524519a55a5a95a575e97cfd250952570
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247550"
---
# <span data-ttu-id="6f466-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6f466-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="6f466-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f466-102">SYNOPSIS</span></span>
<span data-ttu-id="6f466-103">Удаление правила брандмауэра из кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="6f466-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="6f466-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f466-104">SYNTAX</span></span>

### <span data-ttu-id="6f466-105">NormalParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f466-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f466-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="6f466-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f466-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f466-107">DESCRIPTION</span></span>
<span data-ttu-id="6f466-108">Удаление правила брандмауэра из кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="6f466-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="6f466-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f466-109">EXAMPLES</span></span>

### <span data-ttu-id="6f466-110">Пример 1: Удаление одного правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="6f466-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="6f466-111">Эта команда удаляет правило брандмауэра с именем ruleone из кэша Redis с именем mycache.</span><span class="sxs-lookup"><span data-stu-id="6f466-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="6f466-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f466-112">PARAMETERS</span></span>

### <span data-ttu-id="6f466-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f466-113">-DefaultProfile</span></span>
<span data-ttu-id="6f466-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f466-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f466-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f466-115">-InputObject</span></span>
<span data-ttu-id="6f466-116">Объект типа PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6f466-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="6f466-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6f466-117">-Name</span></span>
<span data-ttu-id="6f466-118">Имя кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="6f466-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="6f466-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f466-119">-PassThru</span></span>
<span data-ttu-id="6f466-120">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="6f466-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6f466-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f466-121">-ResourceGroupName</span></span>
<span data-ttu-id="6f466-122">Имя группы ресурсов, в которой находится кэш.</span><span class="sxs-lookup"><span data-stu-id="6f466-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="6f466-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="6f466-123">-RuleName</span></span>
<span data-ttu-id="6f466-124">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="6f466-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="6f466-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f466-125">-Confirm</span></span>
<span data-ttu-id="6f466-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6f466-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f466-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f466-127">-WhatIf</span></span>
<span data-ttu-id="6f466-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6f466-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f466-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6f466-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f466-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f466-130">CommonParameters</span></span>
<span data-ttu-id="6f466-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f466-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f466-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f466-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f466-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f466-133">INPUTS</span></span>

### <span data-ttu-id="6f466-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6f466-134">System.String</span></span>

### <span data-ttu-id="6f466-135">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6f466-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="6f466-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f466-136">OUTPUTS</span></span>

### <span data-ttu-id="6f466-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f466-137">System.Boolean</span></span>

## <span data-ttu-id="6f466-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f466-138">NOTES</span></span>

## <span data-ttu-id="6f466-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f466-139">RELATED LINKS</span></span>

[<span data-ttu-id="6f466-140">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6f466-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="6f466-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6f466-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="6f466-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6f466-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="6f466-143">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6f466-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="6f466-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6f466-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="6f466-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6f466-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)