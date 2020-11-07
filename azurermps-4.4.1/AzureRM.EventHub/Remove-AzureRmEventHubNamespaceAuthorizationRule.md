---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a980edd1833b37b358f86d2e3ccb6a9efc8d836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733120"
---
# <span data-ttu-id="e9fa0-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e9fa0-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="e9fa0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e9fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="e9fa0-103">Удаляет указанное правило авторизации на заданное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="e9fa0-103">Deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9fa0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e9fa0-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e9fa0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9fa0-105">DESCRIPTION</span></span>
<span data-ttu-id="e9fa0-106">Командлет Remove-AzureRmEventHubNamespaceAuthorizationRule удаляет и удаляет указанное правило авторизации на заданное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="e9fa0-106">The Remove-AzureRmEventHubNamespaceAuthorizationRule cmdlet removes and deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

## <span data-ttu-id="e9fa0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e9fa0-107">EXAMPLES</span></span>

### <span data-ttu-id="e9fa0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e9fa0-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="e9fa0-109">Удаляет правило авторизации \` MyAuthRuleName \` из пространства имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="e9fa0-109">Removes the authorization rule \`MyAuthRuleName\` from the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="e9fa0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e9fa0-110">PARAMETERS</span></span>

### <span data-ttu-id="e9fa0-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="e9fa0-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="e9fa0-112">Имя правила авторизации пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="e9fa0-112">The Event Hubs namespace authorization rule name.</span></span>

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

### <span data-ttu-id="e9fa0-113">-+ +</span><span class="sxs-lookup"><span data-stu-id="e9fa0-113">-NamespaceName</span></span>
<span data-ttu-id="e9fa0-114">Имя пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="e9fa0-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="e9fa0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9fa0-115">-ResourceGroupName</span></span>
<span data-ttu-id="e9fa0-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e9fa0-116">Resource group name.</span></span>

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

### <span data-ttu-id="e9fa0-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9fa0-117">-Confirm</span></span>
<span data-ttu-id="e9fa0-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e9fa0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9fa0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9fa0-119">-WhatIf</span></span>
<span data-ttu-id="e9fa0-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e9fa0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9fa0-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e9fa0-121">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="e9fa0-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e9fa0-122">INPUTS</span></span>

### <span data-ttu-id="e9fa0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e9fa0-123">System.String</span></span>

## <span data-ttu-id="e9fa0-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9fa0-124">OUTPUTS</span></span>

### <span data-ttu-id="e9fa0-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e9fa0-125">System.Boolean</span></span>

## <span data-ttu-id="e9fa0-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="e9fa0-126">NOTES</span></span>

## <span data-ttu-id="e9fa0-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9fa0-127">RELATED LINKS</span></span>

