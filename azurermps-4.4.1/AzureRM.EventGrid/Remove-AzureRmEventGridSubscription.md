---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
ms.openlocfilehash: a15cb222108d79544d38ce730897e03fa61066ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569512"
---
# <span data-ttu-id="63e47-101">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="63e47-101">Remove-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="63e47-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63e47-102">SYNOPSIS</span></span>
<span data-ttu-id="63e47-103">Удаляет подписку на событие сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="63e47-103">Removes an Azure Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63e47-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63e47-104">SYNTAX</span></span>

### <span data-ttu-id="63e47-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="63e47-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e47-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="63e47-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e47-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="63e47-107">EventSubscriptionInputObjectSet</span></span>
```
Remove-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e47-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="63e47-108">TopicNameParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63e47-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63e47-109">DESCRIPTION</span></span>
<span data-ttu-id="63e47-110">Удаляет подписку на событие сетки событий Azure для таблицы событий Azure: ресурс, подписку или группу ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="63e47-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="63e47-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63e47-111">EXAMPLES</span></span>

### <span data-ttu-id="63e47-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63e47-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="63e47-113">Удаляет подписку на события \` EventSubscription1 в \` разделе сетки событий Azure \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="63e47-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="63e47-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="63e47-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="63e47-115">Удаляет подписку на событие \` EventSubscription1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="63e47-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="63e47-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="63e47-116">Example 3</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="63e47-117">Удаляет подписку на событие \` EventSubscription1 \` к подписке по умолчанию Azure.</span><span class="sxs-lookup"><span data-stu-id="63e47-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="63e47-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="63e47-118">Example 4</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="63e47-119">Удаляет подписку на событие \` EventSubscription1 \` в пространство имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="63e47-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="63e47-120">Пример 5</span><span class="sxs-lookup"><span data-stu-id="63e47-120">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="63e47-121">Удаляет подписку на событие \` EventSubscription1 \` в разделе сетки событий.</span><span class="sxs-lookup"><span data-stu-id="63e47-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="63e47-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63e47-122">PARAMETERS</span></span>

### <span data-ttu-id="63e47-123">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="63e47-123">-EventSubscriptionName</span></span>
<span data-ttu-id="63e47-124">Имя подписки на событие, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="63e47-124">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e47-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63e47-125">-InputObject</span></span>
<span data-ttu-id="63e47-126">Объект EventGrid EventSubscription.</span><span class="sxs-lookup"><span data-stu-id="63e47-126">EventGrid EventSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63e47-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63e47-127">-PassThru</span></span>
<span data-ttu-id="63e47-128">Возвращает состояние операции удаления.</span><span class="sxs-lookup"><span data-stu-id="63e47-128">Returns the status of the Remove operation.</span></span> <span data-ttu-id="63e47-129">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="63e47-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="63e47-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63e47-130">-ResourceGroupName</span></span>
<span data-ttu-id="63e47-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63e47-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e47-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63e47-132">-ResourceId</span></span>
<span data-ttu-id="63e47-133">Идентификатор ресурса, для которого требуется удалить подписку на события.</span><span class="sxs-lookup"><span data-stu-id="63e47-133">Identifier of the resource whose event subscription needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e47-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="63e47-134">-TopicName</span></span>
<span data-ttu-id="63e47-135">Название темы сетки событий.</span><span class="sxs-lookup"><span data-stu-id="63e47-135">Event Grid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e47-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63e47-136">-Confirm</span></span>
<span data-ttu-id="63e47-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63e47-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63e47-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e47-138">-WhatIf</span></span>
<span data-ttu-id="63e47-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63e47-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63e47-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63e47-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63e47-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e47-141">-DefaultProfile</span></span>
<span data-ttu-id="63e47-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63e47-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63e47-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e47-143">CommonParameters</span></span>
<span data-ttu-id="63e47-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63e47-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e47-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63e47-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e47-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63e47-146">INPUTS</span></span>

### <span data-ttu-id="63e47-147">System. String</span><span class="sxs-lookup"><span data-stu-id="63e47-147">System.String</span></span>
<span data-ttu-id="63e47-148">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="63e47-148">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="63e47-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63e47-149">OUTPUTS</span></span>

### <span data-ttu-id="63e47-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="63e47-150">System.Object</span></span>

## <span data-ttu-id="63e47-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="63e47-151">NOTES</span></span>

## <span data-ttu-id="63e47-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63e47-152">RELATED LINKS</span></span>

