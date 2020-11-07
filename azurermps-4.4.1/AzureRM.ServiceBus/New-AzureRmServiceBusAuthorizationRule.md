---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: be2b841511669ffa2ac3ffd416fd86072edcfb52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734229"
---
# <span data-ttu-id="84dd2-101">New-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="84dd2-101">New-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="84dd2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="84dd2-103">Создает новое правило авторизации для указанной шины обслуживания, которое заданное пространство имен или очередь или тема.</span><span class="sxs-lookup"><span data-stu-id="84dd2-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84dd2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84dd2-104">SYNTAX</span></span>

### <span data-ttu-id="84dd2-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="84dd2-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84dd2-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="84dd2-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84dd2-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="84dd2-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84dd2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84dd2-108">DESCRIPTION</span></span>
<span data-ttu-id="84dd2-109">Командлет **New-AzureRmServiceBusAuthorizationRule** создает новое правило авторизации для указанного пространства имен служебной шины или очереди или темы.</span><span class="sxs-lookup"><span data-stu-id="84dd2-109">The **New-AzureRmServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="84dd2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84dd2-110">EXAMPLES</span></span>

### <span data-ttu-id="84dd2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="84dd2-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="84dd2-112">Создание `AuthoRule1` с правами на **прослушивание** и **отправку** для пространства имен `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="84dd2-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="84dd2-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="84dd2-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="84dd2-114">Создание `AuthoRule1` с правами **прослушивания** и **отправки** для очереди `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="84dd2-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="84dd2-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="84dd2-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="84dd2-116">Создание `AuthoRule1` с помощью прав на **прослушивание** и **отправку** для темы `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="84dd2-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="84dd2-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84dd2-117">PARAMETERS</span></span>

### <span data-ttu-id="84dd2-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84dd2-118">-Confirm</span></span>
<span data-ttu-id="84dd2-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="84dd2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84dd2-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="84dd2-120">-Name</span></span>
<span data-ttu-id="84dd2-121">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="84dd2-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="84dd2-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="84dd2-122">-Namespace</span></span>
<span data-ttu-id="84dd2-123">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="84dd2-123">Namespace Name.</span></span>

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

### <span data-ttu-id="84dd2-124">-Очередь</span><span class="sxs-lookup"><span data-stu-id="84dd2-124">-Queue</span></span>
<span data-ttu-id="84dd2-125">Имя очереди.</span><span class="sxs-lookup"><span data-stu-id="84dd2-125">Queue Name.</span></span>

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

### <span data-ttu-id="84dd2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84dd2-126">-ResourceGroupName</span></span>
<span data-ttu-id="84dd2-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84dd2-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="84dd2-128">-Права</span><span class="sxs-lookup"><span data-stu-id="84dd2-128">-Rights</span></span>
<span data-ttu-id="84dd2-129">Права, например "прослушать", "Отправить", "Управление"</span><span class="sxs-lookup"><span data-stu-id="84dd2-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="84dd2-130">-Темы</span><span class="sxs-lookup"><span data-stu-id="84dd2-130">-Topic</span></span>
<span data-ttu-id="84dd2-131">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="84dd2-131">Topic Name.</span></span>

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

### <span data-ttu-id="84dd2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84dd2-132">-WhatIf</span></span>
<span data-ttu-id="84dd2-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="84dd2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84dd2-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="84dd2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84dd2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84dd2-135">-DefaultProfile</span></span>
<span data-ttu-id="84dd2-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84dd2-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84dd2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84dd2-137">CommonParameters</span></span>
<span data-ttu-id="84dd2-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84dd2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84dd2-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84dd2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84dd2-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84dd2-140">INPUTS</span></span>

### <span data-ttu-id="84dd2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="84dd2-141">System.String</span></span>
<span data-ttu-id="84dd2-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="84dd2-142">System.String[]</span></span>

## <span data-ttu-id="84dd2-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84dd2-143">OUTPUTS</span></span>

### <span data-ttu-id="84dd2-144">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="84dd2-144">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="84dd2-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="84dd2-145">NOTES</span></span>

## <span data-ttu-id="84dd2-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84dd2-146">RELATED LINKS</span></span>

