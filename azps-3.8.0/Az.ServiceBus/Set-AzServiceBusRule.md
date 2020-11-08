---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: b86b9629062515afb1ee70e7c7372cbc7687bfa5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065553"
---
# <span data-ttu-id="43ccf-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="43ccf-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="43ccf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="43ccf-103">Обновляет указанное описание правила для данной подписки.</span><span class="sxs-lookup"><span data-stu-id="43ccf-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="43ccf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43ccf-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43ccf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43ccf-105">DESCRIPTION</span></span>
<span data-ttu-id="43ccf-106">Командлет **Set-AzServiceBusRule** обновляет описание указанного правила данной подписки.</span><span class="sxs-lookup"><span data-stu-id="43ccf-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="43ccf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43ccf-107">EXAMPLES</span></span>

### <span data-ttu-id="43ccf-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="43ccf-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="43ccf-109">Обновляет выражение SQL Expression **mysqlexpression = "Condition"** правила `SBRule` подписки `SBSubscription` в разделе `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="43ccf-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="43ccf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43ccf-110">PARAMETERS</span></span>

### <span data-ttu-id="43ccf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ccf-111">-DefaultProfile</span></span>
<span data-ttu-id="43ccf-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43ccf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43ccf-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43ccf-113">-InputObject</span></span>
<span data-ttu-id="43ccf-114">Определение правил ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="43ccf-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ccf-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="43ccf-115">-Name</span></span>
<span data-ttu-id="43ccf-116">Имя правила.</span><span class="sxs-lookup"><span data-stu-id="43ccf-116">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ccf-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="43ccf-117">-Namespace</span></span>
<span data-ttu-id="43ccf-118">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="43ccf-118">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ccf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43ccf-119">-ResourceGroupName</span></span>
<span data-ttu-id="43ccf-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="43ccf-120">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ccf-121">-Подписка</span><span class="sxs-lookup"><span data-stu-id="43ccf-121">-Subscription</span></span>
<span data-ttu-id="43ccf-122">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="43ccf-122">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ccf-123">-Темы</span><span class="sxs-lookup"><span data-stu-id="43ccf-123">-Topic</span></span>
<span data-ttu-id="43ccf-124">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="43ccf-124">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ccf-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43ccf-125">-Confirm</span></span>
<span data-ttu-id="43ccf-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="43ccf-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ccf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43ccf-127">-WhatIf</span></span>
<span data-ttu-id="43ccf-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="43ccf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43ccf-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="43ccf-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ccf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ccf-130">CommonParameters</span></span>
<span data-ttu-id="43ccf-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43ccf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ccf-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43ccf-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ccf-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43ccf-133">INPUTS</span></span>

### <span data-ttu-id="43ccf-134">System. String</span><span class="sxs-lookup"><span data-stu-id="43ccf-134">System.String</span></span>

### <span data-ttu-id="43ccf-135">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="43ccf-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="43ccf-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43ccf-136">OUTPUTS</span></span>

### <span data-ttu-id="43ccf-137">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="43ccf-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="43ccf-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="43ccf-138">NOTES</span></span>

## <span data-ttu-id="43ccf-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43ccf-139">RELATED LINKS</span></span>
