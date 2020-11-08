---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: e2cd8cfeadf0c9574cbf39a642133109aa02ec39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079638"
---
# <span data-ttu-id="d8a9d-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="d8a9d-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="d8a9d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8a9d-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a9d-103">Получает сведения о типах тем, поддерживаемых таблицей событий Azure.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="d8a9d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8a9d-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8a9d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8a9d-105">DESCRIPTION</span></span>
<span data-ttu-id="d8a9d-106">Получает сведения о типах тем, поддерживаемых таблицей событий Azure.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="d8a9d-107">Если указано имя типа раздела, возвращаются сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="d8a9d-108">Если имя типа темы не задано, возвращаются сведения обо всех типах тем.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="d8a9d-109">Если указан IncludeEventTypes, в ответ включаются сведения о типах событий, поддерживаемых каждым типом тем.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="d8a9d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8a9d-110">EXAMPLES</span></span>

### <span data-ttu-id="d8a9d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d8a9d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="d8a9d-112">Получает список типов тем.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="d8a9d-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d8a9d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="d8a9d-114">Получает сведения о типе темы StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="d8a9d-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d8a9d-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="d8a9d-116">Получает сведения о типе темы StorageAccounts, включая типы событий, поддерживаемые StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="d8a9d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8a9d-117">PARAMETERS</span></span>

### <span data-ttu-id="d8a9d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8a9d-118">-DefaultProfile</span></span>
<span data-ttu-id="d8a9d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d8a9d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8a9d-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="d8a9d-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="d8a9d-121">Если указан, в ответ будут включены типы событий, которые поддерживаются типом раздела.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-121">If specified, the response will include the event types supported by a topic type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8a9d-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d8a9d-122">-Name</span></span>
<span data-ttu-id="d8a9d-123">Название типа раздела "EventGrid".</span><span class="sxs-lookup"><span data-stu-id="d8a9d-123">EventGrid Topic Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8a9d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a9d-124">CommonParameters</span></span>
<span data-ttu-id="d8a9d-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a9d-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8a9d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a9d-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8a9d-127">INPUTS</span></span>

### <span data-ttu-id="d8a9d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d8a9d-128">System.String</span></span>

## <span data-ttu-id="d8a9d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8a9d-129">OUTPUTS</span></span>

### <span data-ttu-id="d8a9d-130">Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="d8a9d-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="d8a9d-131">Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="d8a9d-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="d8a9d-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8a9d-132">NOTES</span></span>

## <span data-ttu-id="d8a9d-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8a9d-133">RELATED LINKS</span></span>
