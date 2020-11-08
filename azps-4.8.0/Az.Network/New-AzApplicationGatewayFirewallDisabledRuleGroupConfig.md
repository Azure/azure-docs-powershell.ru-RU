---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5eafcfc825b710e31954e247e4114d0f90e97c41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243029"
---
# <span data-ttu-id="f7bb7-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="f7bb7-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="f7bb7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7bb7-102">SYNOPSIS</span></span>
<span data-ttu-id="f7bb7-103">Создание новой конфигурации отключенной группы правил.</span><span class="sxs-lookup"><span data-stu-id="f7bb7-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="f7bb7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7bb7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7bb7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7bb7-105">DESCRIPTION</span></span>
<span data-ttu-id="f7bb7-106">Командлет **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** создает новую конфигурацию отключенной группы правил.</span><span class="sxs-lookup"><span data-stu-id="f7bb7-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="f7bb7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7bb7-107">EXAMPLES</span></span>

### <span data-ttu-id="f7bb7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f7bb7-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="f7bb7-109">Команда создает новую конфигурацию отключенной группы правил для группы правил с именем "запрос-942-приложение-АТАКа-SQLI" с правилом 942130 и отключением правила 942140.</span><span class="sxs-lookup"><span data-stu-id="f7bb7-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="f7bb7-110">Новая отключенная Конфигурация группы правил сохраняется в $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="f7bb7-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="f7bb7-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7bb7-111">PARAMETERS</span></span>

### <span data-ttu-id="f7bb7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7bb7-112">-DefaultProfile</span></span>
<span data-ttu-id="f7bb7-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7bb7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7bb7-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="f7bb7-114">-RuleGroupName</span></span>
<span data-ttu-id="f7bb7-115">Имя группы правил, которая будет отключена.</span><span class="sxs-lookup"><span data-stu-id="f7bb7-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="f7bb7-116">-Правила</span><span class="sxs-lookup"><span data-stu-id="f7bb7-116">-Rules</span></span>
<span data-ttu-id="f7bb7-117">Список правил, которые будут отключены.</span><span class="sxs-lookup"><span data-stu-id="f7bb7-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="f7bb7-118">Если значение равно null, все правила группы правил будут отключены.</span><span class="sxs-lookup"><span data-stu-id="f7bb7-118">If null, all rules of the rule group will be disabled.</span></span>

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

### <span data-ttu-id="f7bb7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7bb7-119">CommonParameters</span></span>
<span data-ttu-id="f7bb7-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7bb7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7bb7-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7bb7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7bb7-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7bb7-122">INPUTS</span></span>

### <span data-ttu-id="f7bb7-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="f7bb7-123">None</span></span>

## <span data-ttu-id="f7bb7-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7bb7-124">OUTPUTS</span></span>

### <span data-ttu-id="f7bb7-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="f7bb7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="f7bb7-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7bb7-126">NOTES</span></span>

## <span data-ttu-id="f7bb7-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7bb7-127">RELATED LINKS</span></span>

[<span data-ttu-id="f7bb7-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7bb7-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="f7bb7-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7bb7-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)
