---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
ms.openlocfilehash: 621fb15d3a83b7c704e5828d6541ad9d4404875c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567637"
---
# <span data-ttu-id="dfe85-101">Get-AzureRmEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="dfe85-101">Get-AzureRmEventGridTopicType</span></span>

## <span data-ttu-id="dfe85-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dfe85-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe85-103">Получает сведения о типах тем, поддерживаемых таблицей событий Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe85-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfe85-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dfe85-104">SYNTAX</span></span>

```
Get-AzureRmEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfe85-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfe85-105">DESCRIPTION</span></span>
<span data-ttu-id="dfe85-106">Получает сведения о типах тем, поддерживаемых таблицей событий Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe85-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="dfe85-107">Если указано имя типа раздела, возвращаются сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="dfe85-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="dfe85-108">Если имя типа темы не задано, возвращаются сведения обо всех типах тем.</span><span class="sxs-lookup"><span data-stu-id="dfe85-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="dfe85-109">Если указан IncludeEventTypes, в ответ включаются сведения о типах событий, поддерживаемых каждым типом тем.</span><span class="sxs-lookup"><span data-stu-id="dfe85-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="dfe85-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dfe85-110">EXAMPLES</span></span>

### <span data-ttu-id="dfe85-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dfe85-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType
```

<span data-ttu-id="dfe85-112">Получает список типов тем.</span><span class="sxs-lookup"><span data-stu-id="dfe85-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="dfe85-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dfe85-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="dfe85-114">Получает сведения о типе темы StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="dfe85-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="dfe85-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="dfe85-115">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="dfe85-116">Получает сведения о типе темы StorageAccounts, включая типы событий, поддерживаемые StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="dfe85-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="dfe85-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dfe85-117">PARAMETERS</span></span>

### <span data-ttu-id="dfe85-118">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="dfe85-118">-IncludeEventTypeData</span></span>
<span data-ttu-id="dfe85-119">Если указан, в ответ будут включены типы событий, которые поддерживаются типом раздела.</span><span class="sxs-lookup"><span data-stu-id="dfe85-119">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="dfe85-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dfe85-120">-Name</span></span>
<span data-ttu-id="dfe85-121">Название типа раздела "EventGrid".</span><span class="sxs-lookup"><span data-stu-id="dfe85-121">EventGrid Topic Type Name.</span></span>

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

### <span data-ttu-id="dfe85-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe85-122">-DefaultProfile</span></span>
<span data-ttu-id="dfe85-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe85-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfe85-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe85-124">CommonParameters</span></span>
<span data-ttu-id="dfe85-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dfe85-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe85-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfe85-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe85-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dfe85-127">INPUTS</span></span>

### <span data-ttu-id="dfe85-128">System. String</span><span class="sxs-lookup"><span data-stu-id="dfe85-128">System.String</span></span>
<span data-ttu-id="dfe85-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dfe85-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dfe85-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfe85-130">OUTPUTS</span></span>

### <span data-ttu-id="dfe85-131">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfoListInstance, Microsoft. Azure. Commands = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="dfe85-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="dfe85-132">Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="dfe85-132">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="dfe85-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="dfe85-133">NOTES</span></span>

## <span data-ttu-id="dfe85-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dfe85-134">RELATED LINKS</span></span>

