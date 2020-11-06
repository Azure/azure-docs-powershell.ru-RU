---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e4600b44943170256d2c8ef999496d2160e369ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566724"
---
# <span data-ttu-id="6727d-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6727d-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="6727d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6727d-102">SYNOPSIS</span></span>
<span data-ttu-id="6727d-103">Обновляет указанное правило авторизации на концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="6727d-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6727d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6727d-104">SYNTAX</span></span>

### <span data-ttu-id="6727d-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6727d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6727d-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6727d-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6727d-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6727d-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String>
 -InputObject <AuthorizationRuleAttributes> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6727d-108">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="6727d-108">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String> -Rights <String[]> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="6727d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6727d-109">DESCRIPTION</span></span>
<span data-ttu-id="6727d-110">Командлет Set-AzureRmEventHubAuthorizationRule обновляет указанное правило авторизации на данном концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="6727d-110">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="6727d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6727d-111">EXAMPLES</span></span>

### <span data-ttu-id="6727d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6727d-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="6727d-113">Обновляет MyAuthRuleName правила авторизации \` \` , чтобы предоставить доступ к управлению правами для центра событий \` MyEventHubName \` , областью которого является пространство имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="6727d-113">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="6727d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6727d-114">PARAMETERS</span></span>

### <span data-ttu-id="6727d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6727d-115">-ResourceGroupName</span></span>
<span data-ttu-id="6727d-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6727d-116">Resource group name.</span></span>

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

### <span data-ttu-id="6727d-117">-Права</span><span class="sxs-lookup"><span data-stu-id="6727d-117">-Rights</span></span>
<span data-ttu-id="6727d-118">Обязательно, если не указана "AuthruleObj".</span><span class="sxs-lookup"><span data-stu-id="6727d-118">Required if 'AuthruleObj' not specified.</span></span>
<span data-ttu-id="6727d-119">Администратора Например, @ ("прослушать", "Отправить", "Управление")</span><span class="sxs-lookup"><span data-stu-id="6727d-119">Rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6727d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6727d-120">-Confirm</span></span>
<span data-ttu-id="6727d-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6727d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6727d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6727d-122">-WhatIf</span></span>
<span data-ttu-id="6727d-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6727d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6727d-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6727d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6727d-125">-EventHub</span><span class="sxs-lookup"><span data-stu-id="6727d-125">-EventHub</span></span>
<span data-ttu-id="6727d-126">Имя EventHub.</span><span class="sxs-lookup"><span data-stu-id="6727d-126">EventHub Name.</span></span>

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

### <span data-ttu-id="6727d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6727d-127">-InputObject</span></span>
<span data-ttu-id="6727d-128">{{Fill InputObject описание}}</span><span class="sxs-lookup"><span data-stu-id="6727d-128">{{Fill InputObject Description}}</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6727d-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6727d-129">-Name</span></span>
<span data-ttu-id="6727d-130">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="6727d-130">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="6727d-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6727d-131">-Namespace</span></span>
<span data-ttu-id="6727d-132">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="6727d-132">Namespace Name.</span></span>

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

## <span data-ttu-id="6727d-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6727d-133">INPUTS</span></span>

### <span data-ttu-id="6727d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6727d-134">System.String</span></span>

## <span data-ttu-id="6727d-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6727d-135">OUTPUTS</span></span>

### <span data-ttu-id="6727d-136">Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="6727d-136">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="6727d-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="6727d-137">NOTES</span></span>

## <span data-ttu-id="6727d-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6727d-138">RELATED LINKS</span></span>

