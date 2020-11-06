---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c8684e9af0bca55dca52f336a458f4c428ca67a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566728"
---
# <span data-ttu-id="5f156-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5f156-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="5f156-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5f156-102">SYNOPSIS</span></span>
<span data-ttu-id="5f156-103">Удаляет указанную группу потребителей концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="5f156-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f156-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5f156-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="5f156-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f156-105">DESCRIPTION</span></span>
<span data-ttu-id="5f156-106">Командлет Remove-AzureRmEventHubConsumerGroup удаляет указанную группу потребителей из заданного концентратора событий и удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="5f156-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="5f156-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5f156-107">EXAMPLES</span></span>

### <span data-ttu-id="5f156-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5f156-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="5f156-109">Удаляет группу потребителей \` MyConsumerGroupName \` из MyEventHubName концентратора событий \` с \` областью в \` \` пространство имен MyNamespaceName.</span><span class="sxs-lookup"><span data-stu-id="5f156-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="5f156-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5f156-110">PARAMETERS</span></span>

### <span data-ttu-id="5f156-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f156-111">-ResourceGroupName</span></span>
<span data-ttu-id="5f156-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5f156-112">Resource group name.</span></span>

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

### <span data-ttu-id="5f156-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f156-113">-Confirm</span></span>
<span data-ttu-id="5f156-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5f156-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f156-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f156-115">-WhatIf</span></span>
<span data-ttu-id="5f156-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5f156-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f156-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5f156-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f156-118">-EventHub</span><span class="sxs-lookup"><span data-stu-id="5f156-118">-EventHub</span></span>
<span data-ttu-id="5f156-119">Имя EventHub.</span><span class="sxs-lookup"><span data-stu-id="5f156-119">EventHub Name.</span></span>

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

### <span data-ttu-id="5f156-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5f156-120">-Name</span></span>
<span data-ttu-id="5f156-121">ConsumerGroup имя.</span><span class="sxs-lookup"><span data-stu-id="5f156-121">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="5f156-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5f156-122">-Namespace</span></span>
<span data-ttu-id="5f156-123">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="5f156-123">Namespace Name.</span></span>

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

## <span data-ttu-id="5f156-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5f156-124">INPUTS</span></span>

### <span data-ttu-id="5f156-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5f156-125">System.String</span></span>

## <span data-ttu-id="5f156-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f156-126">OUTPUTS</span></span>

### <span data-ttu-id="5f156-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="5f156-127">System.Object</span></span>

## <span data-ttu-id="5f156-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="5f156-128">NOTES</span></span>

## <span data-ttu-id="5f156-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f156-129">RELATED LINKS</span></span>

