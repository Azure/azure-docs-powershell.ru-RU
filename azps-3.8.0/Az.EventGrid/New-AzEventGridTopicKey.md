---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: 8749f5ad542d55f167f866e436acf72aacf3bc14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065901"
---
# <span data-ttu-id="69519-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="69519-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="69519-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69519-102">SYNOPSIS</span></span>
<span data-ttu-id="69519-103">Повторное создание ключа общего доступа для раздела сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="69519-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="69519-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69519-104">SYNTAX</span></span>

### <span data-ttu-id="69519-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="69519-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69519-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69519-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69519-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="69519-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69519-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69519-108">DESCRIPTION</span></span>
<span data-ttu-id="69519-109">Повторное создание ключа общего доступа для раздела сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="69519-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="69519-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69519-110">EXAMPLES</span></span>

### <span data-ttu-id="69519-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="69519-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="69519-112">Повторное создание ключа, соответствующего ключу \' Key1 "\ из сетки событий" \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="69519-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="69519-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="69519-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="69519-114">Повторное создание ключа, соответствующего ключу \' Key1 "\ из сетки событий" \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="69519-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="69519-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69519-115">PARAMETERS</span></span>

### <span data-ttu-id="69519-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69519-116">-DefaultProfile</span></span>
<span data-ttu-id="69519-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="69519-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69519-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69519-118">-InputObject</span></span>
<span data-ttu-id="69519-119">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="69519-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="69519-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="69519-120">-KeyName</span></span>
<span data-ttu-id="69519-121">Имя ключа, который должен быть повторно сгенерирован</span><span class="sxs-lookup"><span data-stu-id="69519-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69519-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69519-122">-ResourceGroupName</span></span>
<span data-ttu-id="69519-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="69519-123">Resource group name.</span></span>

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

### <span data-ttu-id="69519-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69519-124">-ResourceId</span></span>
<span data-ttu-id="69519-125">Идентификатор ресурса, представляющий раздел сетки событий.</span><span class="sxs-lookup"><span data-stu-id="69519-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="69519-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="69519-126">-TopicName</span></span>
<span data-ttu-id="69519-127">Название темы.</span><span class="sxs-lookup"><span data-stu-id="69519-127">The name of the topic.</span></span>

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

### <span data-ttu-id="69519-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69519-128">-Confirm</span></span>
<span data-ttu-id="69519-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="69519-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69519-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69519-130">-WhatIf</span></span>
<span data-ttu-id="69519-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="69519-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69519-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="69519-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69519-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69519-133">CommonParameters</span></span>
<span data-ttu-id="69519-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69519-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69519-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69519-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69519-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69519-136">INPUTS</span></span>

### <span data-ttu-id="69519-137">System. String</span><span class="sxs-lookup"><span data-stu-id="69519-137">System.String</span></span>

### <span data-ttu-id="69519-138">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="69519-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="69519-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69519-139">OUTPUTS</span></span>

### <span data-ttu-id="69519-140">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="69519-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="69519-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="69519-141">NOTES</span></span>

## <span data-ttu-id="69519-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69519-142">RELATED LINKS</span></span>
