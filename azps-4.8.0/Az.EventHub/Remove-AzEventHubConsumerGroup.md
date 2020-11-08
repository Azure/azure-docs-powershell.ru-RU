---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: f84464d366ae84cf0a83ecc616a80b90475af8d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243589"
---
# <span data-ttu-id="7a90d-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7a90d-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="7a90d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a90d-102">SYNOPSIS</span></span>
<span data-ttu-id="7a90d-103">Удаляет указанную группу потребителей концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="7a90d-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="7a90d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a90d-104">SYNTAX</span></span>

### <span data-ttu-id="7a90d-105">ConsumergroupPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a90d-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a90d-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7a90d-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a90d-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a90d-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a90d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a90d-108">DESCRIPTION</span></span>
<span data-ttu-id="7a90d-109">Командлет Remove-AzEventHubConsumerGroup удаляет указанную группу потребителей из заданного концентратора событий и удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="7a90d-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="7a90d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a90d-110">EXAMPLES</span></span>

### <span data-ttu-id="7a90d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7a90d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="7a90d-112">Удаляет группу потребителей \` MyConsumerGroupName \` из MyEventHubName концентратора событий \` с \` областью в \` \` пространство имен MyNamespaceName.</span><span class="sxs-lookup"><span data-stu-id="7a90d-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="7a90d-113">Пример 2: InputObject — использование переменной</span><span class="sxs-lookup"><span data-stu-id="7a90d-113">Example 2: InputObject - Using Variable</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="7a90d-114">Пример 3: InputObject-использование трубопроводов</span><span class="sxs-lookup"><span data-stu-id="7a90d-114">Example 3: InputObject - Using Piping</span></span>
```powershell
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="7a90d-115">Пример 4: ResourceId с помощью переменной</span><span class="sxs-lookup"><span data-stu-id="7a90d-115">Example 4: ResourceId Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="7a90d-116">Пример 5: ResourceId с помощью String</span><span class="sxs-lookup"><span data-stu-id="7a90d-116">Example 5: ResourceId Using string</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="7a90d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a90d-117">PARAMETERS</span></span>

### <span data-ttu-id="7a90d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a90d-118">-AsJob</span></span>
<span data-ttu-id="7a90d-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7a90d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a90d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a90d-120">-DefaultProfile</span></span>
<span data-ttu-id="7a90d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a90d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a90d-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="7a90d-122">-EventHub</span></span>
<span data-ttu-id="7a90d-123">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="7a90d-123">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a90d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a90d-124">-InputObject</span></span>
<span data-ttu-id="7a90d-125">Объект ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7a90d-125">ConsumerGroup Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes
Parameter Sets: ConsumergroupInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a90d-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7a90d-126">-Name</span></span>
<span data-ttu-id="7a90d-127">Имя ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7a90d-127">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a90d-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7a90d-128">-Namespace</span></span>
<span data-ttu-id="7a90d-129">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="7a90d-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a90d-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a90d-130">-PassThru</span></span>
<span data-ttu-id="7a90d-131">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7a90d-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7a90d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a90d-132">-ResourceGroupName</span></span>
<span data-ttu-id="7a90d-133">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7a90d-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a90d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a90d-134">-ResourceId</span></span>
<span data-ttu-id="7a90d-135">Идентификатор ресурса ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7a90d-135">ConsumerGroup Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a90d-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a90d-136">-Confirm</span></span>
<span data-ttu-id="7a90d-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7a90d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a90d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a90d-138">-WhatIf</span></span>
<span data-ttu-id="7a90d-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7a90d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a90d-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7a90d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a90d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a90d-141">CommonParameters</span></span>
<span data-ttu-id="7a90d-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a90d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a90d-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a90d-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a90d-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a90d-144">INPUTS</span></span>

### <span data-ttu-id="7a90d-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7a90d-145">System.String</span></span>

### <span data-ttu-id="7a90d-146">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="7a90d-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="7a90d-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a90d-147">OUTPUTS</span></span>

### <span data-ttu-id="7a90d-148">System. void</span><span class="sxs-lookup"><span data-stu-id="7a90d-148">System.Void</span></span>

## <span data-ttu-id="7a90d-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a90d-149">NOTES</span></span>

## <span data-ttu-id="7a90d-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a90d-150">RELATED LINKS</span></span>
