---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 7a7c70dc9cf106aebc44df4733c4f8f9abaa78a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248680"
---
# <span data-ttu-id="d238b-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d238b-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="d238b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d238b-102">SYNOPSIS</span></span>
<span data-ttu-id="d238b-103">Создает новое правило авторизации концентраторов событий для пространства имен или eventhub.</span><span class="sxs-lookup"><span data-stu-id="d238b-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="d238b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d238b-104">SYNTAX</span></span>

### <span data-ttu-id="d238b-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d238b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d238b-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d238b-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d238b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d238b-107">DESCRIPTION</span></span>
<span data-ttu-id="d238b-108">Командлет New-AzEventHubAuthorizationRule создает новое правило авторизации концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="d238b-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="d238b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d238b-109">EXAMPLES</span></span>

### <span data-ttu-id="d238b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d238b-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="d238b-111">Создание правила авторизации \` , MyAuthRuleName \` предоставлять права на прослушивание и отправку для пространства имен \` MyNamespaceName \` с помощью группы ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="d238b-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d238b-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d238b-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="d238b-113">Создает правило авторизации \` MyAuthRuleName \` предоставляющего права на прослушивание и отправку в центр событий \` MyEventHubName \` в пространстве имен \` MyNamespaceName \` , с группировкой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="d238b-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d238b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d238b-114">PARAMETERS</span></span>

### <span data-ttu-id="d238b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d238b-115">-DefaultProfile</span></span>
<span data-ttu-id="d238b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d238b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d238b-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="d238b-117">-EventHub</span></span>
<span data-ttu-id="d238b-118">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="d238b-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d238b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d238b-119">-Name</span></span>
<span data-ttu-id="d238b-120">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d238b-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="d238b-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d238b-121">-Namespace</span></span>
<span data-ttu-id="d238b-122">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="d238b-122">Namespace Name</span></span>

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

### <span data-ttu-id="d238b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d238b-123">-ResourceGroupName</span></span>
<span data-ttu-id="d238b-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d238b-124">Resource Group Name</span></span>

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

### <span data-ttu-id="d238b-125">-Права</span><span class="sxs-lookup"><span data-stu-id="d238b-125">-Rights</span></span>
<span data-ttu-id="d238b-126">Права, например "прослушать", "Отправить", "Управление"</span><span class="sxs-lookup"><span data-stu-id="d238b-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="d238b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d238b-127">-Confirm</span></span>
<span data-ttu-id="d238b-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d238b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d238b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d238b-129">-WhatIf</span></span>
<span data-ttu-id="d238b-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d238b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d238b-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d238b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d238b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d238b-132">CommonParameters</span></span>
<span data-ttu-id="d238b-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d238b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d238b-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d238b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d238b-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d238b-135">INPUTS</span></span>

### <span data-ttu-id="d238b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d238b-136">System.String</span></span>

### <span data-ttu-id="d238b-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="d238b-137">System.String[]</span></span>

## <span data-ttu-id="d238b-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d238b-138">OUTPUTS</span></span>

### <span data-ttu-id="d238b-139">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d238b-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="d238b-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="d238b-140">NOTES</span></span>

## <span data-ttu-id="d238b-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d238b-141">RELATED LINKS</span></span>
