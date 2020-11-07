---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 91e3acd227acd8a83dcd5ccb0beb2ed12d1cca99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734862"
---
# <span data-ttu-id="db6c0-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="db6c0-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="db6c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db6c0-102">SYNOPSIS</span></span>
<span data-ttu-id="db6c0-103">Получает общие ключи доступа, используемые для публикации событий в разделе сетки событий.</span><span class="sxs-lookup"><span data-stu-id="db6c0-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db6c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db6c0-104">SYNTAX</span></span>

### <span data-ttu-id="db6c0-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="db6c0-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db6c0-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db6c0-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db6c0-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="db6c0-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db6c0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db6c0-108">DESCRIPTION</span></span>
<span data-ttu-id="db6c0-109">Получает общие ключи доступа, используемые для публикации событий в разделе сетки событий.</span><span class="sxs-lookup"><span data-stu-id="db6c0-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="db6c0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db6c0-110">EXAMPLES</span></span>

### <span data-ttu-id="db6c0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="db6c0-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="db6c0-112">Получает общие ключи доступа к сетке событий, раздел \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="db6c0-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="db6c0-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="db6c0-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="db6c0-114">Получает общие ключи доступа к сетке событий, раздел \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="db6c0-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="db6c0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db6c0-115">PARAMETERS</span></span>

### <span data-ttu-id="db6c0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db6c0-116">-InputObject</span></span>
<span data-ttu-id="db6c0-117">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="db6c0-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="db6c0-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="db6c0-118">-Name</span></span>
<span data-ttu-id="db6c0-119">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="db6c0-119">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="db6c0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db6c0-120">-ResourceGroupName</span></span>
<span data-ttu-id="db6c0-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db6c0-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="db6c0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db6c0-122">-ResourceId</span></span>
<span data-ttu-id="db6c0-123">Идентификатор ресурса, представляющий раздел сетки событий.</span><span class="sxs-lookup"><span data-stu-id="db6c0-123">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="db6c0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6c0-124">-DefaultProfile</span></span>
<span data-ttu-id="db6c0-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db6c0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db6c0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6c0-126">CommonParameters</span></span>
<span data-ttu-id="db6c0-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db6c0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6c0-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db6c0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6c0-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db6c0-129">INPUTS</span></span>

### <span data-ttu-id="db6c0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="db6c0-130">System.String</span></span>

## <span data-ttu-id="db6c0-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db6c0-131">OUTPUTS</span></span>

### <span data-ttu-id="db6c0-132">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="db6c0-132">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="db6c0-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="db6c0-133">NOTES</span></span>

## <span data-ttu-id="db6c0-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db6c0-134">RELATED LINKS</span></span>

