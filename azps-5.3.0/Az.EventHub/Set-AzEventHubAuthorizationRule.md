---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 862b6f295a997b2027520a3f9c6a9f4f9cfb5ae9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504907"
---
# <span data-ttu-id="e204b-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e204b-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="e204b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e204b-102">SYNOPSIS</span></span>
<span data-ttu-id="e204b-103">Обновляет указанное правило авторизации в центре событий.</span><span class="sxs-lookup"><span data-stu-id="e204b-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="e204b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e204b-104">SYNTAX</span></span>

### <span data-ttu-id="e204b-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e204b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e204b-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e204b-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e204b-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e204b-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e204b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e204b-108">DESCRIPTION</span></span>
<span data-ttu-id="e204b-109">Этот Set-AzEventHubAuthorizationRule обновляет указанное правило авторизации в этом центре событий.</span><span class="sxs-lookup"><span data-stu-id="e204b-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="e204b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e204b-110">EXAMPLES</span></span>

### <span data-ttu-id="e204b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e204b-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="e204b-112">Обновляет правило авторизации MyAuthRuleName, чтобы предоставить управление правами на центр событий \` \` \` MyEventHubName в области имен \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="e204b-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="e204b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e204b-113">PARAMETERS</span></span>

### <span data-ttu-id="e204b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e204b-114">-DefaultProfile</span></span>
<span data-ttu-id="e204b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e204b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e204b-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e204b-116">-EventHub</span></span>
<span data-ttu-id="e204b-117">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="e204b-117">EventHub Name</span></span>

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

### <span data-ttu-id="e204b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e204b-118">-InputObject</span></span>
<span data-ttu-id="e204b-119">Объект AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e204b-119">AuthorizationRule Object</span></span>

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

### <span data-ttu-id="e204b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e204b-120">-Name</span></span>
<span data-ttu-id="e204b-121">Имяrule authorizationRule</span><span class="sxs-lookup"><span data-stu-id="e204b-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="e204b-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e204b-122">-Namespace</span></span>
<span data-ttu-id="e204b-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="e204b-123">Namespace Name</span></span>

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

### <span data-ttu-id="e204b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e204b-124">-ResourceGroupName</span></span>
<span data-ttu-id="e204b-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e204b-125">Resource Group Name</span></span>

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

### <span data-ttu-id="e204b-126">-Rights</span><span class="sxs-lookup"><span data-stu-id="e204b-126">-Rights</span></span>
<span data-ttu-id="e204b-127">Права, например @("Прослушивание";"Отправить";"Управление")</span><span class="sxs-lookup"><span data-stu-id="e204b-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="e204b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e204b-128">-Confirm</span></span>
<span data-ttu-id="e204b-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e204b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e204b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e204b-130">-WhatIf</span></span>
<span data-ttu-id="e204b-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e204b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e204b-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e204b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e204b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e204b-133">CommonParameters</span></span>
<span data-ttu-id="e204b-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e204b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e204b-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e204b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e204b-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e204b-136">INPUTS</span></span>

### <span data-ttu-id="e204b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e204b-137">System.String</span></span>

### <span data-ttu-id="e204b-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e204b-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="e204b-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e204b-139">System.String[]</span></span>

## <span data-ttu-id="e204b-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e204b-140">OUTPUTS</span></span>

### <span data-ttu-id="e204b-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e204b-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e204b-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e204b-142">NOTES</span></span>

## <span data-ttu-id="e204b-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e204b-143">RELATED LINKS</span></span>
