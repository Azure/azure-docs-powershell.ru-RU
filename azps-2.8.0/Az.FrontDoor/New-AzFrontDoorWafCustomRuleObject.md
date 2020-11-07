---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 6c40a54dd230bc4c7e45f97b4fa6f969940e1673
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720886"
---
# <span data-ttu-id="f2913-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="f2913-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="f2913-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2913-102">SYNOPSIS</span></span>
<span data-ttu-id="f2913-103">Создание объекта CustomRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="f2913-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="f2913-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2913-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2913-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2913-105">DESCRIPTION</span></span>
<span data-ttu-id="f2913-106">Создание объекта CustomRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="f2913-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="f2913-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2913-107">EXAMPLES</span></span>

### <span data-ttu-id="f2913-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f2913-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="f2913-109">Создание объекта CustomRule</span><span class="sxs-lookup"><span data-stu-id="f2913-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="f2913-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2913-110">PARAMETERS</span></span>

### <span data-ttu-id="f2913-111">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="f2913-111">-Action</span></span>
<span data-ttu-id="f2913-112">Тип действий.</span><span class="sxs-lookup"><span data-stu-id="f2913-112">Type of Actions.</span></span>
<span data-ttu-id="f2913-113">Возможные значения: "разрешить", "блок", "журнал"</span><span class="sxs-lookup"><span data-stu-id="f2913-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="f2913-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2913-114">-DefaultProfile</span></span>
<span data-ttu-id="f2913-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2913-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2913-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="f2913-116">-MatchCondition</span></span>
<span data-ttu-id="f2913-117">Список условий соответствия.</span><span class="sxs-lookup"><span data-stu-id="f2913-117">List of match conditions.</span></span>

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

### <span data-ttu-id="f2913-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f2913-118">-Name</span></span>
<span data-ttu-id="f2913-119">Имя правила</span><span class="sxs-lookup"><span data-stu-id="f2913-119">Name of the rule</span></span>

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

### <span data-ttu-id="f2913-120">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="f2913-120">-Priority</span></span>
<span data-ttu-id="f2913-121">Описывает приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="f2913-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="f2913-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="f2913-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="f2913-123">Продолжительность ограничения нормы.</span><span class="sxs-lookup"><span data-stu-id="f2913-123">Rate limit duration.</span></span> <span data-ttu-id="f2913-124">По умолчанию — 1 минута</span><span class="sxs-lookup"><span data-stu-id="f2913-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="f2913-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="f2913-125">-RateLimitThreshold</span></span>
<span data-ttu-id="f2913-126">Порог ограничения скорости</span><span class="sxs-lookup"><span data-stu-id="f2913-126">Rate limit threshold</span></span>

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

### <span data-ttu-id="f2913-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="f2913-127">-RuleType</span></span>
<span data-ttu-id="f2913-128">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="f2913-128">Type of the rule.</span></span>
<span data-ttu-id="f2913-129">Возможные значения: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="f2913-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="f2913-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2913-130">CommonParameters</span></span>
<span data-ttu-id="f2913-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2913-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2913-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2913-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2913-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2913-133">INPUTS</span></span>

### <span data-ttu-id="f2913-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="f2913-134">None</span></span>

## <span data-ttu-id="f2913-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2913-135">OUTPUTS</span></span>

### <span data-ttu-id="f2913-136">Microsoft. Azure. Commands. FrontDoor. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="f2913-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="f2913-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2913-137">NOTES</span></span>

## <span data-ttu-id="f2913-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2913-138">RELATED LINKS</span></span>

<span data-ttu-id="f2913-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f2913-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span></span>
