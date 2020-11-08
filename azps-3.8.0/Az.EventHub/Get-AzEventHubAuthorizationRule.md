---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 7fa3b4780e4c25dd716b851fd80c698b8d98d0b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066294"
---
# <span data-ttu-id="09579-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="09579-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="09579-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09579-102">SYNOPSIS</span></span>
<span data-ttu-id="09579-103">Получает сведения о правиле авторизации или получает список правил авторизации.</span><span class="sxs-lookup"><span data-stu-id="09579-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="09579-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09579-104">SYNTAX</span></span>

### <span data-ttu-id="09579-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="09579-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09579-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="09579-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09579-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="09579-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09579-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09579-108">DESCRIPTION</span></span>
<span data-ttu-id="09579-109">Командлет Get-AzEventHubAuthorizationRule получает либо сведения о правиле авторизации, либо список всех правил авторизации для определенного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="09579-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="09579-110">Если указано имя правила авторизации, возвращается информация об этом отдельном правиле авторизации.</span><span class="sxs-lookup"><span data-stu-id="09579-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="09579-111">Если имя правила авторизации не задано, возвращается список всех правил авторизации для указанного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="09579-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="09579-112">Если задано имя псевдонима (аварийное восстановление), возвращается информация о правиле авторизации пространства имен для указанного псевдонима.</span><span class="sxs-lookup"><span data-stu-id="09579-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="09579-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09579-113">EXAMPLES</span></span>

### <span data-ttu-id="09579-114">Пример 1,0-AuthorizationRule для пространства имен</span><span class="sxs-lookup"><span data-stu-id="09579-114">Example 1.0 - AuthorizationRule for namespace</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="09579-115">Возвращает правило авторизации \` , MyAuthRuleName \` в пространстве имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="09579-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="09579-116">Пример 1,1-AuthorizationRules для пространства имен</span><span class="sxs-lookup"><span data-stu-id="09579-116">Example 1.1 - AuthorizationRules for namespace</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="09579-117">Получает список всех правил авторизации в пространстве имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="09579-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="09579-118">Пример 2,0-AuthorizationRule для EventHub</span><span class="sxs-lookup"><span data-stu-id="09579-118">Example 2.0 - AuthorizationRule for EventHub</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="09579-119">Получает правило авторизации \` MyAuthRuleName \` в MyEventHubName концентратора событий \` \` , область которого ограничена пространством имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="09579-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="09579-120">Пример 2,1-AuthorizationRules для EventHub</span><span class="sxs-lookup"><span data-stu-id="09579-120">Example 2.1 - AuthorizationRules for EventHub</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="09579-121">Получает правила авторизации списка в центре событий \` MyEventHubName \` , областью действия которых является пространство имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="09579-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="09579-122">Пример 3,0-AuthorizationRule для псевдонима (конфигурация с геовосстановлением)</span><span class="sxs-lookup"><span data-stu-id="09579-122">Example 3.0 - AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="09579-123">Возвращает правило авторизации \` , MyAuthRuleName \` в пространстве имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="09579-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="09579-124">Пример 3,1-AuthorizationRules для псевдонима (конфигурация с геовосстановлением)</span><span class="sxs-lookup"><span data-stu-id="09579-124">Example 3.1 -AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="09579-125">Получает список всех MyAuthRuleName правил авторизации \` \` в пространстве имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="09579-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="09579-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09579-126">PARAMETERS</span></span>

### <span data-ttu-id="09579-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="09579-127">-AliasName</span></span>
<span data-ttu-id="09579-128">Имя псевдонима</span><span class="sxs-lookup"><span data-stu-id="09579-128">Alias Name</span></span>

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

### <span data-ttu-id="09579-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09579-129">-DefaultProfile</span></span>
<span data-ttu-id="09579-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="09579-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09579-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="09579-131">-Eventhub</span></span>
<span data-ttu-id="09579-132">Имя Eventhub</span><span class="sxs-lookup"><span data-stu-id="09579-132">Eventhub Name</span></span>

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

### <span data-ttu-id="09579-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="09579-133">-Name</span></span>
<span data-ttu-id="09579-134">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="09579-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="09579-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="09579-135">-Namespace</span></span>
<span data-ttu-id="09579-136">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="09579-136">Namespace Name</span></span>

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

### <span data-ttu-id="09579-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09579-137">-ResourceGroupName</span></span>
<span data-ttu-id="09579-138">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="09579-138">Resource Group Name</span></span>

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

### <span data-ttu-id="09579-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09579-139">CommonParameters</span></span>
<span data-ttu-id="09579-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09579-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09579-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09579-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09579-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09579-142">INPUTS</span></span>

### <span data-ttu-id="09579-143">System. String</span><span class="sxs-lookup"><span data-stu-id="09579-143">System.String</span></span>

## <span data-ttu-id="09579-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09579-144">OUTPUTS</span></span>

### <span data-ttu-id="09579-145">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="09579-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="09579-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="09579-146">NOTES</span></span>

## <span data-ttu-id="09579-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09579-147">RELATED LINKS</span></span>
