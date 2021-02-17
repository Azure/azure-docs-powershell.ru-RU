---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: c59e0f90ae8b6d7839c7bb845b56e31a42b2d033
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412798"
---
# <span data-ttu-id="ff05b-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="ff05b-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="ff05b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff05b-102">SYNOPSIS</span></span>
<span data-ttu-id="ff05b-103">Создание объекта CustomRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="ff05b-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="ff05b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ff05b-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff05b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff05b-105">DESCRIPTION</span></span>
<span data-ttu-id="ff05b-106">Создание объекта CustomRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="ff05b-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="ff05b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ff05b-107">EXAMPLES</span></span>

### <span data-ttu-id="ff05b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ff05b-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="ff05b-109">Создание объекта CustomRule</span><span class="sxs-lookup"><span data-stu-id="ff05b-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="ff05b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff05b-110">PARAMETERS</span></span>

### <span data-ttu-id="ff05b-111">-Action</span><span class="sxs-lookup"><span data-stu-id="ff05b-111">-Action</span></span>
<span data-ttu-id="ff05b-112">Тип действий.</span><span class="sxs-lookup"><span data-stu-id="ff05b-112">Type of Actions.</span></span>
<span data-ttu-id="ff05b-113">Возможные значения: 'Allow', 'Block', 'Log'</span><span class="sxs-lookup"><span data-stu-id="ff05b-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="ff05b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff05b-114">-DefaultProfile</span></span>
<span data-ttu-id="ff05b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff05b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff05b-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="ff05b-116">-MatchCondition</span></span>
<span data-ttu-id="ff05b-117">Список условий совпадения.</span><span class="sxs-lookup"><span data-stu-id="ff05b-117">List of match conditions.</span></span>

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

### <span data-ttu-id="ff05b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ff05b-118">-Name</span></span>
<span data-ttu-id="ff05b-119">Имя правила</span><span class="sxs-lookup"><span data-stu-id="ff05b-119">Name of the rule</span></span>

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

### <span data-ttu-id="ff05b-120">-Priority</span><span class="sxs-lookup"><span data-stu-id="ff05b-120">-Priority</span></span>
<span data-ttu-id="ff05b-121">В нем описывается приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="ff05b-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="ff05b-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="ff05b-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="ff05b-123">Ограничение срока действия тарифа.</span><span class="sxs-lookup"><span data-stu-id="ff05b-123">Rate limit duration.</span></span> <span data-ttu-id="ff05b-124">По умолчанию — 1 минута</span><span class="sxs-lookup"><span data-stu-id="ff05b-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="ff05b-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="ff05b-125">-RateLimitThreshold</span></span>
<span data-ttu-id="ff05b-126">Пороговое значение ограничения ставки</span><span class="sxs-lookup"><span data-stu-id="ff05b-126">Rate limit threshold</span></span>

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

### <span data-ttu-id="ff05b-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="ff05b-127">-RuleType</span></span>
<span data-ttu-id="ff05b-128">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="ff05b-128">Type of the rule.</span></span>
<span data-ttu-id="ff05b-129">Возможные значения: 'MatchRule', 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="ff05b-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="ff05b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff05b-130">CommonParameters</span></span>
<span data-ttu-id="ff05b-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff05b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff05b-132">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff05b-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff05b-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff05b-133">INPUTS</span></span>

### <span data-ttu-id="ff05b-134">Нет</span><span class="sxs-lookup"><span data-stu-id="ff05b-134">None</span></span>

## <span data-ttu-id="ff05b-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ff05b-135">OUTPUTS</span></span>

### <span data-ttu-id="ff05b-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="ff05b-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="ff05b-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ff05b-137">NOTES</span></span>

## <span data-ttu-id="ff05b-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff05b-138">RELATED LINKS</span></span>

<span data-ttu-id="ff05b-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="ff05b-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
