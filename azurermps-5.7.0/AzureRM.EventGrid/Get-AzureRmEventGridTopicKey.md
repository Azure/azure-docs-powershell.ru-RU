---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 741a888287ba7fcb4a9b54c1281a6a27be5fbb0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734030"
---
# <span data-ttu-id="21c91-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="21c91-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="21c91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="21c91-102">SYNOPSIS</span></span>
<span data-ttu-id="21c91-103">Получает общие ключи доступа, используемые для публикации событий в разделе сетки событий.</span><span class="sxs-lookup"><span data-stu-id="21c91-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21c91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="21c91-104">SYNTAX</span></span>

### <span data-ttu-id="21c91-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="21c91-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21c91-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21c91-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21c91-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="21c91-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21c91-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21c91-108">DESCRIPTION</span></span>
<span data-ttu-id="21c91-109">Получает общие ключи доступа, используемые для публикации событий в разделе сетки событий.</span><span class="sxs-lookup"><span data-stu-id="21c91-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="21c91-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="21c91-110">EXAMPLES</span></span>

### <span data-ttu-id="21c91-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="21c91-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="21c91-112">Получает общие ключи доступа к сетке событий, раздел \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="21c91-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="21c91-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="21c91-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="21c91-114">Получает общие ключи доступа к сетке событий, раздел \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="21c91-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="21c91-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="21c91-115">PARAMETERS</span></span>

### <span data-ttu-id="21c91-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c91-116">-DefaultProfile</span></span>
<span data-ttu-id="21c91-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="21c91-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21c91-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21c91-118">-InputObject</span></span>
<span data-ttu-id="21c91-119">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="21c91-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="21c91-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="21c91-120">-Name</span></span>
<span data-ttu-id="21c91-121">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="21c91-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="21c91-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c91-122">-ResourceGroupName</span></span>
<span data-ttu-id="21c91-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="21c91-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="21c91-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21c91-124">-ResourceId</span></span>
<span data-ttu-id="21c91-125">Идентификатор ресурса, представляющий раздел сетки событий.</span><span class="sxs-lookup"><span data-stu-id="21c91-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="21c91-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c91-126">CommonParameters</span></span>
<span data-ttu-id="21c91-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="21c91-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c91-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21c91-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c91-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="21c91-129">INPUTS</span></span>

### <span data-ttu-id="21c91-130">System. String</span><span class="sxs-lookup"><span data-stu-id="21c91-130">System.String</span></span>

## <span data-ttu-id="21c91-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="21c91-131">OUTPUTS</span></span>

### <span data-ttu-id="21c91-132">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="21c91-132">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="21c91-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="21c91-133">NOTES</span></span>

## <span data-ttu-id="21c91-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21c91-134">RELATED LINKS</span></span>

