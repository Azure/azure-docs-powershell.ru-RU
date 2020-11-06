---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: 509f10432139ca0f2d9aaca216f22d998b7963a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569503"
---
# <span data-ttu-id="0b41f-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="0b41f-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="0b41f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0b41f-102">SYNOPSIS</span></span>
<span data-ttu-id="0b41f-103">Задайте свойства раздела сетки событий.</span><span class="sxs-lookup"><span data-stu-id="0b41f-103">Set the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b41f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0b41f-104">SYNTAX</span></span>

### <span data-ttu-id="0b41f-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0b41f-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b41f-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b41f-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b41f-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b41f-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b41f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b41f-108">DESCRIPTION</span></span>
<span data-ttu-id="0b41f-109">Задайте свойства раздела сетки событий.</span><span class="sxs-lookup"><span data-stu-id="0b41f-109">Set the properties of an Event Grid topic.</span></span> <span data-ttu-id="0b41f-110">Это можно использовать для замены тегов в разделе сетки событий.</span><span class="sxs-lookup"><span data-stu-id="0b41f-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="0b41f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0b41f-111">EXAMPLES</span></span>

### <span data-ttu-id="0b41f-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0b41f-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="0b41f-113">Задает свойства сетки событий \` в разделе элемент1 \` в группе ресурсов \` MyResourceGroupName \` , чтобы заменить Теги заданными тегами "Department" и "Environment".</span><span class="sxs-lookup"><span data-stu-id="0b41f-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="0b41f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0b41f-114">PARAMETERS</span></span>

### <span data-ttu-id="0b41f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b41f-115">-InputObject</span></span>
<span data-ttu-id="0b41f-116">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="0b41f-116">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="0b41f-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0b41f-117">-Name</span></span>
<span data-ttu-id="0b41f-118">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="0b41f-118">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="0b41f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b41f-119">-ResourceGroupName</span></span>
<span data-ttu-id="0b41f-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b41f-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="0b41f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b41f-121">-ResourceId</span></span>
<span data-ttu-id="0b41f-122">EventGrid темы (ResourceID).</span><span class="sxs-lookup"><span data-stu-id="0b41f-122">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="0b41f-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="0b41f-123">-Tag</span></span>
<span data-ttu-id="0b41f-124">Хэш-таблицы, представляющие тег ресурса.</span><span class="sxs-lookup"><span data-stu-id="0b41f-124">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="0b41f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b41f-125">-Confirm</span></span>
<span data-ttu-id="0b41f-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0b41f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b41f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b41f-127">-WhatIf</span></span>
<span data-ttu-id="0b41f-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0b41f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b41f-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0b41f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b41f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b41f-130">-DefaultProfile</span></span>
<span data-ttu-id="0b41f-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0b41f-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b41f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b41f-132">CommonParameters</span></span>
<span data-ttu-id="0b41f-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0b41f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b41f-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b41f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b41f-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0b41f-135">INPUTS</span></span>

### <span data-ttu-id="0b41f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0b41f-136">System.String</span></span>
<span data-ttu-id="0b41f-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b41f-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0b41f-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b41f-138">OUTPUTS</span></span>

### <span data-ttu-id="0b41f-139">Microsoft. Azure. Management. EventGrid. Models. Topic</span><span class="sxs-lookup"><span data-stu-id="0b41f-139">Microsoft.Azure.Management.EventGrid.Models.Topic</span></span>

## <span data-ttu-id="0b41f-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="0b41f-140">NOTES</span></span>

## <span data-ttu-id="0b41f-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b41f-141">RELATED LINKS</span></span>

