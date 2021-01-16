---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: b25c25b642f8c912f62f75788e69e96c3ebdc73c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421919"
---
# <span data-ttu-id="7d3a9-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="7d3a9-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="7d3a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d3a9-102">SYNOPSIS</span></span>
<span data-ttu-id="7d3a9-103">Создает новое пользовательское правило для политики брандмауэра шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="7d3a9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7d3a9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d3a9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d3a9-105">DESCRIPTION</span></span>
<span data-ttu-id="7d3a9-106">**New-AzApplicationGatewayFirewallCustomRule** создает пользовательское правило для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="7d3a9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7d3a9-107">EXAMPLES</span></span>

### <span data-ttu-id="7d3a9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7d3a9-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -MatchCondition $condtion -Action Allow
```

<span data-ttu-id="7d3a9-109">Команда создает новое пользовательское правило с именем примера правила, приоритетом 1 и типом "Правило MatchRule" с условием, определенным в переменной условия, действие разрешает.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="7d3a9-110">Новое пользовательское правило для совпадений будет сохранено в $customRule.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="7d3a9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d3a9-111">PARAMETERS</span></span>

### <span data-ttu-id="7d3a9-112">-Action</span><span class="sxs-lookup"><span data-stu-id="7d3a9-112">-Action</span></span>
<span data-ttu-id="7d3a9-113">Тип действий.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-113">Type of Actions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d3a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d3a9-114">-DefaultProfile</span></span>
<span data-ttu-id="7d3a9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d3a9-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="7d3a9-116">-MatchCondition</span></span>
<span data-ttu-id="7d3a9-117">Список условий совпадения.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-117">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d3a9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7d3a9-118">-Name</span></span>
<span data-ttu-id="7d3a9-119">Имя правила.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="7d3a9-120">-Priority</span><span class="sxs-lookup"><span data-stu-id="7d3a9-120">-Priority</span></span>
<span data-ttu-id="7d3a9-121">В нем описывается приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-121">Describes priority of the rule.</span></span>
<span data-ttu-id="7d3a9-122">Правила с низким значением будут оцениваться перед правилами с более высоким значением.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d3a9-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="7d3a9-123">-RuleType</span></span>
<span data-ttu-id="7d3a9-124">Описание типа правила.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-124">Describes type of rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d3a9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d3a9-125">CommonParameters</span></span>
<span data-ttu-id="7d3a9-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d3a9-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d3a9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d3a9-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d3a9-128">INPUTS</span></span>

### <span data-ttu-id="7d3a9-129">Нет</span><span class="sxs-lookup"><span data-stu-id="7d3a9-129">None</span></span>

## <span data-ttu-id="7d3a9-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d3a9-130">OUTPUTS</span></span>

### <span data-ttu-id="7d3a9-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="7d3a9-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="7d3a9-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7d3a9-132">NOTES</span></span>

## <span data-ttu-id="7d3a9-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d3a9-133">RELATED LINKS</span></span>