---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: 39bba687e355b1742210fb0c37fc8f1a65d957a0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421119"
---
# <span data-ttu-id="8af02-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8af02-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="8af02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8af02-102">SYNOPSIS</span></span>
<span data-ttu-id="8af02-103">Создание правила авторизации для указанных сущностями ретрансляции (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="8af02-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="8af02-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8af02-104">SYNTAX</span></span>

### <span data-ttu-id="8af02-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8af02-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8af02-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8af02-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8af02-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8af02-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8af02-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8af02-108">DESCRIPTION</span></span>
<span data-ttu-id="8af02-109">Командлет **New-AzRelayAuthorizationRule** создает новое правило авторизации для указанных сущностями Relay (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="8af02-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="8af02-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8af02-110">EXAMPLES</span></span>

### <span data-ttu-id="8af02-111">Пример 1. Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8af02-111">Example 1: Namespace</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="8af02-112">Создается `AuthoRule1` с **правами на** прослушивание для пространства `TestNameSpace-Relay1` имен.</span><span class="sxs-lookup"><span data-stu-id="8af02-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="8af02-113">Пример 2. WcfRelay</span><span class="sxs-lookup"><span data-stu-id="8af02-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="8af02-114">Создает правило авторизации `AuthoRule1` с **правами на** прослушивание для WcfRelay. `TestWCFRelay1`</span><span class="sxs-lookup"><span data-stu-id="8af02-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="8af02-115">Пример 3. Гибриднаясоединение</span><span class="sxs-lookup"><span data-stu-id="8af02-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="8af02-116">Создается `AuthoRule1` с **правами на прослушивание** для гибридного `TestHybridConnection` подключения.</span><span class="sxs-lookup"><span data-stu-id="8af02-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="8af02-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8af02-117">PARAMETERS</span></span>

### <span data-ttu-id="8af02-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af02-118">-DefaultProfile</span></span>
<span data-ttu-id="8af02-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8af02-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8af02-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="8af02-120">-HybridConnection</span></span>
<span data-ttu-id="8af02-121">Имя HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="8af02-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="8af02-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8af02-122">-Name</span></span>
<span data-ttu-id="8af02-123">Имяrule authorizationRule.</span><span class="sxs-lookup"><span data-stu-id="8af02-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="8af02-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8af02-124">-Namespace</span></span>
<span data-ttu-id="8af02-125">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="8af02-125">Namespace Name.</span></span>

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

### <span data-ttu-id="8af02-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8af02-126">-ResourceGroupName</span></span>
<span data-ttu-id="8af02-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8af02-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="8af02-128">-Rights</span><span class="sxs-lookup"><span data-stu-id="8af02-128">-Rights</span></span>
<span data-ttu-id="8af02-129">Права, например "Прослушивание", "Отправить", "Управление"</span><span class="sxs-lookup"><span data-stu-id="8af02-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="8af02-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="8af02-130">-WcfRelay</span></span>
<span data-ttu-id="8af02-131">Имя WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="8af02-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="8af02-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8af02-132">-Confirm</span></span>
<span data-ttu-id="8af02-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8af02-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8af02-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8af02-134">-WhatIf</span></span>
<span data-ttu-id="8af02-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8af02-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8af02-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8af02-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8af02-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af02-137">CommonParameters</span></span>
<span data-ttu-id="8af02-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8af02-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af02-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8af02-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af02-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8af02-140">INPUTS</span></span>

### <span data-ttu-id="8af02-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8af02-141">System.String</span></span>

### <span data-ttu-id="8af02-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="8af02-142">System.String[]</span></span>

## <span data-ttu-id="8af02-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8af02-143">OUTPUTS</span></span>

### <span data-ttu-id="8af02-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8af02-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="8af02-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8af02-145">NOTES</span></span>

## <span data-ttu-id="8af02-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8af02-146">RELATED LINKS</span></span>
