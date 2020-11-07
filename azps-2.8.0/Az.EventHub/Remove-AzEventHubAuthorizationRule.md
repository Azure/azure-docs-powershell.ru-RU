---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 9e7cfbe1ec0810b9d18f884306535d37a6110dd2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720939"
---
# <span data-ttu-id="691bc-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="691bc-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="691bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="691bc-102">SYNOPSIS</span></span>
<span data-ttu-id="691bc-103">Удаляет указанное правило авторизации центра событий.</span><span class="sxs-lookup"><span data-stu-id="691bc-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="691bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="691bc-104">SYNTAX</span></span>

### <span data-ttu-id="691bc-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="691bc-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="691bc-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="691bc-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="691bc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="691bc-107">DESCRIPTION</span></span>
<span data-ttu-id="691bc-108">Командлет Remove-AzEventHubAuthorizationRule удаляет и удаляет указанное правило авторизации из заданного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="691bc-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="691bc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="691bc-109">EXAMPLES</span></span>

### <span data-ttu-id="691bc-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="691bc-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="691bc-111">Удаляет правило авторизации \` MyAuthRuleName \` из пространства имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="691bc-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="691bc-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="691bc-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="691bc-113">Удаляет правило авторизации \` MyAuthRuleName \` из центра событий \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="691bc-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="691bc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="691bc-114">PARAMETERS</span></span>

### <span data-ttu-id="691bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="691bc-115">-DefaultProfile</span></span>
<span data-ttu-id="691bc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="691bc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="691bc-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="691bc-117">-EventHub</span></span>
<span data-ttu-id="691bc-118">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="691bc-118">EventHub Name</span></span>

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

### <span data-ttu-id="691bc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="691bc-119">-Force</span></span>
<span data-ttu-id="691bc-120">Не запрашивать подтверждение</span><span class="sxs-lookup"><span data-stu-id="691bc-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="691bc-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="691bc-121">-Name</span></span>
<span data-ttu-id="691bc-122">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="691bc-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="691bc-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="691bc-123">-Namespace</span></span>
<span data-ttu-id="691bc-124">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="691bc-124">Namespace Name</span></span>

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

### <span data-ttu-id="691bc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="691bc-125">-PassThru</span></span>
<span data-ttu-id="691bc-126">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="691bc-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="691bc-127">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="691bc-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="691bc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="691bc-128">-ResourceGroupName</span></span>
<span data-ttu-id="691bc-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="691bc-129">Resource Group Name</span></span>

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

### <span data-ttu-id="691bc-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="691bc-130">-Confirm</span></span>
<span data-ttu-id="691bc-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="691bc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="691bc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="691bc-132">-WhatIf</span></span>
<span data-ttu-id="691bc-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="691bc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="691bc-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="691bc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="691bc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="691bc-135">CommonParameters</span></span>
<span data-ttu-id="691bc-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="691bc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="691bc-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="691bc-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="691bc-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="691bc-138">INPUTS</span></span>

### <span data-ttu-id="691bc-139">System. String</span><span class="sxs-lookup"><span data-stu-id="691bc-139">System.String</span></span>

## <span data-ttu-id="691bc-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="691bc-140">OUTPUTS</span></span>

### <span data-ttu-id="691bc-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="691bc-141">System.Boolean</span></span>

## <span data-ttu-id="691bc-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="691bc-142">NOTES</span></span>

## <span data-ttu-id="691bc-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="691bc-143">RELATED LINKS</span></span>
