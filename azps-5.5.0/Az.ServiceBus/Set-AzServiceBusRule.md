---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: b86b9629062515afb1ee70e7c7372cbc7687bfa5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217564"
---
# <span data-ttu-id="197c1-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="197c1-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="197c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="197c1-102">SYNOPSIS</span></span>
<span data-ttu-id="197c1-103">Обновляет описание указанного правила для данной подписки.</span><span class="sxs-lookup"><span data-stu-id="197c1-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="197c1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="197c1-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="197c1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="197c1-105">DESCRIPTION</span></span>
<span data-ttu-id="197c1-106">С **его учетом** можно обновить описание указанного правила данной подписки.</span><span class="sxs-lookup"><span data-stu-id="197c1-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="197c1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="197c1-107">EXAMPLES</span></span>

### <span data-ttu-id="197c1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="197c1-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="197c1-109">Обновляет условие sql expression **mysqlexpression='condition'** для правила `SBRule` подписки `SBSubscription` в разделе "Тема". `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="197c1-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="197c1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="197c1-110">PARAMETERS</span></span>

### <span data-ttu-id="197c1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="197c1-111">-DefaultProfile</span></span>
<span data-ttu-id="197c1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="197c1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="197c1-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="197c1-113">-InputObject</span></span>
<span data-ttu-id="197c1-114">Определение правил ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="197c1-114">ServiceBus Rules definition.</span></span>

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

### <span data-ttu-id="197c1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="197c1-115">-Name</span></span>
<span data-ttu-id="197c1-116">Имя правила.</span><span class="sxs-lookup"><span data-stu-id="197c1-116">Rule Name.</span></span>

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

### <span data-ttu-id="197c1-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="197c1-117">-Namespace</span></span>
<span data-ttu-id="197c1-118">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="197c1-118">Namespace Name.</span></span>

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

### <span data-ttu-id="197c1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="197c1-119">-ResourceGroupName</span></span>
<span data-ttu-id="197c1-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="197c1-120">The name of the resource group</span></span>

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

### <span data-ttu-id="197c1-121">-Подписка</span><span class="sxs-lookup"><span data-stu-id="197c1-121">-Subscription</span></span>
<span data-ttu-id="197c1-122">Имя подписки.</span><span class="sxs-lookup"><span data-stu-id="197c1-122">Subscription Name.</span></span>

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

### <span data-ttu-id="197c1-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="197c1-123">-Topic</span></span>
<span data-ttu-id="197c1-124">Имя темы.</span><span class="sxs-lookup"><span data-stu-id="197c1-124">Topic Name.</span></span>

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

### <span data-ttu-id="197c1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="197c1-125">-Confirm</span></span>
<span data-ttu-id="197c1-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="197c1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="197c1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="197c1-127">-WhatIf</span></span>
<span data-ttu-id="197c1-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="197c1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="197c1-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="197c1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="197c1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="197c1-130">CommonParameters</span></span>
<span data-ttu-id="197c1-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="197c1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="197c1-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="197c1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="197c1-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="197c1-133">INPUTS</span></span>

### <span data-ttu-id="197c1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="197c1-134">System.String</span></span>

### <span data-ttu-id="197c1-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="197c1-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="197c1-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="197c1-136">OUTPUTS</span></span>

### <span data-ttu-id="197c1-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="197c1-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="197c1-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="197c1-138">NOTES</span></span>

## <span data-ttu-id="197c1-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="197c1-139">RELATED LINKS</span></span>
