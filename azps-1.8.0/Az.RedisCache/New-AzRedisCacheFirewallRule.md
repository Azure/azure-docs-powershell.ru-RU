---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: dc52668a7d0f17d9cdbf9221a174228be1fa0f5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729546"
---
# <span data-ttu-id="dc56f-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dc56f-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="dc56f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc56f-102">SYNOPSIS</span></span>
<span data-ttu-id="dc56f-103">Создайте правило межсетевого экрана для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="dc56f-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="dc56f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc56f-104">SYNTAX</span></span>

### <span data-ttu-id="dc56f-105">NormalParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc56f-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc56f-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="dc56f-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc56f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc56f-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc56f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc56f-108">DESCRIPTION</span></span>
<span data-ttu-id="dc56f-109">Создайте правило межсетевого экрана для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="dc56f-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="dc56f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc56f-110">EXAMPLES</span></span>

### <span data-ttu-id="dc56f-111">Пример 1: Создание правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="dc56f-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="dc56f-112">Эта команда создает правило межсетевого экрана с именем ruleone в кэше Redis с именем mycache.</span><span class="sxs-lookup"><span data-stu-id="dc56f-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="dc56f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc56f-113">PARAMETERS</span></span>

### <span data-ttu-id="dc56f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc56f-114">-DefaultProfile</span></span>
<span data-ttu-id="dc56f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc56f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc56f-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="dc56f-116">-EndIP</span></span>
<span data-ttu-id="dc56f-117">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="dc56f-117">Ending IP address.</span></span>

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

### <span data-ttu-id="dc56f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc56f-118">-InputObject</span></span>
<span data-ttu-id="dc56f-119">Объект типа RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="dc56f-119">object of type RedisCacheAttributes</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes
Parameter Sets: RedisCacheAttributesObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc56f-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc56f-120">-Name</span></span>
<span data-ttu-id="dc56f-121">Имя кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="dc56f-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="dc56f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc56f-122">-ResourceGroupName</span></span>
<span data-ttu-id="dc56f-123">Имя группы ресурсов, в которой находится кэш.</span><span class="sxs-lookup"><span data-stu-id="dc56f-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="dc56f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc56f-124">-ResourceId</span></span>
<span data-ttu-id="dc56f-125">Идентификатор ARM из кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="dc56f-125">ARM Id of Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc56f-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="dc56f-126">-RuleName</span></span>
<span data-ttu-id="dc56f-127">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="dc56f-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="dc56f-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="dc56f-128">-StartIP</span></span>
<span data-ttu-id="dc56f-129">Начальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="dc56f-129">Starting IP address.</span></span>

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

### <span data-ttu-id="dc56f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc56f-130">-Confirm</span></span>
<span data-ttu-id="dc56f-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dc56f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc56f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc56f-132">-WhatIf</span></span>
<span data-ttu-id="dc56f-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dc56f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc56f-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dc56f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc56f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc56f-135">CommonParameters</span></span>
<span data-ttu-id="dc56f-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc56f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc56f-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc56f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc56f-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc56f-138">INPUTS</span></span>

### <span data-ttu-id="dc56f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dc56f-139">System.String</span></span>

### <span data-ttu-id="dc56f-140">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="dc56f-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="dc56f-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc56f-141">OUTPUTS</span></span>

### <span data-ttu-id="dc56f-142">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dc56f-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="dc56f-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc56f-143">NOTES</span></span>

## <span data-ttu-id="dc56f-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc56f-144">RELATED LINKS</span></span>

[<span data-ttu-id="dc56f-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dc56f-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="dc56f-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dc56f-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="dc56f-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dc56f-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="dc56f-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dc56f-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="dc56f-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dc56f-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="dc56f-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dc56f-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)