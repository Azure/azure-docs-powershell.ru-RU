---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 9d05502b518dcd10a22c9583546a2d010b424902
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230369"
---
# <span data-ttu-id="ea3a8-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="ea3a8-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="ea3a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea3a8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea3a8-103">Создание объекта RuleGroupOverride для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="ea3a8-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="ea3a8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ea3a8-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea3a8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea3a8-105">DESCRIPTION</span></span>
<span data-ttu-id="ea3a8-106">Создание объекта RuleGroupOverride для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="ea3a8-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="ea3a8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ea3a8-107">EXAMPLES</span></span>

### <span data-ttu-id="ea3a8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ea3a8-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="ea3a8-109">Создание объекта RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="ea3a8-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="ea3a8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea3a8-110">PARAMETERS</span></span>

### <span data-ttu-id="ea3a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea3a8-111">-DefaultProfile</span></span>
<span data-ttu-id="ea3a8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea3a8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea3a8-113">-Исключение</span><span class="sxs-lookup"><span data-stu-id="ea3a8-113">-Exclusion</span></span>
<span data-ttu-id="ea3a8-114">Исключение</span><span class="sxs-lookup"><span data-stu-id="ea3a8-114">Exclusion</span></span>

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

### <span data-ttu-id="ea3a8-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="ea3a8-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="ea3a8-116">Список переопределения правил</span><span class="sxs-lookup"><span data-stu-id="ea3a8-116">Rule override list</span></span>

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

### <span data-ttu-id="ea3a8-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="ea3a8-117">-RuleGroupName</span></span>
<span data-ttu-id="ea3a8-118">Имя группы правил, для которой применяются эти переопределения</span><span class="sxs-lookup"><span data-stu-id="ea3a8-118">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="ea3a8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea3a8-119">CommonParameters</span></span>
<span data-ttu-id="ea3a8-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea3a8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea3a8-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea3a8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea3a8-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea3a8-122">INPUTS</span></span>

### <span data-ttu-id="ea3a8-123">Нет</span><span class="sxs-lookup"><span data-stu-id="ea3a8-123">None</span></span>

## <span data-ttu-id="ea3a8-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ea3a8-124">OUTPUTS</span></span>

### <span data-ttu-id="ea3a8-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="ea3a8-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="ea3a8-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ea3a8-126">NOTES</span></span>

## <span data-ttu-id="ea3a8-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea3a8-127">RELATED LINKS</span></span>

[<span data-ttu-id="ea3a8-128">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="ea3a8-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
