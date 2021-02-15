---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
ms.openlocfilehash: 8602bd4636e3e6034552f48a6f6514a453b816a0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400677"
---
# <span data-ttu-id="ecfb5-101">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="ecfb5-101">New-AzFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="ecfb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecfb5-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfb5-103">Создание объекта CustomRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="ecfb5-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="ecfb5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ecfb5-104">SYNTAX</span></span>

```
New-AzFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ecfb5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecfb5-105">DESCRIPTION</span></span>
<span data-ttu-id="ecfb5-106">Создание объекта CustomRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="ecfb5-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="ecfb5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ecfb5-107">EXAMPLES</span></span>

### <span data-ttu-id="ecfb5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ecfb5-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="ecfb5-109">Создание объекта CustomRule</span><span class="sxs-lookup"><span data-stu-id="ecfb5-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="ecfb5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecfb5-110">PARAMETERS</span></span>

### <span data-ttu-id="ecfb5-111">-Action</span><span class="sxs-lookup"><span data-stu-id="ecfb5-111">-Action</span></span>
<span data-ttu-id="ecfb5-112">Тип действий.</span><span class="sxs-lookup"><span data-stu-id="ecfb5-112">Type of Actions.</span></span>
<span data-ttu-id="ecfb5-113">Возможные значения: 'Allow', 'Block', 'Log'</span><span class="sxs-lookup"><span data-stu-id="ecfb5-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="ecfb5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfb5-114">-DefaultProfile</span></span>
<span data-ttu-id="ecfb5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ecfb5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecfb5-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="ecfb5-116">-MatchCondition</span></span>
<span data-ttu-id="ecfb5-117">Список условий совпадения.</span><span class="sxs-lookup"><span data-stu-id="ecfb5-117">List of match conditions.</span></span>

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

### <span data-ttu-id="ecfb5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ecfb5-118">-Name</span></span>
<span data-ttu-id="ecfb5-119">Имя правила</span><span class="sxs-lookup"><span data-stu-id="ecfb5-119">Name of the rule</span></span>

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

### <span data-ttu-id="ecfb5-120">-Priority</span><span class="sxs-lookup"><span data-stu-id="ecfb5-120">-Priority</span></span>
<span data-ttu-id="ecfb5-121">В нем описывается приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="ecfb5-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="ecfb5-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="ecfb5-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="ecfb5-123">Ограничение срока действия тарифа.</span><span class="sxs-lookup"><span data-stu-id="ecfb5-123">Rate limit duration.</span></span> <span data-ttu-id="ecfb5-124">По умолчанию — 1 минута</span><span class="sxs-lookup"><span data-stu-id="ecfb5-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="ecfb5-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="ecfb5-125">-RateLimitThreshold</span></span>
<span data-ttu-id="ecfb5-126">Ограничив допустимый предел ставок</span><span class="sxs-lookup"><span data-stu-id="ecfb5-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="ecfb5-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="ecfb5-127">-RuleType</span></span>
<span data-ttu-id="ecfb5-128">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="ecfb5-128">Type of the rule.</span></span>
<span data-ttu-id="ecfb5-129">Возможные значения: 'MatchRule', 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="ecfb5-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="ecfb5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfb5-130">CommonParameters</span></span>
<span data-ttu-id="ecfb5-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecfb5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfb5-132">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecfb5-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfb5-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ecfb5-133">INPUTS</span></span>

### <span data-ttu-id="ecfb5-134">Нет</span><span class="sxs-lookup"><span data-stu-id="ecfb5-134">None</span></span>

## <span data-ttu-id="ecfb5-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ecfb5-135">OUTPUTS</span></span>

### <span data-ttu-id="ecfb5-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="ecfb5-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="ecfb5-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ecfb5-137">NOTES</span></span>

## <span data-ttu-id="ecfb5-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ecfb5-138">RELATED LINKS</span></span>

<span data-ttu-id="ecfb5-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="ecfb5-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span></span>
