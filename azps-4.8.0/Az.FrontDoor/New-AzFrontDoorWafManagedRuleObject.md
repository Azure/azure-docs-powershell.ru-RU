---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 7c9ace339da9639404072fd802782aee43d8ab37
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243572"
---
# <span data-ttu-id="088bd-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="088bd-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="088bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="088bd-102">SYNOPSIS</span></span>
<span data-ttu-id="088bd-103">Создание объекта ManagedRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="088bd-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="088bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="088bd-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="088bd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="088bd-105">DESCRIPTION</span></span>
<span data-ttu-id="088bd-106">Создание объекта ManagedRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="088bd-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="088bd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="088bd-107">EXAMPLES</span></span>

### <span data-ttu-id="088bd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="088bd-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="088bd-109">Создание объекта ManagedRule</span><span class="sxs-lookup"><span data-stu-id="088bd-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="088bd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="088bd-110">PARAMETERS</span></span>

### <span data-ttu-id="088bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="088bd-111">-DefaultProfile</span></span>
<span data-ttu-id="088bd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="088bd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="088bd-113">-Исключение</span><span class="sxs-lookup"><span data-stu-id="088bd-113">-Exclusion</span></span>
<span data-ttu-id="088bd-114">Глобаль</span><span class="sxs-lookup"><span data-stu-id="088bd-114">Exclusion</span></span>

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

### <span data-ttu-id="088bd-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="088bd-115">-RuleGroupOverride</span></span>
<span data-ttu-id="088bd-116">Список конфигурации переопределения поставщика управляемых служб Azure</span><span class="sxs-lookup"><span data-stu-id="088bd-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="088bd-117">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="088bd-117">-Type</span></span>
<span data-ttu-id="088bd-118">Тип набора правил</span><span class="sxs-lookup"><span data-stu-id="088bd-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="088bd-119">-Version</span><span class="sxs-lookup"><span data-stu-id="088bd-119">-Version</span></span>
<span data-ttu-id="088bd-120">Версия набора правил</span><span class="sxs-lookup"><span data-stu-id="088bd-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="088bd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="088bd-121">CommonParameters</span></span>
<span data-ttu-id="088bd-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="088bd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="088bd-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="088bd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="088bd-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="088bd-124">INPUTS</span></span>

### <span data-ttu-id="088bd-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="088bd-125">None</span></span>

## <span data-ttu-id="088bd-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="088bd-126">OUTPUTS</span></span>

### <span data-ttu-id="088bd-127">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="088bd-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="088bd-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="088bd-128">NOTES</span></span>

## <span data-ttu-id="088bd-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="088bd-129">RELATED LINKS</span></span>

<span data-ttu-id="088bd-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="088bd-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
