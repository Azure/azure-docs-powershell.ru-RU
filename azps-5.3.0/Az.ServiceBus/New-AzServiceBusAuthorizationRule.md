---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: beba9c457378949dfe82811186bde84522b46ae5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517446"
---
# <span data-ttu-id="81d45-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="81d45-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="81d45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81d45-102">SYNOPSIS</span></span>
<span data-ttu-id="81d45-103">Создает новое правило авторизации для указанного автобусы обслуживания, указанного в пространстве имен, очереди или теме.</span><span class="sxs-lookup"><span data-stu-id="81d45-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="81d45-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="81d45-104">SYNTAX</span></span>

### <span data-ttu-id="81d45-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="81d45-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81d45-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="81d45-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81d45-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="81d45-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81d45-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81d45-108">DESCRIPTION</span></span>
<span data-ttu-id="81d45-109">Для **указанного пространства имен автобусов** службы, очереди или раздела создается новое правило авторизации.</span><span class="sxs-lookup"><span data-stu-id="81d45-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="81d45-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="81d45-110">EXAMPLES</span></span>

### <span data-ttu-id="81d45-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="81d45-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="81d45-112">Создается `AuthoRule1` с **правами на** прослушивание и **отправку** для пространства `SB-Example1` имен.</span><span class="sxs-lookup"><span data-stu-id="81d45-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="81d45-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="81d45-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="81d45-114">Создается `AuthoRule1` с **правами на** прослушивание и **отправку** для очереди. `SBQueue`</span><span class="sxs-lookup"><span data-stu-id="81d45-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="81d45-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="81d45-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="81d45-116">Создается `AuthoRule1` с **правами** на прослушивание **и отправку** для данной темы. `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="81d45-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="81d45-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81d45-117">PARAMETERS</span></span>

### <span data-ttu-id="81d45-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d45-118">-DefaultProfile</span></span>
<span data-ttu-id="81d45-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81d45-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81d45-120">-Name</span><span class="sxs-lookup"><span data-stu-id="81d45-120">-Name</span></span>
<span data-ttu-id="81d45-121">Имяrule authorizationRule</span><span class="sxs-lookup"><span data-stu-id="81d45-121">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81d45-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="81d45-122">-Namespace</span></span>
<span data-ttu-id="81d45-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="81d45-123">Namespace Name</span></span>

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

### <span data-ttu-id="81d45-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="81d45-124">-Queue</span></span>
<span data-ttu-id="81d45-125">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="81d45-125">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81d45-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d45-126">-ResourceGroupName</span></span>
<span data-ttu-id="81d45-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="81d45-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81d45-128">-Rights</span><span class="sxs-lookup"><span data-stu-id="81d45-128">-Rights</span></span>
<span data-ttu-id="81d45-129">Права, например "Прослушивание", "Отправить", "Управление"</span><span class="sxs-lookup"><span data-stu-id="81d45-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81d45-130">-Topic</span><span class="sxs-lookup"><span data-stu-id="81d45-130">-Topic</span></span>
<span data-ttu-id="81d45-131">Название темы</span><span class="sxs-lookup"><span data-stu-id="81d45-131">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81d45-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81d45-132">-Confirm</span></span>
<span data-ttu-id="81d45-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="81d45-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81d45-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81d45-134">-WhatIf</span></span>
<span data-ttu-id="81d45-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81d45-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81d45-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="81d45-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81d45-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d45-137">CommonParameters</span></span>
<span data-ttu-id="81d45-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81d45-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d45-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81d45-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d45-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81d45-140">INPUTS</span></span>

### <span data-ttu-id="81d45-141">System.String</span><span class="sxs-lookup"><span data-stu-id="81d45-141">System.String</span></span>

### <span data-ttu-id="81d45-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="81d45-142">System.String[]</span></span>

## <span data-ttu-id="81d45-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="81d45-143">OUTPUTS</span></span>

### <span data-ttu-id="81d45-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="81d45-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="81d45-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="81d45-145">NOTES</span></span>

## <span data-ttu-id="81d45-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81d45-146">RELATED LINKS</span></span>
