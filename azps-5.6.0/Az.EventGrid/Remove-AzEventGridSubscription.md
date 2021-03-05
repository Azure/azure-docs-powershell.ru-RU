---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: 1625e3325164156b1809640c54d4b75698ae7363
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991192"
---
# <span data-ttu-id="6bd01-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6bd01-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="6bd01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bd01-102">SYNOPSIS</span></span>
<span data-ttu-id="6bd01-103">Удаляет подписку на событие сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="6bd01-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="6bd01-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6bd01-104">SYNTAX</span></span>

### <span data-ttu-id="6bd01-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6bd01-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bd01-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bd01-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bd01-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bd01-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bd01-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bd01-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bd01-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bd01-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bd01-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bd01-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6bd01-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bd01-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bd01-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bd01-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bd01-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bd01-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bd01-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bd01-114">DESCRIPTION</span></span>
<span data-ttu-id="6bd01-115">Удаляет подписку на события сетки событий Azure для темы сетки событий Azure, ресурса, подписки Azure или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6bd01-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="6bd01-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6bd01-116">EXAMPLES</span></span>

### <span data-ttu-id="6bd01-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6bd01-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="6bd01-118">Удаляет подписку на событие EventSubscription1 в раздел Azure Event Grid Topic1 в группе ресурсов \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="6bd01-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6bd01-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6bd01-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="6bd01-120">Удаляет подписку на \` событие EventSubscription1 \` для группы ресурсов \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="6bd01-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6bd01-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6bd01-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="6bd01-122">Удаляет подписку на \` событие EventSubscription1 \` в стандартную подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="6bd01-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="6bd01-123">Пример 4</span><span class="sxs-lookup"><span data-stu-id="6bd01-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="6bd01-124">Удаляет подписку на \` событие EventSubscription1 \` в пространство имен Концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="6bd01-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="6bd01-125">Пример 5</span><span class="sxs-lookup"><span data-stu-id="6bd01-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="6bd01-126">Удаляет подписку на \` событие EventSubscription1 \` в раздел сетки событий.</span><span class="sxs-lookup"><span data-stu-id="6bd01-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="6bd01-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bd01-127">PARAMETERS</span></span>

### <span data-ttu-id="6bd01-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bd01-128">-DefaultProfile</span></span>
<span data-ttu-id="6bd01-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6bd01-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bd01-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="6bd01-130">-DomainInputObject</span></span>
<span data-ttu-id="6bd01-131">Объект EventGrid Domain.</span><span class="sxs-lookup"><span data-stu-id="6bd01-131">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd01-132">-DomainName</span><span class="sxs-lookup"><span data-stu-id="6bd01-132">-DomainName</span></span>
<span data-ttu-id="6bd01-133">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="6bd01-133">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd01-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="6bd01-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="6bd01-135">Объект EventGrid Domain Topic.</span><span class="sxs-lookup"><span data-stu-id="6bd01-135">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd01-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="6bd01-136">-DomainTopicName</span></span>
<span data-ttu-id="6bd01-137">Имя темы домена EventGrid.</span><span class="sxs-lookup"><span data-stu-id="6bd01-137">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd01-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="6bd01-138">-EventSubscriptionName</span></span>
<span data-ttu-id="6bd01-139">Название подписки на событие, которое необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="6bd01-139">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet, DomainNameParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd01-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bd01-140">-InputObject</span></span>
<span data-ttu-id="6bd01-141">Объект EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="6bd01-141">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd01-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bd01-142">-PassThru</span></span>
<span data-ttu-id="6bd01-143">Возвращает состояние операции удаления.</span><span class="sxs-lookup"><span data-stu-id="6bd01-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="6bd01-144">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6bd01-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6bd01-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bd01-145">-ResourceGroupName</span></span>
<span data-ttu-id="6bd01-146">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6bd01-146">Resource Group Name.</span></span>

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
Parameter Sets: TopicNameParameterSet, DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd01-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bd01-147">-ResourceId</span></span>
<span data-ttu-id="6bd01-148">Идентификатор ресурса, подписку на событие которого необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="6bd01-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="6bd01-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="6bd01-149">-TopicName</span></span>
<span data-ttu-id="6bd01-150">Название темы сетки событий.</span><span class="sxs-lookup"><span data-stu-id="6bd01-150">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="6bd01-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bd01-151">-Confirm</span></span>
<span data-ttu-id="6bd01-152">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6bd01-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bd01-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bd01-153">-WhatIf</span></span>
<span data-ttu-id="6bd01-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bd01-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bd01-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6bd01-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bd01-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bd01-156">CommonParameters</span></span>
<span data-ttu-id="6bd01-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bd01-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bd01-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bd01-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bd01-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6bd01-159">INPUTS</span></span>

### <span data-ttu-id="6bd01-160">System.String</span><span class="sxs-lookup"><span data-stu-id="6bd01-160">System.String</span></span>

### <span data-ttu-id="6bd01-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="6bd01-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="6bd01-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="6bd01-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="6bd01-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6bd01-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="6bd01-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6bd01-164">OUTPUTS</span></span>

### <span data-ttu-id="6bd01-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6bd01-165">System.Boolean</span></span>

## <span data-ttu-id="6bd01-166">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6bd01-166">NOTES</span></span>

## <span data-ttu-id="6bd01-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6bd01-167">RELATED LINKS</span></span>
