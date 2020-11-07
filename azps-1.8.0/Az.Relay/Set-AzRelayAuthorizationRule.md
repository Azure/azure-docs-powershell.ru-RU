---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
ms.openlocfilehash: ed95b9aa2e914d8f7c37132c372c4c1acaeafca1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729488"
---
# <span data-ttu-id="f53fe-101">Set-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f53fe-101">Set-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="f53fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f53fe-102">SYNOPSIS</span></span>
<span data-ttu-id="f53fe-103">Обновляет указанное описание правила авторизации для заданных сущностей ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="f53fe-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f53fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f53fe-104">SYNTAX</span></span>

### <span data-ttu-id="f53fe-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f53fe-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f53fe-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f53fe-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f53fe-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f53fe-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f53fe-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f53fe-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f53fe-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="f53fe-109">AuthoRulePropertiesSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f53fe-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f53fe-110">DESCRIPTION</span></span>
<span data-ttu-id="f53fe-111">Командлет **Set-AzRelayAuthorizationRule** обновляет описание указанного правила авторизации для заданных сущностей ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="f53fe-111">The **Set-AzRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f53fe-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f53fe-112">EXAMPLES</span></span>

### <span data-ttu-id="f53fe-113">Пример 1,1-Namespace с InputObject</span><span class="sxs-lookup"><span data-stu-id="f53fe-113">Example 1.1 - Namespace with InputObject</span></span>
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

<span data-ttu-id="f53fe-114">Добавляет " **Отправить** " из прав доступа правила авторизации `AuthoRule1` в пространстве имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="f53fe-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="f53fe-115">Пример 1,2-Namespace с параметром rights</span><span class="sxs-lookup"><span data-stu-id="f53fe-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="f53fe-116">Добавляет " **Отправить** " из прав доступа правила авторизации `AuthoRule1` в пространстве имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="f53fe-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="f53fe-117">Пример 2,1-WcfRelay с InputObject</span><span class="sxs-lookup"><span data-stu-id="f53fe-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="f53fe-118">Добавление **прав** доступа для правила авторизации `AuthoRule1` WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="f53fe-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="f53fe-119">Пример 2,2-WcfRelay с параметром rights</span><span class="sxs-lookup"><span data-stu-id="f53fe-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="f53fe-120">Добавление **прав** доступа для правила авторизации `AuthoRule1` WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="f53fe-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="f53fe-121">Пример 3,1-HybridConnection с InputObject</span><span class="sxs-lookup"><span data-stu-id="f53fe-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="f53fe-122">Добавление **прав** доступа для правила авторизации `AuthoRule1` HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="f53fe-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="f53fe-123">Пример 3,2-HybridConnection с параметром rights</span><span class="sxs-lookup"><span data-stu-id="f53fe-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="f53fe-124">Добавление **прав** доступа для правила авторизации `AuthoRule1` HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="f53fe-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="f53fe-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f53fe-125">PARAMETERS</span></span>

### <span data-ttu-id="f53fe-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f53fe-126">-DefaultProfile</span></span>
<span data-ttu-id="f53fe-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f53fe-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f53fe-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f53fe-128">-HybridConnection</span></span>
<span data-ttu-id="f53fe-129">HybridConnection имя.</span><span class="sxs-lookup"><span data-stu-id="f53fe-129">HybridConnection Name.</span></span>

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

### <span data-ttu-id="f53fe-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f53fe-130">-InputObject</span></span>
<span data-ttu-id="f53fe-131">Объект AuthorizationRule ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="f53fe-131">Relay AuthorizationRule Object.</span></span>

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

### <span data-ttu-id="f53fe-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f53fe-132">-Name</span></span>
<span data-ttu-id="f53fe-133">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="f53fe-133">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f53fe-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f53fe-134">-Namespace</span></span>
<span data-ttu-id="f53fe-135">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f53fe-135">Namespace Name.</span></span>

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

### <span data-ttu-id="f53fe-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f53fe-136">-ResourceGroupName</span></span>
<span data-ttu-id="f53fe-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f53fe-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="f53fe-138">-Права</span><span class="sxs-lookup"><span data-stu-id="f53fe-138">-Rights</span></span>
<span data-ttu-id="f53fe-139">Права, например @ ("прослушать", "Отправить", "Управление")</span><span class="sxs-lookup"><span data-stu-id="f53fe-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="f53fe-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f53fe-140">-WcfRelay</span></span>
<span data-ttu-id="f53fe-141">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="f53fe-141">WcfRelay Name.</span></span>

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

### <span data-ttu-id="f53fe-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f53fe-142">-Confirm</span></span>
<span data-ttu-id="f53fe-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f53fe-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f53fe-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f53fe-144">-WhatIf</span></span>
<span data-ttu-id="f53fe-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f53fe-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f53fe-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f53fe-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f53fe-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f53fe-147">CommonParameters</span></span>
<span data-ttu-id="f53fe-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f53fe-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f53fe-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f53fe-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f53fe-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f53fe-150">INPUTS</span></span>

### <span data-ttu-id="f53fe-151">System. String</span><span class="sxs-lookup"><span data-stu-id="f53fe-151">System.String</span></span>

### <span data-ttu-id="f53fe-152">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f53fe-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="f53fe-153">System. String []</span><span class="sxs-lookup"><span data-stu-id="f53fe-153">System.String[]</span></span>

## <span data-ttu-id="f53fe-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f53fe-154">OUTPUTS</span></span>

### <span data-ttu-id="f53fe-155">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f53fe-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f53fe-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="f53fe-156">NOTES</span></span>

## <span data-ttu-id="f53fe-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f53fe-157">RELATED LINKS</span></span>
