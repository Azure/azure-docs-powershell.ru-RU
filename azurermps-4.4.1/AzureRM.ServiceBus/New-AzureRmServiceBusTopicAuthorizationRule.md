---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 603eb1363e15b58a324f7131dd986a7c84371a89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732409"
---
# <span data-ttu-id="fdc30-101">New-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fdc30-101">New-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="fdc30-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fdc30-102">SYNOPSIS</span></span>
<span data-ttu-id="fdc30-103">Создание нового правила авторизации для указанной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="fdc30-103">Creates a new authorization rule for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdc30-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fdc30-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fdc30-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fdc30-105">DESCRIPTION</span></span>
<span data-ttu-id="fdc30-106">Командлет **New-AzureRmServiceBusTopicAuthorizationRule** создает новое правило авторизации для указанной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="fdc30-106">The **New-AzureRmServiceBusTopicAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus topic.</span></span>

## <span data-ttu-id="fdc30-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fdc30-107">EXAMPLES</span></span>

### <span data-ttu-id="fdc30-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fdc30-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="fdc30-109">Создание правила авторизации `SBTopicAuthoRule1` с правами **прослушивания** и **отправки** для темы `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="fdc30-109">Creates authorization rule `SBTopicAuthoRule1` with **Listen** and **Send** rights for the topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="fdc30-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fdc30-110">PARAMETERS</span></span>

### <span data-ttu-id="fdc30-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fdc30-111">-ResourceGroup</span></span>
<span data-ttu-id="fdc30-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fdc30-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="fdc30-113">-Права</span><span class="sxs-lookup"><span data-stu-id="fdc30-113">-Rights</span></span>
<span data-ttu-id="fdc30-114">Права доступа; Например, @ ("прослушать", "Отправить", "Управление")</span><span class="sxs-lookup"><span data-stu-id="fdc30-114">The rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdc30-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fdc30-115">-Confirm</span></span>
<span data-ttu-id="fdc30-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fdc30-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdc30-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdc30-117">-WhatIf</span></span>
<span data-ttu-id="fdc30-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fdc30-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdc30-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fdc30-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdc30-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdc30-120">-DefaultProfile</span></span>
<span data-ttu-id="fdc30-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fdc30-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdc30-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fdc30-122">-Name</span></span>
<span data-ttu-id="fdc30-123">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="fdc30-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdc30-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fdc30-124">-Namespace</span></span>
<span data-ttu-id="fdc30-125">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="fdc30-125">Namespace Name.</span></span>

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

### <span data-ttu-id="fdc30-126">-Темы</span><span class="sxs-lookup"><span data-stu-id="fdc30-126">-Topic</span></span>
<span data-ttu-id="fdc30-127">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="fdc30-127">Topic Name.</span></span>

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

### <span data-ttu-id="fdc30-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdc30-128">CommonParameters</span></span>
<span data-ttu-id="fdc30-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fdc30-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdc30-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdc30-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdc30-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fdc30-131">INPUTS</span></span>

### <span data-ttu-id="fdc30-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fdc30-132">-ResourceGroup</span></span>
 <span data-ttu-id="fdc30-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fdc30-133">System.String</span></span>
 

### <span data-ttu-id="fdc30-134">-+ +</span><span class="sxs-lookup"><span data-stu-id="fdc30-134">-NamespaceName</span></span>
 <span data-ttu-id="fdc30-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fdc30-135">System.String</span></span>
 

### <span data-ttu-id="fdc30-136">-TopicName</span><span class="sxs-lookup"><span data-stu-id="fdc30-136">-TopicName</span></span>
 <span data-ttu-id="fdc30-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fdc30-137">System.String</span></span>
 

### <span data-ttu-id="fdc30-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="fdc30-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="fdc30-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fdc30-139">System.String</span></span>

## <span data-ttu-id="fdc30-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fdc30-140">OUTPUTS</span></span>

### <span data-ttu-id="fdc30-141">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="fdc30-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="fdc30-142">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onruless/SBTopicAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules имя: SBTopicAuthoRule1 расположение: Западная часть тегов US: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="fdc30-142">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="fdc30-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="fdc30-143">NOTES</span></span>

## <span data-ttu-id="fdc30-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fdc30-144">RELATED LINKS</span></span>

