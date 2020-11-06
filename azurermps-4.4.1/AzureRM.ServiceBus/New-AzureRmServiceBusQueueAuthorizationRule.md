---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 098c61be4eaf405d3c3a031601b48f20de1e234a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559511"
---
# <span data-ttu-id="3ba0d-101">New-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3ba0d-101">New-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="3ba0d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ba0d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ba0d-103">Создание нового правила авторизации для указанной очереди обслуживания служебной шины.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-103">Creates a new authorization rule for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ba0d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ba0d-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ba0d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ba0d-105">DESCRIPTION</span></span>
<span data-ttu-id="3ba0d-106">Командлет **New-AzureRmServiceBusQueueAuthorizationRule** создает новое правило авторизации для указанной очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-106">The **New-AzureRmServiceBusQueueAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus queue.</span></span>

## <span data-ttu-id="3ba0d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ba0d-107">EXAMPLES</span></span>

### <span data-ttu-id="3ba0d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3ba0d-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="3ba0d-109">Создание правила авторизации `SBAuthoRule1` с правами **прослушивания и отправки** для очереди `SB-Queue_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="3ba0d-109">Creates authorization rule `SBAuthoRule1` with **Listen and Send** rights for the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="3ba0d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ba0d-110">PARAMETERS</span></span>

### <span data-ttu-id="3ba0d-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3ba0d-111">-ResourceGroup</span></span>
<span data-ttu-id="3ba0d-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="3ba0d-113">-Права</span><span class="sxs-lookup"><span data-stu-id="3ba0d-113">-Rights</span></span>
<span data-ttu-id="3ba0d-114">Задает права доступа; Например</span><span class="sxs-lookup"><span data-stu-id="3ba0d-114">Specifies the rights; for example,</span></span>  
<span data-ttu-id="3ba0d-115">@ ("Прослушать", "Отправить", "Управление")</span><span class="sxs-lookup"><span data-stu-id="3ba0d-115">@("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="3ba0d-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ba0d-116">-Confirm</span></span>
<span data-ttu-id="3ba0d-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ba0d-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ba0d-118">-WhatIf</span></span>
<span data-ttu-id="3ba0d-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ba0d-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ba0d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ba0d-121">-DefaultProfile</span></span>
<span data-ttu-id="3ba0d-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ba0d-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3ba0d-123">-Name</span></span>
<span data-ttu-id="3ba0d-124">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-124">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="3ba0d-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3ba0d-125">-Namespace</span></span>
<span data-ttu-id="3ba0d-126">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-126">Namespace Name.</span></span>

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

### <span data-ttu-id="3ba0d-127">-Очередь</span><span class="sxs-lookup"><span data-stu-id="3ba0d-127">-Queue</span></span>
<span data-ttu-id="3ba0d-128">Имя очереди.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-128">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba0d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ba0d-129">CommonParameters</span></span>
<span data-ttu-id="3ba0d-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ba0d-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ba0d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ba0d-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ba0d-132">INPUTS</span></span>

### <span data-ttu-id="3ba0d-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3ba0d-133">-ResourceGroup</span></span>
 <span data-ttu-id="3ba0d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3ba0d-134">System.String</span></span>
 

### <span data-ttu-id="3ba0d-135">-+ +</span><span class="sxs-lookup"><span data-stu-id="3ba0d-135">-NamespaceName</span></span>
 <span data-ttu-id="3ba0d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3ba0d-136">System.String</span></span>
 

### <span data-ttu-id="3ba0d-137">-QueueName</span><span class="sxs-lookup"><span data-stu-id="3ba0d-137">-QueueName</span></span>
 <span data-ttu-id="3ba0d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3ba0d-138">System.String</span></span>
 

### <span data-ttu-id="3ba0d-139">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="3ba0d-139">-AuthorizationRuleName</span></span>
 <span data-ttu-id="3ba0d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3ba0d-140">System.String</span></span>

## <span data-ttu-id="3ba0d-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ba0d-141">OUTPUTS</span></span>

### <span data-ttu-id="3ba0d-142">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="3ba0d-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="3ba0d-143">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onruless/SBAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules имя: SBAuthoRule1 расположение: Западная часть тегов US: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="3ba0d-143">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="3ba0d-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ba0d-144">NOTES</span></span>

## <span data-ttu-id="3ba0d-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ba0d-145">RELATED LINKS</span></span>

