---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: b86b9629062515afb1ee70e7c7372cbc7687bfa5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517342"
---
# <span data-ttu-id="3f523-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="3f523-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="3f523-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f523-102">SYNOPSIS</span></span>
<span data-ttu-id="3f523-103">Обновляет описание указанного правила для данной подписки.</span><span class="sxs-lookup"><span data-stu-id="3f523-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="3f523-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3f523-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f523-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f523-105">DESCRIPTION</span></span>
<span data-ttu-id="3f523-106">Для указанного правила данной подписки обновляется описание с его учетом на основе **cmdlet Set-AzServiceBusRule.**</span><span class="sxs-lookup"><span data-stu-id="3f523-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="3f523-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3f523-107">EXAMPLES</span></span>

### <span data-ttu-id="3f523-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3f523-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="3f523-109">Обновляет условие sql expression **mysqlexpression='condition'** для правила `SBRule` подписки `SBSubscription` в разделе "Тема". `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="3f523-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="3f523-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f523-110">PARAMETERS</span></span>

### <span data-ttu-id="3f523-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f523-111">-DefaultProfile</span></span>
<span data-ttu-id="3f523-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f523-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f523-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f523-113">-InputObject</span></span>
<span data-ttu-id="3f523-114">Определение правил ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="3f523-114">ServiceBus Rules definition.</span></span>

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

### <span data-ttu-id="3f523-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3f523-115">-Name</span></span>
<span data-ttu-id="3f523-116">Имя правила.</span><span class="sxs-lookup"><span data-stu-id="3f523-116">Rule Name.</span></span>

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

### <span data-ttu-id="3f523-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3f523-117">-Namespace</span></span>
<span data-ttu-id="3f523-118">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3f523-118">Namespace Name.</span></span>

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

### <span data-ttu-id="3f523-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f523-119">-ResourceGroupName</span></span>
<span data-ttu-id="3f523-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3f523-120">The name of the resource group</span></span>

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

### <span data-ttu-id="3f523-121">-Подписка</span><span class="sxs-lookup"><span data-stu-id="3f523-121">-Subscription</span></span>
<span data-ttu-id="3f523-122">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="3f523-122">Subscription Name.</span></span>

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

### <span data-ttu-id="3f523-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="3f523-123">-Topic</span></span>
<span data-ttu-id="3f523-124">Имя темы.</span><span class="sxs-lookup"><span data-stu-id="3f523-124">Topic Name.</span></span>

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

### <span data-ttu-id="3f523-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f523-125">-Confirm</span></span>
<span data-ttu-id="3f523-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3f523-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f523-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f523-127">-WhatIf</span></span>
<span data-ttu-id="3f523-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f523-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f523-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3f523-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f523-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f523-130">CommonParameters</span></span>
<span data-ttu-id="3f523-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f523-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f523-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f523-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f523-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f523-133">INPUTS</span></span>

### <span data-ttu-id="3f523-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3f523-134">System.String</span></span>

### <span data-ttu-id="3f523-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="3f523-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="3f523-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3f523-136">OUTPUTS</span></span>

### <span data-ttu-id="3f523-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="3f523-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="3f523-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3f523-138">NOTES</span></span>

## <span data-ttu-id="3f523-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f523-139">RELATED LINKS</span></span>
