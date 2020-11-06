---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
ms.openlocfilehash: bb9cd92ff614a944c144f056d8d59aa1d4239b25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569515"
---
# <span data-ttu-id="5536f-101">New-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="5536f-101">New-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="5536f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5536f-102">SYNOPSIS</span></span>
<span data-ttu-id="5536f-103">Повторное создание ключа общего доступа для раздела сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="5536f-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5536f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5536f-104">SYNTAX</span></span>

### <span data-ttu-id="5536f-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5536f-105">TopicNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5536f-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5536f-106">TopicInputObjectParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5536f-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5536f-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5536f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5536f-108">DESCRIPTION</span></span>
<span data-ttu-id="5536f-109">Повторное создание ключа общего доступа для раздела сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="5536f-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="5536f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5536f-110">EXAMPLES</span></span>

### <span data-ttu-id="5536f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5536f-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="5536f-112">Повторное создание ключа, соответствующего ключу \' Key1 "\ из сетки событий" \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="5536f-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5536f-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5536f-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzureRmEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="5536f-114">Повторное создание ключа, соответствующего ключу \' Key1 "\ из сетки событий" \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="5536f-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="5536f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5536f-115">PARAMETERS</span></span>

### <span data-ttu-id="5536f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5536f-116">-InputObject</span></span>
<span data-ttu-id="5536f-117">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="5536f-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="5536f-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="5536f-118">-KeyName</span></span>
<span data-ttu-id="5536f-119">Имя ключа, который должен быть повторно сгенерирован</span><span class="sxs-lookup"><span data-stu-id="5536f-119">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5536f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5536f-120">-ResourceGroupName</span></span>
<span data-ttu-id="5536f-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5536f-121">Resource group name.</span></span>

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

### <span data-ttu-id="5536f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5536f-122">-ResourceId</span></span>
<span data-ttu-id="5536f-123">Идентификатор ресурса, представляющий раздел сетки событий.</span><span class="sxs-lookup"><span data-stu-id="5536f-123">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="5536f-124">-TopicName</span><span class="sxs-lookup"><span data-stu-id="5536f-124">-TopicName</span></span>
<span data-ttu-id="5536f-125">Название темы.</span><span class="sxs-lookup"><span data-stu-id="5536f-125">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5536f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5536f-126">-Confirm</span></span>
<span data-ttu-id="5536f-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5536f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5536f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5536f-128">-WhatIf</span></span>
<span data-ttu-id="5536f-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5536f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5536f-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5536f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5536f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5536f-131">-DefaultProfile</span></span>
<span data-ttu-id="5536f-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5536f-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5536f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5536f-133">CommonParameters</span></span>
<span data-ttu-id="5536f-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5536f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5536f-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5536f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5536f-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5536f-136">INPUTS</span></span>

### <span data-ttu-id="5536f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5536f-137">System.String</span></span>

## <span data-ttu-id="5536f-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5536f-138">OUTPUTS</span></span>

### <span data-ttu-id="5536f-139">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="5536f-139">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="5536f-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="5536f-140">NOTES</span></span>

## <span data-ttu-id="5536f-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5536f-141">RELATED LINKS</span></span>

