---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 6940e12f813cbc4292f02ab98f0b35774da67025
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420316"
---
# <span data-ttu-id="c36f0-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c36f0-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="c36f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c36f0-102">SYNOPSIS</span></span>
<span data-ttu-id="c36f0-103">Получает сведения о правиле авторизации или список правил авторизации.</span><span class="sxs-lookup"><span data-stu-id="c36f0-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="c36f0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c36f0-104">SYNTAX</span></span>

### <span data-ttu-id="c36f0-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c36f0-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c36f0-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c36f0-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c36f0-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="c36f0-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c36f0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c36f0-108">DESCRIPTION</span></span>
<span data-ttu-id="c36f0-109">Этот Get-AzEventHubAuthorizationRule получает либо сведения о правиле авторизации, либо список всех правил авторизации для указанного центра событий.</span><span class="sxs-lookup"><span data-stu-id="c36f0-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="c36f0-110">Если за предоставлено имя правила авторизации, возвращаются его сведения.</span><span class="sxs-lookup"><span data-stu-id="c36f0-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="c36f0-111">Если имя правила авторизации не указано, возвращается список всех правил авторизации для указанного центра событий.</span><span class="sxs-lookup"><span data-stu-id="c36f0-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="c36f0-112">Если предоставлен псевдоним (Аварийное восстановление), возвращаются сведения о правиле авторизации для настроенного пространства имен для псевдонима.</span><span class="sxs-lookup"><span data-stu-id="c36f0-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="c36f0-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c36f0-113">EXAMPLES</span></span>

### <span data-ttu-id="c36f0-114">Пример 1. AuthorizationRule для пространства имен</span><span class="sxs-lookup"><span data-stu-id="c36f0-114">Example 1: AuthorizationRule for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="c36f0-115">Получает правило авторизации \` MyAuthRuleName в области имен \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="c36f0-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="c36f0-116">Пример 2. AuthorizationRules для пространства имен</span><span class="sxs-lookup"><span data-stu-id="c36f0-116">Example 2: AuthorizationRules for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="c36f0-117">Получает список всех правил авторизации в области имен \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="c36f0-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="c36f0-118">Пример 3. AuthorizationRule для EventHub</span><span class="sxs-lookup"><span data-stu-id="c36f0-118">Example 3: AuthorizationRule for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="c36f0-119">Получает правило авторизации \` MyAuthRuleName в центре событий MyEventHubName, область действия которого составляется областью имен \` \` \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="c36f0-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="c36f0-120">Пример 4. AuthorizationRules для EventHub</span><span class="sxs-lookup"><span data-stu-id="c36f0-120">Example 4: AuthorizationRules for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="c36f0-121">Получает правила авторизации списка в центре событий MyEventHubName, область действия которого составляется по пространствам имен \` \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="c36f0-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="c36f0-122">Пример 5. AuthorizationRule для псевдонима (GeoRecovery Configuration)</span><span class="sxs-lookup"><span data-stu-id="c36f0-122">Example 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="c36f0-123">Получает правило авторизации \` MyAuthRuleName в области имен \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="c36f0-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="c36f0-124">Пример 6. AuthorizationRules for Alias (GeoRecovery Configuration)</span><span class="sxs-lookup"><span data-stu-id="c36f0-124">Example 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="c36f0-125">Получает список всех правил авторизации \` MyAuthRuleName в области имен \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="c36f0-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="c36f0-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c36f0-126">PARAMETERS</span></span>

### <span data-ttu-id="c36f0-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="c36f0-127">-AliasName</span></span>
<span data-ttu-id="c36f0-128">Alias Name</span><span class="sxs-lookup"><span data-stu-id="c36f0-128">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36f0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c36f0-129">-DefaultProfile</span></span>
<span data-ttu-id="c36f0-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c36f0-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c36f0-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="c36f0-131">-Eventhub</span></span>
<span data-ttu-id="c36f0-132">Имя Евthub</span><span class="sxs-lookup"><span data-stu-id="c36f0-132">Eventhub Name</span></span>

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

### <span data-ttu-id="c36f0-133">-Name</span><span class="sxs-lookup"><span data-stu-id="c36f0-133">-Name</span></span>
<span data-ttu-id="c36f0-134">Имяrule authorizationRule</span><span class="sxs-lookup"><span data-stu-id="c36f0-134">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36f0-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c36f0-135">-Namespace</span></span>
<span data-ttu-id="c36f0-136">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="c36f0-136">Namespace Name</span></span>

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

### <span data-ttu-id="c36f0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c36f0-137">-ResourceGroupName</span></span>
<span data-ttu-id="c36f0-138">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c36f0-138">Resource Group Name</span></span>

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

### <span data-ttu-id="c36f0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c36f0-139">CommonParameters</span></span>
<span data-ttu-id="c36f0-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c36f0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c36f0-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c36f0-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c36f0-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c36f0-142">INPUTS</span></span>

### <span data-ttu-id="c36f0-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c36f0-143">System.String</span></span>

## <span data-ttu-id="c36f0-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c36f0-144">OUTPUTS</span></span>

### <span data-ttu-id="c36f0-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c36f0-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="c36f0-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c36f0-146">NOTES</span></span>

## <span data-ttu-id="c36f0-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c36f0-147">RELATED LINKS</span></span>
