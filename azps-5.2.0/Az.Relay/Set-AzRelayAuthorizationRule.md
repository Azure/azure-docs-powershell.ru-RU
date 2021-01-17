---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
ms.openlocfilehash: 4ca8156e80a827c9916def7ef749cfa9abb9389a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416604"
---
# <span data-ttu-id="1a9ff-101">Set-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1a9ff-101">Set-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="1a9ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a9ff-102">SYNOPSIS</span></span>
<span data-ttu-id="1a9ff-103">Обновляет описание указанного правила авторизации для указанных сущностями Relay (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="1a9ff-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1a9ff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1a9ff-104">SYNTAX</span></span>

### <span data-ttu-id="1a9ff-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1a9ff-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a9ff-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1a9ff-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a9ff-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1a9ff-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a9ff-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1a9ff-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a9ff-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="1a9ff-109">AuthoRulePropertiesSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a9ff-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a9ff-110">DESCRIPTION</span></span>
<span data-ttu-id="1a9ff-111">Командлет **Set-AzRelayAuthorizationRule** обновляет описание указанного правила авторизации для указанных сущностями relay (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="1a9ff-111">The **Set-AzRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1a9ff-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1a9ff-112">EXAMPLES</span></span>

### <span data-ttu-id="1a9ff-113">Пример 1.1. Пространство имен с inputObject</span><span class="sxs-lookup"><span data-stu-id="1a9ff-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="1a9ff-114">Добавляет **"Отправить"** из прав на доступ правила авторизации `AuthoRule1` в области `TestNameSpace-Relay1` имен.</span><span class="sxs-lookup"><span data-stu-id="1a9ff-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="1a9ff-115">Пример 1.2. Пространство имен с параметром Rights</span><span class="sxs-lookup"><span data-stu-id="1a9ff-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="1a9ff-116">Добавляет **"Отправить"** из прав на доступ правила авторизации `AuthoRule1` в области `TestNameSpace-Relay1` имен.</span><span class="sxs-lookup"><span data-stu-id="1a9ff-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="1a9ff-117">Пример 2.1. WcfRelay с InputObject</span><span class="sxs-lookup"><span data-stu-id="1a9ff-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="1a9ff-118">Добавляет **"Отправить"** в права на доступ правила авторизации `AuthoRule1` для WcfRelay. `TestWCFRelay1`</span><span class="sxs-lookup"><span data-stu-id="1a9ff-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="1a9ff-119">Пример 2.2. WcfRelay с параметром Rights</span><span class="sxs-lookup"><span data-stu-id="1a9ff-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="1a9ff-120">Добавляет **"Отправить"** в права на доступ правила авторизации `AuthoRule1` для WcfRelay. `TestWCFRelay1`</span><span class="sxs-lookup"><span data-stu-id="1a9ff-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="1a9ff-121">Пример 3.1. Гибридное подключение с inputObject</span><span class="sxs-lookup"><span data-stu-id="1a9ff-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="1a9ff-122">Добавляет **"Отправить"** в права доступа правила авторизации `AuthoRule1` гибридной `TestHybridConnection` сети.</span><span class="sxs-lookup"><span data-stu-id="1a9ff-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="1a9ff-123">Пример 3.2. Гибридное подключение с параметром Rights</span><span class="sxs-lookup"><span data-stu-id="1a9ff-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="1a9ff-124">Добавляет **"Отправить"** в права доступа к правилу авторизации `AuthoRule1` гибридной `TestHybridConnection` сети.</span><span class="sxs-lookup"><span data-stu-id="1a9ff-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="1a9ff-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a9ff-125">PARAMETERS</span></span>

### <span data-ttu-id="1a9ff-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a9ff-126">-DefaultProfile</span></span>
<span data-ttu-id="1a9ff-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a9ff-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a9ff-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1a9ff-128">-HybridConnection</span></span>
<span data-ttu-id="1a9ff-129">Имя HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="1a9ff-129">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a9ff-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a9ff-130">-InputObject</span></span>
<span data-ttu-id="1a9ff-131">Объект Relay AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="1a9ff-131">Relay AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9ff-132">-Name</span><span class="sxs-lookup"><span data-stu-id="1a9ff-132">-Name</span></span>
<span data-ttu-id="1a9ff-133">Имяrule authorizationRule.</span><span class="sxs-lookup"><span data-stu-id="1a9ff-133">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a9ff-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1a9ff-134">-Namespace</span></span>
<span data-ttu-id="1a9ff-135">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1a9ff-135">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a9ff-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a9ff-136">-ResourceGroupName</span></span>
<span data-ttu-id="1a9ff-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a9ff-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="1a9ff-138">-Rights</span><span class="sxs-lookup"><span data-stu-id="1a9ff-138">-Rights</span></span>
<span data-ttu-id="1a9ff-139">Права, например @("Прослушивание";"Отправить";"Управление")</span><span class="sxs-lookup"><span data-stu-id="1a9ff-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9ff-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1a9ff-140">-WcfRelay</span></span>
<span data-ttu-id="1a9ff-141">Имя WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="1a9ff-141">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a9ff-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a9ff-142">-Confirm</span></span>
<span data-ttu-id="1a9ff-143">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1a9ff-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a9ff-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a9ff-144">-WhatIf</span></span>
<span data-ttu-id="1a9ff-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a9ff-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a9ff-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1a9ff-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a9ff-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a9ff-147">CommonParameters</span></span>
<span data-ttu-id="1a9ff-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a9ff-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a9ff-149">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a9ff-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a9ff-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a9ff-150">INPUTS</span></span>

### <span data-ttu-id="1a9ff-151">System.String</span><span class="sxs-lookup"><span data-stu-id="1a9ff-151">System.String</span></span>

### <span data-ttu-id="1a9ff-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="1a9ff-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="1a9ff-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="1a9ff-153">System.String[]</span></span>

## <span data-ttu-id="1a9ff-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1a9ff-154">OUTPUTS</span></span>

### <span data-ttu-id="1a9ff-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="1a9ff-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="1a9ff-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1a9ff-156">NOTES</span></span>

## <span data-ttu-id="1a9ff-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a9ff-157">RELATED LINKS</span></span>
