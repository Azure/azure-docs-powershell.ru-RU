---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: a41ddb9ee845bce0687448d0745904b9cec9ba05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566113"
---
# <span data-ttu-id="f9984-101">Remove-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f9984-101">Remove-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="f9984-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f9984-102">SYNOPSIS</span></span>
<span data-ttu-id="f9984-103">Удаление правила авторизации пространства имен или очереди или темы из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f9984-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9984-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f9984-104">SYNTAX</span></span>

### <span data-ttu-id="f9984-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f9984-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9984-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9984-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9984-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9984-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9984-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9984-108">DESCRIPTION</span></span>
<span data-ttu-id="f9984-109">Командлет **Remove-AzureRmServiceBusAuthorizationRule** удаляет правило авторизации пространства имен или очереди или темы для указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f9984-109">The **Remove-AzureRmServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="f9984-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f9984-110">EXAMPLES</span></span>

### <span data-ttu-id="f9984-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f9984-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="f9984-112">Удаление правила авторизации `SBAuthoRule1` пространства имен `SB-Example1` из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f9984-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="f9984-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f9984-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="f9984-114">Удаление правила авторизации `SBAuthoRule1` очереди `SBQueue` из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f9984-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="f9984-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f9984-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="f9984-116">Удаление правила авторизации `SBAuthoRule1` темы `SBTopic` из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f9984-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="f9984-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f9984-117">PARAMETERS</span></span>

### <span data-ttu-id="f9984-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9984-118">-DefaultProfile</span></span>
<span data-ttu-id="f9984-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f9984-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9984-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f9984-120">-Force</span></span>
<span data-ttu-id="f9984-121">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f9984-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f9984-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9984-122">-InputObject</span></span>
<span data-ttu-id="f9984-123">Объект ServiceBus AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f9984-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9984-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f9984-124">-Name</span></span>
<span data-ttu-id="f9984-125">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f9984-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="f9984-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f9984-126">-Namespace</span></span>
<span data-ttu-id="f9984-127">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="f9984-127">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9984-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9984-128">-PassThru</span></span>
<span data-ttu-id="f9984-129">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f9984-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f9984-130">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f9984-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f9984-131">-Очередь</span><span class="sxs-lookup"><span data-stu-id="f9984-131">-Queue</span></span>
<span data-ttu-id="f9984-132">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="f9984-132">Queue Name</span></span>

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

### <span data-ttu-id="f9984-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9984-133">-ResourceGroupName</span></span>
<span data-ttu-id="f9984-134">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f9984-134">Resource Group Name</span></span>

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

### <span data-ttu-id="f9984-135">-Темы</span><span class="sxs-lookup"><span data-stu-id="f9984-135">-Topic</span></span>
<span data-ttu-id="f9984-136">Название раздела</span><span class="sxs-lookup"><span data-stu-id="f9984-136">Topic Name</span></span>

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

### <span data-ttu-id="f9984-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9984-137">-Confirm</span></span>
<span data-ttu-id="f9984-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f9984-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9984-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9984-139">-WhatIf</span></span>
<span data-ttu-id="f9984-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f9984-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9984-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f9984-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9984-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9984-142">CommonParameters</span></span>
<span data-ttu-id="f9984-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f9984-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f9984-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9984-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9984-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f9984-145">INPUTS</span></span>

### <span data-ttu-id="f9984-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f9984-146">System.String</span></span>
<span data-ttu-id="f9984-147">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f9984-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="f9984-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9984-148">OUTPUTS</span></span>

### <span data-ttu-id="f9984-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f9984-149">System.Boolean</span></span>


## <span data-ttu-id="f9984-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="f9984-150">NOTES</span></span>

## <span data-ttu-id="f9984-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9984-151">RELATED LINKS</span></span>
