---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 7722ee1a84aee6ef16642a84ac9f72f259d9772f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732408"
---
# <span data-ttu-id="48419-101">Remove-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="48419-101">Remove-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="48419-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48419-102">SYNOPSIS</span></span>
<span data-ttu-id="48419-103">Удаление правила авторизации пространства имен или очереди или темы из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48419-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48419-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48419-104">SYNTAX</span></span>

### <span data-ttu-id="48419-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48419-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="48419-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="48419-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Queue] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="48419-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="48419-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Topic] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="48419-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48419-108">DESCRIPTION</span></span>
<span data-ttu-id="48419-109">Командлет **Remove-AzureRmServiceBusAuthorizationRule** удаляет правило авторизации пространства имен или очереди или темы для указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48419-109">The **Remove-AzureRmServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="48419-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48419-110">EXAMPLES</span></span>

### <span data-ttu-id="48419-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="48419-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```
<span data-ttu-id="48419-112">Удаление правила авторизации `SBAuthoRule1` пространства имен `SB-Example1` из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48419-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="48419-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="48419-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```
<span data-ttu-id="48419-114">Удаление правила авторизации `SBAuthoRule1` очереди `SBQueue` из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48419-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="48419-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="48419-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```
<span data-ttu-id="48419-116">Удаление правила авторизации `SBAuthoRule1` темы `SBTopic` из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48419-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="48419-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48419-117">PARAMETERS</span></span>

### <span data-ttu-id="48419-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48419-118">-Confirm</span></span>
<span data-ttu-id="48419-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="48419-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48419-120">-Force</span><span class="sxs-lookup"><span data-stu-id="48419-120">-Force</span></span>
<span data-ttu-id="48419-121">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="48419-121">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48419-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="48419-122">-Name</span></span>
<span data-ttu-id="48419-123">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="48419-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="48419-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="48419-124">-Namespace</span></span>
<span data-ttu-id="48419-125">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="48419-125">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48419-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48419-126">-PassThru</span></span>
<span data-ttu-id="48419-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="48419-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48419-128">-Очередь</span><span class="sxs-lookup"><span data-stu-id="48419-128">-Queue</span></span>
<span data-ttu-id="48419-129">Имя очереди.</span><span class="sxs-lookup"><span data-stu-id="48419-129">Queue Name.</span></span>

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

### <span data-ttu-id="48419-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48419-130">-ResourceGroupName</span></span>
<span data-ttu-id="48419-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48419-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="48419-132">-Темы</span><span class="sxs-lookup"><span data-stu-id="48419-132">-Topic</span></span>
<span data-ttu-id="48419-133">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="48419-133">Topic Name.</span></span>

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

### <span data-ttu-id="48419-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48419-134">-WhatIf</span></span>
<span data-ttu-id="48419-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48419-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48419-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="48419-136">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="48419-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48419-137">INPUTS</span></span>

### <span data-ttu-id="48419-138">System. String</span><span class="sxs-lookup"><span data-stu-id="48419-138">System.String</span></span>


## <span data-ttu-id="48419-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48419-139">OUTPUTS</span></span>

### <span data-ttu-id="48419-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48419-140">System.Boolean</span></span>


## <span data-ttu-id="48419-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="48419-141">NOTES</span></span>

## <span data-ttu-id="48419-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48419-142">RELATED LINKS</span></span>

