---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a2608ee3d3f874183a35fe6b81f7cd169123416
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569492"
---
# <span data-ttu-id="98f01-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="98f01-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="98f01-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98f01-102">SYNOPSIS</span></span>
<span data-ttu-id="98f01-103">Получает сведения о группе потребителей указанных концентраторов событий или получает список групп потребителей в концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="98f01-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98f01-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98f01-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 [-Name <String>]
```

## <span data-ttu-id="98f01-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98f01-105">DESCRIPTION</span></span>
<span data-ttu-id="98f01-106">Командлет Get-AzureRmEventHubConsumerGroup возвращает либо сведения о указанной группе потребителей для концентратора событий, либо список групп потребителей в заданном концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="98f01-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="98f01-107">Если указано имя группы потребителей, возвращаются сведения о одной группе потребителей.</span><span class="sxs-lookup"><span data-stu-id="98f01-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="98f01-108">Если имя группы потребителей не задано, возвращается список групп потребителей в указанном концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="98f01-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="98f01-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98f01-109">EXAMPLES</span></span>

### <span data-ttu-id="98f01-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98f01-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="98f01-111">Получает группу потребителей \` MyConsumerGroupName \` в центре событий \` MyEventHubName \` , который существует в пространстве имен \` MyNamespaceName \` с группой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="98f01-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="98f01-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="98f01-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="98f01-113">Получает список групп потребителей в центре событий \` MyEventHubName \` , который существует в пространстве имен \` MyNamespaceName \` с группой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="98f01-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="98f01-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98f01-114">PARAMETERS</span></span>

### <span data-ttu-id="98f01-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f01-115">-ResourceGroupName</span></span>
<span data-ttu-id="98f01-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98f01-116">Resource group name.</span></span>

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

### <span data-ttu-id="98f01-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="98f01-117">-EventHub</span></span>
<span data-ttu-id="98f01-118">Имя EventHub.</span><span class="sxs-lookup"><span data-stu-id="98f01-118">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98f01-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="98f01-119">-Name</span></span>
<span data-ttu-id="98f01-120">ConsumerGroup имя.</span><span class="sxs-lookup"><span data-stu-id="98f01-120">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98f01-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="98f01-121">-Namespace</span></span>
<span data-ttu-id="98f01-122">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="98f01-122">Namespace Name.</span></span>

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

## <span data-ttu-id="98f01-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98f01-123">INPUTS</span></span>

### <span data-ttu-id="98f01-124">System. String</span><span class="sxs-lookup"><span data-stu-id="98f01-124">System.String</span></span>

## <span data-ttu-id="98f01-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98f01-125">OUTPUTS</span></span>

### <span data-ttu-id="98f01-126">System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. eventhub, версия = 0.0.1.0, культура = нейтраль, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="98f01-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="98f01-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="98f01-127">NOTES</span></span>

## <span data-ttu-id="98f01-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98f01-128">RELATED LINKS</span></span>

