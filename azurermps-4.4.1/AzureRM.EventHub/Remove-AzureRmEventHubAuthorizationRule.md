---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 439d4ea871d70fa830bb5a0f327cbc0f75d137df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569467"
---
# <span data-ttu-id="6c39d-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6c39d-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="6c39d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6c39d-102">SYNOPSIS</span></span>
<span data-ttu-id="6c39d-103">Удаляет указанное правило авторизации центра событий.</span><span class="sxs-lookup"><span data-stu-id="6c39d-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c39d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6c39d-104">SYNTAX</span></span>

### <span data-ttu-id="6c39d-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6c39d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6c39d-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6c39d-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="6c39d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c39d-107">DESCRIPTION</span></span>
<span data-ttu-id="6c39d-108">Командлет Remove-AzureRmEventHubAuthorizationRule удаляет и удаляет указанное правило авторизации из заданного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="6c39d-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="6c39d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6c39d-109">EXAMPLES</span></span>

### <span data-ttu-id="6c39d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6c39d-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

### <span data-ttu-id="6c39d-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6c39d-111">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="6c39d-112">Удаляет правило авторизации \` MyAuthRuleName \` из центра событий \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="6c39d-112">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="6c39d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6c39d-113">PARAMETERS</span></span>

### <span data-ttu-id="6c39d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c39d-114">-ResourceGroupName</span></span>
<span data-ttu-id="6c39d-115">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c39d-115">Resource group name.</span></span>

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

### <span data-ttu-id="6c39d-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c39d-116">-Confirm</span></span>
<span data-ttu-id="6c39d-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6c39d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c39d-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c39d-118">-WhatIf</span></span>
<span data-ttu-id="6c39d-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6c39d-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c39d-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6c39d-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c39d-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="6c39d-121">-EventHub</span></span>
<span data-ttu-id="6c39d-122">Имя EventHub.</span><span class="sxs-lookup"><span data-stu-id="6c39d-122">EventHub Name.</span></span>

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

### <span data-ttu-id="6c39d-123">-Force</span><span class="sxs-lookup"><span data-stu-id="6c39d-123">-Force</span></span>
<span data-ttu-id="6c39d-124">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6c39d-124">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c39d-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6c39d-125">-Name</span></span>
<span data-ttu-id="6c39d-126">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="6c39d-126">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="6c39d-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6c39d-127">-Namespace</span></span>
<span data-ttu-id="6c39d-128">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="6c39d-128">Namespace Name.</span></span>

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

### <span data-ttu-id="6c39d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c39d-129">-PassThru</span></span>
<span data-ttu-id="6c39d-130">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="6c39d-130">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="6c39d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6c39d-131">INPUTS</span></span>

### <span data-ttu-id="6c39d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6c39d-132">System.String</span></span>

## <span data-ttu-id="6c39d-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c39d-133">OUTPUTS</span></span>

### <span data-ttu-id="6c39d-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c39d-134">System.Boolean</span></span>

## <span data-ttu-id="6c39d-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="6c39d-135">NOTES</span></span>

## <span data-ttu-id="6c39d-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c39d-136">RELATED LINKS</span></span>

