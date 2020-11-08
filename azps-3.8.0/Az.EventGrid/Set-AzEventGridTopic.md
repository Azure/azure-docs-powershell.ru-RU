---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: edccb9bf46a75c8a9f6fe0c577a87e13d11a2ba9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065403"
---
# <span data-ttu-id="18cd1-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="18cd1-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="18cd1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="18cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="18cd1-103">Задает свойства раздела сетки событий.</span><span class="sxs-lookup"><span data-stu-id="18cd1-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="18cd1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="18cd1-104">SYNTAX</span></span>

### <span data-ttu-id="18cd1-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="18cd1-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18cd1-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="18cd1-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18cd1-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18cd1-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18cd1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18cd1-108">DESCRIPTION</span></span>
<span data-ttu-id="18cd1-109">Задает свойства раздела сетки событий.</span><span class="sxs-lookup"><span data-stu-id="18cd1-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="18cd1-110">Это можно использовать для замены тегов в разделе сетки событий.</span><span class="sxs-lookup"><span data-stu-id="18cd1-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="18cd1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="18cd1-111">EXAMPLES</span></span>

### <span data-ttu-id="18cd1-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="18cd1-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="18cd1-113">Задает свойства сетки событий \` в разделе элемент1 \` в группе ресурсов \` MyResourceGroupName \` , чтобы заменить Теги заданными тегами "Department" и "Environment".</span><span class="sxs-lookup"><span data-stu-id="18cd1-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="18cd1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="18cd1-114">PARAMETERS</span></span>

### <span data-ttu-id="18cd1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18cd1-115">-DefaultProfile</span></span>
<span data-ttu-id="18cd1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="18cd1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18cd1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18cd1-117">-InputObject</span></span>
<span data-ttu-id="18cd1-118">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="18cd1-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="18cd1-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="18cd1-119">-Name</span></span>
<span data-ttu-id="18cd1-120">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="18cd1-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="18cd1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18cd1-121">-ResourceGroupName</span></span>
<span data-ttu-id="18cd1-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="18cd1-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="18cd1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18cd1-123">-ResourceId</span></span>
<span data-ttu-id="18cd1-124">EventGrid темы (ResourceID).</span><span class="sxs-lookup"><span data-stu-id="18cd1-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="18cd1-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="18cd1-125">-Tag</span></span>
<span data-ttu-id="18cd1-126">Хэш-таблицы, представляющие тег ресурса.</span><span class="sxs-lookup"><span data-stu-id="18cd1-126">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18cd1-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18cd1-127">-Confirm</span></span>
<span data-ttu-id="18cd1-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="18cd1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18cd1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18cd1-129">-WhatIf</span></span>
<span data-ttu-id="18cd1-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="18cd1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18cd1-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="18cd1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18cd1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18cd1-132">CommonParameters</span></span>
<span data-ttu-id="18cd1-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="18cd1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18cd1-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18cd1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18cd1-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="18cd1-135">INPUTS</span></span>

### <span data-ttu-id="18cd1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="18cd1-136">System.String</span></span>

### <span data-ttu-id="18cd1-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="18cd1-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="18cd1-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="18cd1-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="18cd1-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="18cd1-139">OUTPUTS</span></span>

### <span data-ttu-id="18cd1-140">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="18cd1-140">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="18cd1-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="18cd1-141">NOTES</span></span>

## <span data-ttu-id="18cd1-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18cd1-142">RELATED LINKS</span></span>
