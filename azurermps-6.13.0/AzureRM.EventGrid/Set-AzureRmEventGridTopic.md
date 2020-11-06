---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/set-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: 384c05e6424ab7b8d4fbb01a0c4822b73702c419
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565438"
---
# <span data-ttu-id="f39d5-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="f39d5-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="f39d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f39d5-102">SYNOPSIS</span></span>
<span data-ttu-id="f39d5-103">Задает свойства раздела сетки событий.</span><span class="sxs-lookup"><span data-stu-id="f39d5-103">Sets the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f39d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f39d5-104">SYNTAX</span></span>

### <span data-ttu-id="f39d5-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f39d5-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f39d5-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f39d5-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f39d5-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f39d5-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f39d5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f39d5-108">DESCRIPTION</span></span>
<span data-ttu-id="f39d5-109">Задает свойства раздела сетки событий.</span><span class="sxs-lookup"><span data-stu-id="f39d5-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="f39d5-110">Это можно использовать для замены тегов в разделе сетки событий.</span><span class="sxs-lookup"><span data-stu-id="f39d5-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="f39d5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f39d5-111">EXAMPLES</span></span>

### <span data-ttu-id="f39d5-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f39d5-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="f39d5-113">Задает свойства сетки событий \` в разделе элемент1 \` в группе ресурсов \` MyResourceGroupName \` , чтобы заменить Теги заданными тегами "Department" и "Environment".</span><span class="sxs-lookup"><span data-stu-id="f39d5-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="f39d5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f39d5-114">PARAMETERS</span></span>

### <span data-ttu-id="f39d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f39d5-115">-DefaultProfile</span></span>
<span data-ttu-id="f39d5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f39d5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f39d5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f39d5-117">-InputObject</span></span>
<span data-ttu-id="f39d5-118">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="f39d5-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="f39d5-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f39d5-119">-Name</span></span>
<span data-ttu-id="f39d5-120">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="f39d5-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="f39d5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f39d5-121">-ResourceGroupName</span></span>
<span data-ttu-id="f39d5-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f39d5-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="f39d5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f39d5-123">-ResourceId</span></span>
<span data-ttu-id="f39d5-124">EventGrid темы (ResourceID).</span><span class="sxs-lookup"><span data-stu-id="f39d5-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="f39d5-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="f39d5-125">-Tag</span></span>
<span data-ttu-id="f39d5-126">Хэш-таблицы, представляющие тег ресурса.</span><span class="sxs-lookup"><span data-stu-id="f39d5-126">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="f39d5-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f39d5-127">-Confirm</span></span>
<span data-ttu-id="f39d5-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f39d5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f39d5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f39d5-129">-WhatIf</span></span>
<span data-ttu-id="f39d5-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f39d5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f39d5-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f39d5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f39d5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f39d5-132">CommonParameters</span></span>
<span data-ttu-id="f39d5-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f39d5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f39d5-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f39d5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f39d5-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f39d5-135">INPUTS</span></span>

### <span data-ttu-id="f39d5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f39d5-136">System.String</span></span>

### <span data-ttu-id="f39d5-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="f39d5-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="f39d5-138">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f39d5-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f39d5-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f39d5-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f39d5-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f39d5-140">OUTPUTS</span></span>

### <span data-ttu-id="f39d5-141">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="f39d5-141">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="f39d5-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f39d5-142">NOTES</span></span>

## <span data-ttu-id="f39d5-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f39d5-143">RELATED LINKS</span></span>
