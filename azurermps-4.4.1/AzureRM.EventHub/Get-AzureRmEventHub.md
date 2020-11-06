---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bbe600feb7618bef94a0d1799e1d2709ce7f0157
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569504"
---
# <span data-ttu-id="ddc8b-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="ddc8b-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="ddc8b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ddc8b-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc8b-103">Получение сведений об одном концентраторе событий или получение списка концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="ddc8b-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddc8b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ddc8b-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

## <span data-ttu-id="ddc8b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddc8b-105">DESCRIPTION</span></span>
<span data-ttu-id="ddc8b-106">Командлет Get-AzureRmEventHub возвращает либо сведения о концентраторе событий, либо список всех концентраторов событий в текущем пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="ddc8b-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="ddc8b-107">Если указано имя концентратора событий, возвращаются сведения об одном концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="ddc8b-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="ddc8b-108">Если имя концентратора событий не указано, возвращается список всех концентраторов событий в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="ddc8b-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="ddc8b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ddc8b-109">EXAMPLES</span></span>

### <span data-ttu-id="ddc8b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ddc8b-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="ddc8b-111">Возвращает сведения о концентраторе событий \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="ddc8b-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="ddc8b-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ddc8b-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="ddc8b-113">Возвращает список концентраторов событий в MyNamespaceName пространства имен \` \` .</span><span class="sxs-lookup"><span data-stu-id="ddc8b-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="ddc8b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ddc8b-114">PARAMETERS</span></span>

### <span data-ttu-id="ddc8b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc8b-115">-ResourceGroupName</span></span>
<span data-ttu-id="ddc8b-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ddc8b-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc8b-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ddc8b-117">-Name</span></span>
<span data-ttu-id="ddc8b-118">Имя EventHub.</span><span class="sxs-lookup"><span data-stu-id="ddc8b-118">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc8b-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ddc8b-119">-Namespace</span></span>
<span data-ttu-id="ddc8b-120">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ddc8b-120">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="ddc8b-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ddc8b-121">INPUTS</span></span>

### <span data-ttu-id="ddc8b-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ddc8b-122">System.String</span></span>

## <span data-ttu-id="ddc8b-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddc8b-123">OUTPUTS</span></span>

### <span data-ttu-id="ddc8b-124">System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. eventhub, версия = 0.0.1.0, культура = нейтраль, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="ddc8b-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ddc8b-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="ddc8b-125">NOTES</span></span>

## <span data-ttu-id="ddc8b-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddc8b-126">RELATED LINKS</span></span>

