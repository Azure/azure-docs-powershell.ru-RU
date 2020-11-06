---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
ms.openlocfilehash: cd3182a2a00f488dabd70a97d06693362068768c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568173"
---
# <span data-ttu-id="3f5f6-101">Get-AzureRmEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="3f5f6-101">Get-AzureRmEventGridTopicType</span></span>

## <span data-ttu-id="3f5f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f5f6-102">SYNOPSIS</span></span>
<span data-ttu-id="3f5f6-103">Получает сведения о типах тем, поддерживаемых таблицей событий Azure.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f5f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f5f6-104">SYNTAX</span></span>

```
Get-AzureRmEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f5f6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f5f6-105">DESCRIPTION</span></span>
<span data-ttu-id="3f5f6-106">Получает сведения о типах тем, поддерживаемых таблицей событий Azure.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="3f5f6-107">Если указано имя типа раздела, возвращаются сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="3f5f6-108">Если имя типа темы не задано, возвращаются сведения обо всех типах тем.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="3f5f6-109">Если указан IncludeEventTypes, в ответ включаются сведения о типах событий, поддерживаемых каждым типом тем.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="3f5f6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f5f6-110">EXAMPLES</span></span>

### <span data-ttu-id="3f5f6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3f5f6-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType
```

<span data-ttu-id="3f5f6-112">Получает список типов тем.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="3f5f6-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3f5f6-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="3f5f6-114">Получает сведения о типе темы StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="3f5f6-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3f5f6-115">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="3f5f6-116">Получает сведения о типе темы StorageAccounts, включая типы событий, поддерживаемые StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="3f5f6-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f5f6-117">PARAMETERS</span></span>

### <span data-ttu-id="3f5f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f5f6-118">-DefaultProfile</span></span>
<span data-ttu-id="3f5f6-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3f5f6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f5f6-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="3f5f6-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="3f5f6-121">Если указан, в ответ будут включены типы событий, которые поддерживаются типом раздела.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="3f5f6-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3f5f6-122">-Name</span></span>
<span data-ttu-id="3f5f6-123">Название типа раздела "EventGrid".</span><span class="sxs-lookup"><span data-stu-id="3f5f6-123">EventGrid Topic Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f5f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f5f6-124">CommonParameters</span></span>
<span data-ttu-id="3f5f6-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f5f6-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f5f6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f5f6-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f5f6-127">INPUTS</span></span>

### <span data-ttu-id="3f5f6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3f5f6-128">System.String</span></span>

## <span data-ttu-id="3f5f6-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f5f6-129">OUTPUTS</span></span>

### <span data-ttu-id="3f5f6-130">Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="3f5f6-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="3f5f6-131">Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="3f5f6-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="3f5f6-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f5f6-132">NOTES</span></span>

## <span data-ttu-id="3f5f6-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f5f6-133">RELATED LINKS</span></span>
