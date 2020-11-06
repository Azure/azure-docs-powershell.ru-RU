---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 3600d7523e95b937f20d9d0b97d677c5cf02ca0f
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93570483"
---
# <span data-ttu-id="51060-101">New-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="51060-101">New-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="51060-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51060-102">SYNOPSIS</span></span>
<span data-ttu-id="51060-103">Повторное создание ключа общего доступа для раздела сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="51060-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51060-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51060-104">SYNTAX</span></span>

### <span data-ttu-id="51060-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="51060-105">TopicNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51060-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51060-106">TopicInputObjectParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51060-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="51060-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51060-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51060-108">DESCRIPTION</span></span>
<span data-ttu-id="51060-109">Повторное создание ключа общего доступа для раздела сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="51060-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="51060-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51060-110">EXAMPLES</span></span>

### <span data-ttu-id="51060-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="51060-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="51060-112">Повторное создание ключа, соответствующего ключу \' Key1 "\ из сетки событий" \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="51060-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="51060-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="51060-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzureRmEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="51060-114">Повторное создание ключа, соответствующего ключу \' Key1 "\ из сетки событий" \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="51060-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="51060-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51060-115">PARAMETERS</span></span>

### <span data-ttu-id="51060-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51060-116">-DefaultProfile</span></span>
<span data-ttu-id="51060-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="51060-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51060-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51060-118">-InputObject</span></span>
<span data-ttu-id="51060-119">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="51060-119">EventGrid Topic object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51060-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="51060-120">-KeyName</span></span>
<span data-ttu-id="51060-121">Имя ключа, который должен быть повторно сгенерирован</span><span class="sxs-lookup"><span data-stu-id="51060-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51060-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51060-122">-ResourceGroupName</span></span>
<span data-ttu-id="51060-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="51060-123">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51060-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51060-124">-ResourceId</span></span>
<span data-ttu-id="51060-125">Идентификатор ресурса, представляющий раздел сетки событий.</span><span class="sxs-lookup"><span data-stu-id="51060-125">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51060-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="51060-126">-TopicName</span></span>
<span data-ttu-id="51060-127">Название темы.</span><span class="sxs-lookup"><span data-stu-id="51060-127">The name of the topic.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51060-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51060-128">-Confirm</span></span>
<span data-ttu-id="51060-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="51060-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51060-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51060-130">-WhatIf</span></span>
<span data-ttu-id="51060-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="51060-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51060-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="51060-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51060-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51060-133">CommonParameters</span></span>
<span data-ttu-id="51060-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51060-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51060-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51060-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51060-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51060-136">INPUTS</span></span>

### <span data-ttu-id="51060-137">System. String</span><span class="sxs-lookup"><span data-stu-id="51060-137">System.String</span></span>

## <span data-ttu-id="51060-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51060-138">OUTPUTS</span></span>

### <span data-ttu-id="51060-139">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="51060-139">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="51060-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="51060-140">NOTES</span></span>

## <span data-ttu-id="51060-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51060-141">RELATED LINKS</span></span>

