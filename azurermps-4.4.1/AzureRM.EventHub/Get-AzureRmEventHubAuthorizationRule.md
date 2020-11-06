---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 69bff610bdcb7795ed582fb6fe882a9e7cc27c8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569500"
---
# <span data-ttu-id="8f561-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8f561-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="8f561-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f561-102">SYNOPSIS</span></span>
<span data-ttu-id="8f561-103">Получает сведения о правиле авторизации или получает список правил авторизации.</span><span class="sxs-lookup"><span data-stu-id="8f561-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f561-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f561-104">SYNTAX</span></span>

### <span data-ttu-id="8f561-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8f561-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

### <span data-ttu-id="8f561-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8f561-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -Eventhub <String>
 [-Name <String>]
```

## <span data-ttu-id="8f561-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f561-107">DESCRIPTION</span></span>
<span data-ttu-id="8f561-108">Командлет Get-AzureRmEventHubAuthorizationRule получает либо сведения о правиле авторизации, либо список всех правил авторизации для определенного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="8f561-108">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="8f561-109">Если указано имя правила авторизации, возвращается информация об этом отдельном правиле авторизации.</span><span class="sxs-lookup"><span data-stu-id="8f561-109">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="8f561-110">Если имя правила авторизации не задано, возвращается список всех правил авторизации для указанного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="8f561-110">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>

## <span data-ttu-id="8f561-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f561-111">EXAMPLES</span></span>

### <span data-ttu-id="8f561-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8f561-112">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="8f561-113">Получает правило авторизации \` MyAuthRuleName \` в MyEventHubName концентратора событий \` \` , область которого ограничена пространством имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="8f561-113">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="8f561-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8f561-114">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="8f561-115">Получает список всех правил авторизации в концентраторе событий \` MyEventHubName \` , область которого ограничена пространством имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="8f561-115">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="8f561-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f561-116">PARAMETERS</span></span>

### <span data-ttu-id="8f561-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f561-117">-ResourceGroupName</span></span>
<span data-ttu-id="8f561-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f561-118">Resource group name.</span></span>

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

### <span data-ttu-id="8f561-119">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="8f561-119">-Eventhub</span></span>
<span data-ttu-id="8f561-120">Имя Eventhub.</span><span class="sxs-lookup"><span data-stu-id="8f561-120">Eventhub Name.</span></span>

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

### <span data-ttu-id="8f561-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f561-121">-Name</span></span>
<span data-ttu-id="8f561-122">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="8f561-122">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f561-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8f561-123">-Namespace</span></span>
<span data-ttu-id="8f561-124">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="8f561-124">Namespace Name.</span></span>

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

## <span data-ttu-id="8f561-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f561-125">INPUTS</span></span>

### <span data-ttu-id="8f561-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8f561-126">System.String</span></span>

## <span data-ttu-id="8f561-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f561-127">OUTPUTS</span></span>

### <span data-ttu-id="8f561-128">System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. eventhub, версия = 0.0.1.0, культура = нейтраль, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="8f561-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8f561-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f561-129">NOTES</span></span>

## <span data-ttu-id="8f561-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f561-130">RELATED LINKS</span></span>

