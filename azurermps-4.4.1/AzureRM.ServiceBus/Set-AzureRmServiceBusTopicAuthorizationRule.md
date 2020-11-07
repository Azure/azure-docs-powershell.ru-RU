---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: bbc6c0119f0f8f424b508adc38b5de80cd097734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734226"
---
# <span data-ttu-id="4cc5a-101">Set-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4cc5a-101">Set-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="4cc5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4cc5a-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc5a-103">Обновляет указанное описание правила авторизации для указанной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="4cc5a-103">Updates the specified authorization rule description for the given Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cc5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4cc5a-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cc5a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4cc5a-105">DESCRIPTION</span></span>
<span data-ttu-id="4cc5a-106">Командлет **Set-AzureRmServiceBusTopicAuthorizationRule** обновляет описание указанного правила авторизации для данной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="4cc5a-106">The **Set-AzureRmServiceBusTopicAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus topic.</span></span>

## <span data-ttu-id="4cc5a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4cc5a-107">EXAMPLES</span></span>

### <span data-ttu-id="4cc5a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4cc5a-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="4cc5a-109">Добавляет **Управление** правами доступа для правила авторизации `SBTopicAuthoRule1` в разделе `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="4cc5a-109">Adds **Manage** to the access rights of the authorization rule `SBTopicAuthoRule1` on topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="4cc5a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4cc5a-110">PARAMETERS</span></span>

### <span data-ttu-id="4cc5a-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4cc5a-111">-ResourceGroup</span></span>
<span data-ttu-id="4cc5a-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4cc5a-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="4cc5a-113">-Права</span><span class="sxs-lookup"><span data-stu-id="4cc5a-113">-Rights</span></span>
<span data-ttu-id="4cc5a-114">Администратора Например, @ ("прослушать", "Отправить", "Управление").</span><span class="sxs-lookup"><span data-stu-id="4cc5a-114">Rights; for example, @("Listen","Send","Manage").</span></span> <span data-ttu-id="4cc5a-115">Обязательно, если не указан аргумент **-AuthruleObj** .</span><span class="sxs-lookup"><span data-stu-id="4cc5a-115">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cc5a-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4cc5a-116">-Confirm</span></span>
<span data-ttu-id="4cc5a-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4cc5a-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc5a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cc5a-118">-WhatIf</span></span>
<span data-ttu-id="4cc5a-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4cc5a-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cc5a-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4cc5a-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc5a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc5a-121">-DefaultProfile</span></span>
<span data-ttu-id="4cc5a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4cc5a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc5a-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="4cc5a-123">-InputObj</span></span>
<span data-ttu-id="4cc5a-124">Объект AuthorizationRule темы ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="4cc5a-124">ServiceBus Topic AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cc5a-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4cc5a-125">-Name</span></span>
<span data-ttu-id="4cc5a-126">AuthorizationRule имя — требуется, если не указан аргумент "AuthruleObj".</span><span class="sxs-lookup"><span data-stu-id="4cc5a-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cc5a-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4cc5a-127">-Namespace</span></span>
<span data-ttu-id="4cc5a-128">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="4cc5a-128">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cc5a-129">-Темы</span><span class="sxs-lookup"><span data-stu-id="4cc5a-129">-Topic</span></span>
<span data-ttu-id="4cc5a-130">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="4cc5a-130">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cc5a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc5a-131">CommonParameters</span></span>
<span data-ttu-id="4cc5a-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4cc5a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc5a-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cc5a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc5a-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4cc5a-134">INPUTS</span></span>

### <span data-ttu-id="4cc5a-135">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4cc5a-135">-ResourceGroup</span></span>
 <span data-ttu-id="4cc5a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4cc5a-136">System.String</span></span>

### <span data-ttu-id="4cc5a-137">-+ +</span><span class="sxs-lookup"><span data-stu-id="4cc5a-137">-NamespaceName</span></span>
 <span data-ttu-id="4cc5a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4cc5a-138">System.String</span></span>

### <span data-ttu-id="4cc5a-139">-TopicName</span><span class="sxs-lookup"><span data-stu-id="4cc5a-139">-TopicName</span></span>
 <span data-ttu-id="4cc5a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4cc5a-140">System.String</span></span>

### <span data-ttu-id="4cc5a-141">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="4cc5a-141">-AuthRuleObj</span></span>
 <span data-ttu-id="4cc5a-142">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4cc5a-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="4cc5a-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4cc5a-143">OUTPUTS</span></span>

### <span data-ttu-id="4cc5a-144">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4cc5a-144">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="4cc5a-145">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/Authorization Rules/SBTopicAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules имя: SBTopicAuthoRule1 расположение: западные Теги US: Rights: {Listen, Send, Manage}</span><span class="sxs-lookup"><span data-stu-id="4cc5a-145">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorization Rules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send, Manage}</span></span>

## <span data-ttu-id="4cc5a-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="4cc5a-146">NOTES</span></span>

## <span data-ttu-id="4cc5a-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4cc5a-147">RELATED LINKS</span></span>

