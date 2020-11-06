---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 91f37ad2ed49b4c1bd39306be803776ddce9ecff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567950"
---
# <span data-ttu-id="2ac81-101">Set-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2ac81-101">Set-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="2ac81-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ac81-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac81-103">Обновляет указанное описание правила авторизации для заданных сущностей ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="2ac81-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ac81-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ac81-104">SYNTAX</span></span>

### <span data-ttu-id="2ac81-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ac81-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ac81-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2ac81-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ac81-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2ac81-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>]
 [[-Rights] <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ac81-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2ac81-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <AuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ac81-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="2ac81-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ac81-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ac81-110">DESCRIPTION</span></span>
<span data-ttu-id="2ac81-111">Командлет **Set-AzureRmRelayAuthorizationRule** обновляет описание указанного правила авторизации для заданных сущностей ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="2ac81-111">The **Set-AzureRmRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2ac81-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ac81-112">EXAMPLES</span></span>

### <span data-ttu-id="2ac81-113">Пример 1,1-Namespace с InputObject</span><span class="sxs-lookup"><span data-stu-id="2ac81-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule
```

<span data-ttu-id="2ac81-114">Добавляет " **Отправить** " из прав доступа правила авторизации `AuthoRule1` в пространстве имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="2ac81-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="2ac81-115">Пример 1,2-Namespace с параметром rights</span><span class="sxs-lookup"><span data-stu-id="2ac81-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"
```

<span data-ttu-id="2ac81-116">Добавляет " **Отправить** " из прав доступа правила авторизации `AuthoRule1` в пространстве имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="2ac81-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="2ac81-117">Пример 2,1-WcfRelay с InputObject</span><span class="sxs-lookup"><span data-stu-id="2ac81-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho
```

<span data-ttu-id="2ac81-118">Добавление **прав** доступа для правила авторизации `AuthoRule1` WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="2ac81-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="2ac81-119">Пример 2,2-WcfRelay с параметром rights</span><span class="sxs-lookup"><span data-stu-id="2ac81-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="2ac81-120">Добавление **прав** доступа для правила авторизации `AuthoRule1` WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="2ac81-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="2ac81-121">Пример 3,1-HybridConnection с InputObject</span><span class="sxs-lookup"><span data-stu-id="2ac81-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho
```

<span data-ttu-id="2ac81-122">Добавление **прав** доступа для правила авторизации `AuthoRule1` HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="2ac81-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="2ac81-123">Пример 3,2-HybridConnection с параметром rights</span><span class="sxs-lookup"><span data-stu-id="2ac81-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="2ac81-124">Добавление **прав** доступа для правила авторизации `AuthoRule1` HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="2ac81-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="2ac81-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ac81-125">PARAMETERS</span></span>

### <span data-ttu-id="2ac81-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac81-126">-DefaultProfile</span></span>
<span data-ttu-id="2ac81-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ac81-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ac81-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2ac81-128">-HybridConnection</span></span>
<span data-ttu-id="2ac81-129">HybridConnection имя.</span><span class="sxs-lookup"><span data-stu-id="2ac81-129">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac81-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ac81-130">-InputObject</span></span>
<span data-ttu-id="2ac81-131">Объект ретрансляции AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2ac81-131">Relay AuthorizationRule Object</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac81-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2ac81-132">-Name</span></span>
<span data-ttu-id="2ac81-133">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="2ac81-133">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac81-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2ac81-134">-Namespace</span></span>
<span data-ttu-id="2ac81-135">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="2ac81-135">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac81-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac81-136">-ResourceGroupName</span></span>
<span data-ttu-id="2ac81-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ac81-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="2ac81-138">-Права</span><span class="sxs-lookup"><span data-stu-id="2ac81-138">-Rights</span></span>
<span data-ttu-id="2ac81-139">Права, например @ ("прослушать", "Отправить", "Управление")</span><span class="sxs-lookup"><span data-stu-id="2ac81-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac81-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2ac81-140">-WcfRelay</span></span>
<span data-ttu-id="2ac81-141">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="2ac81-141">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac81-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ac81-142">-Confirm</span></span>
<span data-ttu-id="2ac81-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2ac81-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ac81-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ac81-144">-WhatIf</span></span>
<span data-ttu-id="2ac81-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2ac81-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ac81-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2ac81-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ac81-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac81-147">CommonParameters</span></span>
<span data-ttu-id="2ac81-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ac81-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac81-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ac81-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac81-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ac81-150">INPUTS</span></span>

### <span data-ttu-id="2ac81-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac81-151">-ResourceGroupName</span></span>
 <span data-ttu-id="2ac81-152">System. String</span><span class="sxs-lookup"><span data-stu-id="2ac81-152">System.String</span></span> 

### <span data-ttu-id="2ac81-153">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2ac81-153">-Namespace</span></span>
 <span data-ttu-id="2ac81-154">System. String</span><span class="sxs-lookup"><span data-stu-id="2ac81-154">System.String</span></span> 
 

### <span data-ttu-id="2ac81-155">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2ac81-155">-WcfRelay</span></span>
 <span data-ttu-id="2ac81-156">System. String</span><span class="sxs-lookup"><span data-stu-id="2ac81-156">System.String</span></span> 

### <span data-ttu-id="2ac81-157">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2ac81-157">-HybridConnection</span></span>
 <span data-ttu-id="2ac81-158">System. String</span><span class="sxs-lookup"><span data-stu-id="2ac81-158">System.String</span></span> 
 

### <span data-ttu-id="2ac81-159">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2ac81-159">-Name</span></span>
 <span data-ttu-id="2ac81-160">System. String</span><span class="sxs-lookup"><span data-stu-id="2ac81-160">System.String</span></span>

### <span data-ttu-id="2ac81-161">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ac81-161">-InputObject</span></span>
 <span data-ttu-id="2ac81-162">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2ac81-162">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>
 

### <span data-ttu-id="2ac81-163">-Права</span><span class="sxs-lookup"><span data-stu-id="2ac81-163">-Rights</span></span>
 <span data-ttu-id="2ac81-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="2ac81-164">System.String []</span></span>

## <span data-ttu-id="2ac81-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ac81-165">OUTPUTS</span></span>

### <span data-ttu-id="2ac81-166">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2ac81-166">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="2ac81-167">Пример 1 — пространство имен</span><span class="sxs-lookup"><span data-stu-id="2ac81-167">Example 1 - Namespace</span></span>
<span data-ttu-id="2ac81-168">Права: {Listen, Send} Name: AuthoRule1 Type: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="2ac81-168">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="2ac81-169">Пример 2 — WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2ac81-169">Example 2 - WcfRelay</span></span>
<span data-ttu-id="2ac81-170">Права: {Listen, Send} Name: AuthoRule1 Type: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="2ac81-170">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="2ac81-171">Пример 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2ac81-171">Example 3 - HybridConnection</span></span>
<span data-ttu-id="2ac81-172">Права: {Listen, Send} Name: AuthoRule1 Type: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="2ac81-172">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="2ac81-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ac81-173">NOTES</span></span>

## <span data-ttu-id="2ac81-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ac81-174">RELATED LINKS</span></span>

