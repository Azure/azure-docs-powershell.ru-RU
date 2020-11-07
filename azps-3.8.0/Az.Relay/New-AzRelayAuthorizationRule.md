---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: ed50beeddbb0e9d85457952b1fcc524d8ee2dcd5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912671"
---
# <span data-ttu-id="ea3a4-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ea3a4-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="ea3a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea3a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ea3a4-103">Создание нового правила авторизации для указанных ретранслируемых сущностей (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="ea3a4-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="ea3a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea3a4-104">SYNTAX</span></span>

### <span data-ttu-id="ea3a4-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ea3a4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea3a4-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ea3a4-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea3a4-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ea3a4-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea3a4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea3a4-108">DESCRIPTION</span></span>
<span data-ttu-id="ea3a4-109">Командлет **New-AzRelayAuthorizationRule** создает новое правило авторизации для указанных ретранслируемых сущностей (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="ea3a4-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="ea3a4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea3a4-110">EXAMPLES</span></span>

### <span data-ttu-id="ea3a4-111">Пример 1 — пространство имен</span><span class="sxs-lookup"><span data-stu-id="ea3a4-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="ea3a4-112">Создает `AuthoRule1` с правами **прослушивания** для пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="ea3a4-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="ea3a4-113">Пример 2 — WcfRelay</span><span class="sxs-lookup"><span data-stu-id="ea3a4-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="ea3a4-114">Создает правило авторизации `AuthoRule1` с правами **прослушивания** для WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="ea3a4-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="ea3a4-115">Пример 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="ea3a4-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="ea3a4-116">Создает `AuthoRule1` с правами **прослушивания** для гибридного подключения `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="ea3a4-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="ea3a4-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea3a4-117">PARAMETERS</span></span>

### <span data-ttu-id="ea3a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea3a4-118">-DefaultProfile</span></span>
<span data-ttu-id="ea3a4-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea3a4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea3a4-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="ea3a4-120">-HybridConnection</span></span>
<span data-ttu-id="ea3a4-121">HybridConnection имя.</span><span class="sxs-lookup"><span data-stu-id="ea3a4-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="ea3a4-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ea3a4-122">-Name</span></span>
<span data-ttu-id="ea3a4-123">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="ea3a4-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="ea3a4-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ea3a4-124">-Namespace</span></span>
<span data-ttu-id="ea3a4-125">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ea3a4-125">Namespace Name.</span></span>

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

### <span data-ttu-id="ea3a4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea3a4-126">-ResourceGroupName</span></span>
<span data-ttu-id="ea3a4-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ea3a4-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="ea3a4-128">-Права</span><span class="sxs-lookup"><span data-stu-id="ea3a4-128">-Rights</span></span>
<span data-ttu-id="ea3a4-129">Права, например "прослушать", "Отправить", "Управление"</span><span class="sxs-lookup"><span data-stu-id="ea3a4-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea3a4-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="ea3a4-130">-WcfRelay</span></span>
<span data-ttu-id="ea3a4-131">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="ea3a4-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="ea3a4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea3a4-132">-Confirm</span></span>
<span data-ttu-id="ea3a4-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea3a4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea3a4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea3a4-134">-WhatIf</span></span>
<span data-ttu-id="ea3a4-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea3a4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea3a4-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea3a4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea3a4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea3a4-137">CommonParameters</span></span>
<span data-ttu-id="ea3a4-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea3a4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea3a4-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea3a4-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea3a4-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea3a4-140">INPUTS</span></span>

### <span data-ttu-id="ea3a4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ea3a4-141">System.String</span></span>

### <span data-ttu-id="ea3a4-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="ea3a4-142">System.String[]</span></span>

## <span data-ttu-id="ea3a4-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea3a4-143">OUTPUTS</span></span>

### <span data-ttu-id="ea3a4-144">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ea3a4-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ea3a4-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea3a4-145">NOTES</span></span>

## <span data-ttu-id="ea3a4-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea3a4-146">RELATED LINKS</span></span>
