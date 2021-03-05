---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 496806b6d5ab6b7d6e1c788b7b42424b7e97a8c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992757"
---
# <span data-ttu-id="f1795-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f1795-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="f1795-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1795-102">SYNOPSIS</span></span>
<span data-ttu-id="f1795-103">Удаляет указанное правило авторизации в Центре событий.</span><span class="sxs-lookup"><span data-stu-id="f1795-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="f1795-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f1795-104">SYNTAX</span></span>

### <span data-ttu-id="f1795-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f1795-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1795-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1795-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1795-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1795-107">DESCRIPTION</span></span>
<span data-ttu-id="f1795-108">Этот Remove-AzEventHubAuthorizationRule удаляет указанное правило авторизации из данного центра событий.</span><span class="sxs-lookup"><span data-stu-id="f1795-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="f1795-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f1795-109">EXAMPLES</span></span>

### <span data-ttu-id="f1795-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f1795-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="f1795-111">Удаляет правило авторизации \` MyAuthRuleName \` из пространства имен \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="f1795-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="f1795-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f1795-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="f1795-113">Удаляет правило авторизации \` MyAuthRuleName из Центра событий \` \` MyEventHubName. \`</span><span class="sxs-lookup"><span data-stu-id="f1795-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="f1795-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1795-114">PARAMETERS</span></span>

### <span data-ttu-id="f1795-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1795-115">-DefaultProfile</span></span>
<span data-ttu-id="f1795-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1795-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1795-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f1795-117">-EventHub</span></span>
<span data-ttu-id="f1795-118">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="f1795-118">EventHub Name</span></span>

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

### <span data-ttu-id="f1795-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f1795-119">-Force</span></span>
<span data-ttu-id="f1795-120">Не запросить подтверждение</span><span class="sxs-lookup"><span data-stu-id="f1795-120">Do not ask for confirmation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1795-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f1795-121">-Name</span></span>
<span data-ttu-id="f1795-122">Имяrule authorizationRule</span><span class="sxs-lookup"><span data-stu-id="f1795-122">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1795-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f1795-123">-Namespace</span></span>
<span data-ttu-id="f1795-124">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="f1795-124">Namespace Name</span></span>

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

### <span data-ttu-id="f1795-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1795-125">-PassThru</span></span>
<span data-ttu-id="f1795-126">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f1795-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f1795-127">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f1795-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1795-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1795-128">-ResourceGroupName</span></span>
<span data-ttu-id="f1795-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f1795-129">Resource Group Name</span></span>

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

### <span data-ttu-id="f1795-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1795-130">-Confirm</span></span>
<span data-ttu-id="f1795-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1795-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1795-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1795-132">-WhatIf</span></span>
<span data-ttu-id="f1795-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1795-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1795-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f1795-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1795-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1795-135">CommonParameters</span></span>
<span data-ttu-id="f1795-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1795-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1795-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1795-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1795-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1795-138">INPUTS</span></span>

### <span data-ttu-id="f1795-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f1795-139">System.String</span></span>

## <span data-ttu-id="f1795-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f1795-140">OUTPUTS</span></span>

### <span data-ttu-id="f1795-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f1795-141">System.Boolean</span></span>

## <span data-ttu-id="f1795-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f1795-142">NOTES</span></span>

## <span data-ttu-id="f1795-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1795-143">RELATED LINKS</span></span>
