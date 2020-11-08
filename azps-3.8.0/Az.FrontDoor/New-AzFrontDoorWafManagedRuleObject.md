---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 6e56ff9b174ec13d0844a1ac860d34043f8b73cf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073836"
---
# <span data-ttu-id="b8a48-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="b8a48-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="b8a48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8a48-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a48-103">Создание объекта ManagedRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="b8a48-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="b8a48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8a48-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8a48-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8a48-105">DESCRIPTION</span></span>
<span data-ttu-id="b8a48-106">Создание объекта ManagedRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="b8a48-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="b8a48-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8a48-107">EXAMPLES</span></span>

### <span data-ttu-id="b8a48-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b8a48-108">Example 1</span></span>
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

<span data-ttu-id="b8a48-109">Создание объекта ManagedRule</span><span class="sxs-lookup"><span data-stu-id="b8a48-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="b8a48-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8a48-110">PARAMETERS</span></span>

### <span data-ttu-id="b8a48-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a48-111">-DefaultProfile</span></span>
<span data-ttu-id="b8a48-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8a48-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8a48-113">-Исключение</span><span class="sxs-lookup"><span data-stu-id="b8a48-113">-Exclusion</span></span>
<span data-ttu-id="b8a48-114">Глобаль</span><span class="sxs-lookup"><span data-stu-id="b8a48-114">Exclusion</span></span>

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

### <span data-ttu-id="b8a48-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="b8a48-115">-RuleGroupOverride</span></span>
<span data-ttu-id="b8a48-116">Список конфигурации переопределения поставщика управляемых служб Azure</span><span class="sxs-lookup"><span data-stu-id="b8a48-116">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="b8a48-117">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="b8a48-117">-Type</span></span>
<span data-ttu-id="b8a48-118">Тип набора правил</span><span class="sxs-lookup"><span data-stu-id="b8a48-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="b8a48-119">-Version</span><span class="sxs-lookup"><span data-stu-id="b8a48-119">-Version</span></span>
<span data-ttu-id="b8a48-120">Версия набора правил</span><span class="sxs-lookup"><span data-stu-id="b8a48-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="b8a48-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a48-121">CommonParameters</span></span>
<span data-ttu-id="b8a48-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8a48-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a48-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8a48-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a48-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8a48-124">INPUTS</span></span>

### <span data-ttu-id="b8a48-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="b8a48-125">None</span></span>

## <span data-ttu-id="b8a48-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8a48-126">OUTPUTS</span></span>

### <span data-ttu-id="b8a48-127">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="b8a48-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="b8a48-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8a48-128">NOTES</span></span>

## <span data-ttu-id="b8a48-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8a48-129">RELATED LINKS</span></span>

<span data-ttu-id="b8a48-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="b8a48-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
