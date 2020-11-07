---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: c55be8e72e3c5bb5418d3be4b74555eb20168113
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720875"
---
# <span data-ttu-id="36abb-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="36abb-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="36abb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36abb-102">SYNOPSIS</span></span>
<span data-ttu-id="36abb-103">Создание объекта RuleGroupOverride для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="36abb-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="36abb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36abb-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36abb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36abb-105">DESCRIPTION</span></span>
<span data-ttu-id="36abb-106">Создание объекта RuleGroupOverride для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="36abb-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="36abb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36abb-107">EXAMPLES</span></span>

### <span data-ttu-id="36abb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="36abb-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="36abb-109">Создание объекта RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="36abb-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="36abb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36abb-110">PARAMETERS</span></span>

### <span data-ttu-id="36abb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36abb-111">-DefaultProfile</span></span>
<span data-ttu-id="36abb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36abb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36abb-113">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="36abb-113">-ManagedRuleOverride</span></span>
<span data-ttu-id="36abb-114">Список переопределения правила</span><span class="sxs-lookup"><span data-stu-id="36abb-114">Rule override list</span></span>

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

### <span data-ttu-id="36abb-115">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="36abb-115">-RuleGroupName</span></span>
<span data-ttu-id="36abb-116">Имя группы правил, к которой применяются эти переопределения</span><span class="sxs-lookup"><span data-stu-id="36abb-116">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="36abb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36abb-117">CommonParameters</span></span>
<span data-ttu-id="36abb-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36abb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36abb-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36abb-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36abb-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36abb-120">INPUTS</span></span>

### <span data-ttu-id="36abb-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="36abb-121">None</span></span>

## <span data-ttu-id="36abb-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36abb-122">OUTPUTS</span></span>

### <span data-ttu-id="36abb-123">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="36abb-123">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="36abb-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="36abb-124">NOTES</span></span>

## <span data-ttu-id="36abb-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36abb-125">RELATED LINKS</span></span>

[<span data-ttu-id="36abb-126">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="36abb-126">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
