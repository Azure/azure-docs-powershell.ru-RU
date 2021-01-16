---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: b86b9629062515afb1ee70e7c7372cbc7687bfa5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397335"
---
# <span data-ttu-id="8b5c4-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="8b5c4-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="8b5c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b5c4-102">SYNOPSIS</span></span>
<span data-ttu-id="8b5c4-103">Обновляет описание указанного правила для данной подписки.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="8b5c4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8b5c4-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b5c4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b5c4-105">DESCRIPTION</span></span>
<span data-ttu-id="8b5c4-106">С **его учетом** можно обновить описание указанного правила данной подписки.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="8b5c4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8b5c4-107">EXAMPLES</span></span>

### <span data-ttu-id="8b5c4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b5c4-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="8b5c4-109">Обновляет условие sql expression **mysqlexpression='condition'** для правила `SBRule` подписки `SBSubscription` в разделе "Тема" `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="8b5c4-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="8b5c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b5c4-110">PARAMETERS</span></span>

### <span data-ttu-id="8b5c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b5c4-111">-DefaultProfile</span></span>
<span data-ttu-id="8b5c4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b5c4-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b5c4-113">-InputObject</span></span>
<span data-ttu-id="8b5c4-114">Определение правил ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-114">ServiceBus Rules definition.</span></span>

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

### <span data-ttu-id="8b5c4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8b5c4-115">-Name</span></span>
<span data-ttu-id="8b5c4-116">Имя правила.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-116">Rule Name.</span></span>

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

### <span data-ttu-id="8b5c4-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8b5c4-117">-Namespace</span></span>
<span data-ttu-id="8b5c4-118">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-118">Namespace Name.</span></span>

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

### <span data-ttu-id="8b5c4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b5c4-119">-ResourceGroupName</span></span>
<span data-ttu-id="8b5c4-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8b5c4-120">The name of the resource group</span></span>

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

### <span data-ttu-id="8b5c4-121">-Подписка</span><span class="sxs-lookup"><span data-stu-id="8b5c4-121">-Subscription</span></span>
<span data-ttu-id="8b5c4-122">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-122">Subscription Name.</span></span>

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

### <span data-ttu-id="8b5c4-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="8b5c4-123">-Topic</span></span>
<span data-ttu-id="8b5c4-124">Название темы.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-124">Topic Name.</span></span>

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

### <span data-ttu-id="8b5c4-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b5c4-125">-Confirm</span></span>
<span data-ttu-id="8b5c4-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b5c4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b5c4-127">-WhatIf</span></span>
<span data-ttu-id="8b5c4-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b5c4-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b5c4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b5c4-130">CommonParameters</span></span>
<span data-ttu-id="8b5c4-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b5c4-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b5c4-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b5c4-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b5c4-133">INPUTS</span></span>

### <span data-ttu-id="8b5c4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8b5c4-134">System.String</span></span>

### <span data-ttu-id="8b5c4-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="8b5c4-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="8b5c4-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b5c4-136">OUTPUTS</span></span>

### <span data-ttu-id="8b5c4-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="8b5c4-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="8b5c4-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8b5c4-138">NOTES</span></span>

## <span data-ttu-id="8b5c4-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b5c4-139">RELATED LINKS</span></span>
