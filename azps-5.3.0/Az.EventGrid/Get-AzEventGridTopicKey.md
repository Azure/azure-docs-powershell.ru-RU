---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b0690882cc230a92fd6e81e38832f2fc352e131c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504929"
---
# <span data-ttu-id="f7f9c-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="f7f9c-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="f7f9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7f9c-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f9c-103">Получает общие ключи доступа, используемые для публикации событий в теме сетки событий.</span><span class="sxs-lookup"><span data-stu-id="f7f9c-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="f7f9c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f7f9c-104">SYNTAX</span></span>

### <span data-ttu-id="f7f9c-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7f9c-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7f9c-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7f9c-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7f9c-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7f9c-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7f9c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7f9c-108">DESCRIPTION</span></span>
<span data-ttu-id="f7f9c-109">Получает общие ключи доступа, используемые для публикации событий в теме сетки событий.</span><span class="sxs-lookup"><span data-stu-id="f7f9c-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="f7f9c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f7f9c-110">EXAMPLES</span></span>

### <span data-ttu-id="f7f9c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f7f9c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="f7f9c-112">Получает общие ключи доступа к теме "Тема1" сетки событий в группе ресурсов \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="f7f9c-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f7f9c-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f7f9c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="f7f9c-114">Получает общие ключи доступа к теме "Тема1" сетки событий в группе ресурсов \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="f7f9c-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f7f9c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7f9c-115">PARAMETERS</span></span>

### <span data-ttu-id="f7f9c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f9c-116">-DefaultProfile</span></span>
<span data-ttu-id="f7f9c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f7f9c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7f9c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7f9c-118">-InputObject</span></span>
<span data-ttu-id="f7f9c-119">Объект EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="f7f9c-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="f7f9c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f7f9c-120">-Name</span></span>
<span data-ttu-id="f7f9c-121">Имя темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="f7f9c-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="f7f9c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7f9c-122">-ResourceGroupName</span></span>
<span data-ttu-id="f7f9c-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7f9c-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="f7f9c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7f9c-124">-ResourceId</span></span>
<span data-ttu-id="f7f9c-125">Идентификатор ресурса, представляющий раздел сетки событий.</span><span class="sxs-lookup"><span data-stu-id="f7f9c-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="f7f9c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f9c-126">CommonParameters</span></span>
<span data-ttu-id="f7f9c-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7f9c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f9c-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7f9c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f9c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7f9c-129">INPUTS</span></span>

### <span data-ttu-id="f7f9c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f7f9c-130">System.String</span></span>

### <span data-ttu-id="f7f9c-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="f7f9c-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="f7f9c-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f7f9c-132">OUTPUTS</span></span>

### <span data-ttu-id="f7f9c-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="f7f9c-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="f7f9c-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f7f9c-134">NOTES</span></span>

## <span data-ttu-id="f7f9c-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7f9c-135">RELATED LINKS</span></span>
