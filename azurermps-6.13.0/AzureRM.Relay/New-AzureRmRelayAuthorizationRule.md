---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 825c6060a77df4adf59465e372ee2511fec80803
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558327"
---
# <span data-ttu-id="9ebbb-101">New-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9ebbb-101">New-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="9ebbb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ebbb-102">SYNOPSIS</span></span>
<span data-ttu-id="9ebbb-103">Создание нового правила авторизации для указанных ретранслируемых сущностей (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="9ebbb-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ebbb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ebbb-104">SYNTAX</span></span>

### <span data-ttu-id="9ebbb-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ebbb-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ebbb-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9ebbb-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ebbb-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9ebbb-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ebbb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ebbb-108">DESCRIPTION</span></span>
<span data-ttu-id="9ebbb-109">Командлет **New-AzureRmRelayAuthorizationRule** создает новое правило авторизации для указанных ретранслируемых сущностей (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="9ebbb-109">The **New-AzureRmRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="9ebbb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ebbb-110">EXAMPLES</span></span>

### <span data-ttu-id="9ebbb-111">Пример 1 — пространство имен</span><span class="sxs-lookup"><span data-stu-id="9ebbb-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="9ebbb-112">Создает `AuthoRule1` с правами **прослушивания** для пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="9ebbb-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="9ebbb-113">Пример 2 — WcfRelay</span><span class="sxs-lookup"><span data-stu-id="9ebbb-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="9ebbb-114">Создает правило авторизации `AuthoRule1` с правами **прослушивания** для WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="9ebbb-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="9ebbb-115">Пример 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="9ebbb-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="9ebbb-116">Создает `AuthoRule1` с правами **прослушивания** для гибридного подключения `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="9ebbb-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="9ebbb-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ebbb-117">PARAMETERS</span></span>

### <span data-ttu-id="9ebbb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ebbb-118">-DefaultProfile</span></span>
<span data-ttu-id="9ebbb-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ebbb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ebbb-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="9ebbb-120">-HybridConnection</span></span>
<span data-ttu-id="9ebbb-121">HybridConnection имя.</span><span class="sxs-lookup"><span data-stu-id="9ebbb-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="9ebbb-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9ebbb-122">-Name</span></span>
<span data-ttu-id="9ebbb-123">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="9ebbb-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="9ebbb-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9ebbb-124">-Namespace</span></span>
<span data-ttu-id="9ebbb-125">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="9ebbb-125">Namespace Name.</span></span>

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

### <span data-ttu-id="9ebbb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ebbb-126">-ResourceGroupName</span></span>
<span data-ttu-id="9ebbb-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ebbb-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="9ebbb-128">-Права</span><span class="sxs-lookup"><span data-stu-id="9ebbb-128">-Rights</span></span>
<span data-ttu-id="9ebbb-129">Права, например "прослушать", "Отправить", "Управление"</span><span class="sxs-lookup"><span data-stu-id="9ebbb-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="9ebbb-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="9ebbb-130">-WcfRelay</span></span>
<span data-ttu-id="9ebbb-131">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="9ebbb-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="9ebbb-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ebbb-132">-Confirm</span></span>
<span data-ttu-id="9ebbb-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9ebbb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ebbb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ebbb-134">-WhatIf</span></span>
<span data-ttu-id="9ebbb-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9ebbb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ebbb-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9ebbb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ebbb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ebbb-137">CommonParameters</span></span>
<span data-ttu-id="9ebbb-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ebbb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9ebbb-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ebbb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ebbb-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ebbb-140">INPUTS</span></span>

### <span data-ttu-id="9ebbb-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9ebbb-141">System.String</span></span>
<span data-ttu-id="9ebbb-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="9ebbb-142">System.String[]</span></span>


## <span data-ttu-id="9ebbb-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ebbb-143">OUTPUTS</span></span>

### <span data-ttu-id="9ebbb-144">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="9ebbb-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="9ebbb-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ebbb-145">NOTES</span></span>

## <span data-ttu-id="9ebbb-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ebbb-146">RELATED LINKS</span></span>
