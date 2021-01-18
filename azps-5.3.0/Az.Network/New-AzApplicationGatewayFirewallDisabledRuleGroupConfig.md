---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5eafcfc825b710e31954e247e4114d0f90e97c41
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506479"
---
# <span data-ttu-id="677b5-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="677b5-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="677b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="677b5-102">SYNOPSIS</span></span>
<span data-ttu-id="677b5-103">Создает новую отключенную группу правил.</span><span class="sxs-lookup"><span data-stu-id="677b5-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="677b5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="677b5-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="677b5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="677b5-105">DESCRIPTION</span></span>
<span data-ttu-id="677b5-106">Для создания новой отключенной группы правил будет создаваться новый cmdlet **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.**</span><span class="sxs-lookup"><span data-stu-id="677b5-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="677b5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="677b5-107">EXAMPLES</span></span>

### <span data-ttu-id="677b5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="677b5-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="677b5-109">Команда создает конфигурацию отключенной группы правил для группы правил REQUEST-942-APPLICATION-ATTACK-SQLI, включаемую правило 942130 и правило 942140.</span><span class="sxs-lookup"><span data-stu-id="677b5-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="677b5-110">Новая отключенная конфигурация группы правил будет сохранена в $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="677b5-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="677b5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="677b5-111">PARAMETERS</span></span>

### <span data-ttu-id="677b5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="677b5-112">-DefaultProfile</span></span>
<span data-ttu-id="677b5-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="677b5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="677b5-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="677b5-114">-RuleGroupName</span></span>
<span data-ttu-id="677b5-115">Имя группы правил, которая будет отключена.</span><span class="sxs-lookup"><span data-stu-id="677b5-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="677b5-116">-Rules</span><span class="sxs-lookup"><span data-stu-id="677b5-116">-Rules</span></span>
<span data-ttu-id="677b5-117">Список отключенных правил.</span><span class="sxs-lookup"><span data-stu-id="677b5-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="677b5-118">Если NULL, все правила группы правил будут отключены.</span><span class="sxs-lookup"><span data-stu-id="677b5-118">If null, all rules of the rule group will be disabled.</span></span>

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

### <span data-ttu-id="677b5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="677b5-119">CommonParameters</span></span>
<span data-ttu-id="677b5-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="677b5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="677b5-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="677b5-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="677b5-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="677b5-122">INPUTS</span></span>

### <span data-ttu-id="677b5-123">Нет</span><span class="sxs-lookup"><span data-stu-id="677b5-123">None</span></span>

## <span data-ttu-id="677b5-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="677b5-124">OUTPUTS</span></span>

### <span data-ttu-id="677b5-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="677b5-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="677b5-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="677b5-126">NOTES</span></span>

## <span data-ttu-id="677b5-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="677b5-127">RELATED LINKS</span></span>

[<span data-ttu-id="677b5-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="677b5-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="677b5-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="677b5-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

