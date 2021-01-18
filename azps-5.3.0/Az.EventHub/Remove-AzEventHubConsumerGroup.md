---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: f84464d366ae84cf0a83ecc616a80b90475af8d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507493"
---
# <span data-ttu-id="5cd60-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5cd60-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="5cd60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cd60-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd60-103">Удаляет указанную группу "Концентраторы событий".</span><span class="sxs-lookup"><span data-stu-id="5cd60-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="5cd60-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5cd60-104">SYNTAX</span></span>

### <span data-ttu-id="5cd60-105">ConsumergroupPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5cd60-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5cd60-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5cd60-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cd60-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cd60-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cd60-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cd60-108">DESCRIPTION</span></span>
<span data-ttu-id="5cd60-109">Этот Remove-AzEventHubConsumerGroup удаляет указанную группу потребителей из данного Концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="5cd60-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="5cd60-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5cd60-110">EXAMPLES</span></span>

### <span data-ttu-id="5cd60-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5cd60-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="5cd60-112">Удаляет группу пользователей \` MyConsumerGroupName из Концентратора событий \` \` MyEventHubName в области имен \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="5cd60-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="5cd60-113">Пример 2. InputObject — использование переменной</span><span class="sxs-lookup"><span data-stu-id="5cd60-113">Example 2: InputObject - Using Variable</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="5cd60-114">Пример 3. InputObject — использование piping</span><span class="sxs-lookup"><span data-stu-id="5cd60-114">Example 3: InputObject - Using Piping</span></span>
```powershell
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="5cd60-115">Пример 4. ResourceId с переменной</span><span class="sxs-lookup"><span data-stu-id="5cd60-115">Example 4: ResourceId Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="5cd60-116">Пример 5. Строка "ИД Ресурса"</span><span class="sxs-lookup"><span data-stu-id="5cd60-116">Example 5: ResourceId Using string</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="5cd60-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cd60-117">PARAMETERS</span></span>

### <span data-ttu-id="5cd60-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5cd60-118">-AsJob</span></span>
<span data-ttu-id="5cd60-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5cd60-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5cd60-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd60-120">-DefaultProfile</span></span>
<span data-ttu-id="5cd60-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5cd60-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cd60-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="5cd60-122">-EventHub</span></span>
<span data-ttu-id="5cd60-123">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="5cd60-123">EventHub Name</span></span>

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

### <span data-ttu-id="5cd60-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cd60-124">-InputObject</span></span>
<span data-ttu-id="5cd60-125">Объект ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5cd60-125">ConsumerGroup Object</span></span>

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

### <span data-ttu-id="5cd60-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5cd60-126">-Name</span></span>
<span data-ttu-id="5cd60-127">Имя группы потребителей</span><span class="sxs-lookup"><span data-stu-id="5cd60-127">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="5cd60-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5cd60-128">-Namespace</span></span>
<span data-ttu-id="5cd60-129">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="5cd60-129">Namespace Name</span></span>

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

### <span data-ttu-id="5cd60-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cd60-130">-PassThru</span></span>
<span data-ttu-id="5cd60-131">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="5cd60-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="5cd60-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cd60-132">-ResourceGroupName</span></span>
<span data-ttu-id="5cd60-133">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5cd60-133">Resource Group Name</span></span>

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

### <span data-ttu-id="5cd60-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cd60-134">-ResourceId</span></span>
<span data-ttu-id="5cd60-135">ConsumerGroup Resource Id</span><span class="sxs-lookup"><span data-stu-id="5cd60-135">ConsumerGroup Resource Id</span></span>

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

### <span data-ttu-id="5cd60-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cd60-136">-Confirm</span></span>
<span data-ttu-id="5cd60-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5cd60-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cd60-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cd60-138">-WhatIf</span></span>
<span data-ttu-id="5cd60-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cd60-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cd60-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5cd60-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cd60-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd60-141">CommonParameters</span></span>
<span data-ttu-id="5cd60-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cd60-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd60-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cd60-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd60-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5cd60-144">INPUTS</span></span>

### <span data-ttu-id="5cd60-145">System.String</span><span class="sxs-lookup"><span data-stu-id="5cd60-145">System.String</span></span>

### <span data-ttu-id="5cd60-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="5cd60-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="5cd60-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5cd60-147">OUTPUTS</span></span>

### <span data-ttu-id="5cd60-148">System.Void</span><span class="sxs-lookup"><span data-stu-id="5cd60-148">System.Void</span></span>

## <span data-ttu-id="5cd60-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5cd60-149">NOTES</span></span>

## <span data-ttu-id="5cd60-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5cd60-150">RELATED LINKS</span></span>
