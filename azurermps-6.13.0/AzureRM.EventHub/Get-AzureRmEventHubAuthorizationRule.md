---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 70b5ac9eb40bf6c50ebb6d09849e8185c23927e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563040"
---
# <span data-ttu-id="12024-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="12024-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="12024-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12024-102">SYNOPSIS</span></span>
<span data-ttu-id="12024-103">Получает сведения о правиле авторизации или получает список правил авторизации.</span><span class="sxs-lookup"><span data-stu-id="12024-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12024-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12024-104">SYNTAX</span></span>

### <span data-ttu-id="12024-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="12024-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12024-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="12024-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12024-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="12024-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12024-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12024-108">DESCRIPTION</span></span>
<span data-ttu-id="12024-109">Командлет Get-AzureRmEventHubAuthorizationRule получает либо сведения о правиле авторизации, либо список всех правил авторизации для определенного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="12024-109">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="12024-110">Если указано имя правила авторизации, возвращается информация об этом отдельном правиле авторизации.</span><span class="sxs-lookup"><span data-stu-id="12024-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="12024-111">Если имя правила авторизации не задано, возвращается список всех правил авторизации для указанного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="12024-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="12024-112">Если задано имя псевдонима (аварийное восстановление), возвращается информация о правиле авторизации пространства имен для указанного псевдонима.</span><span class="sxs-lookup"><span data-stu-id="12024-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="12024-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12024-113">EXAMPLES</span></span>

### <span data-ttu-id="12024-114">Пример 1,0-AuthorizationRule для пространства имен</span><span class="sxs-lookup"><span data-stu-id="12024-114">Example 1.0 - AuthorizationRule for namespace</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="12024-115">Возвращает правило авторизации \` , MyAuthRuleName \` в пространстве имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="12024-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="12024-116">Пример 1,1-AuthorizationRules для пространства имен</span><span class="sxs-lookup"><span data-stu-id="12024-116">Example 1.1 - AuthorizationRules for namespace</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="12024-117">Получает список всех правил авторизации в пространстве имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="12024-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="12024-118">Пример 2,0-AuthorizationRule для EventHub</span><span class="sxs-lookup"><span data-stu-id="12024-118">Example 2.0 - AuthorizationRule for EventHub</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="12024-119">Получает правило авторизации \` MyAuthRuleName \` в MyEventHubName концентратора событий \` \` , область которого ограничена пространством имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="12024-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="12024-120">Пример 2,1-AuthorizationRules для EventHub</span><span class="sxs-lookup"><span data-stu-id="12024-120">Example 2.1 - AuthorizationRules for EventHub</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="12024-121">Получает правила авторизации списка в центре событий \` MyEventHubName \` , областью действия которых является пространство имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="12024-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="12024-122">Пример 3,0-AuthorizationRule для псевдонима (конфигурация с геовосстановлением)</span><span class="sxs-lookup"><span data-stu-id="12024-122">Example 3.0 - AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="12024-123">Возвращает правило авторизации \` , MyAuthRuleName \` в пространстве имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="12024-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="12024-124">Пример 3,1-AuthorizationRules для псевдонима (конфигурация с геовосстановлением)</span><span class="sxs-lookup"><span data-stu-id="12024-124">Example 3.1 -AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="12024-125">Получает список всех MyAuthRuleName правил авторизации \` \` в пространстве имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="12024-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="12024-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12024-126">PARAMETERS</span></span>

### <span data-ttu-id="12024-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="12024-127">-AliasName</span></span>
<span data-ttu-id="12024-128">Имя псевдонима</span><span class="sxs-lookup"><span data-stu-id="12024-128">Alias Name</span></span>

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

### <span data-ttu-id="12024-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12024-129">-DefaultProfile</span></span>
<span data-ttu-id="12024-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12024-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12024-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="12024-131">-Eventhub</span></span>
<span data-ttu-id="12024-132">Имя Eventhub</span><span class="sxs-lookup"><span data-stu-id="12024-132">Eventhub Name</span></span>

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

### <span data-ttu-id="12024-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="12024-133">-Name</span></span>
<span data-ttu-id="12024-134">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="12024-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="12024-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="12024-135">-Namespace</span></span>
<span data-ttu-id="12024-136">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="12024-136">Namespace Name</span></span>

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

### <span data-ttu-id="12024-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12024-137">-ResourceGroupName</span></span>
<span data-ttu-id="12024-138">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="12024-138">Resource Group Name</span></span>

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

### <span data-ttu-id="12024-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12024-139">CommonParameters</span></span>
<span data-ttu-id="12024-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12024-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12024-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12024-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12024-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12024-142">INPUTS</span></span>

### <span data-ttu-id="12024-143">System. String</span><span class="sxs-lookup"><span data-stu-id="12024-143">System.String</span></span>

## <span data-ttu-id="12024-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12024-144">OUTPUTS</span></span>

### <span data-ttu-id="12024-145">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="12024-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="12024-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="12024-146">NOTES</span></span>

## <span data-ttu-id="12024-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12024-147">RELATED LINKS</span></span>
