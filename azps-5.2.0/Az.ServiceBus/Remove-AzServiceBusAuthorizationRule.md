---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e6e3fb3c1998a009b10599c3ea059a147ab7f9ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411863"
---
# <span data-ttu-id="1f40e-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1f40e-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="1f40e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f40e-102">SYNOPSIS</span></span>
<span data-ttu-id="1f40e-103">Удаляет правило авторизации пространства имен или очереди или темы для группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f40e-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="1f40e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1f40e-104">SYNTAX</span></span>

### <span data-ttu-id="1f40e-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1f40e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f40e-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1f40e-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f40e-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1f40e-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f40e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f40e-108">DESCRIPTION</span></span>
<span data-ttu-id="1f40e-109">Для указанной группы ресурсов удаляется правило авторизации пространства имен или очереди или раздела группы ресурсов **Remove-AzServiceBusAuthorizationRule.**</span><span class="sxs-lookup"><span data-stu-id="1f40e-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="1f40e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1f40e-110">EXAMPLES</span></span>

### <span data-ttu-id="1f40e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1f40e-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="1f40e-112">Удаляет правило авторизации пространства имен из указанной группы `SBAuthoRule1` `SB-Example1` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f40e-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="1f40e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1f40e-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="1f40e-114">Удаляет правило авторизации для `SBAuthoRule1` очереди из указанной группы `SBQueue` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f40e-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="1f40e-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="1f40e-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="1f40e-116">Удаляет правило авторизации `SBAuthoRule1` для темы из указанной группы `SBTopic` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f40e-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="1f40e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f40e-117">PARAMETERS</span></span>

### <span data-ttu-id="1f40e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f40e-118">-DefaultProfile</span></span>
<span data-ttu-id="1f40e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f40e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f40e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="1f40e-120">-Force</span></span>
<span data-ttu-id="1f40e-121">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1f40e-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f40e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f40e-122">-InputObject</span></span>
<span data-ttu-id="1f40e-123">Объект AuthorizationRule ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1f40e-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f40e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1f40e-124">-Name</span></span>
<span data-ttu-id="1f40e-125">Имяrule authorizationRule</span><span class="sxs-lookup"><span data-stu-id="1f40e-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="1f40e-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1f40e-126">-Namespace</span></span>
<span data-ttu-id="1f40e-127">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="1f40e-127">Namespace Name</span></span>

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

### <span data-ttu-id="1f40e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f40e-128">-PassThru</span></span>
<span data-ttu-id="1f40e-129">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="1f40e-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1f40e-130">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1f40e-130">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f40e-131">-Queue</span><span class="sxs-lookup"><span data-stu-id="1f40e-131">-Queue</span></span>
<span data-ttu-id="1f40e-132">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="1f40e-132">Queue Name</span></span>

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

### <span data-ttu-id="1f40e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f40e-133">-ResourceGroupName</span></span>
<span data-ttu-id="1f40e-134">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1f40e-134">Resource Group Name</span></span>

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

### <span data-ttu-id="1f40e-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="1f40e-135">-Topic</span></span>
<span data-ttu-id="1f40e-136">Название темы</span><span class="sxs-lookup"><span data-stu-id="1f40e-136">Topic Name</span></span>

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

### <span data-ttu-id="1f40e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f40e-137">-Confirm</span></span>
<span data-ttu-id="1f40e-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f40e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f40e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f40e-139">-WhatIf</span></span>
<span data-ttu-id="1f40e-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f40e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f40e-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1f40e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f40e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f40e-142">CommonParameters</span></span>
<span data-ttu-id="1f40e-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f40e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f40e-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f40e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f40e-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f40e-145">INPUTS</span></span>

### <span data-ttu-id="1f40e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="1f40e-146">System.String</span></span>

### <span data-ttu-id="1f40e-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="1f40e-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="1f40e-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1f40e-148">OUTPUTS</span></span>

### <span data-ttu-id="1f40e-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1f40e-149">System.Boolean</span></span>

## <span data-ttu-id="1f40e-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1f40e-150">NOTES</span></span>

## <span data-ttu-id="1f40e-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f40e-151">RELATED LINKS</span></span>
