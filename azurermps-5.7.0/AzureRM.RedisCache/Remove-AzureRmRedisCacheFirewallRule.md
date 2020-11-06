---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 7f2e9a3bb54aab9def9eba7bdc2a84680fe121c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557200"
---
# <span data-ttu-id="6dca1-101">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6dca1-101">Remove-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="6dca1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6dca1-102">SYNOPSIS</span></span>
<span data-ttu-id="6dca1-103">Удаление правила брандмауэра из кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="6dca1-103">Remove a firewall rule from a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dca1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6dca1-104">SYNTAX</span></span>

### <span data-ttu-id="6dca1-105">NormalParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6dca1-105">NormalParameterSet (Default)</span></span>
```
Remove-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dca1-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="6dca1-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzureRmRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dca1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dca1-107">DESCRIPTION</span></span>
<span data-ttu-id="6dca1-108">Удаление правила брандмауэра из кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="6dca1-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="6dca1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6dca1-109">EXAMPLES</span></span>

### <span data-ttu-id="6dca1-110">Пример 1: Удаление одного правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="6dca1-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="6dca1-111">Эта команда удаляет правило брандмауэра с именем ruleone из кэша Redis с именем mycache.</span><span class="sxs-lookup"><span data-stu-id="6dca1-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="6dca1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6dca1-112">PARAMETERS</span></span>

### <span data-ttu-id="6dca1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dca1-113">-DefaultProfile</span></span>
<span data-ttu-id="6dca1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6dca1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dca1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dca1-115">-InputObject</span></span>
<span data-ttu-id="6dca1-116">Объект типа PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6dca1-116">object of type PSRedisFirewallRule</span></span>

```yaml
Type: PSRedisFirewallRule
Parameter Sets: PSRedisFirewallRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6dca1-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6dca1-117">-Name</span></span>
<span data-ttu-id="6dca1-118">Имя кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="6dca1-118">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dca1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6dca1-119">-PassThru</span></span>
<span data-ttu-id="6dca1-120">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="6dca1-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dca1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dca1-121">-ResourceGroupName</span></span>
<span data-ttu-id="6dca1-122">Имя группы ресурсов, в которой находится кэш.</span><span class="sxs-lookup"><span data-stu-id="6dca1-122">Name of resource group in which cache exists.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dca1-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="6dca1-123">-RuleName</span></span>
<span data-ttu-id="6dca1-124">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="6dca1-124">Name of firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dca1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6dca1-125">-Confirm</span></span>
<span data-ttu-id="6dca1-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6dca1-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dca1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dca1-127">-WhatIf</span></span>
<span data-ttu-id="6dca1-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6dca1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dca1-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6dca1-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dca1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dca1-130">CommonParameters</span></span>
<span data-ttu-id="6dca1-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6dca1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dca1-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dca1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dca1-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6dca1-133">INPUTS</span></span>

### <span data-ttu-id="6dca1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6dca1-134">System.String</span></span>

## <span data-ttu-id="6dca1-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dca1-135">OUTPUTS</span></span>

### <span data-ttu-id="6dca1-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6dca1-136">System.Boolean</span></span>

## <span data-ttu-id="6dca1-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="6dca1-137">NOTES</span></span>

## <span data-ttu-id="6dca1-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6dca1-138">RELATED LINKS</span></span>

[<span data-ttu-id="6dca1-139">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6dca1-139">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="6dca1-140">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6dca1-140">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="6dca1-141">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6dca1-141">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="6dca1-142">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6dca1-142">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="6dca1-143">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6dca1-143">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="6dca1-144">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6dca1-144">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
