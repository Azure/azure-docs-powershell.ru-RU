---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: c89589d966c03614255751bf13769689ff875332
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732516"
---
# <span data-ttu-id="df783-101">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="df783-101">New-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="df783-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df783-102">SYNOPSIS</span></span>
<span data-ttu-id="df783-103">Создайте правило межсетевого экрана для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="df783-103">Create a firewall rule on a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df783-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df783-104">SYNTAX</span></span>

### <span data-ttu-id="df783-105">NormalParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="df783-105">NormalParameterSet (Default)</span></span>
```
New-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 -StartIP <String> -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df783-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="df783-106">RedisCacheAttributesObject</span></span>
```
New-AzureRmRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df783-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df783-107">ResourceIdParameterSet</span></span>
```
New-AzureRmRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df783-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df783-108">DESCRIPTION</span></span>
<span data-ttu-id="df783-109">Создайте правило межсетевого экрана для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="df783-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="df783-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df783-110">EXAMPLES</span></span>

### <span data-ttu-id="df783-111">Пример 1: Создание правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="df783-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="df783-112">Эта команда создает правило межсетевого экрана с именем ruleone в кэше Redis с именем mycache.</span><span class="sxs-lookup"><span data-stu-id="df783-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="df783-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df783-113">PARAMETERS</span></span>

### <span data-ttu-id="df783-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df783-114">-DefaultProfile</span></span>
<span data-ttu-id="df783-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df783-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df783-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="df783-116">-EndIP</span></span>
<span data-ttu-id="df783-117">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="df783-117">Ending IP address.</span></span>

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

### <span data-ttu-id="df783-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df783-118">-InputObject</span></span>
<span data-ttu-id="df783-119">Объект типа RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="df783-119">object of type RedisCacheAttributes</span></span>

```yaml
Type: RedisCacheAttributes
Parameter Sets: RedisCacheAttributesObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df783-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="df783-120">-Name</span></span>
<span data-ttu-id="df783-121">Имя кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="df783-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="df783-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df783-122">-ResourceGroupName</span></span>
<span data-ttu-id="df783-123">Имя группы ресурсов, в которой находится кэш.</span><span class="sxs-lookup"><span data-stu-id="df783-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="df783-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df783-124">-ResourceId</span></span>
<span data-ttu-id="df783-125">Идентификатор ARM из кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="df783-125">ARM Id of Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df783-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="df783-126">-RuleName</span></span>
<span data-ttu-id="df783-127">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="df783-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="df783-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="df783-128">-StartIP</span></span>
<span data-ttu-id="df783-129">Начальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="df783-129">Starting IP address.</span></span>

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

### <span data-ttu-id="df783-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df783-130">-Confirm</span></span>
<span data-ttu-id="df783-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="df783-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df783-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df783-132">-WhatIf</span></span>
<span data-ttu-id="df783-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="df783-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df783-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="df783-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df783-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df783-135">CommonParameters</span></span>
<span data-ttu-id="df783-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df783-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df783-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df783-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df783-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df783-138">INPUTS</span></span>

### <span data-ttu-id="df783-139">System. String</span><span class="sxs-lookup"><span data-stu-id="df783-139">System.String</span></span>

## <span data-ttu-id="df783-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df783-140">OUTPUTS</span></span>

### <span data-ttu-id="df783-141">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="df783-141">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="df783-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="df783-142">NOTES</span></span>

## <span data-ttu-id="df783-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df783-143">RELATED LINKS</span></span>

[<span data-ttu-id="df783-144">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="df783-144">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="df783-145">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="df783-145">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="df783-146">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="df783-146">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="df783-147">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="df783-147">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="df783-148">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="df783-148">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="df783-149">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="df783-149">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
