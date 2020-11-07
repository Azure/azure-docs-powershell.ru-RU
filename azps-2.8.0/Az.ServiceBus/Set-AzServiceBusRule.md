---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: 0beea3a39fdad5348d84f42ff2fe95cbf3ed6b9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905329"
---
# <span data-ttu-id="27513-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="27513-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="27513-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27513-102">SYNOPSIS</span></span>
<span data-ttu-id="27513-103">Обновляет указанное описание правила для данной подписки.</span><span class="sxs-lookup"><span data-stu-id="27513-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="27513-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27513-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27513-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27513-105">DESCRIPTION</span></span>
<span data-ttu-id="27513-106">Командлет **Set-AzServiceBusRule** обновляет описание указанного правила данной подписки.</span><span class="sxs-lookup"><span data-stu-id="27513-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="27513-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27513-107">EXAMPLES</span></span>

### <span data-ttu-id="27513-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="27513-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="27513-109">Обновляет выражение SQL Expression **mysqlexpression = "Condition"** правила `SBRule` подписки `SBSubscription` в разделе `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="27513-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="27513-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27513-110">PARAMETERS</span></span>

### <span data-ttu-id="27513-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27513-111">-DefaultProfile</span></span>
<span data-ttu-id="27513-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27513-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27513-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27513-113">-InputObject</span></span>
<span data-ttu-id="27513-114">Определение правил ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="27513-114">ServiceBus Rules definition.</span></span>

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

### <span data-ttu-id="27513-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="27513-115">-Name</span></span>
<span data-ttu-id="27513-116">Имя правила.</span><span class="sxs-lookup"><span data-stu-id="27513-116">Rule Name.</span></span>

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

### <span data-ttu-id="27513-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="27513-117">-Namespace</span></span>
<span data-ttu-id="27513-118">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="27513-118">Namespace Name.</span></span>

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

### <span data-ttu-id="27513-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27513-119">-ResourceGroupName</span></span>
<span data-ttu-id="27513-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27513-120">The name of the resource group</span></span>

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

### <span data-ttu-id="27513-121">-Подписка</span><span class="sxs-lookup"><span data-stu-id="27513-121">-Subscription</span></span>
<span data-ttu-id="27513-122">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="27513-122">Subscription Name.</span></span>

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

### <span data-ttu-id="27513-123">-Темы</span><span class="sxs-lookup"><span data-stu-id="27513-123">-Topic</span></span>
<span data-ttu-id="27513-124">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="27513-124">Topic Name.</span></span>

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

### <span data-ttu-id="27513-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27513-125">-Confirm</span></span>
<span data-ttu-id="27513-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="27513-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27513-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27513-127">-WhatIf</span></span>
<span data-ttu-id="27513-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="27513-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27513-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="27513-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27513-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27513-130">CommonParameters</span></span>
<span data-ttu-id="27513-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27513-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27513-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27513-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27513-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27513-133">INPUTS</span></span>

### <span data-ttu-id="27513-134">System. String</span><span class="sxs-lookup"><span data-stu-id="27513-134">System.String</span></span>

### <span data-ttu-id="27513-135">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="27513-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="27513-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27513-136">OUTPUTS</span></span>

### <span data-ttu-id="27513-137">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="27513-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="27513-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="27513-138">NOTES</span></span>

## <span data-ttu-id="27513-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27513-139">RELATED LINKS</span></span>
