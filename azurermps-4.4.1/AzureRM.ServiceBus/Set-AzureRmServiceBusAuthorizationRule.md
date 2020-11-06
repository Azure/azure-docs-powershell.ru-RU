---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 9e4612f8b688181ca54c7fa8414d28e3a444b446
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568680"
---
# <span data-ttu-id="5a426-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5a426-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="5a426-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a426-102">SYNOPSIS</span></span>
<span data-ttu-id="5a426-103">Обновляет указанное описание правила авторизации для заданного пространства имен служебной шины или очереди или темы.</span><span class="sxs-lookup"><span data-stu-id="5a426-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a426-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a426-104">SYNTAX</span></span>

### <span data-ttu-id="5a426-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5a426-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a426-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5a426-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a426-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5a426-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a426-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5a426-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a426-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="5a426-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a426-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a426-110">DESCRIPTION</span></span>
<span data-ttu-id="5a426-111">Командлет **Set-AzureRmServiceBusAuthorizationRule** обновляет описание указанного правила авторизации в заданном пространстве имен служебной шины или очереди или разделе.</span><span class="sxs-lookup"><span data-stu-id="5a426-111">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="5a426-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a426-112">EXAMPLES</span></span>

### <span data-ttu-id="5a426-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5a426-113">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="5a426-114">Удаляет **Управление** из прав доступа правила авторизации `AuthoRule1` в пространстве имен `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="5a426-114">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="5a426-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5a426-115">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="5a426-116">Удаление **управления** из прав доступа правила авторизации `AuthoRule1` в очереди `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="5a426-116">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="5a426-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5a426-117">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="5a426-118">Удаление **Manage** из прав доступа для правила авторизации `AuthoRule1` в разделе "Управление" `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="5a426-118">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="5a426-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a426-119">PARAMETERS</span></span>

### <span data-ttu-id="5a426-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a426-120">-Confirm</span></span>
<span data-ttu-id="5a426-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a426-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a426-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a426-122">-InputObject</span></span>
<span data-ttu-id="5a426-123">Объект ServiceBus AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="5a426-123">ServiceBus AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a426-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5a426-124">-Name</span></span>
<span data-ttu-id="5a426-125">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="5a426-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="5a426-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5a426-126">-Namespace</span></span>
<span data-ttu-id="5a426-127">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="5a426-127">Namespace Name.</span></span>

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

### <span data-ttu-id="5a426-128">-Очередь</span><span class="sxs-lookup"><span data-stu-id="5a426-128">-Queue</span></span>
<span data-ttu-id="5a426-129">Имя очереди.</span><span class="sxs-lookup"><span data-stu-id="5a426-129">Queue Name.</span></span>

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

### <span data-ttu-id="5a426-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a426-130">-ResourceGroupName</span></span>
<span data-ttu-id="5a426-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a426-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="5a426-132">-Права</span><span class="sxs-lookup"><span data-stu-id="5a426-132">-Rights</span></span>
<span data-ttu-id="5a426-133">Права, например @ ("прослушать", "Отправить", "Управление")</span><span class="sxs-lookup"><span data-stu-id="5a426-133">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a426-134">-Темы</span><span class="sxs-lookup"><span data-stu-id="5a426-134">-Topic</span></span>
<span data-ttu-id="5a426-135">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="5a426-135">Topic Name.</span></span>

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

### <span data-ttu-id="5a426-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a426-136">-WhatIf</span></span>
<span data-ttu-id="5a426-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a426-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a426-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a426-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a426-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a426-139">-DefaultProfile</span></span>
<span data-ttu-id="5a426-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a426-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a426-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a426-141">CommonParameters</span></span>
<span data-ttu-id="5a426-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a426-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a426-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a426-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a426-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a426-144">INPUTS</span></span>

### <span data-ttu-id="5a426-145">System. String</span><span class="sxs-lookup"><span data-stu-id="5a426-145">System.String</span></span>
<span data-ttu-id="5a426-146">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes System. String []</span><span class="sxs-lookup"><span data-stu-id="5a426-146">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes System.String[]</span></span>

## <span data-ttu-id="5a426-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a426-147">OUTPUTS</span></span>

### <span data-ttu-id="5a426-148">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="5a426-148">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="5a426-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a426-149">NOTES</span></span>

## <span data-ttu-id="5a426-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a426-150">RELATED LINKS</span></span>

