---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 938949ae1eada6d85bb6e01728f5be09655c3e06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720771"
---
# <span data-ttu-id="63547-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="63547-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="63547-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63547-102">SYNOPSIS</span></span>
<span data-ttu-id="63547-103">Создает группу потребителей eventhub.</span><span class="sxs-lookup"><span data-stu-id="63547-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="63547-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63547-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63547-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63547-105">DESCRIPTION</span></span>
<span data-ttu-id="63547-106">Создает группу потребителей в Eventhub, связанной с указанным IotHub.</span><span class="sxs-lookup"><span data-stu-id="63547-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="63547-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63547-107">EXAMPLES</span></span>

### <span data-ttu-id="63547-108">Пример 1: Добавление группы потребителей к eventhub телеметрии</span><span class="sxs-lookup"><span data-stu-id="63547-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="63547-109">Добавляет новый consumergroup с именем "myconsumergroup" для событий eventhub для телеметрии в iothub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="63547-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="63547-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63547-110">PARAMETERS</span></span>

### <span data-ttu-id="63547-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63547-111">-DefaultProfile</span></span>
<span data-ttu-id="63547-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="63547-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63547-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="63547-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="63547-114">Имя ConsumerGroup EventHub, которое вы хотите добавить.</span><span class="sxs-lookup"><span data-stu-id="63547-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="63547-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="63547-115">-EventHubEndpointName</span></span>
<span data-ttu-id="63547-116">Имя конечной точки EventHub.</span><span class="sxs-lookup"><span data-stu-id="63547-116">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="63547-117">Возможные события с значениями, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="63547-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="63547-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63547-118">-Name</span></span>
<span data-ttu-id="63547-119">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="63547-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="63547-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63547-120">-ResourceGroupName</span></span>
<span data-ttu-id="63547-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63547-121">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="63547-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63547-122">-Confirm</span></span>
<span data-ttu-id="63547-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63547-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63547-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63547-124">-WhatIf</span></span>
<span data-ttu-id="63547-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63547-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63547-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63547-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63547-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63547-127">CommonParameters</span></span>
<span data-ttu-id="63547-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63547-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63547-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63547-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63547-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63547-130">INPUTS</span></span>

### <span data-ttu-id="63547-131">System. String</span><span class="sxs-lookup"><span data-stu-id="63547-131">System.String</span></span>

## <span data-ttu-id="63547-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63547-132">OUTPUTS</span></span>

### <span data-ttu-id="63547-133">System. String</span><span class="sxs-lookup"><span data-stu-id="63547-133">System.String</span></span>

## <span data-ttu-id="63547-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="63547-134">NOTES</span></span>

## <span data-ttu-id="63547-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63547-135">RELATED LINKS</span></span>
