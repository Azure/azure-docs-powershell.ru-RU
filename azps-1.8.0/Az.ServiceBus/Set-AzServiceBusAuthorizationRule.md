---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e9ab4d4d2fb2c60561d85582f2dda922ba9eaae1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729153"
---
# <span data-ttu-id="840d0-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="840d0-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="840d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="840d0-102">SYNOPSIS</span></span>
<span data-ttu-id="840d0-103">Обновляет указанное описание правила авторизации для заданного пространства имен служебной шины или очереди или темы.</span><span class="sxs-lookup"><span data-stu-id="840d0-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="840d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="840d0-104">SYNTAX</span></span>

### <span data-ttu-id="840d0-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="840d0-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="840d0-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="840d0-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="840d0-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="840d0-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="840d0-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="840d0-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="840d0-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="840d0-109">DESCRIPTION</span></span>
<span data-ttu-id="840d0-110">Командлет **Set-AzServiceBusAuthorizationRule** обновляет описание указанного правила авторизации в заданном пространстве имен служебной шины или очереди или разделе.</span><span class="sxs-lookup"><span data-stu-id="840d0-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="840d0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="840d0-111">EXAMPLES</span></span>

### <span data-ttu-id="840d0-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="840d0-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="840d0-113">Удаляет **Управление** из прав доступа правила авторизации `AuthoRule1` в пространстве имен `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="840d0-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="840d0-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="840d0-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="840d0-115">Удаление **управления** из прав доступа правила авторизации `AuthoRule1` в очереди `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="840d0-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="840d0-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="840d0-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="840d0-117">Удаление **Manage** из прав доступа для правила авторизации `AuthoRule1` в разделе "Управление" `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="840d0-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="840d0-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="840d0-118">PARAMETERS</span></span>

### <span data-ttu-id="840d0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="840d0-119">-DefaultProfile</span></span>
<span data-ttu-id="840d0-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="840d0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="840d0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="840d0-121">-InputObject</span></span>
<span data-ttu-id="840d0-122">Объект ServiceBus AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="840d0-122">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="840d0-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="840d0-123">-Name</span></span>
<span data-ttu-id="840d0-124">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="840d0-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="840d0-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="840d0-125">-Namespace</span></span>
<span data-ttu-id="840d0-126">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="840d0-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="840d0-127">-Очередь</span><span class="sxs-lookup"><span data-stu-id="840d0-127">-Queue</span></span>
<span data-ttu-id="840d0-128">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="840d0-128">Queue Name</span></span>

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

### <span data-ttu-id="840d0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="840d0-129">-ResourceGroupName</span></span>
<span data-ttu-id="840d0-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="840d0-130">Resource Group Name</span></span>

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

### <span data-ttu-id="840d0-131">-Права</span><span class="sxs-lookup"><span data-stu-id="840d0-131">-Rights</span></span>
<span data-ttu-id="840d0-132">Права, например @ ("прослушать", "Отправить", "Управление")</span><span class="sxs-lookup"><span data-stu-id="840d0-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="840d0-133">-Темы</span><span class="sxs-lookup"><span data-stu-id="840d0-133">-Topic</span></span>
<span data-ttu-id="840d0-134">Название раздела</span><span class="sxs-lookup"><span data-stu-id="840d0-134">Topic Name</span></span>

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

### <span data-ttu-id="840d0-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="840d0-135">-Confirm</span></span>
<span data-ttu-id="840d0-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="840d0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="840d0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="840d0-137">-WhatIf</span></span>
<span data-ttu-id="840d0-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="840d0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="840d0-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="840d0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="840d0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="840d0-140">CommonParameters</span></span>
<span data-ttu-id="840d0-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="840d0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="840d0-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="840d0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="840d0-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="840d0-143">INPUTS</span></span>

### <span data-ttu-id="840d0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="840d0-144">System.String</span></span>

### <span data-ttu-id="840d0-145">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="840d0-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="840d0-146">System. String []</span><span class="sxs-lookup"><span data-stu-id="840d0-146">System.String[]</span></span>

## <span data-ttu-id="840d0-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="840d0-147">OUTPUTS</span></span>

### <span data-ttu-id="840d0-148">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="840d0-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="840d0-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="840d0-149">NOTES</span></span>

## <span data-ttu-id="840d0-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="840d0-150">RELATED LINKS</span></span>
