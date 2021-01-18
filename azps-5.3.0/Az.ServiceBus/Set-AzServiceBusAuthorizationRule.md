---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: da981d38f0833adc276a114c42def5d19322e0d9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517369"
---
# <span data-ttu-id="feb36-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="feb36-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="feb36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feb36-102">SYNOPSIS</span></span>
<span data-ttu-id="feb36-103">Обновляет описание указанного правила авторизации для указанного пространства имен автобусов службы, очереди или раздела.</span><span class="sxs-lookup"><span data-stu-id="feb36-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="feb36-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="feb36-104">SYNTAX</span></span>

### <span data-ttu-id="feb36-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="feb36-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feb36-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="feb36-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feb36-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="feb36-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feb36-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="feb36-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="feb36-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="feb36-109">DESCRIPTION</span></span>
<span data-ttu-id="feb36-110">Cmdlet **Set-AzServiceBusAuthorizationRule** обновляет описание указанного правила авторизации в соответствующем пространстве имен автобусов обслуживания, очереди или разделе.</span><span class="sxs-lookup"><span data-stu-id="feb36-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="feb36-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="feb36-111">EXAMPLES</span></span>

### <span data-ttu-id="feb36-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="feb36-112">Example 1</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="feb36-113">Удаляет управление **из** прав доступа правила авторизации `AuthoRule1` в области `SB-Example1` имен.</span><span class="sxs-lookup"><span data-stu-id="feb36-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="feb36-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="feb36-114">Example 2</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="feb36-115">Удаляет управление **из** прав доступа правила авторизации в `AuthoRule1` `SBQueue` очереди.</span><span class="sxs-lookup"><span data-stu-id="feb36-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="feb36-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="feb36-116">Example 3</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="feb36-117">Удаляет **управление из** прав на доступ для правила авторизации в `AuthoRule1` соответствующей `SBTopic` теме.</span><span class="sxs-lookup"><span data-stu-id="feb36-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="feb36-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="feb36-118">PARAMETERS</span></span>

### <span data-ttu-id="feb36-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb36-119">-DefaultProfile</span></span>
<span data-ttu-id="feb36-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="feb36-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feb36-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="feb36-121">-InputObject</span></span>
<span data-ttu-id="feb36-122">Объект AuthorizationRule ServiceBus</span><span class="sxs-lookup"><span data-stu-id="feb36-122">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="feb36-123">-Name</span><span class="sxs-lookup"><span data-stu-id="feb36-123">-Name</span></span>
<span data-ttu-id="feb36-124">Имяrule authorizationRule</span><span class="sxs-lookup"><span data-stu-id="feb36-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="feb36-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="feb36-125">-Namespace</span></span>
<span data-ttu-id="feb36-126">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="feb36-126">Namespace Name</span></span>

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

### <span data-ttu-id="feb36-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="feb36-127">-Queue</span></span>
<span data-ttu-id="feb36-128">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="feb36-128">Queue Name</span></span>

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

### <span data-ttu-id="feb36-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feb36-129">-ResourceGroupName</span></span>
<span data-ttu-id="feb36-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="feb36-130">Resource Group Name</span></span>

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

### <span data-ttu-id="feb36-131">-Rights</span><span class="sxs-lookup"><span data-stu-id="feb36-131">-Rights</span></span>
<span data-ttu-id="feb36-132">Права, например @("Прослушивание";"Отправить";"Управление")</span><span class="sxs-lookup"><span data-stu-id="feb36-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="feb36-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="feb36-133">-Topic</span></span>
<span data-ttu-id="feb36-134">Название темы</span><span class="sxs-lookup"><span data-stu-id="feb36-134">Topic Name</span></span>

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

### <span data-ttu-id="feb36-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="feb36-135">-Confirm</span></span>
<span data-ttu-id="feb36-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="feb36-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feb36-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feb36-137">-WhatIf</span></span>
<span data-ttu-id="feb36-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="feb36-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="feb36-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="feb36-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feb36-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb36-140">CommonParameters</span></span>
<span data-ttu-id="feb36-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feb36-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb36-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feb36-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb36-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="feb36-143">INPUTS</span></span>

### <span data-ttu-id="feb36-144">System.String</span><span class="sxs-lookup"><span data-stu-id="feb36-144">System.String</span></span>

### <span data-ttu-id="feb36-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="feb36-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="feb36-146">System.String[]</span><span class="sxs-lookup"><span data-stu-id="feb36-146">System.String[]</span></span>

## <span data-ttu-id="feb36-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="feb36-147">OUTPUTS</span></span>

### <span data-ttu-id="feb36-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="feb36-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="feb36-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="feb36-149">NOTES</span></span>

## <span data-ttu-id="feb36-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="feb36-150">RELATED LINKS</span></span>
