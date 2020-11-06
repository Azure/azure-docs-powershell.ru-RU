---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 52bf68f1105ea6aa6ec0a78fac1a75defa1d865a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570412"
---
# <span data-ttu-id="a4fc0-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a4fc0-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="a4fc0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="a4fc0-103">Обновляет правило авторизации для указанного пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="a4fc0-103">Updates the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4fc0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4fc0-104">SYNTAX</span></span>

```
Set-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthRuleObj] <AuthorizationRuleAttributes> [[-AuthorizationRuleName] <String>] [-Rights <String[]>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a4fc0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4fc0-105">DESCRIPTION</span></span>
<span data-ttu-id="a4fc0-106">Командлет Set-AzureRmEventHubNamespaceAuthorizationRule обновляет правило авторизации для указанного пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="a4fc0-106">The Set-AzureRmEventHubNamespaceAuthorizationRule cmdlet updates the authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="a4fc0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4fc0-107">EXAMPLES</span></span>

### <span data-ttu-id="a4fc0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a4fc0-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="a4fc0-109">Обновление правила авторизации \` MyAuthRuleName \` для предоставления прав на управление.</span><span class="sxs-lookup"><span data-stu-id="a4fc0-109">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights.</span></span>

## <span data-ttu-id="a4fc0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4fc0-110">PARAMETERS</span></span>

### <span data-ttu-id="a4fc0-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="a4fc0-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="a4fc0-112">Имя правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="a4fc0-112">The authorization rule name.</span></span>
<span data-ttu-id="a4fc0-113">Обязательно, если не указан аргумент-AuthruleObj.</span><span class="sxs-lookup"><span data-stu-id="a4fc0-113">Required if -AuthruleObj is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4fc0-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="a4fc0-114">-AuthRuleObj</span></span>
<span data-ttu-id="a4fc0-115">Объект правила авторизации пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="a4fc0-115">The Event Hubs namespace authorization rule object.</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4fc0-116">-+ +</span><span class="sxs-lookup"><span data-stu-id="a4fc0-116">-NamespaceName</span></span>
<span data-ttu-id="a4fc0-117">Имя пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="a4fc0-117">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="a4fc0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4fc0-118">-ResourceGroupName</span></span>
<span data-ttu-id="a4fc0-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4fc0-119">Resource group name.</span></span>

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

### <span data-ttu-id="a4fc0-120">-Права</span><span class="sxs-lookup"><span data-stu-id="a4fc0-120">-Rights</span></span>
<span data-ttu-id="a4fc0-121">Обязательно, если не указан аргумент-AuthruleObj.</span><span class="sxs-lookup"><span data-stu-id="a4fc0-121">Required if -AuthruleObj is not specified.</span></span>
<span data-ttu-id="a4fc0-122">Администратора Например, @ ("прослушать", "Отправить", "Управление")</span><span class="sxs-lookup"><span data-stu-id="a4fc0-122">Rights; for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4fc0-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4fc0-123">-Confirm</span></span>
<span data-ttu-id="a4fc0-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4fc0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4fc0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4fc0-125">-WhatIf</span></span>
<span data-ttu-id="a4fc0-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4fc0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4fc0-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4fc0-127">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="a4fc0-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4fc0-128">INPUTS</span></span>

### <span data-ttu-id="a4fc0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a4fc0-129">System.String</span></span>

## <span data-ttu-id="a4fc0-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4fc0-130">OUTPUTS</span></span>

### <span data-ttu-id="a4fc0-131">Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a4fc0-131">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a4fc0-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4fc0-132">NOTES</span></span>

## <span data-ttu-id="a4fc0-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4fc0-133">RELATED LINKS</span></span>

