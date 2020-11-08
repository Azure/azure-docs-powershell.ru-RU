---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: beba9c457378949dfe82811186bde84522b46ae5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245683"
---
# <span data-ttu-id="66608-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="66608-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="66608-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="66608-102">SYNOPSIS</span></span>
<span data-ttu-id="66608-103">Создает новое правило авторизации для указанной шины обслуживания, которое заданное пространство имен или очередь или тема.</span><span class="sxs-lookup"><span data-stu-id="66608-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="66608-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="66608-104">SYNTAX</span></span>

### <span data-ttu-id="66608-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="66608-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66608-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="66608-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66608-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="66608-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66608-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66608-108">DESCRIPTION</span></span>
<span data-ttu-id="66608-109">Командлет **New-AzServiceBusAuthorizationRule** создает новое правило авторизации для указанного пространства имен служебной шины или очереди или темы.</span><span class="sxs-lookup"><span data-stu-id="66608-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="66608-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="66608-110">EXAMPLES</span></span>

### <span data-ttu-id="66608-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="66608-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="66608-112">Создание `AuthoRule1` с правами на **прослушивание** и **отправку** для пространства имен `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="66608-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="66608-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="66608-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="66608-114">Создание `AuthoRule1` с правами **прослушивания** и **отправки** для очереди `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="66608-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="66608-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="66608-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="66608-116">Создание `AuthoRule1` с помощью прав на **прослушивание** и **отправку** для темы `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="66608-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="66608-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="66608-117">PARAMETERS</span></span>

### <span data-ttu-id="66608-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66608-118">-DefaultProfile</span></span>
<span data-ttu-id="66608-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66608-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66608-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="66608-120">-Name</span></span>
<span data-ttu-id="66608-121">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="66608-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="66608-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="66608-122">-Namespace</span></span>
<span data-ttu-id="66608-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="66608-123">Namespace Name</span></span>

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

### <span data-ttu-id="66608-124">-Очередь</span><span class="sxs-lookup"><span data-stu-id="66608-124">-Queue</span></span>
<span data-ttu-id="66608-125">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="66608-125">Queue Name</span></span>

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

### <span data-ttu-id="66608-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66608-126">-ResourceGroupName</span></span>
<span data-ttu-id="66608-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="66608-127">Resource Group Name</span></span>

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

### <span data-ttu-id="66608-128">-Права</span><span class="sxs-lookup"><span data-stu-id="66608-128">-Rights</span></span>
<span data-ttu-id="66608-129">Права, например "прослушать", "Отправить", "Управление"</span><span class="sxs-lookup"><span data-stu-id="66608-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="66608-130">-Темы</span><span class="sxs-lookup"><span data-stu-id="66608-130">-Topic</span></span>
<span data-ttu-id="66608-131">Название раздела</span><span class="sxs-lookup"><span data-stu-id="66608-131">Topic Name</span></span>

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

### <span data-ttu-id="66608-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66608-132">-Confirm</span></span>
<span data-ttu-id="66608-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="66608-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66608-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66608-134">-WhatIf</span></span>
<span data-ttu-id="66608-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="66608-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66608-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="66608-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66608-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66608-137">CommonParameters</span></span>
<span data-ttu-id="66608-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="66608-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66608-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66608-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66608-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="66608-140">INPUTS</span></span>

### <span data-ttu-id="66608-141">System. String</span><span class="sxs-lookup"><span data-stu-id="66608-141">System.String</span></span>

### <span data-ttu-id="66608-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="66608-142">System.String[]</span></span>

## <span data-ttu-id="66608-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="66608-143">OUTPUTS</span></span>

### <span data-ttu-id="66608-144">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="66608-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="66608-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="66608-145">NOTES</span></span>

## <span data-ttu-id="66608-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66608-146">RELATED LINKS</span></span>
