---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 59e7652d8ca3b2e26246ba4f8924f6a6b9d48f96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560176"
---
# <span data-ttu-id="672ae-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="672ae-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="672ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="672ae-102">SYNOPSIS</span></span>
<span data-ttu-id="672ae-103">Удаляет consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="672ae-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="672ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="672ae-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="672ae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="672ae-105">DESCRIPTION</span></span>
<span data-ttu-id="672ae-106">Удаляет consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="672ae-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="672ae-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="672ae-107">EXAMPLES</span></span>

### <span data-ttu-id="672ae-108">Пример 1. Удаление eventhub consumergroup из eventhub для телеметрии</span><span class="sxs-lookup"><span data-stu-id="672ae-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="672ae-109">Удаляет consumergroup с именем myconsumergroup из IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="672ae-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="672ae-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="672ae-110">PARAMETERS</span></span>

### <span data-ttu-id="672ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="672ae-111">-DefaultProfile</span></span>
<span data-ttu-id="672ae-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="672ae-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="672ae-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="672ae-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="672ae-114">Имя ConsumerGroup EventHub.</span><span class="sxs-lookup"><span data-stu-id="672ae-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="672ae-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="672ae-115">-EventHubEndpointName</span></span>
<span data-ttu-id="672ae-116">Имя конечной точки EventHub.</span><span class="sxs-lookup"><span data-stu-id="672ae-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="672ae-117">Возможные события с значениями, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="672ae-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="672ae-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="672ae-118">-Name</span></span>
<span data-ttu-id="672ae-119">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="672ae-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="672ae-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="672ae-120">-ResourceGroupName</span></span>
<span data-ttu-id="672ae-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="672ae-121">Resource Group Name</span></span>

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

### <span data-ttu-id="672ae-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="672ae-122">-Confirm</span></span>
<span data-ttu-id="672ae-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="672ae-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="672ae-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="672ae-124">-WhatIf</span></span>
<span data-ttu-id="672ae-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="672ae-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="672ae-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="672ae-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="672ae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="672ae-127">CommonParameters</span></span>
<span data-ttu-id="672ae-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="672ae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="672ae-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="672ae-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="672ae-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="672ae-130">INPUTS</span></span>

### <span data-ttu-id="672ae-131">System. String</span><span class="sxs-lookup"><span data-stu-id="672ae-131">System.String</span></span>

## <span data-ttu-id="672ae-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="672ae-132">OUTPUTS</span></span>

### <span data-ttu-id="672ae-133">System. String</span><span class="sxs-lookup"><span data-stu-id="672ae-133">System.String</span></span>

## <span data-ttu-id="672ae-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="672ae-134">NOTES</span></span>

## <span data-ttu-id="672ae-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="672ae-135">RELATED LINKS</span></span>
