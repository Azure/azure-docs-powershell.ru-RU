---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 4612f1ef1dac22d87b6794e35f9541a39f6312ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247409"
---
# <span data-ttu-id="c1530-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="c1530-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="c1530-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1530-102">SYNOPSIS</span></span>
<span data-ttu-id="c1530-103">Создание объекта CustomRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="c1530-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="c1530-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1530-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1530-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1530-105">DESCRIPTION</span></span>
<span data-ttu-id="c1530-106">Создание объекта CustomRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="c1530-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="c1530-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1530-107">EXAMPLES</span></span>

### <span data-ttu-id="c1530-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c1530-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="c1530-109">Создание объекта CustomRule</span><span class="sxs-lookup"><span data-stu-id="c1530-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="c1530-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1530-110">PARAMETERS</span></span>

### <span data-ttu-id="c1530-111">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="c1530-111">-Action</span></span>
<span data-ttu-id="c1530-112">Тип действий.</span><span class="sxs-lookup"><span data-stu-id="c1530-112">Type of Actions.</span></span>
<span data-ttu-id="c1530-113">Возможные значения: "разрешить", "блок", "журнал"</span><span class="sxs-lookup"><span data-stu-id="c1530-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="c1530-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1530-114">-DefaultProfile</span></span>
<span data-ttu-id="c1530-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1530-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1530-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="c1530-116">-EnabledState</span></span>
<span data-ttu-id="c1530-117">Включенное состояние.</span><span class="sxs-lookup"><span data-stu-id="c1530-117">Enabled State.</span></span> <span data-ttu-id="c1530-118">Возможные значения: "включено", "отключено".</span><span class="sxs-lookup"><span data-stu-id="c1530-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="c1530-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="c1530-119">-MatchCondition</span></span>
<span data-ttu-id="c1530-120">Список условий соответствия.</span><span class="sxs-lookup"><span data-stu-id="c1530-120">List of match conditions.</span></span>

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

### <span data-ttu-id="c1530-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c1530-121">-Name</span></span>
<span data-ttu-id="c1530-122">Имя правила</span><span class="sxs-lookup"><span data-stu-id="c1530-122">Name of the rule</span></span>

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

### <span data-ttu-id="c1530-123">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="c1530-123">-Priority</span></span>
<span data-ttu-id="c1530-124">Описывает приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="c1530-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="c1530-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="c1530-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="c1530-126">Продолжительность ограничения нормы.</span><span class="sxs-lookup"><span data-stu-id="c1530-126">Rate limit duration.</span></span> <span data-ttu-id="c1530-127">По умолчанию — 1 минута</span><span class="sxs-lookup"><span data-stu-id="c1530-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="c1530-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="c1530-128">-RateLimitThreshold</span></span>
<span data-ttu-id="c1530-129">Порог ограничения скорости</span><span class="sxs-lookup"><span data-stu-id="c1530-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="c1530-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="c1530-130">-RuleType</span></span>
<span data-ttu-id="c1530-131">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="c1530-131">Type of the rule.</span></span>
<span data-ttu-id="c1530-132">Возможные значения: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="c1530-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="c1530-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1530-133">CommonParameters</span></span>
<span data-ttu-id="c1530-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1530-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1530-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1530-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1530-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1530-136">INPUTS</span></span>

### <span data-ttu-id="c1530-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="c1530-137">None</span></span>

## <span data-ttu-id="c1530-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1530-138">OUTPUTS</span></span>

### <span data-ttu-id="c1530-139">Microsoft. Azure. Commands. FrontDoor. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="c1530-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="c1530-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1530-140">NOTES</span></span>

## <span data-ttu-id="c1530-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1530-141">RELATED LINKS</span></span>

<span data-ttu-id="c1530-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="c1530-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
