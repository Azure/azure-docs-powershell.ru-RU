---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: ab9c9401b0f8d929be1a4aa244f407957d886e4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222561"
---
# <span data-ttu-id="bbc6a-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="bbc6a-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="bbc6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbc6a-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc6a-103">Повторное сгенерирует общий ключ доступа для темы сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="bbc6a-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="bbc6a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bbc6a-104">SYNTAX</span></span>

### <span data-ttu-id="bbc6a-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bbc6a-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc6a-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbc6a-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc6a-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbc6a-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbc6a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbc6a-108">DESCRIPTION</span></span>
<span data-ttu-id="bbc6a-109">Повторное сгенерирует общий ключ доступа для темы сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="bbc6a-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="bbc6a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bbc6a-110">EXAMPLES</span></span>

### <span data-ttu-id="bbc6a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bbc6a-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="bbc6a-112">Regenerate the key corresponding to \' key1'\ of Event Grid \` topic1 \` in resource group \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="bbc6a-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="bbc6a-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bbc6a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="bbc6a-114">Regenerate the key corresponding to \' key1'\ of Event Grid \` topic1 \` in resource group \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="bbc6a-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="bbc6a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbc6a-115">PARAMETERS</span></span>

### <span data-ttu-id="bbc6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc6a-116">-DefaultProfile</span></span>
<span data-ttu-id="bbc6a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bbc6a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbc6a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbc6a-118">-InputObject</span></span>
<span data-ttu-id="bbc6a-119">Объект EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="bbc6a-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="bbc6a-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="bbc6a-120">-KeyName</span></span>
<span data-ttu-id="bbc6a-121">Имя ключа, который требуется сгенерировать повторно</span><span class="sxs-lookup"><span data-stu-id="bbc6a-121">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="bbc6a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbc6a-122">-ResourceGroupName</span></span>
<span data-ttu-id="bbc6a-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bbc6a-123">Resource group name.</span></span>

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

### <span data-ttu-id="bbc6a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbc6a-124">-ResourceId</span></span>
<span data-ttu-id="bbc6a-125">Идентификатор ресурса, представляющий раздел сетки событий.</span><span class="sxs-lookup"><span data-stu-id="bbc6a-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="bbc6a-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="bbc6a-126">-TopicName</span></span>
<span data-ttu-id="bbc6a-127">Название темы.</span><span class="sxs-lookup"><span data-stu-id="bbc6a-127">The name of the topic.</span></span>

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

### <span data-ttu-id="bbc6a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbc6a-128">-Confirm</span></span>
<span data-ttu-id="bbc6a-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bbc6a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbc6a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbc6a-130">-WhatIf</span></span>
<span data-ttu-id="bbc6a-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbc6a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbc6a-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bbc6a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbc6a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc6a-133">CommonParameters</span></span>
<span data-ttu-id="bbc6a-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbc6a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc6a-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbc6a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc6a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbc6a-136">INPUTS</span></span>

### <span data-ttu-id="bbc6a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="bbc6a-137">System.String</span></span>

### <span data-ttu-id="bbc6a-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="bbc6a-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="bbc6a-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bbc6a-139">OUTPUTS</span></span>

### <span data-ttu-id="bbc6a-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="bbc6a-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="bbc6a-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bbc6a-141">NOTES</span></span>

## <span data-ttu-id="bbc6a-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbc6a-142">RELATED LINKS</span></span>
