---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: fc108c633b70cc1eed32bcc0574ad25109a065fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220012"
---
# <span data-ttu-id="a0006-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a0006-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="a0006-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0006-102">SYNOPSIS</span></span>
<span data-ttu-id="a0006-103">Получает сведения о указанной группе потребительских концентраторов событий или список групп потребителей в центре событий.</span><span class="sxs-lookup"><span data-stu-id="a0006-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="a0006-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a0006-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0006-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0006-105">DESCRIPTION</span></span>
<span data-ttu-id="a0006-106">Этот Get-AzEventHubConsumerGroup возвращает сведения о указанной группе "Концентраторы событий" или список групп потребителей в этом центре событий.</span><span class="sxs-lookup"><span data-stu-id="a0006-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="a0006-107">Если за предоставлено имя группы потребителей, возвращаются сведения об отдельной группе потребителей.</span><span class="sxs-lookup"><span data-stu-id="a0006-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="a0006-108">Если имя группы потребителей не указано, возвращается список групп потребителей в указанном Центре событий.</span><span class="sxs-lookup"><span data-stu-id="a0006-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="a0006-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a0006-109">EXAMPLES</span></span>

### <span data-ttu-id="a0006-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a0006-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="a0006-111">Возвращает группу потребителей \` MyConsumerGroupName в Центре событий MyEventHubName, который существует в пространствах имен MyNamespaceName с группой ресурсов \` \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="a0006-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a0006-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a0006-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="a0006-113">Список групп потребителей в Центре событий MyEventHubName, который существует в области имен MyNamespaceName с группой ресурсов \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="a0006-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="a0006-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0006-114">PARAMETERS</span></span>

### <span data-ttu-id="a0006-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0006-115">-DefaultProfile</span></span>
<span data-ttu-id="a0006-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0006-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0006-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="a0006-117">-EventHub</span></span>
<span data-ttu-id="a0006-118">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="a0006-118">EventHub Name</span></span>

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

### <span data-ttu-id="a0006-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a0006-119">-MaxCount</span></span>
<span data-ttu-id="a0006-120">Определите максимальное число групп ConsumerGroups, которые нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="a0006-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

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

### <span data-ttu-id="a0006-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a0006-121">-Name</span></span>
<span data-ttu-id="a0006-122">Имя группы потребителей</span><span class="sxs-lookup"><span data-stu-id="a0006-122">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="a0006-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a0006-123">-Namespace</span></span>
<span data-ttu-id="a0006-124">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="a0006-124">Namespace Name</span></span>

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

### <span data-ttu-id="a0006-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0006-125">-ResourceGroupName</span></span>
<span data-ttu-id="a0006-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a0006-126">Resource Group Name</span></span>

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

### <span data-ttu-id="a0006-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0006-127">CommonParameters</span></span>
<span data-ttu-id="a0006-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0006-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0006-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0006-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0006-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0006-130">INPUTS</span></span>

### <span data-ttu-id="a0006-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a0006-131">System.String</span></span>

## <span data-ttu-id="a0006-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a0006-132">OUTPUTS</span></span>

### <span data-ttu-id="a0006-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="a0006-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="a0006-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a0006-134">NOTES</span></span>

## <span data-ttu-id="a0006-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0006-135">RELATED LINKS</span></span>
