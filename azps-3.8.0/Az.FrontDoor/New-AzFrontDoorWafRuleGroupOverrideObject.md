---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 9d05502b518dcd10a22c9583546a2d010b424902
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065178"
---
# <span data-ttu-id="e0b5a-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="e0b5a-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="e0b5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b5a-103">Создание объекта RuleGroupOverride для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="e0b5a-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="e0b5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0b5a-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0b5a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="e0b5a-106">Создание объекта RuleGroupOverride для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="e0b5a-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="e0b5a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0b5a-107">EXAMPLES</span></span>

### <span data-ttu-id="e0b5a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0b5a-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="e0b5a-109">Создание объекта RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="e0b5a-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="e0b5a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0b5a-110">PARAMETERS</span></span>

### <span data-ttu-id="e0b5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b5a-111">-DefaultProfile</span></span>
<span data-ttu-id="e0b5a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0b5a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0b5a-113">-Исключение</span><span class="sxs-lookup"><span data-stu-id="e0b5a-113">-Exclusion</span></span>
<span data-ttu-id="e0b5a-114">Глобаль</span><span class="sxs-lookup"><span data-stu-id="e0b5a-114">Exclusion</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b5a-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="e0b5a-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="e0b5a-116">Список переопределения правила</span><span class="sxs-lookup"><span data-stu-id="e0b5a-116">Rule override list</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b5a-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="e0b5a-117">-RuleGroupName</span></span>
<span data-ttu-id="e0b5a-118">Имя группы правил, к которой применяются эти переопределения</span><span class="sxs-lookup"><span data-stu-id="e0b5a-118">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="e0b5a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b5a-119">CommonParameters</span></span>
<span data-ttu-id="e0b5a-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0b5a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b5a-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0b5a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b5a-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0b5a-122">INPUTS</span></span>

### <span data-ttu-id="e0b5a-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="e0b5a-123">None</span></span>

## <span data-ttu-id="e0b5a-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0b5a-124">OUTPUTS</span></span>

### <span data-ttu-id="e0b5a-125">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="e0b5a-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="e0b5a-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0b5a-126">NOTES</span></span>

## <span data-ttu-id="e0b5a-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0b5a-127">RELATED LINKS</span></span>

[<span data-ttu-id="e0b5a-128">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="e0b5a-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
