---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 6940e12f813cbc4292f02ab98f0b35774da67025
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248699"
---
# <span data-ttu-id="8fff5-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8fff5-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="8fff5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8fff5-102">SYNOPSIS</span></span>
<span data-ttu-id="8fff5-103">Получает сведения о правиле авторизации или получает список правил авторизации.</span><span class="sxs-lookup"><span data-stu-id="8fff5-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="8fff5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8fff5-104">SYNTAX</span></span>

### <span data-ttu-id="8fff5-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8fff5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fff5-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8fff5-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fff5-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="8fff5-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fff5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fff5-108">DESCRIPTION</span></span>
<span data-ttu-id="8fff5-109">Командлет Get-AzEventHubAuthorizationRule получает либо сведения о правиле авторизации, либо список всех правил авторизации для определенного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="8fff5-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="8fff5-110">Если указано имя правила авторизации, возвращается информация об этом отдельном правиле авторизации.</span><span class="sxs-lookup"><span data-stu-id="8fff5-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="8fff5-111">Если имя правила авторизации не задано, возвращается список всех правил авторизации для указанного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="8fff5-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="8fff5-112">Если задано имя псевдонима (аварийное восстановление), возвращается информация о правиле авторизации пространства имен для указанного псевдонима.</span><span class="sxs-lookup"><span data-stu-id="8fff5-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="8fff5-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8fff5-113">EXAMPLES</span></span>

### <span data-ttu-id="8fff5-114">Пример 1: AuthorizationRule для пространства имен</span><span class="sxs-lookup"><span data-stu-id="8fff5-114">Example 1: AuthorizationRule for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="8fff5-115">Возвращает правило авторизации \` , MyAuthRuleName \` в пространстве имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="8fff5-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="8fff5-116">Пример 2: AuthorizationRules для пространства имен</span><span class="sxs-lookup"><span data-stu-id="8fff5-116">Example 2: AuthorizationRules for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="8fff5-117">Получает список всех правил авторизации в пространстве имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="8fff5-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="8fff5-118">Пример 3: AuthorizationRule для EventHub</span><span class="sxs-lookup"><span data-stu-id="8fff5-118">Example 3: AuthorizationRule for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="8fff5-119">Получает правило авторизации \` MyAuthRuleName \` в MyEventHubName концентратора событий \` \` , область которого ограничена пространством имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="8fff5-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="8fff5-120">Пример 4: AuthorizationRules для EventHub</span><span class="sxs-lookup"><span data-stu-id="8fff5-120">Example 4: AuthorizationRules for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="8fff5-121">Получает правила авторизации списка в центре событий \` MyEventHubName \` , областью действия которых является пространство имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="8fff5-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="8fff5-122">Пример 5: AuthorizationRule для псевдонима (конфигурация с геовосстановлением)</span><span class="sxs-lookup"><span data-stu-id="8fff5-122">Example 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="8fff5-123">Возвращает правило авторизации \` , MyAuthRuleName \` в пространстве имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="8fff5-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="8fff5-124">Пример 6: AuthorizationRules для псевдонима (конфигурация с геовосстановлением)</span><span class="sxs-lookup"><span data-stu-id="8fff5-124">Example 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="8fff5-125">Получает список всех MyAuthRuleName правил авторизации \` \` в пространстве имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="8fff5-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="8fff5-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8fff5-126">PARAMETERS</span></span>

### <span data-ttu-id="8fff5-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="8fff5-127">-AliasName</span></span>
<span data-ttu-id="8fff5-128">Имя псевдонима</span><span class="sxs-lookup"><span data-stu-id="8fff5-128">Alias Name</span></span>

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

### <span data-ttu-id="8fff5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fff5-129">-DefaultProfile</span></span>
<span data-ttu-id="8fff5-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8fff5-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fff5-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="8fff5-131">-Eventhub</span></span>
<span data-ttu-id="8fff5-132">Имя Eventhub</span><span class="sxs-lookup"><span data-stu-id="8fff5-132">Eventhub Name</span></span>

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

### <span data-ttu-id="8fff5-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8fff5-133">-Name</span></span>
<span data-ttu-id="8fff5-134">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8fff5-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="8fff5-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8fff5-135">-Namespace</span></span>
<span data-ttu-id="8fff5-136">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="8fff5-136">Namespace Name</span></span>

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

### <span data-ttu-id="8fff5-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fff5-137">-ResourceGroupName</span></span>
<span data-ttu-id="8fff5-138">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8fff5-138">Resource Group Name</span></span>

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

### <span data-ttu-id="8fff5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fff5-139">CommonParameters</span></span>
<span data-ttu-id="8fff5-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8fff5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fff5-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fff5-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fff5-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8fff5-142">INPUTS</span></span>

### <span data-ttu-id="8fff5-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8fff5-143">System.String</span></span>

## <span data-ttu-id="8fff5-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fff5-144">OUTPUTS</span></span>

### <span data-ttu-id="8fff5-145">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8fff5-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="8fff5-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="8fff5-146">NOTES</span></span>

## <span data-ttu-id="8fff5-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8fff5-147">RELATED LINKS</span></span>