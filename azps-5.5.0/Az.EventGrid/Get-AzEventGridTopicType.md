---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: e2cd8cfeadf0c9574cbf39a642133109aa02ec39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228484"
---
# <span data-ttu-id="553fb-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="553fb-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="553fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="553fb-102">SYNOPSIS</span></span>
<span data-ttu-id="553fb-103">Подробные сведения о типах тем, поддерживаемых сеткой событий Azure.</span><span class="sxs-lookup"><span data-stu-id="553fb-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="553fb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="553fb-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="553fb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="553fb-105">DESCRIPTION</span></span>
<span data-ttu-id="553fb-106">Возвращает сведения о типах тем, поддерживаемых сеткой событий Azure.</span><span class="sxs-lookup"><span data-stu-id="553fb-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="553fb-107">Если задан тип темы, возвращаются сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="553fb-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="553fb-108">Если название темы не указано, возвращаются сведения обо всех типах тем.</span><span class="sxs-lookup"><span data-stu-id="553fb-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="553fb-109">Если задан Тип IncludeEventTypes, в ответ включаются сведения о типах событий, поддерживаемых каждым типом темы.</span><span class="sxs-lookup"><span data-stu-id="553fb-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="553fb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="553fb-110">EXAMPLES</span></span>

### <span data-ttu-id="553fb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="553fb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="553fb-112">Возвращает список типов тем.</span><span class="sxs-lookup"><span data-stu-id="553fb-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="553fb-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="553fb-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="553fb-114">Сведения о типе темы "Данные хранилища".</span><span class="sxs-lookup"><span data-stu-id="553fb-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="553fb-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="553fb-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="553fb-116">Сведения о типе темы "Учетные данные хранилища", в том числе о типах событий, поддерживаемых учетами хранения.</span><span class="sxs-lookup"><span data-stu-id="553fb-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="553fb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="553fb-117">PARAMETERS</span></span>

### <span data-ttu-id="553fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="553fb-118">-DefaultProfile</span></span>
<span data-ttu-id="553fb-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="553fb-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="553fb-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="553fb-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="553fb-121">Если задан этот запрос, ответ будет включать типы событий, поддерживаемые тематическим типом.</span><span class="sxs-lookup"><span data-stu-id="553fb-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="553fb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="553fb-122">-Name</span></span>
<span data-ttu-id="553fb-123">EventGrid Topic Type Name.</span><span class="sxs-lookup"><span data-stu-id="553fb-123">EventGrid Topic Type Name.</span></span>

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

### <span data-ttu-id="553fb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="553fb-124">CommonParameters</span></span>
<span data-ttu-id="553fb-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="553fb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="553fb-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="553fb-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="553fb-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="553fb-127">INPUTS</span></span>

### <span data-ttu-id="553fb-128">System.String</span><span class="sxs-lookup"><span data-stu-id="553fb-128">System.String</span></span>

## <span data-ttu-id="553fb-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="553fb-129">OUTPUTS</span></span>

### <span data-ttu-id="553fb-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="553fb-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="553fb-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="553fb-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="553fb-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="553fb-132">NOTES</span></span>

## <span data-ttu-id="553fb-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="553fb-133">RELATED LINKS</span></span>
