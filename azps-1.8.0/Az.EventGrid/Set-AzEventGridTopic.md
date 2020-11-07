---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: bcba056777cd9a5eef42799b170c2dad69c8bbf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730863"
---
# <span data-ttu-id="e206e-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="e206e-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="e206e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e206e-102">SYNOPSIS</span></span>
<span data-ttu-id="e206e-103">Задает свойства раздела сетки событий.</span><span class="sxs-lookup"><span data-stu-id="e206e-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="e206e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e206e-104">SYNTAX</span></span>

### <span data-ttu-id="e206e-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e206e-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e206e-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e206e-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e206e-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e206e-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e206e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e206e-108">DESCRIPTION</span></span>
<span data-ttu-id="e206e-109">Задает свойства раздела сетки событий.</span><span class="sxs-lookup"><span data-stu-id="e206e-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="e206e-110">Это можно использовать для замены тегов в разделе сетки событий.</span><span class="sxs-lookup"><span data-stu-id="e206e-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="e206e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e206e-111">EXAMPLES</span></span>

### <span data-ttu-id="e206e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e206e-112">Example 1</span></span>
```
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="e206e-113">Задает свойства сетки событий \` в разделе элемент1 \` в группе ресурсов \` MyResourceGroupName \` , чтобы заменить Теги заданными тегами "Department" и "Environment".</span><span class="sxs-lookup"><span data-stu-id="e206e-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="e206e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e206e-114">PARAMETERS</span></span>

### <span data-ttu-id="e206e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e206e-115">-DefaultProfile</span></span>
<span data-ttu-id="e206e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e206e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e206e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e206e-117">-InputObject</span></span>
<span data-ttu-id="e206e-118">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="e206e-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="e206e-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e206e-119">-Name</span></span>
<span data-ttu-id="e206e-120">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="e206e-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="e206e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e206e-121">-ResourceGroupName</span></span>
<span data-ttu-id="e206e-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e206e-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="e206e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e206e-123">-ResourceId</span></span>
<span data-ttu-id="e206e-124">EventGrid темы (ResourceID).</span><span class="sxs-lookup"><span data-stu-id="e206e-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="e206e-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="e206e-125">-Tag</span></span>
<span data-ttu-id="e206e-126">Хэш-таблицы, представляющие тег ресурса.</span><span class="sxs-lookup"><span data-stu-id="e206e-126">Hashtables which represents resource Tag.</span></span>

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

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e206e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e206e-127">-Confirm</span></span>
<span data-ttu-id="e206e-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e206e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e206e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e206e-129">-WhatIf</span></span>
<span data-ttu-id="e206e-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e206e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e206e-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e206e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e206e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e206e-132">CommonParameters</span></span>
<span data-ttu-id="e206e-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e206e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e206e-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e206e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e206e-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e206e-135">INPUTS</span></span>

### <span data-ttu-id="e206e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e206e-136">System.String</span></span>

### <span data-ttu-id="e206e-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="e206e-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="e206e-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e206e-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e206e-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e206e-139">OUTPUTS</span></span>

### <span data-ttu-id="e206e-140">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="e206e-140">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="e206e-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="e206e-141">NOTES</span></span>

## <span data-ttu-id="e206e-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e206e-142">RELATED LINKS</span></span>
