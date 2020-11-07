---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 59a180d422a27ca9d2c3e1e4932d843ba7c70093
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900305"
---
# <span data-ttu-id="591fa-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="591fa-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="591fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="591fa-102">SYNOPSIS</span></span>
<span data-ttu-id="591fa-103">Удаляет consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="591fa-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="591fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="591fa-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="591fa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="591fa-105">DESCRIPTION</span></span>
<span data-ttu-id="591fa-106">Удаляет consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="591fa-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="591fa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="591fa-107">EXAMPLES</span></span>

### <span data-ttu-id="591fa-108">Пример 1. Удаление eventhub consumergroup из eventhub для телеметрии</span><span class="sxs-lookup"><span data-stu-id="591fa-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="591fa-109">Удаляет consumergroup с именем myconsumergroup из IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="591fa-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="591fa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="591fa-110">PARAMETERS</span></span>

### <span data-ttu-id="591fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591fa-111">-DefaultProfile</span></span>
<span data-ttu-id="591fa-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="591fa-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="591fa-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="591fa-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="591fa-114">Имя ConsumerGroup EventHub.</span><span class="sxs-lookup"><span data-stu-id="591fa-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591fa-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="591fa-115">-EventHubEndpointName</span></span>
<span data-ttu-id="591fa-116">Имя конечной точки EventHub.</span><span class="sxs-lookup"><span data-stu-id="591fa-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="591fa-117">Возможные события с значениями, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="591fa-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="591fa-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="591fa-118">-Name</span></span>
<span data-ttu-id="591fa-119">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="591fa-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="591fa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="591fa-120">-ResourceGroupName</span></span>
<span data-ttu-id="591fa-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="591fa-121">Resource Group Name</span></span>

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

### <span data-ttu-id="591fa-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="591fa-122">-Confirm</span></span>
<span data-ttu-id="591fa-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="591fa-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="591fa-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="591fa-124">-WhatIf</span></span>
<span data-ttu-id="591fa-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="591fa-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="591fa-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="591fa-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="591fa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591fa-127">CommonParameters</span></span>
<span data-ttu-id="591fa-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="591fa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591fa-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="591fa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591fa-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="591fa-130">INPUTS</span></span>

### <span data-ttu-id="591fa-131">System. String</span><span class="sxs-lookup"><span data-stu-id="591fa-131">System.String</span></span>

## <span data-ttu-id="591fa-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="591fa-132">OUTPUTS</span></span>

### <span data-ttu-id="591fa-133">System. String</span><span class="sxs-lookup"><span data-stu-id="591fa-133">System.String</span></span>

## <span data-ttu-id="591fa-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="591fa-134">NOTES</span></span>

## <span data-ttu-id="591fa-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="591fa-135">RELATED LINKS</span></span>
