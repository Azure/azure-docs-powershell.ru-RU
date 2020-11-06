---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: dc384ca6056ef13d5517241d550bacddf2e7d0d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569476"
---
# <span data-ttu-id="a2ce4-101">New-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a2ce4-101">New-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="a2ce4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ce4-103">Создает новое правило авторизации для указанного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="a2ce4-103">Creates a new authorization rule on the specified namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2ce4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2ce4-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-Rights] <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a2ce4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2ce4-105">DESCRIPTION</span></span>
<span data-ttu-id="a2ce4-106">Командлет New-AzureRmEventHubNamespaceAuthorizationRule создает новое правило авторизации для указанного пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="a2ce4-106">The New-AzureRmEventHubNamespaceAuthorizationRule cmdlet creates a new authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="a2ce4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2ce4-107">EXAMPLES</span></span>

### <span data-ttu-id="a2ce4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2ce4-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="a2ce4-109">Создание правила авторизации \` MyAuthRuleName \` с правами прослушивания и отправки для пространства имен MyNamespaceNameных концентраторов событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a2ce4-109">Creates the authorization rule \`MyAuthRuleName\` with Listen and Send rights, for Event Hubs namespace \`MyNamespaceName\`, in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="a2ce4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2ce4-110">PARAMETERS</span></span>

### <span data-ttu-id="a2ce4-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="a2ce4-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="a2ce4-112">Имя правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="a2ce4-112">Authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2ce4-113">-+ +</span><span class="sxs-lookup"><span data-stu-id="a2ce4-113">-NamespaceName</span></span>
<span data-ttu-id="a2ce4-114">Имя пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="a2ce4-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="a2ce4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2ce4-115">-ResourceGroupName</span></span>
<span data-ttu-id="a2ce4-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2ce4-116">Resource group name.</span></span>

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

### <span data-ttu-id="a2ce4-117">-Права</span><span class="sxs-lookup"><span data-stu-id="a2ce4-117">-Rights</span></span>
<span data-ttu-id="a2ce4-118">Права; например, @ ("прослушать", "Отправить", "Управление")</span><span class="sxs-lookup"><span data-stu-id="a2ce4-118">Rights;for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2ce4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2ce4-119">-Confirm</span></span>
<span data-ttu-id="a2ce4-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a2ce4-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ce4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2ce4-121">-WhatIf</span></span>
<span data-ttu-id="a2ce4-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a2ce4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2ce4-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a2ce4-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="a2ce4-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2ce4-124">INPUTS</span></span>

### <span data-ttu-id="a2ce4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a2ce4-125">System.String</span></span>

## <span data-ttu-id="a2ce4-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2ce4-126">OUTPUTS</span></span>

### <span data-ttu-id="a2ce4-127">Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a2ce4-127">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a2ce4-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2ce4-128">NOTES</span></span>

## <span data-ttu-id="a2ce4-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2ce4-129">RELATED LINKS</span></span>

