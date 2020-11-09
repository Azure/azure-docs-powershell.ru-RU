---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: ca2afaec702e27b4c20201cbd69984ec3827ded2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247448"
---
# <span data-ttu-id="ca006-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="ca006-101">Get-AzEventHub</span></span>

## <span data-ttu-id="ca006-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ca006-102">SYNOPSIS</span></span>
<span data-ttu-id="ca006-103">Получение сведений об одном концентраторе событий или получение списка концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="ca006-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="ca006-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ca006-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca006-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca006-105">DESCRIPTION</span></span>
<span data-ttu-id="ca006-106">Командлет Get-AzEventHub возвращает либо сведения о концентраторе событий, либо список всех концентраторов событий в текущем пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="ca006-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="ca006-107">Если указано имя концентратора событий, возвращаются сведения об одном концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="ca006-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="ca006-108">Если имя концентратора событий не указано, возвращается список всех концентраторов событий в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="ca006-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="ca006-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ca006-109">EXAMPLES</span></span>

### <span data-ttu-id="ca006-110">Пример 1: указана EventHub</span><span class="sxs-lookup"><span data-stu-id="ca006-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="ca006-111">Возвращает сведения о концентраторе событий \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="ca006-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="ca006-112">Пример 2: список EventHub в указанном пространстве имен</span><span class="sxs-lookup"><span data-stu-id="ca006-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="ca006-113">Возвращает список концентраторов событий в MyNamespaceName пространства имен \` \` .</span><span class="sxs-lookup"><span data-stu-id="ca006-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="ca006-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ca006-114">PARAMETERS</span></span>

### <span data-ttu-id="ca006-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca006-115">-DefaultProfile</span></span>
<span data-ttu-id="ca006-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca006-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca006-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ca006-117">-MaxCount</span></span>
<span data-ttu-id="ca006-118">Определите максимальное число возвращаемых EventHubs.</span><span class="sxs-lookup"><span data-stu-id="ca006-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="ca006-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ca006-119">-Name</span></span>
<span data-ttu-id="ca006-120">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="ca006-120">EventHub Name</span></span>

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

### <span data-ttu-id="ca006-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ca006-121">-Namespace</span></span>
<span data-ttu-id="ca006-122">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="ca006-122">Namespace Name</span></span>

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

### <span data-ttu-id="ca006-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca006-123">-ResourceGroupName</span></span>
<span data-ttu-id="ca006-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ca006-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ca006-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca006-125">CommonParameters</span></span>
<span data-ttu-id="ca006-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ca006-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca006-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca006-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca006-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ca006-128">INPUTS</span></span>

### <span data-ttu-id="ca006-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ca006-129">System.String</span></span>

## <span data-ttu-id="ca006-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca006-130">OUTPUTS</span></span>

### <span data-ttu-id="ca006-131">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="ca006-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="ca006-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="ca006-132">NOTES</span></span>

## <span data-ttu-id="ca006-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca006-133">RELATED LINKS</span></span>