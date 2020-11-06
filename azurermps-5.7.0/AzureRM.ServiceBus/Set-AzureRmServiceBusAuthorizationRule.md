---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 3d5c1b6b80ff4d2b046b8a4b23adf7407f680e6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566903"
---
# <span data-ttu-id="53bb3-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="53bb3-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="53bb3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="53bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="53bb3-103">Обновляет указанное описание правила авторизации для заданного пространства имен служебной шины или очереди или темы.</span><span class="sxs-lookup"><span data-stu-id="53bb3-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53bb3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="53bb3-104">SYNTAX</span></span>

### <span data-ttu-id="53bb3-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="53bb3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53bb3-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="53bb3-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53bb3-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="53bb3-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53bb3-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="53bb3-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53bb3-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53bb3-109">DESCRIPTION</span></span>
<span data-ttu-id="53bb3-110">Командлет **Set-AzureRmServiceBusAuthorizationRule** обновляет описание указанного правила авторизации в заданном пространстве имен служебной шины или очереди или разделе.</span><span class="sxs-lookup"><span data-stu-id="53bb3-110">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="53bb3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="53bb3-111">EXAMPLES</span></span>

### <span data-ttu-id="53bb3-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="53bb3-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="53bb3-113">Удаляет **Управление** из прав доступа правила авторизации `AuthoRule1` в пространстве имен `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="53bb3-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="53bb3-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="53bb3-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="53bb3-115">Удаление **управления** из прав доступа правила авторизации `AuthoRule1` в очереди `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="53bb3-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="53bb3-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="53bb3-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="53bb3-117">Удаление **Manage** из прав доступа для правила авторизации `AuthoRule1` в разделе "Управление" `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="53bb3-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="53bb3-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="53bb3-118">PARAMETERS</span></span>

### <span data-ttu-id="53bb3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53bb3-119">-DefaultProfile</span></span>
<span data-ttu-id="53bb3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53bb3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bb3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53bb3-121">-InputObject</span></span>
<span data-ttu-id="53bb3-122">Объект ServiceBus AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="53bb3-122">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53bb3-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="53bb3-123">-Name</span></span>
<span data-ttu-id="53bb3-124">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="53bb3-124">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bb3-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="53bb3-125">-Namespace</span></span>
<span data-ttu-id="53bb3-126">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="53bb3-126">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bb3-127">-Очередь</span><span class="sxs-lookup"><span data-stu-id="53bb3-127">-Queue</span></span>
<span data-ttu-id="53bb3-128">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="53bb3-128">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bb3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53bb3-129">-ResourceGroupName</span></span>
<span data-ttu-id="53bb3-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="53bb3-130">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bb3-131">-Права</span><span class="sxs-lookup"><span data-stu-id="53bb3-131">-Rights</span></span>
<span data-ttu-id="53bb3-132">Права, например @ ("прослушать", "Отправить", "Управление")</span><span class="sxs-lookup"><span data-stu-id="53bb3-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bb3-133">-Темы</span><span class="sxs-lookup"><span data-stu-id="53bb3-133">-Topic</span></span>
<span data-ttu-id="53bb3-134">Название раздела</span><span class="sxs-lookup"><span data-stu-id="53bb3-134">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bb3-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53bb3-135">-Confirm</span></span>
<span data-ttu-id="53bb3-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="53bb3-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bb3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53bb3-137">-WhatIf</span></span>
<span data-ttu-id="53bb3-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="53bb3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53bb3-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="53bb3-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bb3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53bb3-140">CommonParameters</span></span>
<span data-ttu-id="53bb3-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="53bb3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="53bb3-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53bb3-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53bb3-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="53bb3-143">INPUTS</span></span>

### <span data-ttu-id="53bb3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="53bb3-144">System.String</span></span>
<span data-ttu-id="53bb3-145">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes System. String []</span><span class="sxs-lookup"><span data-stu-id="53bb3-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes System.String[]</span></span>


## <span data-ttu-id="53bb3-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="53bb3-146">OUTPUTS</span></span>

### <span data-ttu-id="53bb3-147">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="53bb3-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="53bb3-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="53bb3-148">NOTES</span></span>

## <span data-ttu-id="53bb3-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53bb3-149">RELATED LINKS</span></span>
