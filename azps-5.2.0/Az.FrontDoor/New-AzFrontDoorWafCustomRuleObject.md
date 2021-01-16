---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 4612f1ef1dac22d87b6794e35f9541a39f6312ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406287"
---
# <span data-ttu-id="c832a-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="c832a-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="c832a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c832a-102">SYNOPSIS</span></span>
<span data-ttu-id="c832a-103">Создание объекта CustomRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="c832a-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="c832a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c832a-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c832a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c832a-105">DESCRIPTION</span></span>
<span data-ttu-id="c832a-106">Создание объекта CustomRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="c832a-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="c832a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c832a-107">EXAMPLES</span></span>

### <span data-ttu-id="c832a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c832a-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="c832a-109">Создание объекта CustomRule</span><span class="sxs-lookup"><span data-stu-id="c832a-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="c832a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c832a-110">PARAMETERS</span></span>

### <span data-ttu-id="c832a-111">-Action</span><span class="sxs-lookup"><span data-stu-id="c832a-111">-Action</span></span>
<span data-ttu-id="c832a-112">Тип действий.</span><span class="sxs-lookup"><span data-stu-id="c832a-112">Type of Actions.</span></span>
<span data-ttu-id="c832a-113">Возможные значения: 'Allow', 'Block', 'Log'</span><span class="sxs-lookup"><span data-stu-id="c832a-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="c832a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c832a-114">-DefaultProfile</span></span>
<span data-ttu-id="c832a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c832a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c832a-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="c832a-116">-EnabledState</span></span>
<span data-ttu-id="c832a-117">Состояние включено.</span><span class="sxs-lookup"><span data-stu-id="c832a-117">Enabled State.</span></span> <span data-ttu-id="c832a-118">Возможные значения: "Включено", "Отключено".</span><span class="sxs-lookup"><span data-stu-id="c832a-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="c832a-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="c832a-119">-MatchCondition</span></span>
<span data-ttu-id="c832a-120">Список условий совпадения.</span><span class="sxs-lookup"><span data-stu-id="c832a-120">List of match conditions.</span></span>

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

### <span data-ttu-id="c832a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c832a-121">-Name</span></span>
<span data-ttu-id="c832a-122">Имя правила</span><span class="sxs-lookup"><span data-stu-id="c832a-122">Name of the rule</span></span>

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

### <span data-ttu-id="c832a-123">-Priority</span><span class="sxs-lookup"><span data-stu-id="c832a-123">-Priority</span></span>
<span data-ttu-id="c832a-124">В нем описывается приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="c832a-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="c832a-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="c832a-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="c832a-126">Ограничение срока действия тарифа.</span><span class="sxs-lookup"><span data-stu-id="c832a-126">Rate limit duration.</span></span> <span data-ttu-id="c832a-127">По умолчанию — 1 минута</span><span class="sxs-lookup"><span data-stu-id="c832a-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="c832a-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="c832a-128">-RateLimitThreshold</span></span>
<span data-ttu-id="c832a-129">Пороговое значение ограничения ставки</span><span class="sxs-lookup"><span data-stu-id="c832a-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="c832a-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="c832a-130">-RuleType</span></span>
<span data-ttu-id="c832a-131">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="c832a-131">Type of the rule.</span></span>
<span data-ttu-id="c832a-132">Возможные значения: 'MatchRule', 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="c832a-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="c832a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c832a-133">CommonParameters</span></span>
<span data-ttu-id="c832a-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c832a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c832a-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c832a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c832a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c832a-136">INPUTS</span></span>

### <span data-ttu-id="c832a-137">Нет</span><span class="sxs-lookup"><span data-stu-id="c832a-137">None</span></span>

## <span data-ttu-id="c832a-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c832a-138">OUTPUTS</span></span>

### <span data-ttu-id="c832a-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="c832a-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="c832a-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c832a-140">NOTES</span></span>

## <span data-ttu-id="c832a-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c832a-141">RELATED LINKS</span></span>

<span data-ttu-id="c832a-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="c832a-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>