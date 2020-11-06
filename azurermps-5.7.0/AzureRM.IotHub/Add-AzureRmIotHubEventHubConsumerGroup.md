---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 192a20ee3d49bd79dff833a05ffd3ff98bcc30ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568586"
---
# <span data-ttu-id="ae01b-101">Add-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ae01b-101">Add-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="ae01b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae01b-102">SYNOPSIS</span></span>
<span data-ttu-id="ae01b-103">Создает группу потребителей eventhub.</span><span class="sxs-lookup"><span data-stu-id="ae01b-103">Creates an eventhub consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae01b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae01b-104">SYNTAX</span></span>

```
Add-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae01b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae01b-105">DESCRIPTION</span></span>
<span data-ttu-id="ae01b-106">Создает группу потребителей в Eventhub, связанной с указанным IotHub.</span><span class="sxs-lookup"><span data-stu-id="ae01b-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="ae01b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae01b-107">EXAMPLES</span></span>

### <span data-ttu-id="ae01b-108">Пример 1: Добавление группы потребителей к eventhub телеметрии</span><span class="sxs-lookup"><span data-stu-id="ae01b-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="ae01b-109">Добавляет новый consumergroup с именем "myconsumergroup" для событий eventhub для телеметрии в iothub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="ae01b-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="ae01b-110">Пример 2: Добавление группы потребителей к контролю операций в eventhub</span><span class="sxs-lookup"><span data-stu-id="ae01b-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="ae01b-111">Добавляет новую consumergroup с именем "myconsumergroup" в eventhub для событий мониторинга операций в iothub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="ae01b-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="ae01b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae01b-112">PARAMETERS</span></span>

### <span data-ttu-id="ae01b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae01b-113">-DefaultProfile</span></span>
<span data-ttu-id="ae01b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ae01b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae01b-115">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="ae01b-115">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="ae01b-116">Имя ConsumerGroup EventHub, которое вы хотите добавить.</span><span class="sxs-lookup"><span data-stu-id="ae01b-116">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae01b-117">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="ae01b-117">-EventHubEndpointName</span></span>
<span data-ttu-id="ae01b-118">Имя конечной точки EventHub.</span><span class="sxs-lookup"><span data-stu-id="ae01b-118">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="ae01b-119">Возможные события с значениями, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="ae01b-119">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae01b-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ae01b-120">-Name</span></span>
<span data-ttu-id="ae01b-121">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="ae01b-121">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae01b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae01b-122">-ResourceGroupName</span></span>
<span data-ttu-id="ae01b-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae01b-123">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="ae01b-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae01b-124">-Confirm</span></span>
<span data-ttu-id="ae01b-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ae01b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae01b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae01b-126">-WhatIf</span></span>
<span data-ttu-id="ae01b-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ae01b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae01b-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ae01b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae01b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae01b-129">CommonParameters</span></span>
<span data-ttu-id="ae01b-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae01b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae01b-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae01b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae01b-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae01b-132">INPUTS</span></span>

### <span data-ttu-id="ae01b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ae01b-133">System.String</span></span>

## <span data-ttu-id="ae01b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae01b-134">OUTPUTS</span></span>

### <span data-ttu-id="ae01b-135">System. Collections. Generic. IEnumerable "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ae01b-135">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ae01b-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae01b-136">NOTES</span></span>

## <span data-ttu-id="ae01b-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae01b-137">RELATED LINKS</span></span>

