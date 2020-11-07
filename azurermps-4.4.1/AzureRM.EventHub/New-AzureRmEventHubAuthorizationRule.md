---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3085479125219450368322ddb64fee4c06cdce2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733377"
---
# <span data-ttu-id="e2890-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e2890-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="e2890-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2890-102">SYNOPSIS</span></span>
<span data-ttu-id="e2890-103">Создает новое правило авторизации концентраторов событий для пространства имен или eventhub.</span><span class="sxs-lookup"><span data-stu-id="e2890-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2890-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2890-104">SYNTAX</span></span>

### <span data-ttu-id="e2890-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2890-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 -Rights <String[]> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e2890-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2890-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> -Rights <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e2890-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2890-107">DESCRIPTION</span></span>
<span data-ttu-id="e2890-108">Командлет New-AzureRmEventHubAuthorizationRule создает новое правило авторизации концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="e2890-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="e2890-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2890-109">EXAMPLES</span></span>

### <span data-ttu-id="e2890-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e2890-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="e2890-111">Создание правила авторизации \` , MyAuthRuleName \` предоставлять права на прослушивание и отправку для пространства имен \` MyNamespaceName \` с помощью группы ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="e2890-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e2890-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e2890-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="e2890-113">Создает правило авторизации \` MyAuthRuleName \` предоставляющего права на прослушивание и отправку в центр событий \` MyEventHubName \` в пространстве имен \` MyNamespaceName \` , с группировкой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="e2890-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e2890-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2890-114">PARAMETERS</span></span>

### <span data-ttu-id="e2890-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2890-115">-ResourceGroupName</span></span>
<span data-ttu-id="e2890-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2890-116">Resource group name.</span></span>

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

### <span data-ttu-id="e2890-117">-Права</span><span class="sxs-lookup"><span data-stu-id="e2890-117">-Rights</span></span>
<span data-ttu-id="e2890-118">Администратора Например, @ ("прослушать", "Отправить", "Управление").</span><span class="sxs-lookup"><span data-stu-id="e2890-118">Rights; for example @("Listen","Send","Manage").</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2890-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2890-119">-Confirm</span></span>
<span data-ttu-id="e2890-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2890-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2890-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2890-121">-WhatIf</span></span>
<span data-ttu-id="e2890-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2890-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2890-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2890-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2890-124">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e2890-124">-EventHub</span></span>
<span data-ttu-id="e2890-125">Имя EventHub.</span><span class="sxs-lookup"><span data-stu-id="e2890-125">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2890-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2890-126">-Name</span></span>
<span data-ttu-id="e2890-127">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="e2890-127">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2890-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2890-128">-Namespace</span></span>
<span data-ttu-id="e2890-129">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="e2890-129">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="e2890-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2890-130">INPUTS</span></span>

### <span data-ttu-id="e2890-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e2890-131">System.String</span></span>

## <span data-ttu-id="e2890-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2890-132">OUTPUTS</span></span>

### <span data-ttu-id="e2890-133">Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e2890-133">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e2890-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2890-134">NOTES</span></span>

## <span data-ttu-id="e2890-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2890-135">RELATED LINKS</span></span>

