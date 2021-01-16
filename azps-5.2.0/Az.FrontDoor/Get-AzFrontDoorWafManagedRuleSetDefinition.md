---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409420"
---
# <span data-ttu-id="d2c21-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="d2c21-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="d2c21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2c21-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c21-103">Получить определения набора правил для управляемых правил WAF</span><span class="sxs-lookup"><span data-stu-id="d2c21-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="d2c21-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d2c21-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2c21-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2c21-105">DESCRIPTION</span></span>
<span data-ttu-id="d2c21-106">Список определений наборов управляемых правил WAF, которые нужно использовать в качестве справки</span><span class="sxs-lookup"><span data-stu-id="d2c21-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="d2c21-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d2c21-107">EXAMPLES</span></span>

### <span data-ttu-id="d2c21-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2c21-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="d2c21-109">{{ Добавьте здесь описание примера }}</span><span class="sxs-lookup"><span data-stu-id="d2c21-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="d2c21-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2c21-110">PARAMETERS</span></span>

### <span data-ttu-id="d2c21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c21-111">-DefaultProfile</span></span>
<span data-ttu-id="d2c21-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2c21-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2c21-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c21-113">CommonParameters</span></span>
<span data-ttu-id="d2c21-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2c21-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c21-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2c21-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c21-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2c21-116">INPUTS</span></span>

### <span data-ttu-id="d2c21-117">Нет</span><span class="sxs-lookup"><span data-stu-id="d2c21-117">None</span></span>

## <span data-ttu-id="d2c21-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d2c21-118">OUTPUTS</span></span>

### <span data-ttu-id="d2c21-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="d2c21-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="d2c21-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d2c21-120">NOTES</span></span>

## <span data-ttu-id="d2c21-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2c21-121">RELATED LINKS</span></span>

<span data-ttu-id="d2c21-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="d2c21-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
