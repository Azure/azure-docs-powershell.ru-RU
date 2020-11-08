---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: 550668a6ae5b1a7f870410961d32f9b53d4947a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065406"
---
# <span data-ttu-id="03fa0-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="03fa0-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="03fa0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="03fa0-103">Удаляет раздел сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="03fa0-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="03fa0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03fa0-104">SYNTAX</span></span>

### <span data-ttu-id="03fa0-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="03fa0-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03fa0-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="03fa0-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03fa0-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03fa0-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03fa0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03fa0-108">DESCRIPTION</span></span>
<span data-ttu-id="03fa0-109">Удаляет раздел сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="03fa0-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="03fa0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03fa0-110">EXAMPLES</span></span>

### <span data-ttu-id="03fa0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="03fa0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="03fa0-112">Удаляет раздел элемент1 сетки событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="03fa0-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="03fa0-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="03fa0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="03fa0-114">Удаляет раздел элемент1 сетки событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="03fa0-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="03fa0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03fa0-115">PARAMETERS</span></span>

### <span data-ttu-id="03fa0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03fa0-116">-DefaultProfile</span></span>
<span data-ttu-id="03fa0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="03fa0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03fa0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03fa0-118">-InputObject</span></span>
<span data-ttu-id="03fa0-119">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="03fa0-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="03fa0-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="03fa0-120">-Name</span></span>
<span data-ttu-id="03fa0-121">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="03fa0-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="03fa0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03fa0-122">-PassThru</span></span>
<span data-ttu-id="03fa0-123">Возвращает состояние операции удаления.</span><span class="sxs-lookup"><span data-stu-id="03fa0-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="03fa0-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="03fa0-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="03fa0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03fa0-125">-ResourceGroupName</span></span>
<span data-ttu-id="03fa0-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="03fa0-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="03fa0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03fa0-127">-ResourceId</span></span>
<span data-ttu-id="03fa0-128">EventGrid темы (ResourceID).</span><span class="sxs-lookup"><span data-stu-id="03fa0-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="03fa0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03fa0-129">-Confirm</span></span>
<span data-ttu-id="03fa0-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="03fa0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03fa0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03fa0-131">-WhatIf</span></span>
<span data-ttu-id="03fa0-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="03fa0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03fa0-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="03fa0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03fa0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03fa0-134">CommonParameters</span></span>
<span data-ttu-id="03fa0-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="03fa0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03fa0-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03fa0-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03fa0-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03fa0-137">INPUTS</span></span>

### <span data-ttu-id="03fa0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="03fa0-138">System.String</span></span>

### <span data-ttu-id="03fa0-139">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="03fa0-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="03fa0-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03fa0-140">OUTPUTS</span></span>

### <span data-ttu-id="03fa0-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03fa0-141">System.Boolean</span></span>

## <span data-ttu-id="03fa0-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="03fa0-142">NOTES</span></span>

## <span data-ttu-id="03fa0-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03fa0-143">RELATED LINKS</span></span>
