---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: e5e909107d740f67e3407347625270226c87839d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567256"
---
# <span data-ttu-id="ae440-101">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ae440-101">New-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="ae440-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae440-102">SYNOPSIS</span></span>
<span data-ttu-id="ae440-103">Создайте правило межсетевого экрана для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="ae440-103">Create a firewall rule on a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae440-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae440-104">SYNTAX</span></span>

### <span data-ttu-id="ae440-105">NormalParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ae440-105">NormalParameterSet (Default)</span></span>
```
New-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 -StartIP <String> -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae440-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="ae440-106">RedisCacheAttributesObject</span></span>
```
New-AzureRmRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae440-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae440-107">ResourceIdParameterSet</span></span>
```
New-AzureRmRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae440-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae440-108">DESCRIPTION</span></span>
<span data-ttu-id="ae440-109">Создайте правило межсетевого экрана для кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="ae440-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="ae440-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae440-110">EXAMPLES</span></span>

### <span data-ttu-id="ae440-111">Пример 1: Создание правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="ae440-111">Example 1: Create a firewall rule</span></span>
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

<span data-ttu-id="ae440-112">Эта команда создает правило межсетевого экрана с именем ruleone в кэше Redis с именем mycache.</span><span class="sxs-lookup"><span data-stu-id="ae440-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="ae440-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae440-113">PARAMETERS</span></span>

### <span data-ttu-id="ae440-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae440-114">-DefaultProfile</span></span>
<span data-ttu-id="ae440-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae440-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae440-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="ae440-116">-EndIP</span></span>
<span data-ttu-id="ae440-117">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="ae440-117">Ending IP address.</span></span>

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

### <span data-ttu-id="ae440-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae440-118">-InputObject</span></span>
<span data-ttu-id="ae440-119">Объект типа RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="ae440-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="ae440-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ae440-120">-Name</span></span>
<span data-ttu-id="ae440-121">Имя кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="ae440-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="ae440-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae440-122">-ResourceGroupName</span></span>
<span data-ttu-id="ae440-123">Имя группы ресурсов, в которой находится кэш.</span><span class="sxs-lookup"><span data-stu-id="ae440-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="ae440-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae440-124">-ResourceId</span></span>
<span data-ttu-id="ae440-125">Идентификатор ARM из кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="ae440-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="ae440-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="ae440-126">-RuleName</span></span>
<span data-ttu-id="ae440-127">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ae440-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="ae440-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="ae440-128">-StartIP</span></span>
<span data-ttu-id="ae440-129">Начальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="ae440-129">Starting IP address.</span></span>

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

### <span data-ttu-id="ae440-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae440-130">-Confirm</span></span>
<span data-ttu-id="ae440-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ae440-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae440-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae440-132">-WhatIf</span></span>
<span data-ttu-id="ae440-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ae440-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae440-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ae440-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae440-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae440-135">CommonParameters</span></span>
<span data-ttu-id="ae440-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae440-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae440-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae440-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae440-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae440-138">INPUTS</span></span>

### <span data-ttu-id="ae440-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ae440-139">System.String</span></span>

### <span data-ttu-id="ae440-140">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="ae440-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="ae440-141">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae440-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ae440-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae440-142">OUTPUTS</span></span>

### <span data-ttu-id="ae440-143">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ae440-143">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="ae440-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae440-144">NOTES</span></span>

## <span data-ttu-id="ae440-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae440-145">RELATED LINKS</span></span>

[<span data-ttu-id="ae440-146">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ae440-146">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="ae440-147">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ae440-147">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="ae440-148">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ae440-148">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="ae440-149">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ae440-149">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="ae440-150">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ae440-150">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="ae440-151">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ae440-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
