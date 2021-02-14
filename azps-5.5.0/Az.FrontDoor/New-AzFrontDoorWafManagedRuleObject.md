---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 266d553f70cb5c128df1d266f95ee93cb1eb013c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237826"
---
# <span data-ttu-id="cda16-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="cda16-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="cda16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cda16-102">SYNOPSIS</span></span>
<span data-ttu-id="cda16-103">Создание объекта ManagedRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="cda16-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="cda16-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cda16-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cda16-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cda16-105">DESCRIPTION</span></span>
<span data-ttu-id="cda16-106">Создание объекта ManagedRule для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="cda16-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="cda16-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cda16-107">EXAMPLES</span></span>

### <span data-ttu-id="cda16-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cda16-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="cda16-109">Создание объекта ManagedRule</span><span class="sxs-lookup"><span data-stu-id="cda16-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="cda16-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cda16-110">PARAMETERS</span></span>

### <span data-ttu-id="cda16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda16-111">-DefaultProfile</span></span>
<span data-ttu-id="cda16-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cda16-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cda16-113">-Исключение</span><span class="sxs-lookup"><span data-stu-id="cda16-113">-Exclusion</span></span>
<span data-ttu-id="cda16-114">Исключение</span><span class="sxs-lookup"><span data-stu-id="cda16-114">Exclusion</span></span>

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

### <span data-ttu-id="cda16-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="cda16-115">-RuleGroupOverride</span></span>
<span data-ttu-id="cda16-116">Список переопределений поставщика, управляемого azure</span><span class="sxs-lookup"><span data-stu-id="cda16-116">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="cda16-117">-Type</span><span class="sxs-lookup"><span data-stu-id="cda16-117">-Type</span></span>
<span data-ttu-id="cda16-118">Тип правила</span><span class="sxs-lookup"><span data-stu-id="cda16-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="cda16-119">-Version</span><span class="sxs-lookup"><span data-stu-id="cda16-119">-Version</span></span>
<span data-ttu-id="cda16-120">Версия правила</span><span class="sxs-lookup"><span data-stu-id="cda16-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="cda16-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda16-121">CommonParameters</span></span>
<span data-ttu-id="cda16-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cda16-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda16-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cda16-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda16-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cda16-124">INPUTS</span></span>

### <span data-ttu-id="cda16-125">Нет</span><span class="sxs-lookup"><span data-stu-id="cda16-125">None</span></span>

## <span data-ttu-id="cda16-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cda16-126">OUTPUTS</span></span>

### <span data-ttu-id="cda16-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="cda16-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="cda16-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cda16-128">NOTES</span></span>

## <span data-ttu-id="cda16-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cda16-129">RELATED LINKS</span></span>

<span data-ttu-id="cda16-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="cda16-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
