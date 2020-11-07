---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bcd20fc9c6f0c08af2ae735558a6fccc6c9814d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734855"
---
# <span data-ttu-id="5128c-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5128c-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="5128c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5128c-102">SYNOPSIS</span></span>
<span data-ttu-id="5128c-103">Создает новую группу потребителей для определенного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="5128c-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5128c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5128c-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="5128c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5128c-105">DESCRIPTION</span></span>
<span data-ttu-id="5128c-106">Командлет New-AzureRmEventHubConsumerGroup создает новую группу потребителей для определенного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="5128c-106">The New-AzureRmEventHubConsumerGroup cmdlet creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="5128c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5128c-107">EXAMPLES</span></span>

### <span data-ttu-id="5128c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5128c-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="5128c-109">Создает группу потребителей \` MyConsumerGroupName \` в центре событий \` MyEventHubName \` , областью которого является пространство имен \` MyNamespaceName \` , с группировкой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="5128c-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="5128c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5128c-110">PARAMETERS</span></span>

### <span data-ttu-id="5128c-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5128c-111">-ResourceGroupName</span></span>
<span data-ttu-id="5128c-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5128c-112">Resource group name.</span></span>

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

### <span data-ttu-id="5128c-113">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="5128c-113">-UserMetadata</span></span>
<span data-ttu-id="5128c-114">Пользовательские метаданные для группы потребителей.</span><span class="sxs-lookup"><span data-stu-id="5128c-114">User metadata for the consumer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5128c-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5128c-115">-Confirm</span></span>
<span data-ttu-id="5128c-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5128c-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5128c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5128c-117">-WhatIf</span></span>
<span data-ttu-id="5128c-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5128c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5128c-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5128c-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5128c-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="5128c-120">-EventHub</span></span>
<span data-ttu-id="5128c-121">Имя EventHub.</span><span class="sxs-lookup"><span data-stu-id="5128c-121">EventHub Name.</span></span>

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

### <span data-ttu-id="5128c-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5128c-122">-Name</span></span>
<span data-ttu-id="5128c-123">ConsumerGroup имя.</span><span class="sxs-lookup"><span data-stu-id="5128c-123">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5128c-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5128c-124">-Namespace</span></span>
<span data-ttu-id="5128c-125">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="5128c-125">Namespace Name.</span></span>

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

## <span data-ttu-id="5128c-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5128c-126">INPUTS</span></span>

### <span data-ttu-id="5128c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5128c-127">System.String</span></span>

## <span data-ttu-id="5128c-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5128c-128">OUTPUTS</span></span>

### <span data-ttu-id="5128c-129">Microsoft. Azure. Commands. EventHub. Models. ConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="5128c-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="5128c-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="5128c-130">NOTES</span></span>

## <span data-ttu-id="5128c-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5128c-131">RELATED LINKS</span></span>

