---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
ms.openlocfilehash: ed78c22f0edda37acff3d11a0d7638a183015a9e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733058"
---
# <span data-ttu-id="772fb-101">New-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="772fb-101">New-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="772fb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="772fb-102">SYNOPSIS</span></span>
<span data-ttu-id="772fb-103">Создание нового раздела сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="772fb-103">Creates a new Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="772fb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="772fb-104">SYNTAX</span></span>

```
New-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="772fb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="772fb-105">DESCRIPTION</span></span>
<span data-ttu-id="772fb-106">Создание нового раздела сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="772fb-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="772fb-107">После создания темы приложение может публиковать события в конечной точке раздела.</span><span class="sxs-lookup"><span data-stu-id="772fb-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="772fb-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="772fb-108">EXAMPLES</span></span>

### <span data-ttu-id="772fb-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="772fb-109">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="772fb-110">Создание сетки событий в разделе \` элемент1 \` в указанном географическом расположении \` westus2 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="772fb-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="772fb-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="772fb-111">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="772fb-112">Создает сетку событий \` в разделе элемент1 \` в указанном географическом расположении \` westus2 \` , в группе ресурсов \` MyResourceGroupName \` с заданными тегами "Отдел" и "среда".</span><span class="sxs-lookup"><span data-stu-id="772fb-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="772fb-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="772fb-113">PARAMETERS</span></span>

### <span data-ttu-id="772fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="772fb-114">-DefaultProfile</span></span>
<span data-ttu-id="772fb-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="772fb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="772fb-116">-Location</span><span class="sxs-lookup"><span data-stu-id="772fb-116">-Location</span></span>
<span data-ttu-id="772fb-117">Расположение темы</span><span class="sxs-lookup"><span data-stu-id="772fb-117">The location of the topic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="772fb-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="772fb-118">-Name</span></span>
<span data-ttu-id="772fb-119">Название темы.</span><span class="sxs-lookup"><span data-stu-id="772fb-119">The name of the topic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="772fb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="772fb-120">-ResourceGroupName</span></span>
<span data-ttu-id="772fb-121">Группа ресурсов, в которой должен быть создан раздел.</span><span class="sxs-lookup"><span data-stu-id="772fb-121">The resource group in which the topic should be created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="772fb-122">-Тег</span><span class="sxs-lookup"><span data-stu-id="772fb-122">-Tag</span></span>
<span data-ttu-id="772fb-123">Хэш-таблицы, представляющие Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="772fb-123">Hashtables which represents resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="772fb-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="772fb-124">-Confirm</span></span>
<span data-ttu-id="772fb-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="772fb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="772fb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="772fb-126">-WhatIf</span></span>
<span data-ttu-id="772fb-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="772fb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="772fb-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="772fb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="772fb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="772fb-129">CommonParameters</span></span>
<span data-ttu-id="772fb-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="772fb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="772fb-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="772fb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="772fb-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="772fb-132">INPUTS</span></span>

### <span data-ttu-id="772fb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="772fb-133">System.String</span></span>
<span data-ttu-id="772fb-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="772fb-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="772fb-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="772fb-135">OUTPUTS</span></span>

### <span data-ttu-id="772fb-136">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="772fb-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="772fb-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="772fb-137">NOTES</span></span>

## <span data-ttu-id="772fb-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="772fb-138">RELATED LINKS</span></span>

