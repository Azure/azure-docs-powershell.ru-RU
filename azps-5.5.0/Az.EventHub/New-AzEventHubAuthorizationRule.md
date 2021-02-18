---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 7a7c70dc9cf106aebc44df4733c4f8f9abaa78a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214753"
---
# <span data-ttu-id="c4f66-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c4f66-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="c4f66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4f66-102">SYNOPSIS</span></span>
<span data-ttu-id="c4f66-103">Создание правила авторизации "Концентраторы событий" для пространства имен или е eventhub.</span><span class="sxs-lookup"><span data-stu-id="c4f66-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="c4f66-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c4f66-104">SYNTAX</span></span>

### <span data-ttu-id="c4f66-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c4f66-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4f66-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c4f66-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4f66-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4f66-107">DESCRIPTION</span></span>
<span data-ttu-id="c4f66-108">С New-AzEventHubAuthorizationRule создается новое правило авторизации "Концентраторы событий".</span><span class="sxs-lookup"><span data-stu-id="c4f66-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="c4f66-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c4f66-109">EXAMPLES</span></span>

### <span data-ttu-id="c4f66-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c4f66-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="c4f66-111">Создание правила авторизации MyAuthRuleName, которое предоставляет права "Прослушивание" и "Отправить" на пространство имен MyNamespaceName с группой ресурсов \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="c4f66-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c4f66-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c4f66-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="c4f66-113">Создание правила авторизации MyAuthRuleName, которое предоставляет права "Прослушивание" и "Отправить" центру событий MyEventHubName в пространствах имен MyNamespaceName с группой ресурсов \` \` \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="c4f66-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c4f66-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4f66-114">PARAMETERS</span></span>

### <span data-ttu-id="c4f66-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4f66-115">-DefaultProfile</span></span>
<span data-ttu-id="c4f66-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4f66-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4f66-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="c4f66-117">-EventHub</span></span>
<span data-ttu-id="c4f66-118">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="c4f66-118">EventHub Name</span></span>

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

### <span data-ttu-id="c4f66-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c4f66-119">-Name</span></span>
<span data-ttu-id="c4f66-120">Имяrule authorizationRule</span><span class="sxs-lookup"><span data-stu-id="c4f66-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="c4f66-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c4f66-121">-Namespace</span></span>
<span data-ttu-id="c4f66-122">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="c4f66-122">Namespace Name</span></span>

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

### <span data-ttu-id="c4f66-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4f66-123">-ResourceGroupName</span></span>
<span data-ttu-id="c4f66-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c4f66-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c4f66-125">-Rights</span><span class="sxs-lookup"><span data-stu-id="c4f66-125">-Rights</span></span>
<span data-ttu-id="c4f66-126">Права, например "Прослушивание", "Отправить", "Управление"</span><span class="sxs-lookup"><span data-stu-id="c4f66-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="c4f66-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4f66-127">-Confirm</span></span>
<span data-ttu-id="c4f66-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4f66-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4f66-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4f66-129">-WhatIf</span></span>
<span data-ttu-id="c4f66-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4f66-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4f66-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c4f66-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4f66-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4f66-132">CommonParameters</span></span>
<span data-ttu-id="c4f66-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4f66-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4f66-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4f66-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4f66-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4f66-135">INPUTS</span></span>

### <span data-ttu-id="c4f66-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c4f66-136">System.String</span></span>

### <span data-ttu-id="c4f66-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c4f66-137">System.String[]</span></span>

## <span data-ttu-id="c4f66-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c4f66-138">OUTPUTS</span></span>

### <span data-ttu-id="c4f66-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c4f66-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="c4f66-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c4f66-140">NOTES</span></span>

## <span data-ttu-id="c4f66-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4f66-141">RELATED LINKS</span></span>
