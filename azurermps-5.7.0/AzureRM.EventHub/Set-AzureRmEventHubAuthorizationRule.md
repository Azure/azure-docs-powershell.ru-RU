---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4965fb6047ca31d2c5b70276a777235d2a3cb050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564920"
---
# <span data-ttu-id="4e971-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4e971-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="4e971-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e971-102">SYNOPSIS</span></span>
<span data-ttu-id="4e971-103">Обновляет указанное правило авторизации на концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="4e971-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e971-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e971-104">SYNTAX</span></span>

### <span data-ttu-id="4e971-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e971-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e971-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4e971-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e971-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4e971-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e971-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e971-108">DESCRIPTION</span></span>
<span data-ttu-id="4e971-109">Командлет Set-AzureRmEventHubAuthorizationRule обновляет указанное правило авторизации на данном концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="4e971-109">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="4e971-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e971-110">EXAMPLES</span></span>

### <span data-ttu-id="4e971-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e971-111">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="4e971-112">Обновляет MyAuthRuleName правила авторизации \` \` , чтобы предоставить доступ к управлению правами для центра событий \` MyEventHubName \` , областью которого является пространство имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="4e971-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="4e971-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e971-113">PARAMETERS</span></span>

### <span data-ttu-id="4e971-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e971-114">-DefaultProfile</span></span>
<span data-ttu-id="4e971-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e971-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e971-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="4e971-116">-EventHub</span></span>
<span data-ttu-id="4e971-117">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="4e971-117">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e971-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e971-118">-InputObject</span></span>
<span data-ttu-id="4e971-119">Объект AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4e971-119">AuthorizationRule Object</span></span>

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e971-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e971-120">-Name</span></span>
<span data-ttu-id="4e971-121">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4e971-121">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e971-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4e971-122">-Namespace</span></span>
<span data-ttu-id="4e971-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="4e971-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e971-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e971-124">-ResourceGroupName</span></span>
<span data-ttu-id="4e971-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4e971-125">Resource Group Name</span></span>

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

### <span data-ttu-id="4e971-126">-Права</span><span class="sxs-lookup"><span data-stu-id="4e971-126">-Rights</span></span>
<span data-ttu-id="4e971-127">Права, например @ ("прослушать", "Отправить", "Управление")</span><span class="sxs-lookup"><span data-stu-id="4e971-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e971-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e971-128">-Confirm</span></span>
<span data-ttu-id="4e971-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e971-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e971-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e971-130">-WhatIf</span></span>
<span data-ttu-id="4e971-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e971-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e971-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e971-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e971-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e971-133">CommonParameters</span></span>
<span data-ttu-id="4e971-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e971-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4e971-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e971-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e971-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e971-136">INPUTS</span></span>

### <span data-ttu-id="4e971-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4e971-137">System.String</span></span>
<span data-ttu-id="4e971-138">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes System. String []</span><span class="sxs-lookup"><span data-stu-id="4e971-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes System.String[]</span></span>


## <span data-ttu-id="4e971-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e971-139">OUTPUTS</span></span>

### <span data-ttu-id="4e971-140">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4e971-140">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="4e971-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e971-141">NOTES</span></span>

## <span data-ttu-id="4e971-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e971-142">RELATED LINKS</span></span>
