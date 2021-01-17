---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 6940e12f813cbc4292f02ab98f0b35774da67025
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323669"
---
# <span data-ttu-id="6d42e-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6d42e-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="6d42e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d42e-102">SYNOPSIS</span></span>
<span data-ttu-id="6d42e-103">Получает сведения о правиле авторизации или список правил авторизации.</span><span class="sxs-lookup"><span data-stu-id="6d42e-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="6d42e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6d42e-104">SYNTAX</span></span>

### <span data-ttu-id="6d42e-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6d42e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d42e-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d42e-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d42e-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d42e-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d42e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d42e-108">DESCRIPTION</span></span>
<span data-ttu-id="6d42e-109">Этот Get-AzEventHubAuthorizationRule получает либо сведения о правиле авторизации, либо список всех правил авторизации для указанного центра событий.</span><span class="sxs-lookup"><span data-stu-id="6d42e-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="6d42e-110">Если за предоставлено имя правила авторизации, возвращаются его сведения.</span><span class="sxs-lookup"><span data-stu-id="6d42e-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="6d42e-111">Если имя правила авторизации не указано, возвращается список всех правил авторизации для указанного центра событий.</span><span class="sxs-lookup"><span data-stu-id="6d42e-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="6d42e-112">Если предоставлен псевдоним (Аварийное восстановление), возвращаются сведения о правиле авторизации для настроенного пространства имен для псевдонима.</span><span class="sxs-lookup"><span data-stu-id="6d42e-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="6d42e-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6d42e-113">EXAMPLES</span></span>

### <span data-ttu-id="6d42e-114">Пример 1. AuthorizationRule для пространства имен</span><span class="sxs-lookup"><span data-stu-id="6d42e-114">Example 1: AuthorizationRule for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="6d42e-115">Получает правило авторизации \` MyAuthRuleName в области имен \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="6d42e-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="6d42e-116">Пример 2. AuthorizationRules для пространства имен</span><span class="sxs-lookup"><span data-stu-id="6d42e-116">Example 2: AuthorizationRules for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="6d42e-117">Получает список всех правил авторизации в области имен \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="6d42e-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="6d42e-118">Пример 3. AuthorizationRule для EventHub</span><span class="sxs-lookup"><span data-stu-id="6d42e-118">Example 3: AuthorizationRule for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="6d42e-119">Получает правило авторизации \` MyAuthRuleName в Центре событий MyEventHubName, область действия которого составляется областью имен \` \` \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="6d42e-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="6d42e-120">Пример 4. AuthorizationRules для EventHub</span><span class="sxs-lookup"><span data-stu-id="6d42e-120">Example 4: AuthorizationRules for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="6d42e-121">Получает правила авторизации списка в центре событий MyEventHubName, область действия которого составляется по пространствам имен \` \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="6d42e-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="6d42e-122">Пример 5. AuthorizationRule for Alias (GeoRecovery Configuration)</span><span class="sxs-lookup"><span data-stu-id="6d42e-122">Example 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="6d42e-123">Получает правило авторизации \` MyAuthRuleName в области имен \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="6d42e-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="6d42e-124">Пример 6. AuthorizationRules for Alias (GeoRecovery Configuration)</span><span class="sxs-lookup"><span data-stu-id="6d42e-124">Example 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="6d42e-125">Получает список всех правил авторизации \` MyAuthRuleName в области имен \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="6d42e-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="6d42e-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d42e-126">PARAMETERS</span></span>

### <span data-ttu-id="6d42e-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="6d42e-127">-AliasName</span></span>
<span data-ttu-id="6d42e-128">Alias Name</span><span class="sxs-lookup"><span data-stu-id="6d42e-128">Alias Name</span></span>

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

### <span data-ttu-id="6d42e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d42e-129">-DefaultProfile</span></span>
<span data-ttu-id="6d42e-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d42e-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d42e-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="6d42e-131">-Eventhub</span></span>
<span data-ttu-id="6d42e-132">Имя Евthub</span><span class="sxs-lookup"><span data-stu-id="6d42e-132">Eventhub Name</span></span>

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

### <span data-ttu-id="6d42e-133">-Name</span><span class="sxs-lookup"><span data-stu-id="6d42e-133">-Name</span></span>
<span data-ttu-id="6d42e-134">Имяrule authorizationRule</span><span class="sxs-lookup"><span data-stu-id="6d42e-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="6d42e-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6d42e-135">-Namespace</span></span>
<span data-ttu-id="6d42e-136">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="6d42e-136">Namespace Name</span></span>

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

### <span data-ttu-id="6d42e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d42e-137">-ResourceGroupName</span></span>
<span data-ttu-id="6d42e-138">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6d42e-138">Resource Group Name</span></span>

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

### <span data-ttu-id="6d42e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d42e-139">CommonParameters</span></span>
<span data-ttu-id="6d42e-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d42e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d42e-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d42e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d42e-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d42e-142">INPUTS</span></span>

### <span data-ttu-id="6d42e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="6d42e-143">System.String</span></span>

## <span data-ttu-id="6d42e-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6d42e-144">OUTPUTS</span></span>

### <span data-ttu-id="6d42e-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="6d42e-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="6d42e-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6d42e-146">NOTES</span></span>

## <span data-ttu-id="6d42e-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d42e-147">RELATED LINKS</span></span>
