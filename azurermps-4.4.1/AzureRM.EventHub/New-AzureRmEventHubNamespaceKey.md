---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 1a96916d0e3bed080e078226a14304b6ee6cecc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569472"
---
# <span data-ttu-id="67667-101">New-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="67667-101">New-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="67667-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67667-102">SYNOPSIS</span></span>
<span data-ttu-id="67667-103">Создает новый первичный или вторичный ключ для правила авторизации на заданном пространстве имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="67667-103">Creates a new primary or secondary key for the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67667-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67667-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceKey [-ResourceGroup] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="67667-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67667-105">DESCRIPTION</span></span>
<span data-ttu-id="67667-106">Командлет New-AzureRmEventHubNamespaceKey повторно создает первичный или вторичный ключ для заданного правила авторизации в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="67667-106">The New-AzureRmEventHubNamespaceKey cmdlet regenerates the primary or secondary key for the for the given authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="67667-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67667-107">EXAMPLES</span></span>

### <span data-ttu-id="67667-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="67667-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNameSpaceKey -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName  -AuthorizationRuleName MyAuthRuleName -RegenerateKeys PrimaryKey
```

<span data-ttu-id="67667-109">Повторно создает первичный ключ для правила авторизации \` MyAuthRuleName \` в пространстве имен MyNamespaceName "концентраторы событий" \` \` с группой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="67667-109">Regenerates the primary key for the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="67667-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67667-110">PARAMETERS</span></span>

### <span data-ttu-id="67667-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="67667-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="67667-112">Имя правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="67667-112">Authorization rule name.</span></span>

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

### <span data-ttu-id="67667-113">-+ +</span><span class="sxs-lookup"><span data-stu-id="67667-113">-NamespaceName</span></span>
<span data-ttu-id="67667-114">Имя пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="67667-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="67667-115">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="67667-115">-RegenerateKeys</span></span>
<span data-ttu-id="67667-116">Ключ для повторного создания: \` PrimaryKey \` или \` SecondaryKey \` .</span><span class="sxs-lookup"><span data-stu-id="67667-116">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67667-117">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="67667-117">-ResourceGroup</span></span>
<span data-ttu-id="67667-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67667-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="67667-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67667-119">-Confirm</span></span>
<span data-ttu-id="67667-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="67667-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67667-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67667-121">-WhatIf</span></span>
<span data-ttu-id="67667-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="67667-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67667-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="67667-123">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="67667-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67667-124">INPUTS</span></span>

### <span data-ttu-id="67667-125">System. String</span><span class="sxs-lookup"><span data-stu-id="67667-125">System.String</span></span>

## <span data-ttu-id="67667-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67667-126">OUTPUTS</span></span>

### <span data-ttu-id="67667-127">Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="67667-127">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="67667-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="67667-128">NOTES</span></span>

## <span data-ttu-id="67667-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67667-129">RELATED LINKS</span></span>

