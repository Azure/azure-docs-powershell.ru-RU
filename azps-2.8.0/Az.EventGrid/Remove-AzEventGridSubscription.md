---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: 2e2abe03d0df4ccf662f99945c45e837669a1de9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720982"
---
# <span data-ttu-id="8b0a3-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8b0a3-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="8b0a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b0a3-102">SYNOPSIS</span></span>
<span data-ttu-id="8b0a3-103">Удаляет подписку на событие сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="8b0a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b0a3-104">SYNTAX</span></span>

### <span data-ttu-id="8b0a3-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b0a3-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b0a3-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b0a3-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b0a3-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b0a3-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b0a3-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b0a3-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b0a3-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b0a3-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b0a3-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b0a3-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b0a3-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b0a3-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b0a3-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b0a3-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b0a3-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b0a3-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b0a3-114">DESCRIPTION</span></span>
<span data-ttu-id="8b0a3-115">Удаляет подписку на событие сетки событий Azure для таблицы событий Azure: ресурс, подписку или группу ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="8b0a3-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b0a3-116">EXAMPLES</span></span>

### <span data-ttu-id="8b0a3-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b0a3-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8b0a3-118">Удаляет подписку на события \` EventSubscription1 в \` разделе сетки событий Azure \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="8b0a3-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8b0a3-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8b0a3-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8b0a3-120">Удаляет подписку на событие \` EventSubscription1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="8b0a3-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8b0a3-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8b0a3-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8b0a3-122">Удаляет подписку на событие \` EventSubscription1 \` к подписке по умолчанию Azure.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="8b0a3-123">Пример 4</span><span class="sxs-lookup"><span data-stu-id="8b0a3-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8b0a3-124">Удаляет подписку на событие \` EventSubscription1 \` в пространство имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="8b0a3-125">Пример 5</span><span class="sxs-lookup"><span data-stu-id="8b0a3-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8b0a3-126">Удаляет подписку на событие \` EventSubscription1 \` в разделе сетки событий.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="8b0a3-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b0a3-127">PARAMETERS</span></span>

### <span data-ttu-id="8b0a3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b0a3-128">-DefaultProfile</span></span>
<span data-ttu-id="8b0a3-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8b0a3-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b0a3-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="8b0a3-130">-DomainInputObject</span></span>
<span data-ttu-id="8b0a3-131">Объект Domain EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-131">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="8b0a3-132">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="8b0a3-132">-DomainName</span></span>
<span data-ttu-id="8b0a3-133">EventGrid Domain Name (доменное имя).</span><span class="sxs-lookup"><span data-stu-id="8b0a3-133">EventGrid domain name.</span></span>

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

### <span data-ttu-id="8b0a3-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="8b0a3-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="8b0a3-135">Объект темы домена EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-135">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="8b0a3-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="8b0a3-136">-DomainTopicName</span></span>
<span data-ttu-id="8b0a3-137">Доменное имя EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-137">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="8b0a3-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8b0a3-138">-EventSubscriptionName</span></span>
<span data-ttu-id="8b0a3-139">Имя подписки на событие, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-139">Name of the event subscription that needs to be removed.</span></span>

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

### <span data-ttu-id="8b0a3-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b0a3-140">-InputObject</span></span>
<span data-ttu-id="8b0a3-141">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-141">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="8b0a3-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b0a3-142">-PassThru</span></span>
<span data-ttu-id="8b0a3-143">Возвращает состояние операции удаления.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="8b0a3-144">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8b0a3-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b0a3-145">-ResourceGroupName</span></span>
<span data-ttu-id="8b0a3-146">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-146">Resource Group Name.</span></span>

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

### <span data-ttu-id="8b0a3-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b0a3-147">-ResourceId</span></span>
<span data-ttu-id="8b0a3-148">Идентификатор ресурса, для которого требуется удалить подписку на события.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="8b0a3-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="8b0a3-149">-TopicName</span></span>
<span data-ttu-id="8b0a3-150">Название темы сетки событий.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-150">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="8b0a3-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b0a3-151">-Confirm</span></span>
<span data-ttu-id="8b0a3-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b0a3-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b0a3-153">-WhatIf</span></span>
<span data-ttu-id="8b0a3-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b0a3-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b0a3-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b0a3-156">CommonParameters</span></span>
<span data-ttu-id="8b0a3-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b0a3-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b0a3-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b0a3-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b0a3-159">INPUTS</span></span>

### <span data-ttu-id="8b0a3-160">System. String</span><span class="sxs-lookup"><span data-stu-id="8b0a3-160">System.String</span></span>

### <span data-ttu-id="8b0a3-161">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="8b0a3-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="8b0a3-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="8b0a3-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="8b0a3-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8b0a3-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="8b0a3-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b0a3-164">OUTPUTS</span></span>

### <span data-ttu-id="8b0a3-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b0a3-165">System.Boolean</span></span>

## <span data-ttu-id="8b0a3-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b0a3-166">NOTES</span></span>

## <span data-ttu-id="8b0a3-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b0a3-167">RELATED LINKS</span></span>
