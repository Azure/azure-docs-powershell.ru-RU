---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorCustomRuleObject.md
ms.openlocfilehash: a5a1494bd217147a4e6f4c94a85140313429898f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556644"
---
# <span data-ttu-id="d8d20-101">New-AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="d8d20-101">New-AzureRmFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="d8d20-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8d20-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d20-103">Создание объекта CustomRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="d8d20-103">Create CustomRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8d20-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8d20-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8d20-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8d20-105">DESCRIPTION</span></span>
<span data-ttu-id="d8d20-106">Создание объекта CustomRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="d8d20-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="d8d20-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8d20-107">EXAMPLES</span></span>

### <span data-ttu-id="d8d20-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d8d20-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

RuleType                   : MatchRule
Action                     : Block
MatchConditions            : {Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition}
Priority                   : 2
RateLimitDurationInMinutes : 1
RateLimitThreshold         :
Name                       : Rule1
Etag                       :
Transforms                 :
```

<span data-ttu-id="d8d20-109">Создание объекта CustomRule</span><span class="sxs-lookup"><span data-stu-id="d8d20-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="d8d20-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8d20-110">PARAMETERS</span></span>

### <span data-ttu-id="d8d20-111">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="d8d20-111">-Action</span></span>
<span data-ttu-id="d8d20-112">Тип действий.</span><span class="sxs-lookup"><span data-stu-id="d8d20-112">Type of Actions.</span></span>
<span data-ttu-id="d8d20-113">Возможные значения: "разрешить", "блок", "журнал"</span><span class="sxs-lookup"><span data-stu-id="d8d20-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d20-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d20-114">-DefaultProfile</span></span>
<span data-ttu-id="d8d20-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8d20-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8d20-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="d8d20-116">-MatchCondition</span></span>
<span data-ttu-id="d8d20-117">Список условий соответствия.</span><span class="sxs-lookup"><span data-stu-id="d8d20-117">List of match conditions.</span></span>

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

### <span data-ttu-id="d8d20-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d8d20-118">-Name</span></span>
<span data-ttu-id="d8d20-119">Имя правила</span><span class="sxs-lookup"><span data-stu-id="d8d20-119">Name of the rule</span></span>

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

### <span data-ttu-id="d8d20-120">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="d8d20-120">-Priority</span></span>
<span data-ttu-id="d8d20-121">Описывает приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="d8d20-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="d8d20-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="d8d20-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="d8d20-123">Продолжительность ограничения нормы.</span><span class="sxs-lookup"><span data-stu-id="d8d20-123">Rate limit duration.</span></span> <span data-ttu-id="d8d20-124">По умолчанию — 1 минута</span><span class="sxs-lookup"><span data-stu-id="d8d20-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="d8d20-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="d8d20-125">-RateLimitThreshold</span></span>
<span data-ttu-id="d8d20-126">Лимит скорости thresold</span><span class="sxs-lookup"><span data-stu-id="d8d20-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="d8d20-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="d8d20-127">-RuleType</span></span>
<span data-ttu-id="d8d20-128">Тип правила.</span><span class="sxs-lookup"><span data-stu-id="d8d20-128">Type of the rule.</span></span>
<span data-ttu-id="d8d20-129">Возможные значения: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="d8d20-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="d8d20-130">-Transform</span><span class="sxs-lookup"><span data-stu-id="d8d20-130">-Transform</span></span>
<span data-ttu-id="d8d20-131">Список преобразований</span><span class="sxs-lookup"><span data-stu-id="d8d20-131">List of transforms</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d20-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d20-132">CommonParameters</span></span>
<span data-ttu-id="d8d20-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8d20-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d20-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8d20-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d20-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8d20-135">INPUTS</span></span>

### <span data-ttu-id="d8d20-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="d8d20-136">None</span></span>

## <span data-ttu-id="d8d20-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8d20-137">OUTPUTS</span></span>

### <span data-ttu-id="d8d20-138">Microsoft. Azure. Commands. FrontDoor. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="d8d20-138">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="d8d20-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8d20-139">NOTES</span></span>

## <span data-ttu-id="d8d20-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8d20-140">RELATED LINKS</span></span>

<span data-ttu-id="d8d20-141">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="d8d20-141">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)</span></span>
