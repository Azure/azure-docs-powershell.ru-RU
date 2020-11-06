---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 166b47a231b2ca6fc2cf74137212e60123f25445
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568674"
---
# <span data-ttu-id="78d2a-101">Set-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="78d2a-101">Set-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="78d2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="78d2a-103">Обновляет указанное описание правила авторизации для указанной очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="78d2a-103">Updates the specified authorization rule description for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78d2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78d2a-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> [-NamespaceName] <String>
 [-QueueName] <String> [-AuthRuleObj] <SharedAccessAuthorizationRuleAttributes>
 [[-AuthorizationRuleName] <String>] [[-Rights] <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78d2a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78d2a-105">DESCRIPTION</span></span>
<span data-ttu-id="78d2a-106">Командлет **Set-AzureRmServiceBusQueueAuthorizationRule** обновляет описание указанного правила авторизации данной очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="78d2a-106">The **Set-AzureRmServiceBusQueueAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus queue.</span></span>

## <span data-ttu-id="78d2a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78d2a-107">EXAMPLES</span></span>

### <span data-ttu-id="78d2a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="78d2a-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="78d2a-109">Добавляет **Управление** правами доступа для правила авторизации `SBAuthoRule1` очереди `SB-Queue_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="78d2a-109">Adds **Manage** to the access rights of the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="78d2a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78d2a-110">PARAMETERS</span></span>

### <span data-ttu-id="78d2a-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="78d2a-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="78d2a-112">Имя правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="78d2a-112">The authorization rule name.</span></span> <span data-ttu-id="78d2a-113">Обязательно, если не указан аргумент **-AuthruleObj** .</span><span class="sxs-lookup"><span data-stu-id="78d2a-113">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d2a-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="78d2a-114">-AuthRuleObj</span></span>
<span data-ttu-id="78d2a-115">Объект правила авторизации в очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="78d2a-115">The Service Bus queue authorization rule object.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d2a-116">-+ +</span><span class="sxs-lookup"><span data-stu-id="78d2a-116">-NamespaceName</span></span>
<span data-ttu-id="78d2a-117">Имя пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="78d2a-117">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d2a-118">-QueueName</span><span class="sxs-lookup"><span data-stu-id="78d2a-118">-QueueName</span></span>
<span data-ttu-id="78d2a-119">Имя очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="78d2a-119">The Service Bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d2a-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="78d2a-120">-ResourceGroup</span></span>
<span data-ttu-id="78d2a-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78d2a-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="78d2a-122">-Права</span><span class="sxs-lookup"><span data-stu-id="78d2a-122">-Rights</span></span>
<span data-ttu-id="78d2a-123">Права доступа; Например, @ ("прослушать", "Отправить", "Управление").</span><span class="sxs-lookup"><span data-stu-id="78d2a-123">The rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="78d2a-124">Обязательно, если не указана "AuthruleObj".</span><span class="sxs-lookup"><span data-stu-id="78d2a-124">Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d2a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78d2a-125">-Confirm</span></span>
<span data-ttu-id="78d2a-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="78d2a-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78d2a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d2a-127">-WhatIf</span></span>
<span data-ttu-id="78d2a-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="78d2a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78d2a-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="78d2a-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78d2a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d2a-130">CommonParameters</span></span>
<span data-ttu-id="78d2a-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78d2a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d2a-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78d2a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d2a-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78d2a-133">INPUTS</span></span>

### <span data-ttu-id="78d2a-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="78d2a-134">-ResourceGroup</span></span>
 <span data-ttu-id="78d2a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="78d2a-135">System.String</span></span>

### <span data-ttu-id="78d2a-136">-+ +</span><span class="sxs-lookup"><span data-stu-id="78d2a-136">-NamespaceName</span></span>
 <span data-ttu-id="78d2a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="78d2a-137">System.String</span></span>

### <span data-ttu-id="78d2a-138">-QueueName</span><span class="sxs-lookup"><span data-stu-id="78d2a-138">-QueueName</span></span>
 <span data-ttu-id="78d2a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="78d2a-139">System.String</span></span>

### <span data-ttu-id="78d2a-140">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="78d2a-140">-AuthRuleObj</span></span>
 <span data-ttu-id="78d2a-141">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="78d2a-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="78d2a-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78d2a-142">OUTPUTS</span></span>

### <span data-ttu-id="78d2a-143">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="78d2a-143">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="78d2a-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="78d2a-144">NOTES</span></span>

## <span data-ttu-id="78d2a-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78d2a-145">RELATED LINKS</span></span>

