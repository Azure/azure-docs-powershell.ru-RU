---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 23004583a08dbcf5ef8785b62d0457b6b6ee0897
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730878"
---
# <span data-ttu-id="1c4a5-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="1c4a5-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="1c4a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c4a5-102">SYNOPSIS</span></span>
<span data-ttu-id="1c4a5-103">Получает сведения о сетке событий или получает список всех разделов сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="1c4a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c4a5-104">SYNTAX</span></span>

### <span data-ttu-id="1c4a5-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1c4a5-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c4a5-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c4a5-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c4a5-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c4a5-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c4a5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c4a5-108">DESCRIPTION</span></span>
<span data-ttu-id="1c4a5-109">Командлет Get-AzEventGridTopic получает либо сведения о заданной теме сетки событий, либо список всех разделов сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-109">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="1c4a5-110">Если указано название раздела, возвращается информация об одной статье.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="1c4a5-111">Если название темы не указано, возвращается список тем.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="1c4a5-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c4a5-112">EXAMPLES</span></span>

### <span data-ttu-id="1c4a5-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1c4a5-113">Example 1</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="1c4a5-114">Получает сведения о сетке событий \` в разделе элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="1c4a5-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1c4a5-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1c4a5-115">Example 2</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="1c4a5-116">Получает сведения о сетке событий \` в разделе элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="1c4a5-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1c4a5-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="1c4a5-117">Example 3</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="1c4a5-118">Перечислите все разделы сетки событий в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="1c4a5-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1c4a5-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="1c4a5-119">Example 4</span></span>
```
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="1c4a5-120">Список всех подразделов сетки событий в подписке.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="1c4a5-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c4a5-121">PARAMETERS</span></span>

### <span data-ttu-id="1c4a5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c4a5-122">-DefaultProfile</span></span>
<span data-ttu-id="1c4a5-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1c4a5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c4a5-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1c4a5-124">-Name</span></span>
<span data-ttu-id="1c4a5-125">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-125">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="1c4a5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c4a5-126">-ResourceGroupName</span></span>
<span data-ttu-id="1c4a5-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="1c4a5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c4a5-128">-ResourceId</span></span>
<span data-ttu-id="1c4a5-129">Идентификатор ресурса, представляющий раздел сетки событий.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-129">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="1c4a5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c4a5-130">CommonParameters</span></span>
<span data-ttu-id="1c4a5-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c4a5-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c4a5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c4a5-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c4a5-133">INPUTS</span></span>

### <span data-ttu-id="1c4a5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1c4a5-134">System.String</span></span>

## <span data-ttu-id="1c4a5-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c4a5-135">OUTPUTS</span></span>

### <span data-ttu-id="1c4a5-136">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="1c4a5-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="1c4a5-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="1c4a5-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="1c4a5-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c4a5-138">NOTES</span></span>

## <span data-ttu-id="1c4a5-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c4a5-139">RELATED LINKS</span></span>
