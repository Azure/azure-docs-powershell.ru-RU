---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/remove-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
ms.openlocfilehash: 82d386fb0834db3de03d5692ad8b7a241b6eed90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565441"
---
# <span data-ttu-id="4aa55-101">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="4aa55-101">Remove-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="4aa55-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4aa55-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa55-103">Удаляет подписку на событие сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="4aa55-103">Removes an Azure Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aa55-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4aa55-104">SYNTAX</span></span>

### <span data-ttu-id="4aa55-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4aa55-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aa55-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4aa55-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aa55-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4aa55-107">EventSubscriptionInputObjectSet</span></span>
```
Remove-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aa55-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4aa55-108">TopicNameParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4aa55-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4aa55-109">DESCRIPTION</span></span>
<span data-ttu-id="4aa55-110">Удаляет подписку на событие сетки событий Azure для таблицы событий Azure: ресурс, подписку или группу ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="4aa55-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="4aa55-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4aa55-111">EXAMPLES</span></span>

### <span data-ttu-id="4aa55-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4aa55-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="4aa55-113">Удаляет подписку на события \` EventSubscription1 в \` разделе сетки событий Azure \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="4aa55-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4aa55-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4aa55-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="4aa55-115">Удаляет подписку на событие \` EventSubscription1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="4aa55-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4aa55-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4aa55-116">Example 3</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="4aa55-117">Удаляет подписку на событие \` EventSubscription1 \` к подписке по умолчанию Azure.</span><span class="sxs-lookup"><span data-stu-id="4aa55-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="4aa55-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="4aa55-118">Example 4</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="4aa55-119">Удаляет подписку на событие \` EventSubscription1 \` в пространство имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="4aa55-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="4aa55-120">Пример 5</span><span class="sxs-lookup"><span data-stu-id="4aa55-120">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="4aa55-121">Удаляет подписку на событие \` EventSubscription1 \` в разделе сетки событий.</span><span class="sxs-lookup"><span data-stu-id="4aa55-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="4aa55-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4aa55-122">PARAMETERS</span></span>

### <span data-ttu-id="4aa55-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aa55-123">-DefaultProfile</span></span>
<span data-ttu-id="4aa55-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4aa55-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4aa55-125">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="4aa55-125">-EventSubscriptionName</span></span>
<span data-ttu-id="4aa55-126">Имя подписки на событие, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="4aa55-126">Name of the event subscription that needs to be removed.</span></span>

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

### <span data-ttu-id="4aa55-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4aa55-127">-InputObject</span></span>
<span data-ttu-id="4aa55-128">Объект EventGrid EventSubscription.</span><span class="sxs-lookup"><span data-stu-id="4aa55-128">EventGrid EventSubscription object.</span></span>

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

### <span data-ttu-id="4aa55-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4aa55-129">-PassThru</span></span>
<span data-ttu-id="4aa55-130">Возвращает состояние операции удаления.</span><span class="sxs-lookup"><span data-stu-id="4aa55-130">Returns the status of the Remove operation.</span></span> <span data-ttu-id="4aa55-131">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4aa55-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4aa55-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aa55-132">-ResourceGroupName</span></span>
<span data-ttu-id="4aa55-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4aa55-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="4aa55-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4aa55-134">-ResourceId</span></span>
<span data-ttu-id="4aa55-135">Идентификатор ресурса, для которого требуется удалить подписку на события.</span><span class="sxs-lookup"><span data-stu-id="4aa55-135">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="4aa55-136">-TopicName</span><span class="sxs-lookup"><span data-stu-id="4aa55-136">-TopicName</span></span>
<span data-ttu-id="4aa55-137">Название темы сетки событий.</span><span class="sxs-lookup"><span data-stu-id="4aa55-137">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="4aa55-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4aa55-138">-Confirm</span></span>
<span data-ttu-id="4aa55-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4aa55-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aa55-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aa55-140">-WhatIf</span></span>
<span data-ttu-id="4aa55-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4aa55-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aa55-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4aa55-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aa55-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa55-143">CommonParameters</span></span>
<span data-ttu-id="4aa55-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4aa55-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aa55-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aa55-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aa55-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4aa55-146">INPUTS</span></span>

### <span data-ttu-id="4aa55-147">System. String</span><span class="sxs-lookup"><span data-stu-id="4aa55-147">System.String</span></span>

### <span data-ttu-id="4aa55-148">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="4aa55-148">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="4aa55-149">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4aa55-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4aa55-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4aa55-150">OUTPUTS</span></span>

### <span data-ttu-id="4aa55-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4aa55-151">System.Boolean</span></span>

## <span data-ttu-id="4aa55-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="4aa55-152">NOTES</span></span>

## <span data-ttu-id="4aa55-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4aa55-153">RELATED LINKS</span></span>
