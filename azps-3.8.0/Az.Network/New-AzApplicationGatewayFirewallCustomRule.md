---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: d8e22f5eb0e504757bd94fa5235d07ad3e3db998
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074830"
---
# <span data-ttu-id="99462-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="99462-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="99462-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99462-102">SYNOPSIS</span></span>
<span data-ttu-id="99462-103">Создание нового настраиваемого правила для политики брандмауэра для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="99462-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="99462-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99462-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99462-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99462-105">DESCRIPTION</span></span>
<span data-ttu-id="99462-106">Параметр **New-AzApplicationGatewayFirewallCustomRule** создает настраиваемое правило для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="99462-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="99462-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99462-107">EXAMPLES</span></span>

### <span data-ttu-id="99462-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="99462-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -matchConditons $condtion -Action Allow
```

<span data-ttu-id="99462-109">Команда создает новое настраиваемое правило с именем примера-правила, приоритет 1, а тип правила — MatchRule с условием, определенным в переменной Condition, действие будет разрешено.</span><span class="sxs-lookup"><span data-stu-id="99462-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="99462-110">Новое настраиваемое правило соответствия сохраняется в $customRule.</span><span class="sxs-lookup"><span data-stu-id="99462-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="99462-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99462-111">PARAMETERS</span></span>

### <span data-ttu-id="99462-112">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="99462-112">-Action</span></span>
<span data-ttu-id="99462-113">Тип действий.</span><span class="sxs-lookup"><span data-stu-id="99462-113">Type of Actions.</span></span>

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

### <span data-ttu-id="99462-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99462-114">-DefaultProfile</span></span>
<span data-ttu-id="99462-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99462-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99462-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="99462-116">-MatchCondition</span></span>
<span data-ttu-id="99462-117">Список условий соответствия.</span><span class="sxs-lookup"><span data-stu-id="99462-117">List of match conditions.</span></span>

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

### <span data-ttu-id="99462-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="99462-118">-Name</span></span>
<span data-ttu-id="99462-119">Имя правила.</span><span class="sxs-lookup"><span data-stu-id="99462-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="99462-120">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="99462-120">-Priority</span></span>
<span data-ttu-id="99462-121">Описывает приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="99462-121">Describes priority of the rule.</span></span>
<span data-ttu-id="99462-122">Правила с более низким значением будут обрабатываться Раньше правил с более высоким значением.</span><span class="sxs-lookup"><span data-stu-id="99462-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

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

### <span data-ttu-id="99462-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="99462-123">-RuleType</span></span>
<span data-ttu-id="99462-124">Описывает тип правила.</span><span class="sxs-lookup"><span data-stu-id="99462-124">Describes type of rule.</span></span>

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

### <span data-ttu-id="99462-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99462-125">CommonParameters</span></span>
<span data-ttu-id="99462-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99462-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99462-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99462-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99462-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99462-128">INPUTS</span></span>

### <span data-ttu-id="99462-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="99462-129">None</span></span>

## <span data-ttu-id="99462-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99462-130">OUTPUTS</span></span>

### <span data-ttu-id="99462-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="99462-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="99462-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="99462-132">NOTES</span></span>

## <span data-ttu-id="99462-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99462-133">RELATED LINKS</span></span>
