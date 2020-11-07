---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 46f640eefcd429a7fec4d06397f394ef31831183
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730814"
---
# <span data-ttu-id="24b74-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="24b74-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="24b74-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24b74-102">SYNOPSIS</span></span>
<span data-ttu-id="24b74-103">Обновляет указанное правило авторизации на концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="24b74-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="24b74-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24b74-104">SYNTAX</span></span>

### <span data-ttu-id="24b74-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="24b74-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24b74-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="24b74-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24b74-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="24b74-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24b74-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24b74-108">DESCRIPTION</span></span>
<span data-ttu-id="24b74-109">Командлет Set-AzEventHubAuthorizationRule обновляет указанное правило авторизации на данном концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="24b74-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="24b74-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24b74-110">EXAMPLES</span></span>

### <span data-ttu-id="24b74-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="24b74-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="24b74-112">Обновляет MyAuthRuleName правила авторизации \` \` , чтобы предоставить доступ к управлению правами для центра событий \` MyEventHubName \` , областью которого является пространство имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="24b74-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="24b74-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24b74-113">PARAMETERS</span></span>

### <span data-ttu-id="24b74-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b74-114">-DefaultProfile</span></span>
<span data-ttu-id="24b74-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24b74-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24b74-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="24b74-116">-EventHub</span></span>
<span data-ttu-id="24b74-117">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="24b74-117">EventHub Name</span></span>

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

### <span data-ttu-id="24b74-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24b74-118">-InputObject</span></span>
<span data-ttu-id="24b74-119">Объект AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="24b74-119">AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24b74-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="24b74-120">-Name</span></span>
<span data-ttu-id="24b74-121">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="24b74-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="24b74-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="24b74-122">-Namespace</span></span>
<span data-ttu-id="24b74-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="24b74-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24b74-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24b74-124">-ResourceGroupName</span></span>
<span data-ttu-id="24b74-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="24b74-125">Resource Group Name</span></span>

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

### <span data-ttu-id="24b74-126">-Права</span><span class="sxs-lookup"><span data-stu-id="24b74-126">-Rights</span></span>
<span data-ttu-id="24b74-127">Права, например @ ("прослушать", "Отправить", "Управление")</span><span class="sxs-lookup"><span data-stu-id="24b74-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24b74-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24b74-128">-Confirm</span></span>
<span data-ttu-id="24b74-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="24b74-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24b74-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24b74-130">-WhatIf</span></span>
<span data-ttu-id="24b74-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="24b74-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24b74-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="24b74-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24b74-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b74-133">CommonParameters</span></span>
<span data-ttu-id="24b74-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24b74-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24b74-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24b74-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b74-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24b74-136">INPUTS</span></span>

### <span data-ttu-id="24b74-137">System. String</span><span class="sxs-lookup"><span data-stu-id="24b74-137">System.String</span></span>

### <span data-ttu-id="24b74-138">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="24b74-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="24b74-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="24b74-139">System.String[]</span></span>

## <span data-ttu-id="24b74-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24b74-140">OUTPUTS</span></span>

### <span data-ttu-id="24b74-141">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="24b74-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="24b74-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="24b74-142">NOTES</span></span>

## <span data-ttu-id="24b74-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24b74-143">RELATED LINKS</span></span>
