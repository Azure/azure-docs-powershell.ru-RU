---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
ms.openlocfilehash: badbb8c392e053b1f8d994164183bd593843629e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565442"
---
# <span data-ttu-id="09419-101">New-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="09419-101">New-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="09419-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09419-102">SYNOPSIS</span></span>
<span data-ttu-id="09419-103">Повторное создание ключа общего доступа для раздела сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="09419-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09419-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09419-104">SYNTAX</span></span>

### <span data-ttu-id="09419-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="09419-105">TopicNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09419-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09419-106">TopicInputObjectParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09419-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="09419-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09419-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09419-108">DESCRIPTION</span></span>
<span data-ttu-id="09419-109">Повторное создание ключа общего доступа для раздела сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="09419-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="09419-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09419-110">EXAMPLES</span></span>

### <span data-ttu-id="09419-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="09419-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="09419-112">Повторное создание ключа, соответствующего ключу \' Key1 "\ из сетки событий" \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="09419-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="09419-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="09419-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzureRmEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="09419-114">Повторное создание ключа, соответствующего ключу \' Key1 "\ из сетки событий" \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="09419-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="09419-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09419-115">PARAMETERS</span></span>

### <span data-ttu-id="09419-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09419-116">-DefaultProfile</span></span>
<span data-ttu-id="09419-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="09419-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09419-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09419-118">-InputObject</span></span>
<span data-ttu-id="09419-119">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="09419-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="09419-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="09419-120">-KeyName</span></span>
<span data-ttu-id="09419-121">Имя ключа, который должен быть повторно сгенерирован</span><span class="sxs-lookup"><span data-stu-id="09419-121">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="09419-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09419-122">-ResourceGroupName</span></span>
<span data-ttu-id="09419-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="09419-123">Resource group name.</span></span>

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

### <span data-ttu-id="09419-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09419-124">-ResourceId</span></span>
<span data-ttu-id="09419-125">Идентификатор ресурса, представляющий раздел сетки событий.</span><span class="sxs-lookup"><span data-stu-id="09419-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="09419-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="09419-126">-TopicName</span></span>
<span data-ttu-id="09419-127">Название темы.</span><span class="sxs-lookup"><span data-stu-id="09419-127">The name of the topic.</span></span>

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

### <span data-ttu-id="09419-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09419-128">-Confirm</span></span>
<span data-ttu-id="09419-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="09419-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09419-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09419-130">-WhatIf</span></span>
<span data-ttu-id="09419-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="09419-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09419-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="09419-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09419-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09419-133">CommonParameters</span></span>
<span data-ttu-id="09419-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09419-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09419-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09419-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09419-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09419-136">INPUTS</span></span>

### <span data-ttu-id="09419-137">System. String</span><span class="sxs-lookup"><span data-stu-id="09419-137">System.String</span></span>

### <span data-ttu-id="09419-138">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="09419-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="09419-139">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="09419-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="09419-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09419-140">OUTPUTS</span></span>

### <span data-ttu-id="09419-141">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="09419-141">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="09419-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="09419-142">NOTES</span></span>

## <span data-ttu-id="09419-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09419-143">RELATED LINKS</span></span>
