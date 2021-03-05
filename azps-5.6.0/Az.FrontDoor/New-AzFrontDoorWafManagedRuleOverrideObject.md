---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: ee4193fff69e8b46362ac75019cc76178001c2e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970851"
---
# <span data-ttu-id="67ee2-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="67ee2-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="67ee2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67ee2-102">SYNOPSIS</span></span>
<span data-ttu-id="67ee2-103">Создание объекта переопределения управляемых правил</span><span class="sxs-lookup"><span data-stu-id="67ee2-103">Create managed rule override object</span></span>

## <span data-ttu-id="67ee2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67ee2-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67ee2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67ee2-105">DESCRIPTION</span></span>
<span data-ttu-id="67ee2-106">Создайте объект PSAzureManagedRuleOverride для управляемой группы правил WAF, переопределяйте создание объектов.</span><span class="sxs-lookup"><span data-stu-id="67ee2-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="67ee2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67ee2-107">EXAMPLES</span></span>

### <span data-ttu-id="67ee2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="67ee2-108">Example 1</span></span>
<span data-ttu-id="67ee2-109">Создайте объект переопределения правил для правила 942250 (в группе SQLI).</span><span class="sxs-lookup"><span data-stu-id="67ee2-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="67ee2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67ee2-110">PARAMETERS</span></span>

### <span data-ttu-id="67ee2-111">-Action</span><span class="sxs-lookup"><span data-stu-id="67ee2-111">-Action</span></span>
<span data-ttu-id="67ee2-112">Действие переопределения</span><span class="sxs-lookup"><span data-stu-id="67ee2-112">Override Action</span></span>

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

### <span data-ttu-id="67ee2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ee2-113">-DefaultProfile</span></span>
<span data-ttu-id="67ee2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67ee2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67ee2-115">-Disabled</span><span class="sxs-lookup"><span data-stu-id="67ee2-115">-Disabled</span></span>
<span data-ttu-id="67ee2-116">Состояние отключено</span><span class="sxs-lookup"><span data-stu-id="67ee2-116">Disabled state</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ee2-117">-Исключение</span><span class="sxs-lookup"><span data-stu-id="67ee2-117">-Exclusion</span></span>
<span data-ttu-id="67ee2-118">Исключение</span><span class="sxs-lookup"><span data-stu-id="67ee2-118">Exclusion</span></span>

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

### <span data-ttu-id="67ee2-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="67ee2-119">-RuleId</span></span>
<span data-ttu-id="67ee2-120">ИД правила</span><span class="sxs-lookup"><span data-stu-id="67ee2-120">Rule ID</span></span>

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

### <span data-ttu-id="67ee2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ee2-121">CommonParameters</span></span>
<span data-ttu-id="67ee2-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67ee2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ee2-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67ee2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ee2-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67ee2-124">INPUTS</span></span>

### <span data-ttu-id="67ee2-125">Нет</span><span class="sxs-lookup"><span data-stu-id="67ee2-125">None</span></span>

## <span data-ttu-id="67ee2-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67ee2-126">OUTPUTS</span></span>

### <span data-ttu-id="67ee2-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="67ee2-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="67ee2-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67ee2-128">NOTES</span></span>

## <span data-ttu-id="67ee2-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67ee2-129">RELATED LINKS</span></span>

[<span data-ttu-id="67ee2-130">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="67ee2-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)