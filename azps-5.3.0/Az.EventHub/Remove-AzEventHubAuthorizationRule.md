---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 91c38686d8621f3bba521d738cc125e4b8473188
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507494"
---
# <span data-ttu-id="3a757-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3a757-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="3a757-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a757-102">SYNOPSIS</span></span>
<span data-ttu-id="3a757-103">Удаляет указанное правило авторизации в Центре событий.</span><span class="sxs-lookup"><span data-stu-id="3a757-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="3a757-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3a757-104">SYNTAX</span></span>

### <span data-ttu-id="3a757-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3a757-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a757-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a757-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a757-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a757-107">DESCRIPTION</span></span>
<span data-ttu-id="3a757-108">Этот Remove-AzEventHubAuthorizationRule удаляет указанное правило авторизации из данного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="3a757-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="3a757-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3a757-109">EXAMPLES</span></span>

### <span data-ttu-id="3a757-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3a757-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="3a757-111">Удаляет правило авторизации \` MyAuthRuleName \` из пространства имен \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="3a757-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="3a757-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3a757-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="3a757-113">Удаляет правило авторизации \` MyAuthRuleName из Центра событий \` \` MyEventHubName. \`</span><span class="sxs-lookup"><span data-stu-id="3a757-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="3a757-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a757-114">PARAMETERS</span></span>

### <span data-ttu-id="3a757-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a757-115">-DefaultProfile</span></span>
<span data-ttu-id="3a757-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a757-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a757-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="3a757-117">-EventHub</span></span>
<span data-ttu-id="3a757-118">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="3a757-118">EventHub Name</span></span>

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

### <span data-ttu-id="3a757-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3a757-119">-Force</span></span>
<span data-ttu-id="3a757-120">Не запросить подтверждение</span><span class="sxs-lookup"><span data-stu-id="3a757-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="3a757-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3a757-121">-Name</span></span>
<span data-ttu-id="3a757-122">Имяrule authorizationRule</span><span class="sxs-lookup"><span data-stu-id="3a757-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="3a757-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3a757-123">-Namespace</span></span>
<span data-ttu-id="3a757-124">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="3a757-124">Namespace Name</span></span>

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

### <span data-ttu-id="3a757-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a757-125">-PassThru</span></span>
<span data-ttu-id="3a757-126">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="3a757-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3a757-127">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3a757-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a757-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a757-128">-ResourceGroupName</span></span>
<span data-ttu-id="3a757-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3a757-129">Resource Group Name</span></span>

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

### <span data-ttu-id="3a757-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a757-130">-Confirm</span></span>
<span data-ttu-id="3a757-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a757-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a757-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a757-132">-WhatIf</span></span>
<span data-ttu-id="3a757-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a757-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a757-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3a757-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a757-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a757-135">CommonParameters</span></span>
<span data-ttu-id="3a757-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a757-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a757-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a757-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a757-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a757-138">INPUTS</span></span>

### <span data-ttu-id="3a757-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3a757-139">System.String</span></span>

## <span data-ttu-id="3a757-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3a757-140">OUTPUTS</span></span>

### <span data-ttu-id="3a757-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a757-141">System.Boolean</span></span>

## <span data-ttu-id="3a757-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3a757-142">NOTES</span></span>

## <span data-ttu-id="3a757-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a757-143">RELATED LINKS</span></span>
