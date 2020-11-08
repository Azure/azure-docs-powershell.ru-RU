---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 749bd1329537d165cb7c31850fd15ca23f38db2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236435"
---
# <span data-ttu-id="6397c-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="6397c-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="6397c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6397c-102">SYNOPSIS</span></span>
<span data-ttu-id="6397c-103">Создает группу потребителей eventhub.</span><span class="sxs-lookup"><span data-stu-id="6397c-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="6397c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6397c-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6397c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6397c-105">DESCRIPTION</span></span>
<span data-ttu-id="6397c-106">Создает группу потребителей в Eventhub, связанной с указанным IotHub.</span><span class="sxs-lookup"><span data-stu-id="6397c-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="6397c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6397c-107">EXAMPLES</span></span>

### <span data-ttu-id="6397c-108">Пример 1: Добавление группы потребителей к eventhub телеметрии</span><span class="sxs-lookup"><span data-stu-id="6397c-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="6397c-109">Добавляет новый consumergroup с именем "myconsumergroup" для событий eventhub для телеметрии в iothub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="6397c-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="6397c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6397c-110">PARAMETERS</span></span>

### <span data-ttu-id="6397c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6397c-111">-DefaultProfile</span></span>
<span data-ttu-id="6397c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6397c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6397c-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="6397c-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="6397c-114">Имя ConsumerGroup EventHub, которое вы хотите добавить.</span><span class="sxs-lookup"><span data-stu-id="6397c-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6397c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6397c-115">-Name</span></span>
<span data-ttu-id="6397c-116">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="6397c-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6397c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6397c-117">-ResourceGroupName</span></span>
<span data-ttu-id="6397c-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6397c-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="6397c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6397c-119">-Confirm</span></span>
<span data-ttu-id="6397c-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6397c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6397c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6397c-121">-WhatIf</span></span>
<span data-ttu-id="6397c-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6397c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6397c-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6397c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6397c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6397c-124">CommonParameters</span></span>
<span data-ttu-id="6397c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6397c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6397c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6397c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6397c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6397c-127">INPUTS</span></span>

### <span data-ttu-id="6397c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6397c-128">System.String</span></span>

## <span data-ttu-id="6397c-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6397c-129">OUTPUTS</span></span>

### <span data-ttu-id="6397c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6397c-130">System.String</span></span>

## <span data-ttu-id="6397c-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6397c-131">NOTES</span></span>

## <span data-ttu-id="6397c-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6397c-132">RELATED LINKS</span></span>
