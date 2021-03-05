---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: d69e30ff993d2e07c7711d36d8e5ec889bc0f7c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007907"
---
# <span data-ttu-id="b1920-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="b1920-101">Get-AzEventHub</span></span>

## <span data-ttu-id="b1920-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1920-102">SYNOPSIS</span></span>
<span data-ttu-id="b1920-103">Возвращает сведения об одном центре событий или список концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="b1920-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="b1920-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b1920-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1920-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1920-105">DESCRIPTION</span></span>
<span data-ttu-id="b1920-106">Этот Get-AzEventHub возвращает сведения об концентраторе событий или список всех концентраторов событий в текущем пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="b1920-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="b1920-107">Если в центре событий есть имя, возвращаются сведения об одном центре событий.</span><span class="sxs-lookup"><span data-stu-id="b1920-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="b1920-108">Если имя центра событий не указано, возвращается список всех концентраторов событий в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="b1920-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="b1920-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b1920-109">EXAMPLES</span></span>

### <span data-ttu-id="b1920-110">Пример 1: указанный EventHub</span><span class="sxs-lookup"><span data-stu-id="b1920-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="b1920-111">Возвращает сведения о Центре событий \` MyEventHubName. \`</span><span class="sxs-lookup"><span data-stu-id="b1920-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="b1920-112">Пример 2. Список EventHub в указанном пространстве имен</span><span class="sxs-lookup"><span data-stu-id="b1920-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="b1920-113">Возвращает список концентраторов событий в области имен \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="b1920-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="b1920-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1920-114">PARAMETERS</span></span>

### <span data-ttu-id="b1920-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1920-115">-DefaultProfile</span></span>
<span data-ttu-id="b1920-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1920-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1920-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b1920-117">-MaxCount</span></span>
<span data-ttu-id="b1920-118">Определите максимальное количество возвращаемого событияHubs.</span><span class="sxs-lookup"><span data-stu-id="b1920-118">Determine the maximum number of EventHubs to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1920-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b1920-119">-Name</span></span>
<span data-ttu-id="b1920-120">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="b1920-120">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1920-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b1920-121">-Namespace</span></span>
<span data-ttu-id="b1920-122">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="b1920-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1920-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1920-123">-ResourceGroupName</span></span>
<span data-ttu-id="b1920-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b1920-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1920-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1920-125">CommonParameters</span></span>
<span data-ttu-id="b1920-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1920-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1920-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1920-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1920-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1920-128">INPUTS</span></span>

### <span data-ttu-id="b1920-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b1920-129">System.String</span></span>

## <span data-ttu-id="b1920-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b1920-130">OUTPUTS</span></span>

### <span data-ttu-id="b1920-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="b1920-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="b1920-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b1920-132">NOTES</span></span>

## <span data-ttu-id="b1920-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1920-133">RELATED LINKS</span></span>
