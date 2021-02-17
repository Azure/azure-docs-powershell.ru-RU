---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: ca2afaec702e27b4c20201cbd69984ec3827ded2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243632"
---
# <span data-ttu-id="a6420-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="a6420-101">Get-AzEventHub</span></span>

## <span data-ttu-id="a6420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6420-102">SYNOPSIS</span></span>
<span data-ttu-id="a6420-103">Получает сведения об одном центре событий или получает список концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="a6420-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="a6420-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a6420-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6420-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6420-105">DESCRIPTION</span></span>
<span data-ttu-id="a6420-106">Этот Get-AzEventHub возвращает сведения о центре событий или список всех концентраторов событий в текущем пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="a6420-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="a6420-107">Если в центре событий есть имя, возвращаются сведения об одном центре событий.</span><span class="sxs-lookup"><span data-stu-id="a6420-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="a6420-108">Если имя центра событий не указано, возвращается список всех концентраторов событий в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="a6420-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="a6420-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a6420-109">EXAMPLES</span></span>

### <span data-ttu-id="a6420-110">Пример 1: указанный EventHub</span><span class="sxs-lookup"><span data-stu-id="a6420-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="a6420-111">Возвращает сведения о Центре событий \` MyEventHubName. \`</span><span class="sxs-lookup"><span data-stu-id="a6420-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="a6420-112">Пример 2. Список EventHub в указанном пространстве имен</span><span class="sxs-lookup"><span data-stu-id="a6420-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="a6420-113">Возвращает список концентраторов событий в области имен \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="a6420-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="a6420-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6420-114">PARAMETERS</span></span>

### <span data-ttu-id="a6420-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6420-115">-DefaultProfile</span></span>
<span data-ttu-id="a6420-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6420-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6420-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a6420-117">-MaxCount</span></span>
<span data-ttu-id="a6420-118">Определите максимальное количество возвращаемого событияHubs.</span><span class="sxs-lookup"><span data-stu-id="a6420-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="a6420-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a6420-119">-Name</span></span>
<span data-ttu-id="a6420-120">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="a6420-120">EventHub Name</span></span>

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

### <span data-ttu-id="a6420-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a6420-121">-Namespace</span></span>
<span data-ttu-id="a6420-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="a6420-122">Namespace Name</span></span>

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

### <span data-ttu-id="a6420-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6420-123">-ResourceGroupName</span></span>
<span data-ttu-id="a6420-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a6420-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a6420-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6420-125">CommonParameters</span></span>
<span data-ttu-id="a6420-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6420-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6420-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6420-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6420-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6420-128">INPUTS</span></span>

### <span data-ttu-id="a6420-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a6420-129">System.String</span></span>

## <span data-ttu-id="a6420-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a6420-130">OUTPUTS</span></span>

### <span data-ttu-id="a6420-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="a6420-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="a6420-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a6420-132">NOTES</span></span>

## <span data-ttu-id="a6420-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6420-133">RELATED LINKS</span></span>
