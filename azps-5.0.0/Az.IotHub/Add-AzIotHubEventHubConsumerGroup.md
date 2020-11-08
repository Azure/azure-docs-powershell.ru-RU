---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 749bd1329537d165cb7c31850fd15ca23f38db2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247779"
---
# <span data-ttu-id="1d5a9-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1d5a9-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="1d5a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1d5a9-102">SYNOPSIS</span></span>
<span data-ttu-id="1d5a9-103">Создает группу потребителей eventhub.</span><span class="sxs-lookup"><span data-stu-id="1d5a9-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="1d5a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1d5a9-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d5a9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d5a9-105">DESCRIPTION</span></span>
<span data-ttu-id="1d5a9-106">Создает группу потребителей в Eventhub, связанной с указанным IotHub.</span><span class="sxs-lookup"><span data-stu-id="1d5a9-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="1d5a9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1d5a9-107">EXAMPLES</span></span>

### <span data-ttu-id="1d5a9-108">Пример 1: Добавление группы потребителей к eventhub телеметрии</span><span class="sxs-lookup"><span data-stu-id="1d5a9-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="1d5a9-109">Добавляет новый consumergroup с именем "myconsumergroup" для событий eventhub для телеметрии в iothub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="1d5a9-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="1d5a9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1d5a9-110">PARAMETERS</span></span>

### <span data-ttu-id="1d5a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d5a9-111">-DefaultProfile</span></span>
<span data-ttu-id="1d5a9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1d5a9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d5a9-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="1d5a9-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="1d5a9-114">Имя ConsumerGroup EventHub, которое вы хотите добавить.</span><span class="sxs-lookup"><span data-stu-id="1d5a9-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="1d5a9-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1d5a9-115">-Name</span></span>
<span data-ttu-id="1d5a9-116">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="1d5a9-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1d5a9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d5a9-117">-ResourceGroupName</span></span>
<span data-ttu-id="1d5a9-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1d5a9-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="1d5a9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d5a9-119">-Confirm</span></span>
<span data-ttu-id="1d5a9-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1d5a9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d5a9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d5a9-121">-WhatIf</span></span>
<span data-ttu-id="1d5a9-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1d5a9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d5a9-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1d5a9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d5a9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d5a9-124">CommonParameters</span></span>
<span data-ttu-id="1d5a9-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1d5a9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d5a9-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d5a9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d5a9-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1d5a9-127">INPUTS</span></span>

### <span data-ttu-id="1d5a9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1d5a9-128">System.String</span></span>

## <span data-ttu-id="1d5a9-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d5a9-129">OUTPUTS</span></span>

### <span data-ttu-id="1d5a9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1d5a9-130">System.String</span></span>

## <span data-ttu-id="1d5a9-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="1d5a9-131">NOTES</span></span>

## <span data-ttu-id="1d5a9-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d5a9-132">RELATED LINKS</span></span>
