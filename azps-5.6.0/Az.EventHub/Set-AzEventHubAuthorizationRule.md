---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: ef71b8ce2f90fb6275c3bd658289f4e32579cd69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004152"
---
# <span data-ttu-id="062e1-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="062e1-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="062e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="062e1-102">SYNOPSIS</span></span>
<span data-ttu-id="062e1-103">Обновляет указанное правило авторизации в центре событий.</span><span class="sxs-lookup"><span data-stu-id="062e1-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="062e1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="062e1-104">SYNTAX</span></span>

### <span data-ttu-id="062e1-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="062e1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="062e1-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="062e1-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="062e1-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="062e1-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="062e1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="062e1-108">DESCRIPTION</span></span>
<span data-ttu-id="062e1-109">Этот Set-AzEventHubAuthorizationRule обновляет указанное правило авторизации в этом центре событий.</span><span class="sxs-lookup"><span data-stu-id="062e1-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="062e1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="062e1-110">EXAMPLES</span></span>

### <span data-ttu-id="062e1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="062e1-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="062e1-112">Обновляет правило авторизации MyAuthRuleName, чтобы предоставить управление правами на центр событий \` \` \` MyEventHubName в области имен \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="062e1-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="062e1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="062e1-113">PARAMETERS</span></span>

### <span data-ttu-id="062e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="062e1-114">-DefaultProfile</span></span>
<span data-ttu-id="062e1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="062e1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="062e1-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="062e1-116">-EventHub</span></span>
<span data-ttu-id="062e1-117">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="062e1-117">EventHub Name</span></span>

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

### <span data-ttu-id="062e1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="062e1-118">-InputObject</span></span>
<span data-ttu-id="062e1-119">Объект AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="062e1-119">AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="062e1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="062e1-120">-Name</span></span>
<span data-ttu-id="062e1-121">Имяrule authorizationRule</span><span class="sxs-lookup"><span data-stu-id="062e1-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="062e1-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="062e1-122">-Namespace</span></span>
<span data-ttu-id="062e1-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="062e1-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="062e1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="062e1-124">-ResourceGroupName</span></span>
<span data-ttu-id="062e1-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="062e1-125">Resource Group Name</span></span>

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

### <span data-ttu-id="062e1-126">-Rights</span><span class="sxs-lookup"><span data-stu-id="062e1-126">-Rights</span></span>
<span data-ttu-id="062e1-127">Права, например @("Прослушивание";"Отправить";"Управление")</span><span class="sxs-lookup"><span data-stu-id="062e1-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="062e1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="062e1-128">-Confirm</span></span>
<span data-ttu-id="062e1-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="062e1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="062e1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="062e1-130">-WhatIf</span></span>
<span data-ttu-id="062e1-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="062e1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="062e1-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="062e1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="062e1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="062e1-133">CommonParameters</span></span>
<span data-ttu-id="062e1-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="062e1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="062e1-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="062e1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="062e1-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="062e1-136">INPUTS</span></span>

### <span data-ttu-id="062e1-137">System.String</span><span class="sxs-lookup"><span data-stu-id="062e1-137">System.String</span></span>

### <span data-ttu-id="062e1-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="062e1-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="062e1-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="062e1-139">System.String[]</span></span>

## <span data-ttu-id="062e1-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="062e1-140">OUTPUTS</span></span>

### <span data-ttu-id="062e1-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="062e1-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="062e1-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="062e1-142">NOTES</span></span>

## <span data-ttu-id="062e1-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="062e1-143">RELATED LINKS</span></span>
