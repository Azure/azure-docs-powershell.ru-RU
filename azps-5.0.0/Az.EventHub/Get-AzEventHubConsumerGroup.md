---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: fc108c633b70cc1eed32bcc0574ad25109a065fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248693"
---
# <span data-ttu-id="e2623-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e2623-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="e2623-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2623-102">SYNOPSIS</span></span>
<span data-ttu-id="e2623-103">Получает сведения о группе потребителей указанных концентраторов событий или получает список групп потребителей в концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="e2623-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="e2623-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2623-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2623-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2623-105">DESCRIPTION</span></span>
<span data-ttu-id="e2623-106">Командлет Get-AzEventHubConsumerGroup возвращает либо сведения о указанной группе потребителей для концентратора событий, либо список групп потребителей в заданном концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="e2623-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="e2623-107">Если указано имя группы потребителей, возвращаются сведения о одной группе потребителей.</span><span class="sxs-lookup"><span data-stu-id="e2623-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="e2623-108">Если имя группы потребителей не задано, возвращается список групп потребителей в указанном концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="e2623-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="e2623-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2623-109">EXAMPLES</span></span>

### <span data-ttu-id="e2623-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e2623-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="e2623-111">Получает группу потребителей \` MyConsumerGroupName \` в центре событий \` MyEventHubName \` , который существует в пространстве имен \` MyNamespaceName \` с группой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="e2623-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e2623-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e2623-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="e2623-113">Получает список групп потребителей в центре событий \` MyEventHubName \` , который существует в пространстве имен \` MyNamespaceName \` с группой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="e2623-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e2623-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2623-114">PARAMETERS</span></span>

### <span data-ttu-id="e2623-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2623-115">-DefaultProfile</span></span>
<span data-ttu-id="e2623-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2623-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2623-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e2623-117">-EventHub</span></span>
<span data-ttu-id="e2623-118">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="e2623-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2623-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e2623-119">-MaxCount</span></span>
<span data-ttu-id="e2623-120">Определите максимальное число возвращаемых ConsumerGroups.</span><span class="sxs-lookup"><span data-stu-id="e2623-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

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

### <span data-ttu-id="e2623-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2623-121">-Name</span></span>
<span data-ttu-id="e2623-122">Имя ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e2623-122">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2623-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2623-123">-Namespace</span></span>
<span data-ttu-id="e2623-124">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="e2623-124">Namespace Name</span></span>

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

### <span data-ttu-id="e2623-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2623-125">-ResourceGroupName</span></span>
<span data-ttu-id="e2623-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e2623-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e2623-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2623-127">CommonParameters</span></span>
<span data-ttu-id="e2623-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2623-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2623-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2623-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2623-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2623-130">INPUTS</span></span>

### <span data-ttu-id="e2623-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e2623-131">System.String</span></span>

## <span data-ttu-id="e2623-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2623-132">OUTPUTS</span></span>

### <span data-ttu-id="e2623-133">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="e2623-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="e2623-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2623-134">NOTES</span></span>

## <span data-ttu-id="e2623-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2623-135">RELATED LINKS</span></span>