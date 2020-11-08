---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243574"
---
# <span data-ttu-id="668f1-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="668f1-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="668f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="668f1-102">SYNOPSIS</span></span>
<span data-ttu-id="668f1-103">Создание объекта переопределения управляемого правила</span><span class="sxs-lookup"><span data-stu-id="668f1-103">Create managed rule override object</span></span>

## <span data-ttu-id="668f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="668f1-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="668f1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="668f1-105">DESCRIPTION</span></span>
<span data-ttu-id="668f1-106">Создать объект PSAzureManagedRuleOverride для управляемой группы правил WAF, которая переопределяет создание объекта.</span><span class="sxs-lookup"><span data-stu-id="668f1-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="668f1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="668f1-107">EXAMPLES</span></span>

### <span data-ttu-id="668f1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="668f1-108">Example 1</span></span>
<span data-ttu-id="668f1-109">Создайте объект переопределения управляемого правила для правила 942250 (которое находится в группе SQLI).</span><span class="sxs-lookup"><span data-stu-id="668f1-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="668f1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="668f1-110">PARAMETERS</span></span>

### <span data-ttu-id="668f1-111">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="668f1-111">-Action</span></span>
<span data-ttu-id="668f1-112">Переопределение действия</span><span class="sxs-lookup"><span data-stu-id="668f1-112">Override Action</span></span>

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

### <span data-ttu-id="668f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="668f1-113">-DefaultProfile</span></span>
<span data-ttu-id="668f1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="668f1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="668f1-115">-Отключено</span><span class="sxs-lookup"><span data-stu-id="668f1-115">-Disabled</span></span>
<span data-ttu-id="668f1-116">Состояние "отключено"</span><span class="sxs-lookup"><span data-stu-id="668f1-116">Disabled state</span></span>

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

### <span data-ttu-id="668f1-117">-Исключение</span><span class="sxs-lookup"><span data-stu-id="668f1-117">-Exclusion</span></span>
<span data-ttu-id="668f1-118">Глобаль</span><span class="sxs-lookup"><span data-stu-id="668f1-118">Exclusion</span></span>

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

### <span data-ttu-id="668f1-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="668f1-119">-RuleId</span></span>
<span data-ttu-id="668f1-120">КОД правила</span><span class="sxs-lookup"><span data-stu-id="668f1-120">Rule ID</span></span>

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

### <span data-ttu-id="668f1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="668f1-121">CommonParameters</span></span>
<span data-ttu-id="668f1-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="668f1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="668f1-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="668f1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="668f1-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="668f1-124">INPUTS</span></span>

### <span data-ttu-id="668f1-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="668f1-125">None</span></span>

## <span data-ttu-id="668f1-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="668f1-126">OUTPUTS</span></span>

### <span data-ttu-id="668f1-127">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="668f1-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="668f1-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="668f1-128">NOTES</span></span>

## <span data-ttu-id="668f1-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="668f1-129">RELATED LINKS</span></span>

[<span data-ttu-id="668f1-130">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="668f1-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)