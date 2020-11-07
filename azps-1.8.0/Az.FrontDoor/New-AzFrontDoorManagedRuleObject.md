---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
ms.openlocfilehash: b6035e991b585ba296a9fdc591ccbdb44dd1b089
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900606"
---
# <span data-ttu-id="834b6-101">New-AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="834b6-101">New-AzFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="834b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="834b6-102">SYNOPSIS</span></span>
<span data-ttu-id="834b6-103">Создание объекта ManagedRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="834b6-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="834b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="834b6-104">SYNTAX</span></span>

```
New-AzFrontDoorManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="834b6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="834b6-105">DESCRIPTION</span></span>
<span data-ttu-id="834b6-106">Создание объекта ManagedRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="834b6-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="834b6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="834b6-107">EXAMPLES</span></span>

### <span data-ttu-id="834b6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="834b6-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="834b6-109">Создание объекта ManagedRule</span><span class="sxs-lookup"><span data-stu-id="834b6-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="834b6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="834b6-110">PARAMETERS</span></span>

### <span data-ttu-id="834b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="834b6-111">-DefaultProfile</span></span>
<span data-ttu-id="834b6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="834b6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="834b6-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="834b6-113">-RuleGroupOverride</span></span>
<span data-ttu-id="834b6-114">Список конфигурации переопределения поставщика управляемых служб Azure</span><span class="sxs-lookup"><span data-stu-id="834b6-114">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="834b6-115">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="834b6-115">-Type</span></span>
<span data-ttu-id="834b6-116">Тип набора правил</span><span class="sxs-lookup"><span data-stu-id="834b6-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="834b6-117">-Version</span><span class="sxs-lookup"><span data-stu-id="834b6-117">-Version</span></span>
<span data-ttu-id="834b6-118">Версия набора правил</span><span class="sxs-lookup"><span data-stu-id="834b6-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="834b6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="834b6-119">CommonParameters</span></span>
<span data-ttu-id="834b6-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="834b6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="834b6-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="834b6-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="834b6-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="834b6-122">INPUTS</span></span>

### <span data-ttu-id="834b6-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="834b6-123">None</span></span>

## <span data-ttu-id="834b6-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="834b6-124">OUTPUTS</span></span>

### <span data-ttu-id="834b6-125">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="834b6-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="834b6-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="834b6-126">NOTES</span></span>

## <span data-ttu-id="834b6-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="834b6-127">RELATED LINKS</span></span>

<span data-ttu-id="834b6-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md) 
 [New-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="834b6-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span></span>
