---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: d352f70d28b9bfafae46697fb6d69dc50c739b19
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073838"
---
# <span data-ttu-id="b7ff0-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="b7ff0-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="b7ff0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ff0-103">Создание объекта CustomRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="b7ff0-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="b7ff0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7ff0-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7ff0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7ff0-105">DESCRIPTION</span></span>
<span data-ttu-id="b7ff0-106">Создание объекта CustomRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="b7ff0-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="b7ff0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7ff0-107">EXAMPLES</span></span>

### <span data-ttu-id="b7ff0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b7ff0-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="b7ff0-109">Создание объекта CustomRule</span><span class="sxs-lookup"><span data-stu-id="b7ff0-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="b7ff0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7ff0-110">PARAMETERS</span></span>

### <span data-ttu-id="b7ff0-111">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="b7ff0-111">-Action</span></span>
<span data-ttu-id="b7ff0-112">Тип действий.</span><span class="sxs-lookup"><span data-stu-id="b7ff0-112">Type of Actions.</span></span>
<span data-ttu-id="b7ff0-113">Возможные значения: "разрешить", "блок", "журнал"</span><span class="sxs-lookup"><span data-stu-id="b7ff0-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ff0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ff0-114">-DefaultProfile</span></span>
<span data-ttu-id="b7ff0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7ff0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7ff0-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="b7ff0-116">-EnabledState</span></span>
<span data-ttu-id="b7ff0-117">Включенное состояние.</span><span class="sxs-lookup"><span data-stu-id="b7ff0-117">Enabled State.</span></span> <span data-ttu-id="b7ff0-118">Возможные значения: "включено", "отключено".</span><span class="sxs-lookup"><span data-stu-id="b7ff0-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ff0-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="b7ff0-119">-MatchCondition</span></span>
<span data-ttu-id="b7ff0-120">Список условий соответствия.</span><span class="sxs-lookup"><span data-stu-id="b7ff0-120">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ff0-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7ff0-121">-Name</span></span>
<span data-ttu-id="b7ff0-122">Имя правила</span><span class="sxs-lookup"><span data-stu-id="b7ff0-122">Name of the rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ff0-123">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="b7ff0-123">-Priority</span></span>
<span data-ttu-id="b7ff0-124">Описывает приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="b7ff0-124">Describes priority of the rule.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ff0-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="b7ff0-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="b7ff0-126">Продолжительность ограничения нормы.</span><span class="sxs-lookup"><span data-stu-id="b7ff0-126">Rate limit duration.</span></span> <span data-ttu-id="b7ff0-127">По умолчанию — 1 минута</span><span class="sxs-lookup"><span data-stu-id="b7ff0-127">Default - 1 minute</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ff0-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="b7ff0-128">-RateLimitThreshold</span></span>
<span data-ttu-id="b7ff0-129">Порог ограничения скорости</span><span class="sxs-lookup"><span data-stu-id="b7ff0-129">Rate limit threshold</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ff0-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="b7ff0-130">-RuleType</span></span>
<span data-ttu-id="b7ff0-131">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="b7ff0-131">Type of the rule.</span></span>
<span data-ttu-id="b7ff0-132">Возможные значения: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="b7ff0-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ff0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ff0-133">CommonParameters</span></span>
<span data-ttu-id="b7ff0-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7ff0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ff0-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7ff0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ff0-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7ff0-136">INPUTS</span></span>

### <span data-ttu-id="b7ff0-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="b7ff0-137">None</span></span>

## <span data-ttu-id="b7ff0-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7ff0-138">OUTPUTS</span></span>

### <span data-ttu-id="b7ff0-139">Microsoft. Azure. Commands. FrontDoor. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="b7ff0-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="b7ff0-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7ff0-140">NOTES</span></span>

## <span data-ttu-id="b7ff0-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7ff0-141">RELATED LINKS</span></span>

<span data-ttu-id="b7ff0-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="b7ff0-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span></span>
