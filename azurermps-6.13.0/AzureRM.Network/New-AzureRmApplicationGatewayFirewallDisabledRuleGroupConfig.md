---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5ccbeb355834cf1fccb7b4da87c70df72c1f8666
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564271"
---
# <span data-ttu-id="bf3ef-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="bf3ef-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="bf3ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf3ef-102">SYNOPSIS</span></span>
<span data-ttu-id="bf3ef-103">Создание новой конфигурации отключенной группы правил.</span><span class="sxs-lookup"><span data-stu-id="bf3ef-103">Creates a new disabled rule group configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf3ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf3ef-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String>
 [-Rules <System.Collections.Generic.List`1[System.Int32]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf3ef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf3ef-105">DESCRIPTION</span></span>
<span data-ttu-id="bf3ef-106">Командлет **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** создает новую конфигурацию отключенной группы правил.</span><span class="sxs-lookup"><span data-stu-id="bf3ef-106">The **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="bf3ef-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf3ef-107">EXAMPLES</span></span>

### <span data-ttu-id="bf3ef-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bf3ef-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="bf3ef-109">Команда создает новую конфигурацию отключенной группы правил для группы правил с именем "запрос-942-приложение-АТАКа-SQLI" с правилом 942130 и отключением правила 942140.</span><span class="sxs-lookup"><span data-stu-id="bf3ef-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="bf3ef-110">Новая отключенная Конфигурация группы правил сохраняется в $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="bf3ef-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="bf3ef-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf3ef-111">PARAMETERS</span></span>

### <span data-ttu-id="bf3ef-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf3ef-112">-DefaultProfile</span></span>
<span data-ttu-id="bf3ef-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf3ef-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf3ef-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="bf3ef-114">-RuleGroupName</span></span>
<span data-ttu-id="bf3ef-115">Имя группы правил, которая будет отключена.</span><span class="sxs-lookup"><span data-stu-id="bf3ef-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="bf3ef-116">-Правила</span><span class="sxs-lookup"><span data-stu-id="bf3ef-116">-Rules</span></span>
<span data-ttu-id="bf3ef-117">Список правил, которые будут отключены.</span><span class="sxs-lookup"><span data-stu-id="bf3ef-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="bf3ef-118">Если значение равно null, все правила группы правил будут отключены.</span><span class="sxs-lookup"><span data-stu-id="bf3ef-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf3ef-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf3ef-119">CommonParameters</span></span>
<span data-ttu-id="bf3ef-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf3ef-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf3ef-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf3ef-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf3ef-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf3ef-122">INPUTS</span></span>

### <span data-ttu-id="bf3ef-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="bf3ef-123">None</span></span>

## <span data-ttu-id="bf3ef-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf3ef-124">OUTPUTS</span></span>

### <span data-ttu-id="bf3ef-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="bf3ef-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="bf3ef-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf3ef-126">NOTES</span></span>

## <span data-ttu-id="bf3ef-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf3ef-127">RELATED LINKS</span></span>

[<span data-ttu-id="bf3ef-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf3ef-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="bf3ef-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf3ef-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

