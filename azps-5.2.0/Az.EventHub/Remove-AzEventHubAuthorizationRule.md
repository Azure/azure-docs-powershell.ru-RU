---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 91c38686d8621f3bba521d738cc125e4b8473188
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406556"
---
# <span data-ttu-id="eb5c5-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="eb5c5-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="eb5c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb5c5-102">SYNOPSIS</span></span>
<span data-ttu-id="eb5c5-103">Удаляет указанное правило авторизации в Центре событий.</span><span class="sxs-lookup"><span data-stu-id="eb5c5-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="eb5c5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eb5c5-104">SYNTAX</span></span>

### <span data-ttu-id="eb5c5-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eb5c5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb5c5-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb5c5-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb5c5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb5c5-107">DESCRIPTION</span></span>
<span data-ttu-id="eb5c5-108">Этот Remove-AzEventHubAuthorizationRule удаляет указанное правило авторизации из данного центра событий.</span><span class="sxs-lookup"><span data-stu-id="eb5c5-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="eb5c5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eb5c5-109">EXAMPLES</span></span>

### <span data-ttu-id="eb5c5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eb5c5-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="eb5c5-111">Удаляет правило авторизации \` MyAuthRuleName \` из пространства имен \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="eb5c5-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="eb5c5-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="eb5c5-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="eb5c5-113">Удаляет правило авторизации \` MyAuthRuleName из Центра событий \` \` MyEventHubName. \`</span><span class="sxs-lookup"><span data-stu-id="eb5c5-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="eb5c5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb5c5-114">PARAMETERS</span></span>

### <span data-ttu-id="eb5c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb5c5-115">-DefaultProfile</span></span>
<span data-ttu-id="eb5c5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb5c5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb5c5-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="eb5c5-117">-EventHub</span></span>
<span data-ttu-id="eb5c5-118">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="eb5c5-118">EventHub Name</span></span>

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

### <span data-ttu-id="eb5c5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="eb5c5-119">-Force</span></span>
<span data-ttu-id="eb5c5-120">Не запросить подтверждение</span><span class="sxs-lookup"><span data-stu-id="eb5c5-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="eb5c5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="eb5c5-121">-Name</span></span>
<span data-ttu-id="eb5c5-122">Имяrule authorizationRule</span><span class="sxs-lookup"><span data-stu-id="eb5c5-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="eb5c5-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="eb5c5-123">-Namespace</span></span>
<span data-ttu-id="eb5c5-124">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="eb5c5-124">Namespace Name</span></span>

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

### <span data-ttu-id="eb5c5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb5c5-125">-PassThru</span></span>
<span data-ttu-id="eb5c5-126">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="eb5c5-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="eb5c5-127">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="eb5c5-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eb5c5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb5c5-128">-ResourceGroupName</span></span>
<span data-ttu-id="eb5c5-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="eb5c5-129">Resource Group Name</span></span>

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

### <span data-ttu-id="eb5c5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb5c5-130">-Confirm</span></span>
<span data-ttu-id="eb5c5-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb5c5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb5c5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb5c5-132">-WhatIf</span></span>
<span data-ttu-id="eb5c5-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb5c5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb5c5-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eb5c5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb5c5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb5c5-135">CommonParameters</span></span>
<span data-ttu-id="eb5c5-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb5c5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb5c5-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb5c5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb5c5-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb5c5-138">INPUTS</span></span>

### <span data-ttu-id="eb5c5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="eb5c5-139">System.String</span></span>

## <span data-ttu-id="eb5c5-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eb5c5-140">OUTPUTS</span></span>

### <span data-ttu-id="eb5c5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eb5c5-141">System.Boolean</span></span>

## <span data-ttu-id="eb5c5-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eb5c5-142">NOTES</span></span>

## <span data-ttu-id="eb5c5-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb5c5-143">RELATED LINKS</span></span>
