---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/remove-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
ms.openlocfilehash: aa9ef35ec0571628eb209163e91c9415706b57a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563539"
---
# <span data-ttu-id="edaef-101">Remove-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="edaef-101">Remove-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="edaef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="edaef-102">SYNOPSIS</span></span>
<span data-ttu-id="edaef-103">Удаляет раздел сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="edaef-103">Removes an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edaef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="edaef-104">SYNTAX</span></span>

### <span data-ttu-id="edaef-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="edaef-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edaef-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="edaef-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edaef-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="edaef-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edaef-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="edaef-108">DESCRIPTION</span></span>
<span data-ttu-id="edaef-109">Удаляет раздел сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="edaef-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="edaef-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="edaef-110">EXAMPLES</span></span>

### <span data-ttu-id="edaef-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="edaef-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="edaef-112">Удаляет раздел элемент1 сетки событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="edaef-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="edaef-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="edaef-113">Example 2</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzureRmEventGridTopic
```

<span data-ttu-id="edaef-114">Удаляет раздел элемент1 сетки событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="edaef-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="edaef-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="edaef-115">PARAMETERS</span></span>

### <span data-ttu-id="edaef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edaef-116">-DefaultProfile</span></span>
<span data-ttu-id="edaef-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="edaef-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edaef-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edaef-118">-InputObject</span></span>
<span data-ttu-id="edaef-119">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="edaef-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="edaef-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="edaef-120">-Name</span></span>
<span data-ttu-id="edaef-121">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="edaef-121">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edaef-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edaef-122">-PassThru</span></span>
<span data-ttu-id="edaef-123">Возвращает состояние операции удаления.</span><span class="sxs-lookup"><span data-stu-id="edaef-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="edaef-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="edaef-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edaef-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edaef-125">-ResourceGroupName</span></span>
<span data-ttu-id="edaef-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="edaef-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="edaef-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edaef-127">-ResourceId</span></span>
<span data-ttu-id="edaef-128">EventGrid темы (ResourceID).</span><span class="sxs-lookup"><span data-stu-id="edaef-128">EventGrid Topic ResourceID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edaef-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edaef-129">-Confirm</span></span>
<span data-ttu-id="edaef-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="edaef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edaef-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edaef-131">-WhatIf</span></span>
<span data-ttu-id="edaef-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="edaef-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edaef-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="edaef-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edaef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edaef-134">CommonParameters</span></span>
<span data-ttu-id="edaef-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="edaef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edaef-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edaef-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edaef-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="edaef-137">INPUTS</span></span>

### <span data-ttu-id="edaef-138">System. String</span><span class="sxs-lookup"><span data-stu-id="edaef-138">System.String</span></span>
<span data-ttu-id="edaef-139">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="edaef-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="edaef-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="edaef-140">OUTPUTS</span></span>

### <span data-ttu-id="edaef-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="edaef-141">System.Object</span></span>

## <span data-ttu-id="edaef-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="edaef-142">NOTES</span></span>

## <span data-ttu-id="edaef-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="edaef-143">RELATED LINKS</span></span>

