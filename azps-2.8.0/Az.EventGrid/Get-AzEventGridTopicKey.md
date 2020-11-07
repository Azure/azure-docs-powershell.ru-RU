---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b39f9c3c3c1d72624c612d2743b32d306eefa131
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721001"
---
# <span data-ttu-id="dcc3e-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="dcc3e-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="dcc3e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dcc3e-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc3e-103">Получает общие ключи доступа, используемые для публикации событий в разделе сетки событий.</span><span class="sxs-lookup"><span data-stu-id="dcc3e-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="dcc3e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dcc3e-104">SYNTAX</span></span>

### <span data-ttu-id="dcc3e-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dcc3e-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcc3e-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcc3e-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dcc3e-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcc3e-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcc3e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcc3e-108">DESCRIPTION</span></span>
<span data-ttu-id="dcc3e-109">Получает общие ключи доступа, используемые для публикации событий в разделе сетки событий.</span><span class="sxs-lookup"><span data-stu-id="dcc3e-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="dcc3e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dcc3e-110">EXAMPLES</span></span>

### <span data-ttu-id="dcc3e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dcc3e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="dcc3e-112">Получает общие ключи доступа к сетке событий, раздел \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="dcc3e-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="dcc3e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dcc3e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="dcc3e-114">Получает общие ключи доступа к сетке событий, раздел \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="dcc3e-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="dcc3e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dcc3e-115">PARAMETERS</span></span>

### <span data-ttu-id="dcc3e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcc3e-116">-DefaultProfile</span></span>
<span data-ttu-id="dcc3e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dcc3e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcc3e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcc3e-118">-InputObject</span></span>
<span data-ttu-id="dcc3e-119">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="dcc3e-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="dcc3e-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dcc3e-120">-Name</span></span>
<span data-ttu-id="dcc3e-121">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="dcc3e-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="dcc3e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcc3e-122">-ResourceGroupName</span></span>
<span data-ttu-id="dcc3e-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dcc3e-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="dcc3e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcc3e-124">-ResourceId</span></span>
<span data-ttu-id="dcc3e-125">Идентификатор ресурса, представляющий раздел сетки событий.</span><span class="sxs-lookup"><span data-stu-id="dcc3e-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="dcc3e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcc3e-126">CommonParameters</span></span>
<span data-ttu-id="dcc3e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dcc3e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcc3e-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcc3e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcc3e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dcc3e-129">INPUTS</span></span>

### <span data-ttu-id="dcc3e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="dcc3e-130">System.String</span></span>

### <span data-ttu-id="dcc3e-131">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="dcc3e-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="dcc3e-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcc3e-132">OUTPUTS</span></span>

### <span data-ttu-id="dcc3e-133">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="dcc3e-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="dcc3e-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="dcc3e-134">NOTES</span></span>

## <span data-ttu-id="dcc3e-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcc3e-135">RELATED LINKS</span></span>
