---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
ms.openlocfilehash: 19f8215f8feaa1765da871f0fa38cc0120d842ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900634"
---
# <span data-ttu-id="680ad-101">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="680ad-101">New-AzFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="680ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="680ad-102">SYNOPSIS</span></span>
<span data-ttu-id="680ad-103">Создание объекта CustomRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="680ad-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="680ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="680ad-104">SYNTAX</span></span>

```
New-AzFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="680ad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="680ad-105">DESCRIPTION</span></span>
<span data-ttu-id="680ad-106">Создание объекта CustomRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="680ad-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="680ad-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="680ad-107">EXAMPLES</span></span>

### <span data-ttu-id="680ad-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="680ad-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="680ad-109">Создание объекта CustomRule</span><span class="sxs-lookup"><span data-stu-id="680ad-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="680ad-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="680ad-110">PARAMETERS</span></span>

### <span data-ttu-id="680ad-111">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="680ad-111">-Action</span></span>
<span data-ttu-id="680ad-112">Тип действий.</span><span class="sxs-lookup"><span data-stu-id="680ad-112">Type of Actions.</span></span>
<span data-ttu-id="680ad-113">Возможные значения: "разрешить", "блок", "журнал"</span><span class="sxs-lookup"><span data-stu-id="680ad-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log, Redirect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="680ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="680ad-114">-DefaultProfile</span></span>
<span data-ttu-id="680ad-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="680ad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="680ad-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="680ad-116">-MatchCondition</span></span>
<span data-ttu-id="680ad-117">Список условий соответствия.</span><span class="sxs-lookup"><span data-stu-id="680ad-117">List of match conditions.</span></span>

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

### <span data-ttu-id="680ad-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="680ad-118">-Name</span></span>
<span data-ttu-id="680ad-119">Имя правила</span><span class="sxs-lookup"><span data-stu-id="680ad-119">Name of the rule</span></span>

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

### <span data-ttu-id="680ad-120">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="680ad-120">-Priority</span></span>
<span data-ttu-id="680ad-121">Описывает приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="680ad-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="680ad-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="680ad-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="680ad-123">Продолжительность ограничения нормы.</span><span class="sxs-lookup"><span data-stu-id="680ad-123">Rate limit duration.</span></span> <span data-ttu-id="680ad-124">По умолчанию — 1 минута</span><span class="sxs-lookup"><span data-stu-id="680ad-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="680ad-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="680ad-125">-RateLimitThreshold</span></span>
<span data-ttu-id="680ad-126">Лимит скорости thresold</span><span class="sxs-lookup"><span data-stu-id="680ad-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="680ad-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="680ad-127">-RuleType</span></span>
<span data-ttu-id="680ad-128">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="680ad-128">Type of the rule.</span></span>
<span data-ttu-id="680ad-129">Возможные значения: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="680ad-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRuleType
Parameter Sets: (All)
Aliases:
Accepted values: RateLimitRule, MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="680ad-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="680ad-130">CommonParameters</span></span>
<span data-ttu-id="680ad-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="680ad-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="680ad-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="680ad-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="680ad-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="680ad-133">INPUTS</span></span>

### <span data-ttu-id="680ad-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="680ad-134">None</span></span>

## <span data-ttu-id="680ad-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="680ad-135">OUTPUTS</span></span>

### <span data-ttu-id="680ad-136">Microsoft. Azure. Commands. FrontDoor. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="680ad-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="680ad-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="680ad-137">NOTES</span></span>

## <span data-ttu-id="680ad-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="680ad-138">RELATED LINKS</span></span>

<span data-ttu-id="680ad-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="680ad-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span></span>
