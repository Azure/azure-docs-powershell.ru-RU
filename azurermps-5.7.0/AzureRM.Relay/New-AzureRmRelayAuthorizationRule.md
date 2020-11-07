---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: daa2d1539a97b7aff7348fe8e603179c857c73db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734009"
---
# <span data-ttu-id="be698-101">New-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="be698-101">New-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="be698-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be698-102">SYNOPSIS</span></span>
<span data-ttu-id="be698-103">Создание нового правила авторизации для указанных ретранслируемых сущностей (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="be698-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be698-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be698-104">SYNTAX</span></span>

### <span data-ttu-id="be698-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="be698-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be698-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="be698-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be698-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="be698-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be698-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be698-108">DESCRIPTION</span></span>
<span data-ttu-id="be698-109">Командлет **New-AzureRmRelayAuthorizationRule** создает новое правило авторизации для указанных ретранслируемых сущностей (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="be698-109">The **New-AzureRmRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="be698-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be698-110">EXAMPLES</span></span>

### <span data-ttu-id="be698-111">Пример 1 — пространство имен</span><span class="sxs-lookup"><span data-stu-id="be698-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="be698-112">Создает `AuthoRule1` с правами **прослушивания** для пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="be698-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="be698-113">Пример 2 — WcfRelay</span><span class="sxs-lookup"><span data-stu-id="be698-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="be698-114">Создает правило авторизации `AuthoRule1` с правами **прослушивания** для WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="be698-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="be698-115">Пример 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="be698-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="be698-116">Создает `AuthoRule1` с правами **прослушивания** для пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="be698-116">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="be698-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be698-117">PARAMETERS</span></span>

### <span data-ttu-id="be698-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be698-118">-DefaultProfile</span></span>
<span data-ttu-id="be698-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be698-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be698-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="be698-120">-HybridConnection</span></span>
<span data-ttu-id="be698-121">HybridConnection имя.</span><span class="sxs-lookup"><span data-stu-id="be698-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="be698-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="be698-122">-Name</span></span>
<span data-ttu-id="be698-123">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="be698-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="be698-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="be698-124">-Namespace</span></span>
<span data-ttu-id="be698-125">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="be698-125">Namespace Name.</span></span>

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

### <span data-ttu-id="be698-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be698-126">-ResourceGroupName</span></span>
<span data-ttu-id="be698-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="be698-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="be698-128">-Права</span><span class="sxs-lookup"><span data-stu-id="be698-128">-Rights</span></span>
<span data-ttu-id="be698-129">Права, например "прослушать", "Отправить", "Управление"</span><span class="sxs-lookup"><span data-stu-id="be698-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be698-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="be698-130">-WcfRelay</span></span>
<span data-ttu-id="be698-131">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="be698-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="be698-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be698-132">-Confirm</span></span>
<span data-ttu-id="be698-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be698-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be698-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be698-134">-WhatIf</span></span>
<span data-ttu-id="be698-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be698-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be698-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be698-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be698-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be698-137">CommonParameters</span></span>
<span data-ttu-id="be698-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be698-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be698-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be698-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be698-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be698-140">INPUTS</span></span>

### <span data-ttu-id="be698-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be698-141">-ResourceGroupName</span></span>
 <span data-ttu-id="be698-142">System. String</span><span class="sxs-lookup"><span data-stu-id="be698-142">System.String</span></span> 

### <span data-ttu-id="be698-143">-Namespace</span><span class="sxs-lookup"><span data-stu-id="be698-143">-Namespace</span></span>
 <span data-ttu-id="be698-144">System. String</span><span class="sxs-lookup"><span data-stu-id="be698-144">System.String</span></span> 
 

### <span data-ttu-id="be698-145">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="be698-145">-WcfRelay</span></span>
 <span data-ttu-id="be698-146">System. String</span><span class="sxs-lookup"><span data-stu-id="be698-146">System.String</span></span> 

### <span data-ttu-id="be698-147">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="be698-147">-HybridConnection</span></span>
 <span data-ttu-id="be698-148">System. String</span><span class="sxs-lookup"><span data-stu-id="be698-148">System.String</span></span> 
 

### <span data-ttu-id="be698-149">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="be698-149">-Name</span></span>
 <span data-ttu-id="be698-150">System. String</span><span class="sxs-lookup"><span data-stu-id="be698-150">System.String</span></span>
 

### <span data-ttu-id="be698-151">-Права</span><span class="sxs-lookup"><span data-stu-id="be698-151">-Rights</span></span>
 <span data-ttu-id="be698-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="be698-152">System.String []</span></span>

## <span data-ttu-id="be698-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be698-153">OUTPUTS</span></span>

### <span data-ttu-id="be698-154">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="be698-154">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="be698-155">Пример 1 — пространство имен</span><span class="sxs-lookup"><span data-stu-id="be698-155">Example 1 - Namespace</span></span>
<span data-ttu-id="be698-156">Права: {Listen} имя: AuthoRule1 Type: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="be698-156">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="be698-157">Пример 2 — WcfRelay</span><span class="sxs-lookup"><span data-stu-id="be698-157">Example 2 - WcfRelay</span></span>
<span data-ttu-id="be698-158">Права: {Listen} имя: AuthoRule1 Type: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="be698-158">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="be698-159">Пример 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="be698-159">Example 3 - HybridConnection</span></span>
<span data-ttu-id="be698-160">Права: {Listen} имя: AuthoRule1 Type: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="be698-160">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="be698-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="be698-161">NOTES</span></span>

## <span data-ttu-id="be698-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be698-162">RELATED LINKS</span></span>

