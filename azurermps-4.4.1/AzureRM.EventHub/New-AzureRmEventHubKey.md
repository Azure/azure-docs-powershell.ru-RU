---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3bd06ea2534298ba81cd546e8fa6e8de02fa5928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569475"
---
# <span data-ttu-id="86307-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="86307-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="86307-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86307-102">SYNOPSIS</span></span>
<span data-ttu-id="86307-103">Создает новый первичный или вторичный ключ для указанного правила авторизации концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="86307-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86307-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86307-104">SYNTAX</span></span>

### <span data-ttu-id="86307-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="86307-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> -Namespace <String> -Name <String> -RegenerateKey <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="86307-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="86307-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> [-Namespace <String>] -EventHub <String> -Name <String>
 -RegenerateKey <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="86307-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86307-107">DESCRIPTION</span></span>
<span data-ttu-id="86307-108">Командлет New-AzureRmEventHubKey повторно создает первичный или дополнительный ключ SAS для указанного правила авторизации концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="86307-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="86307-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86307-109">EXAMPLES</span></span>

### <span data-ttu-id="86307-110">Пример 1,1</span><span class="sxs-lookup"><span data-stu-id="86307-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="86307-111">Повторно создает первичный ключ для правила авторизации \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="86307-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="86307-112">Пример 1,2</span><span class="sxs-lookup"><span data-stu-id="86307-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="86307-113">Повторно создает первичный ключ для правила авторизации \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="86307-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="86307-114">Пример 2,1</span><span class="sxs-lookup"><span data-stu-id="86307-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="86307-115">Пример 2,2</span><span class="sxs-lookup"><span data-stu-id="86307-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="86307-116">Повторно создает вторичный ключ для правила авторизации \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="86307-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="86307-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86307-117">PARAMETERS</span></span>

### <span data-ttu-id="86307-118">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="86307-118">-RegenerateKey</span></span>
<span data-ttu-id="86307-119">Ключ для повторного создания: \` PrimaryKey \` или \` SecondaryKey \` .</span><span class="sxs-lookup"><span data-stu-id="86307-119">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86307-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86307-120">-Confirm</span></span>
<span data-ttu-id="86307-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="86307-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86307-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86307-122">-WhatIf</span></span>
<span data-ttu-id="86307-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="86307-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86307-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="86307-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86307-125">-EventHub</span><span class="sxs-lookup"><span data-stu-id="86307-125">-EventHub</span></span>
<span data-ttu-id="86307-126">Имя EventHub.</span><span class="sxs-lookup"><span data-stu-id="86307-126">EventHub Name.</span></span>

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

### <span data-ttu-id="86307-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="86307-127">-Name</span></span>
<span data-ttu-id="86307-128">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="86307-128">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86307-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="86307-129">-Namespace</span></span>
<span data-ttu-id="86307-130">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="86307-130">Namespace Name.</span></span>

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

### <span data-ttu-id="86307-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86307-131">-ResourceGroupName</span></span>
<span data-ttu-id="86307-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86307-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="86307-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86307-133">INPUTS</span></span>

### <span data-ttu-id="86307-134">System. String</span><span class="sxs-lookup"><span data-stu-id="86307-134">System.String</span></span>

## <span data-ttu-id="86307-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86307-135">OUTPUTS</span></span>

### <span data-ttu-id="86307-136">Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="86307-136">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="86307-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="86307-137">NOTES</span></span>

## <span data-ttu-id="86307-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86307-138">RELATED LINKS</span></span>

