---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: 3454a3aad2276384588c0ccc550a1b0ef6df7cfc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730877"
---
# <span data-ttu-id="63597-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="63597-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="63597-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63597-102">SYNOPSIS</span></span>
<span data-ttu-id="63597-103">Получает общие ключи доступа, используемые для публикации событий в разделе сетки событий.</span><span class="sxs-lookup"><span data-stu-id="63597-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="63597-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63597-104">SYNTAX</span></span>

### <span data-ttu-id="63597-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="63597-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63597-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63597-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63597-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="63597-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63597-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63597-108">DESCRIPTION</span></span>
<span data-ttu-id="63597-109">Получает общие ключи доступа, используемые для публикации событий в разделе сетки событий.</span><span class="sxs-lookup"><span data-stu-id="63597-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="63597-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63597-110">EXAMPLES</span></span>

### <span data-ttu-id="63597-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63597-111">Example 1</span></span>
```
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="63597-112">Получает общие ключи доступа к сетке событий, раздел \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="63597-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="63597-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="63597-113">Example 2</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="63597-114">Получает общие ключи доступа к сетке событий, раздел \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="63597-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="63597-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63597-115">PARAMETERS</span></span>

### <span data-ttu-id="63597-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63597-116">-DefaultProfile</span></span>
<span data-ttu-id="63597-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="63597-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63597-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63597-118">-InputObject</span></span>
<span data-ttu-id="63597-119">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="63597-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="63597-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63597-120">-Name</span></span>
<span data-ttu-id="63597-121">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="63597-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="63597-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63597-122">-ResourceGroupName</span></span>
<span data-ttu-id="63597-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63597-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="63597-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63597-124">-ResourceId</span></span>
<span data-ttu-id="63597-125">Идентификатор ресурса, представляющий раздел сетки событий.</span><span class="sxs-lookup"><span data-stu-id="63597-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="63597-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63597-126">CommonParameters</span></span>
<span data-ttu-id="63597-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63597-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63597-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63597-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63597-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63597-129">INPUTS</span></span>

### <span data-ttu-id="63597-130">System. String</span><span class="sxs-lookup"><span data-stu-id="63597-130">System.String</span></span>

### <span data-ttu-id="63597-131">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="63597-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="63597-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63597-132">OUTPUTS</span></span>

### <span data-ttu-id="63597-133">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="63597-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="63597-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="63597-134">NOTES</span></span>

## <span data-ttu-id="63597-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63597-135">RELATED LINKS</span></span>
