---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: 3cc0d587713bf287d9cc3bfa720d867e81370a8f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720980"
---
# <span data-ttu-id="5b51c-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="5b51c-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="5b51c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b51c-102">SYNOPSIS</span></span>
<span data-ttu-id="5b51c-103">Удаляет раздел сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="5b51c-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="5b51c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b51c-104">SYNTAX</span></span>

### <span data-ttu-id="5b51c-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5b51c-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b51c-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b51c-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b51c-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b51c-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b51c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b51c-108">DESCRIPTION</span></span>
<span data-ttu-id="5b51c-109">Удаляет раздел сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="5b51c-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="5b51c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b51c-110">EXAMPLES</span></span>

### <span data-ttu-id="5b51c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5b51c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="5b51c-112">Удаляет раздел элемент1 сетки событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="5b51c-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5b51c-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5b51c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="5b51c-114">Удаляет раздел элемент1 сетки событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="5b51c-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="5b51c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b51c-115">PARAMETERS</span></span>

### <span data-ttu-id="5b51c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b51c-116">-DefaultProfile</span></span>
<span data-ttu-id="5b51c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5b51c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b51c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b51c-118">-InputObject</span></span>
<span data-ttu-id="5b51c-119">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="5b51c-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b51c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b51c-120">-Name</span></span>
<span data-ttu-id="5b51c-121">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="5b51c-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b51c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b51c-122">-PassThru</span></span>
<span data-ttu-id="5b51c-123">Возвращает состояние операции удаления.</span><span class="sxs-lookup"><span data-stu-id="5b51c-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="5b51c-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5b51c-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5b51c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b51c-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b51c-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b51c-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b51c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b51c-127">-ResourceId</span></span>
<span data-ttu-id="5b51c-128">EventGrid темы (ResourceID).</span><span class="sxs-lookup"><span data-stu-id="5b51c-128">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b51c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b51c-129">-Confirm</span></span>
<span data-ttu-id="5b51c-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5b51c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b51c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b51c-131">-WhatIf</span></span>
<span data-ttu-id="5b51c-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5b51c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b51c-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5b51c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b51c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b51c-134">CommonParameters</span></span>
<span data-ttu-id="5b51c-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b51c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b51c-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b51c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b51c-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b51c-137">INPUTS</span></span>

### <span data-ttu-id="5b51c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5b51c-138">System.String</span></span>

### <span data-ttu-id="5b51c-139">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="5b51c-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="5b51c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b51c-140">OUTPUTS</span></span>

### <span data-ttu-id="5b51c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b51c-141">System.Boolean</span></span>

## <span data-ttu-id="5b51c-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b51c-142">NOTES</span></span>

## <span data-ttu-id="5b51c-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b51c-143">RELATED LINKS</span></span>
