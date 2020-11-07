---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: 869bfdaa7ff772980b7acf1caee6c7d6a8784d37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729180"
---
# <span data-ttu-id="fc17a-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="fc17a-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="fc17a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc17a-102">SYNOPSIS</span></span>
<span data-ttu-id="fc17a-103">Создает новое правило для конкретной подписки на тему.</span><span class="sxs-lookup"><span data-stu-id="fc17a-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="fc17a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc17a-104">SYNTAX</span></span>

### <span data-ttu-id="fc17a-105">RulePropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fc17a-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc17a-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="fc17a-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc17a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc17a-107">DESCRIPTION</span></span>
<span data-ttu-id="fc17a-108">Командлет **New-AzServiceBusRule** создает новое правило для данной подписки.</span><span class="sxs-lookup"><span data-stu-id="fc17a-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="fc17a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc17a-109">EXAMPLES</span></span>

### <span data-ttu-id="fc17a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fc17a-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="fc17a-111">Командлет New-AzServiceBusRule создает новое правило для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="fc17a-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="fc17a-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fc17a-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="fc17a-113">Командлет New-AzServiceBusRule создает новое правило для указанной подписки с помощью ActionFilter.</span><span class="sxs-lookup"><span data-stu-id="fc17a-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="fc17a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc17a-114">PARAMETERS</span></span>

### <span data-ttu-id="fc17a-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="fc17a-115">-ActionSqlExpression</span></span>
<span data-ttu-id="fc17a-116">Выражение SqlFillter действия</span><span class="sxs-lookup"><span data-stu-id="fc17a-116">Action SqlFillter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc17a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc17a-117">-DefaultProfile</span></span>
<span data-ttu-id="fc17a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc17a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc17a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fc17a-119">-Name</span></span>
<span data-ttu-id="fc17a-120">Имя правила</span><span class="sxs-lookup"><span data-stu-id="fc17a-120">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc17a-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fc17a-121">-Namespace</span></span>
<span data-ttu-id="fc17a-122">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="fc17a-122">Namespace Name</span></span>

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

### <span data-ttu-id="fc17a-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="fc17a-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="fc17a-124">Действие требует предварительной обработки</span><span class="sxs-lookup"><span data-stu-id="fc17a-124">Action Requires Preprocessing</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc17a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc17a-125">-ResourceGroupName</span></span>
<span data-ttu-id="fc17a-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc17a-126">The name of the resource group</span></span>

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

### <span data-ttu-id="fc17a-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="fc17a-127">-SqlExpression</span></span>
<span data-ttu-id="fc17a-128">Выражение SQL фильтрацию</span><span class="sxs-lookup"><span data-stu-id="fc17a-128">Sql Fillter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc17a-129">-Подписка</span><span class="sxs-lookup"><span data-stu-id="fc17a-129">-Subscription</span></span>
<span data-ttu-id="fc17a-130">Название подписки</span><span class="sxs-lookup"><span data-stu-id="fc17a-130">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc17a-131">-Темы</span><span class="sxs-lookup"><span data-stu-id="fc17a-131">-Topic</span></span>
<span data-ttu-id="fc17a-132">Название раздела</span><span class="sxs-lookup"><span data-stu-id="fc17a-132">Topic Name</span></span>

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

### <span data-ttu-id="fc17a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc17a-133">-Confirm</span></span>
<span data-ttu-id="fc17a-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fc17a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc17a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc17a-135">-WhatIf</span></span>
<span data-ttu-id="fc17a-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fc17a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc17a-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fc17a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc17a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc17a-138">CommonParameters</span></span>
<span data-ttu-id="fc17a-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc17a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc17a-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc17a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc17a-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc17a-141">INPUTS</span></span>

### <span data-ttu-id="fc17a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fc17a-142">System.String</span></span>

## <span data-ttu-id="fc17a-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc17a-143">OUTPUTS</span></span>

### <span data-ttu-id="fc17a-144">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="fc17a-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="fc17a-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc17a-145">NOTES</span></span>

## <span data-ttu-id="fc17a-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc17a-146">RELATED LINKS</span></span>
