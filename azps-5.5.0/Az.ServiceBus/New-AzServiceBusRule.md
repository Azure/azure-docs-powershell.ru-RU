---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: d667049fb512545aebfd9681b3ad3d9f44651951
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235721"
---
# <span data-ttu-id="fa286-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="fa286-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="fa286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa286-102">SYNOPSIS</span></span>
<span data-ttu-id="fa286-103">Создание правила для подписки на раздел.</span><span class="sxs-lookup"><span data-stu-id="fa286-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="fa286-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fa286-104">SYNTAX</span></span>

### <span data-ttu-id="fa286-105">Набор свойств правил (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa286-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa286-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="fa286-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa286-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa286-107">DESCRIPTION</span></span>
<span data-ttu-id="fa286-108">Для **данной подписки создается** новое правило.</span><span class="sxs-lookup"><span data-stu-id="fa286-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="fa286-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fa286-109">EXAMPLES</span></span>

### <span data-ttu-id="fa286-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fa286-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="fa286-111">С New-AzServiceBusRule создается новое правило для указанной Подписки.</span><span class="sxs-lookup"><span data-stu-id="fa286-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="fa286-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fa286-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="fa286-113">Для New-AzServiceBusRule с actionFilter будет создаваться новое правило для указанной Подписки.</span><span class="sxs-lookup"><span data-stu-id="fa286-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="fa286-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa286-114">PARAMETERS</span></span>

### <span data-ttu-id="fa286-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="fa286-115">-ActionSqlExpression</span></span>
<span data-ttu-id="fa286-116">Выражение SqlFilter действия</span><span class="sxs-lookup"><span data-stu-id="fa286-116">Action SqlFilter Expression</span></span>

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

### <span data-ttu-id="fa286-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa286-117">-DefaultProfile</span></span>
<span data-ttu-id="fa286-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa286-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa286-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fa286-119">-Name</span></span>
<span data-ttu-id="fa286-120">Имя правила</span><span class="sxs-lookup"><span data-stu-id="fa286-120">Rule Name</span></span>

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

### <span data-ttu-id="fa286-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fa286-121">-Namespace</span></span>
<span data-ttu-id="fa286-122">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="fa286-122">Namespace Name</span></span>

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

### <span data-ttu-id="fa286-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="fa286-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="fa286-124">Для действия требуется предварительное процессыро</span><span class="sxs-lookup"><span data-stu-id="fa286-124">Action Requires Preprocessing</span></span>

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

### <span data-ttu-id="fa286-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa286-125">-ResourceGroupName</span></span>
<span data-ttu-id="fa286-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fa286-126">The name of the resource group</span></span>

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

### <span data-ttu-id="fa286-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="fa286-127">-SqlExpression</span></span>
<span data-ttu-id="fa286-128">Выражение фильтра Sql</span><span class="sxs-lookup"><span data-stu-id="fa286-128">Sql Filter Expression</span></span>

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

### <span data-ttu-id="fa286-129">-Подписка</span><span class="sxs-lookup"><span data-stu-id="fa286-129">-Subscription</span></span>
<span data-ttu-id="fa286-130">Имя подписки</span><span class="sxs-lookup"><span data-stu-id="fa286-130">Subscription Name</span></span>

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

### <span data-ttu-id="fa286-131">-Topic</span><span class="sxs-lookup"><span data-stu-id="fa286-131">-Topic</span></span>
<span data-ttu-id="fa286-132">Название темы</span><span class="sxs-lookup"><span data-stu-id="fa286-132">Topic Name</span></span>

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

### <span data-ttu-id="fa286-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa286-133">-Confirm</span></span>
<span data-ttu-id="fa286-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa286-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa286-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa286-135">-WhatIf</span></span>
<span data-ttu-id="fa286-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa286-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa286-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fa286-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa286-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa286-138">CommonParameters</span></span>
<span data-ttu-id="fa286-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa286-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa286-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa286-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa286-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa286-141">INPUTS</span></span>

### <span data-ttu-id="fa286-142">System.String</span><span class="sxs-lookup"><span data-stu-id="fa286-142">System.String</span></span>

## <span data-ttu-id="fa286-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fa286-143">OUTPUTS</span></span>

### <span data-ttu-id="fa286-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="fa286-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="fa286-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fa286-145">NOTES</span></span>

## <span data-ttu-id="fa286-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa286-146">RELATED LINKS</span></span>
