---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734856"
---
# <span data-ttu-id="08e67-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="08e67-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="08e67-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="08e67-102">SYNOPSIS</span></span>
<span data-ttu-id="08e67-103">Получает сведения о правиле авторизации пространства имен Eventubs или получает список правил авторизации.</span><span class="sxs-lookup"><span data-stu-id="08e67-103">Gets the details of an Eventubs namespace authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08e67-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="08e67-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## <span data-ttu-id="08e67-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08e67-105">DESCRIPTION</span></span>
<span data-ttu-id="08e67-106">Командлет Get-AzureRmEventHubNamespaceAuthorizationRule получает либо сведения о указанном правиле авторизации пространства имен концентраторов событий, либо список правил авторизации пространства имен.</span><span class="sxs-lookup"><span data-stu-id="08e67-106">The Get-AzureRmEventHubNamespaceAuthorizationRule cmdlet gets either the details of a specified Event Hubs namespace authorization rule, or a list of namespace authorization rules.</span></span>
<span data-ttu-id="08e67-107">Если указано имя правила авторизации, возвращается информация об одном правиле авторизации.</span><span class="sxs-lookup"><span data-stu-id="08e67-107">If the authorization rule name is provided, the details of a single authorization rule is returned.</span></span>
<span data-ttu-id="08e67-108">Если имя правила авторизации не задано, возвращается список всех правил авторизации в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="08e67-108">If an authorization rule name is not provided, a list of all authorization rules in the namespace is returned.</span></span>

## <span data-ttu-id="08e67-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="08e67-109">EXAMPLES</span></span>

### <span data-ttu-id="08e67-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="08e67-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="08e67-111">Возвращает правило авторизации \` MyAuthRuleName \` в пространстве имен MyNamespaceName "концентраторы событий" \` \` с группой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="08e67-111">Returns the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="08e67-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="08e67-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

<span data-ttu-id="08e67-113">Возвращает правило авторизации по умолчанию \` RootManageSharedAccessKey \` в пространстве имен MyNamespaceName "концентраторы событий" \` \` с группой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="08e67-113">Returns the default authorization rule \`RootManageSharedAccessKey\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="08e67-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="08e67-114">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="08e67-115">Возвращает все правила авторизации в MyNamespaceName пространства имен "концентраторы событий" \` \` с группой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="08e67-115">Returns all authorization rules in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="08e67-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="08e67-116">PARAMETERS</span></span>

### <span data-ttu-id="08e67-117">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="08e67-117">-AuthorizationRuleName</span></span>
<span data-ttu-id="08e67-118">Имя правила авторизации пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="08e67-118">The Event Hubs namespace authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08e67-119">-+ +</span><span class="sxs-lookup"><span data-stu-id="08e67-119">-NamespaceName</span></span>
<span data-ttu-id="08e67-120">Имя пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="08e67-120">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08e67-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08e67-121">-ResourceGroupName</span></span>
<span data-ttu-id="08e67-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="08e67-122">Resource group name.</span></span>

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

## <span data-ttu-id="08e67-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="08e67-123">INPUTS</span></span>

### <span data-ttu-id="08e67-124">System. String</span><span class="sxs-lookup"><span data-stu-id="08e67-124">System.String</span></span>

## <span data-ttu-id="08e67-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="08e67-125">OUTPUTS</span></span>

### <span data-ttu-id="08e67-126">System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. eventhub, версия = 0.0.1.0, культура = нейтраль, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="08e67-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="08e67-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="08e67-127">NOTES</span></span>

## <span data-ttu-id="08e67-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08e67-128">RELATED LINKS</span></span>

