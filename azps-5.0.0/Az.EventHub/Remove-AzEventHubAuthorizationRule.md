---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 91c38686d8621f3bba521d738cc125e4b8473188
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245463"
---
# <span data-ttu-id="eed15-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="eed15-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="eed15-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eed15-102">SYNOPSIS</span></span>
<span data-ttu-id="eed15-103">Удаляет указанное правило авторизации центра событий.</span><span class="sxs-lookup"><span data-stu-id="eed15-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="eed15-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eed15-104">SYNTAX</span></span>

### <span data-ttu-id="eed15-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eed15-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eed15-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="eed15-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eed15-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eed15-107">DESCRIPTION</span></span>
<span data-ttu-id="eed15-108">Командлет Remove-AzEventHubAuthorizationRule удаляет и удаляет указанное правило авторизации из заданного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="eed15-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="eed15-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eed15-109">EXAMPLES</span></span>

### <span data-ttu-id="eed15-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eed15-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="eed15-111">Удаляет правило авторизации \` MyAuthRuleName \` из пространства имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="eed15-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="eed15-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="eed15-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="eed15-113">Удаляет правило авторизации \` MyAuthRuleName \` из центра событий \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="eed15-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="eed15-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eed15-114">PARAMETERS</span></span>

### <span data-ttu-id="eed15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed15-115">-DefaultProfile</span></span>
<span data-ttu-id="eed15-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eed15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eed15-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="eed15-117">-EventHub</span></span>
<span data-ttu-id="eed15-118">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="eed15-118">EventHub Name</span></span>

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

### <span data-ttu-id="eed15-119">-Force</span><span class="sxs-lookup"><span data-stu-id="eed15-119">-Force</span></span>
<span data-ttu-id="eed15-120">Не запрашивать подтверждение</span><span class="sxs-lookup"><span data-stu-id="eed15-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="eed15-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eed15-121">-Name</span></span>
<span data-ttu-id="eed15-122">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="eed15-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="eed15-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="eed15-123">-Namespace</span></span>
<span data-ttu-id="eed15-124">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="eed15-124">Namespace Name</span></span>

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

### <span data-ttu-id="eed15-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eed15-125">-PassThru</span></span>
<span data-ttu-id="eed15-126">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="eed15-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="eed15-127">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="eed15-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eed15-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eed15-128">-ResourceGroupName</span></span>
<span data-ttu-id="eed15-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="eed15-129">Resource Group Name</span></span>

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

### <span data-ttu-id="eed15-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eed15-130">-Confirm</span></span>
<span data-ttu-id="eed15-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eed15-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eed15-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eed15-132">-WhatIf</span></span>
<span data-ttu-id="eed15-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eed15-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eed15-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eed15-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eed15-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed15-135">CommonParameters</span></span>
<span data-ttu-id="eed15-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eed15-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed15-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eed15-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed15-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eed15-138">INPUTS</span></span>

### <span data-ttu-id="eed15-139">System. String</span><span class="sxs-lookup"><span data-stu-id="eed15-139">System.String</span></span>

## <span data-ttu-id="eed15-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eed15-140">OUTPUTS</span></span>

### <span data-ttu-id="eed15-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eed15-141">System.Boolean</span></span>

## <span data-ttu-id="eed15-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="eed15-142">NOTES</span></span>

## <span data-ttu-id="eed15-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eed15-143">RELATED LINKS</span></span>