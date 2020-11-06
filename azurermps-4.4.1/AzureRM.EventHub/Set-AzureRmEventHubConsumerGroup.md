---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c871036c6f3113bd40e17fb5bbc201fa6297573c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567636"
---
# <span data-ttu-id="3171f-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="3171f-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="3171f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3171f-102">SYNOPSIS</span></span>
<span data-ttu-id="3171f-103">Обновляет указанную группу потребителей концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="3171f-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3171f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3171f-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="3171f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3171f-105">DESCRIPTION</span></span>
<span data-ttu-id="3171f-106">Командлет Set-AzureRmEventHubConsumerGroup обновляет указанную группу потребителей концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="3171f-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="3171f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3171f-107">EXAMPLES</span></span>

### <span data-ttu-id="3171f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3171f-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="3171f-109">Задает пользовательские метаданные группы потребителей \` MyConsumerGroupName \` для "тестирование".</span><span class="sxs-lookup"><span data-stu-id="3171f-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="3171f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3171f-110">PARAMETERS</span></span>

### <span data-ttu-id="3171f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3171f-111">-ResourceGroupName</span></span>
<span data-ttu-id="3171f-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3171f-112">Resource group name.</span></span>

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

### <span data-ttu-id="3171f-113">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="3171f-113">-UserMetadata</span></span>
<span data-ttu-id="3171f-114">Метаданные пользователей для группы потребителей (необязательно).</span><span class="sxs-lookup"><span data-stu-id="3171f-114">User metadata for the consumer group (optional).</span></span>

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

### <span data-ttu-id="3171f-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3171f-115">-Confirm</span></span>
<span data-ttu-id="3171f-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3171f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3171f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3171f-117">-WhatIf</span></span>
<span data-ttu-id="3171f-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3171f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3171f-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3171f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3171f-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="3171f-120">-EventHub</span></span>
<span data-ttu-id="3171f-121">Имя EventHub.</span><span class="sxs-lookup"><span data-stu-id="3171f-121">EventHub Name.</span></span>

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

### <span data-ttu-id="3171f-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3171f-122">-Name</span></span>
<span data-ttu-id="3171f-123">ConsumerGroup имя.</span><span class="sxs-lookup"><span data-stu-id="3171f-123">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="3171f-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3171f-124">-Namespace</span></span>
<span data-ttu-id="3171f-125">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3171f-125">Namespace Name.</span></span>

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

## <span data-ttu-id="3171f-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3171f-126">INPUTS</span></span>

### <span data-ttu-id="3171f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3171f-127">System.String</span></span>

## <span data-ttu-id="3171f-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3171f-128">OUTPUTS</span></span>

### <span data-ttu-id="3171f-129">Microsoft. Azure. Commands. EventHub. Models. ConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="3171f-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="3171f-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="3171f-130">NOTES</span></span>

## <span data-ttu-id="3171f-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3171f-131">RELATED LINKS</span></span>

