---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 5f4324ab7a27b711d33042eede5c3b88d38c4511
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561779"
---
# <span data-ttu-id="25641-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="25641-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="25641-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25641-102">SYNOPSIS</span></span>
<span data-ttu-id="25641-103">Удаляет consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="25641-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25641-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25641-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25641-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25641-105">DESCRIPTION</span></span>
<span data-ttu-id="25641-106">Удаляет consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="25641-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="25641-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25641-107">EXAMPLES</span></span>

### <span data-ttu-id="25641-108">Пример 1. Удаление eventhub consumergroup из eventhub для телеметрии</span><span class="sxs-lookup"><span data-stu-id="25641-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="25641-109">Удаляет consumergroup с именем myconsumergroup из IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="25641-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="25641-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25641-110">PARAMETERS</span></span>

### <span data-ttu-id="25641-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25641-111">-DefaultProfile</span></span>
<span data-ttu-id="25641-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="25641-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25641-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="25641-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="25641-114">Имя ConsumerGroup EventHub.</span><span class="sxs-lookup"><span data-stu-id="25641-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25641-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="25641-115">-EventHubEndpointName</span></span>
<span data-ttu-id="25641-116">Имя конечной точки EventHub.</span><span class="sxs-lookup"><span data-stu-id="25641-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="25641-117">Возможные события с значениями, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="25641-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="25641-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="25641-118">-Name</span></span>
<span data-ttu-id="25641-119">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="25641-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="25641-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25641-120">-ResourceGroupName</span></span>
<span data-ttu-id="25641-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="25641-121">Resource Group Name</span></span>

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

### <span data-ttu-id="25641-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25641-122">-Confirm</span></span>
<span data-ttu-id="25641-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="25641-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25641-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25641-124">-WhatIf</span></span>
<span data-ttu-id="25641-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="25641-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25641-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="25641-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25641-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25641-127">CommonParameters</span></span>
<span data-ttu-id="25641-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25641-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25641-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25641-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25641-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25641-130">INPUTS</span></span>

### <span data-ttu-id="25641-131">System. String</span><span class="sxs-lookup"><span data-stu-id="25641-131">System.String</span></span>

## <span data-ttu-id="25641-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25641-132">OUTPUTS</span></span>

### <span data-ttu-id="25641-133">System. Collections. Generic. IEnumerable "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="25641-133">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="25641-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="25641-134">NOTES</span></span>

## <span data-ttu-id="25641-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25641-135">RELATED LINKS</span></span>

