---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: b326f7228a60f7549fc6dcd227b9bad947f22add
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568769"
---
# <span data-ttu-id="cc7f2-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="cc7f2-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="cc7f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cc7f2-102">SYNOPSIS</span></span>
<span data-ttu-id="cc7f2-103">Удаляет consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="cc7f2-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc7f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cc7f2-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc7f2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc7f2-105">DESCRIPTION</span></span>
<span data-ttu-id="cc7f2-106">Удаляет consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="cc7f2-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="cc7f2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cc7f2-107">EXAMPLES</span></span>

### <span data-ttu-id="cc7f2-108">Пример 1. Удаление eventhub consumergroup из eventhub для телеметрии</span><span class="sxs-lookup"><span data-stu-id="cc7f2-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="cc7f2-109">Удаляет consumergroup с именем myconsumergroup из IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="cc7f2-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="cc7f2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cc7f2-110">PARAMETERS</span></span>

### <span data-ttu-id="cc7f2-111">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="cc7f2-111">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="cc7f2-112">Имя ConsumerGroup EventHub.</span><span class="sxs-lookup"><span data-stu-id="cc7f2-112">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="cc7f2-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="cc7f2-113">-EventHubEndpointName</span></span>
<span data-ttu-id="cc7f2-114">Имя конечной точки EventHub.</span><span class="sxs-lookup"><span data-stu-id="cc7f2-114">EventHub Endpoint Name.</span></span>
<span data-ttu-id="cc7f2-115">Возможные события с значениями, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="cc7f2-115">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="cc7f2-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cc7f2-116">-Name</span></span>
<span data-ttu-id="cc7f2-117">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="cc7f2-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="cc7f2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc7f2-118">-ResourceGroupName</span></span>
<span data-ttu-id="cc7f2-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cc7f2-119">Resource Group Name</span></span>

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

### <span data-ttu-id="cc7f2-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc7f2-120">-Confirm</span></span>
<span data-ttu-id="cc7f2-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cc7f2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc7f2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc7f2-122">-WhatIf</span></span>
<span data-ttu-id="cc7f2-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cc7f2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc7f2-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cc7f2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc7f2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc7f2-125">-DefaultProfile</span></span>
<span data-ttu-id="cc7f2-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc7f2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc7f2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc7f2-127">CommonParameters</span></span>
<span data-ttu-id="cc7f2-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cc7f2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc7f2-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc7f2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc7f2-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cc7f2-130">INPUTS</span></span>

### <span data-ttu-id="cc7f2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cc7f2-131">System.String</span></span>

## <span data-ttu-id="cc7f2-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc7f2-132">OUTPUTS</span></span>

### <span data-ttu-id="cc7f2-133">System. Collections. Generic. IEnumerable "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cc7f2-133">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="cc7f2-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="cc7f2-134">NOTES</span></span>

## <span data-ttu-id="cc7f2-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc7f2-135">RELATED LINKS</span></span>

