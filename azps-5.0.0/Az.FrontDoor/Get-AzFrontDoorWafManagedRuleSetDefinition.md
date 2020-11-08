---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249056"
---
# <span data-ttu-id="28c58-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="28c58-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="28c58-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28c58-102">SYNOPSIS</span></span>
<span data-ttu-id="28c58-103">Получение определений наборов управляемых правил WAF</span><span class="sxs-lookup"><span data-stu-id="28c58-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="28c58-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28c58-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28c58-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28c58-105">DESCRIPTION</span></span>
<span data-ttu-id="28c58-106">Получает список определений наборов правил управляемого WAF, которые можно использовать в качестве ссылки.</span><span class="sxs-lookup"><span data-stu-id="28c58-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="28c58-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28c58-107">EXAMPLES</span></span>

### <span data-ttu-id="28c58-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="28c58-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="28c58-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="28c58-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="28c58-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28c58-110">PARAMETERS</span></span>

### <span data-ttu-id="28c58-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28c58-111">-DefaultProfile</span></span>
<span data-ttu-id="28c58-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28c58-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28c58-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c58-113">CommonParameters</span></span>
<span data-ttu-id="28c58-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28c58-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c58-115">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28c58-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c58-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28c58-116">INPUTS</span></span>

### <span data-ttu-id="28c58-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="28c58-117">None</span></span>

## <span data-ttu-id="28c58-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28c58-118">OUTPUTS</span></span>

### <span data-ttu-id="28c58-119">Microsoft. Azure. Commands. FrontDoor. Models. PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="28c58-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="28c58-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="28c58-120">NOTES</span></span>

## <span data-ttu-id="28c58-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28c58-121">RELATED LINKS</span></span>

<span data-ttu-id="28c58-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="28c58-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
