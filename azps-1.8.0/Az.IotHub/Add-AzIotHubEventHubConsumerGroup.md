---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: c4378b156d17759c180ee3bf966bc20d06d00b41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900393"
---
# <span data-ttu-id="b1d84-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b1d84-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="b1d84-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1d84-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d84-103">Создает группу потребителей eventhub.</span><span class="sxs-lookup"><span data-stu-id="b1d84-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="b1d84-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1d84-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1d84-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1d84-105">DESCRIPTION</span></span>
<span data-ttu-id="b1d84-106">Создает группу потребителей в Eventhub, связанной с указанным IotHub.</span><span class="sxs-lookup"><span data-stu-id="b1d84-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="b1d84-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1d84-107">EXAMPLES</span></span>

### <span data-ttu-id="b1d84-108">Пример 1: Добавление группы потребителей к eventhub телеметрии</span><span class="sxs-lookup"><span data-stu-id="b1d84-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="b1d84-109">Добавляет новый consumergroup с именем "myconsumergroup" для событий eventhub для телеметрии в iothub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="b1d84-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="b1d84-110">Пример 2: Добавление группы потребителей к контролю операций в eventhub</span><span class="sxs-lookup"><span data-stu-id="b1d84-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="b1d84-111">Добавляет новую consumergroup с именем "myconsumergroup" в eventhub для событий мониторинга операций в iothub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="b1d84-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="b1d84-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1d84-112">PARAMETERS</span></span>

### <span data-ttu-id="b1d84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1d84-113">-DefaultProfile</span></span>
<span data-ttu-id="b1d84-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b1d84-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1d84-115">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="b1d84-115">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="b1d84-116">Имя ConsumerGroup EventHub, которое вы хотите добавить.</span><span class="sxs-lookup"><span data-stu-id="b1d84-116">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1d84-117">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="b1d84-117">-EventHubEndpointName</span></span>
<span data-ttu-id="b1d84-118">Имя конечной точки EventHub.</span><span class="sxs-lookup"><span data-stu-id="b1d84-118">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="b1d84-119">Возможные события с значениями, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="b1d84-119">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1d84-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b1d84-120">-Name</span></span>
<span data-ttu-id="b1d84-121">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="b1d84-121">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d84-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1d84-122">-ResourceGroupName</span></span>
<span data-ttu-id="b1d84-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b1d84-123">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="b1d84-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1d84-124">-Confirm</span></span>
<span data-ttu-id="b1d84-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b1d84-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1d84-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1d84-126">-WhatIf</span></span>
<span data-ttu-id="b1d84-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b1d84-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1d84-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b1d84-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1d84-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d84-129">CommonParameters</span></span>
<span data-ttu-id="b1d84-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1d84-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d84-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1d84-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d84-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1d84-132">INPUTS</span></span>

### <span data-ttu-id="b1d84-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b1d84-133">System.String</span></span>

## <span data-ttu-id="b1d84-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1d84-134">OUTPUTS</span></span>

### <span data-ttu-id="b1d84-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b1d84-135">System.String</span></span>

## <span data-ttu-id="b1d84-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1d84-136">NOTES</span></span>

## <span data-ttu-id="b1d84-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1d84-137">RELATED LINKS</span></span>
