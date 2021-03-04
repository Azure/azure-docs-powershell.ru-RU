---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5a96ea5ac1ded346e289d44f54762909d5f96e31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952195"
---
# <span data-ttu-id="4b988-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="4b988-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="4b988-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b988-102">SYNOPSIS</span></span>
<span data-ttu-id="4b988-103">Создает новую отключенную группу правил.</span><span class="sxs-lookup"><span data-stu-id="4b988-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="4b988-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4b988-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b988-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b988-105">DESCRIPTION</span></span>
<span data-ttu-id="4b988-106">Для создания новой отключенной группы правил будет создаваться новый cmdlet **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.**</span><span class="sxs-lookup"><span data-stu-id="4b988-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="4b988-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4b988-107">EXAMPLES</span></span>

### <span data-ttu-id="4b988-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4b988-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="4b988-109">Команда создает конфигурацию отключенной группы правил для группы правил REQUEST-942-APPLICATION-ATTACK-SQLI, для которого отключаются правило 942130 и правило 942140.</span><span class="sxs-lookup"><span data-stu-id="4b988-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="4b988-110">Новая отключенная конфигурация группы правил будет сохранена в $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="4b988-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="4b988-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b988-111">PARAMETERS</span></span>

### <span data-ttu-id="4b988-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b988-112">-DefaultProfile</span></span>
<span data-ttu-id="4b988-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b988-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b988-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="4b988-114">-RuleGroupName</span></span>
<span data-ttu-id="4b988-115">Имя группы правил, которая будет отключена.</span><span class="sxs-lookup"><span data-stu-id="4b988-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="4b988-116">-Rules</span><span class="sxs-lookup"><span data-stu-id="4b988-116">-Rules</span></span>
<span data-ttu-id="4b988-117">Список отключенных правил.</span><span class="sxs-lookup"><span data-stu-id="4b988-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="4b988-118">Если NULL, все правила группы правил будут отключены.</span><span class="sxs-lookup"><span data-stu-id="4b988-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b988-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b988-119">CommonParameters</span></span>
<span data-ttu-id="4b988-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b988-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b988-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b988-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b988-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b988-122">INPUTS</span></span>

### <span data-ttu-id="4b988-123">Нет</span><span class="sxs-lookup"><span data-stu-id="4b988-123">None</span></span>

## <span data-ttu-id="4b988-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4b988-124">OUTPUTS</span></span>

### <span data-ttu-id="4b988-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="4b988-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="4b988-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4b988-126">NOTES</span></span>

## <span data-ttu-id="4b988-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b988-127">RELATED LINKS</span></span>

[<span data-ttu-id="4b988-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b988-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="4b988-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b988-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

