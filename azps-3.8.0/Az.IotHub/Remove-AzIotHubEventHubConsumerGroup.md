---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 9fa0a9d85dc9c7b1a6cc56c3c329b1810cceaa18
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073797"
---
# <span data-ttu-id="174a5-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="174a5-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="174a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="174a5-102">SYNOPSIS</span></span>
<span data-ttu-id="174a5-103">Удаляет consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="174a5-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="174a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="174a5-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="174a5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="174a5-105">DESCRIPTION</span></span>
<span data-ttu-id="174a5-106">Удаляет consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="174a5-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="174a5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="174a5-107">EXAMPLES</span></span>

### <span data-ttu-id="174a5-108">Пример 1. Удаление eventhub consumergroup из eventhub для телеметрии</span><span class="sxs-lookup"><span data-stu-id="174a5-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="174a5-109">Удаляет consumergroup с именем myconsumergroup из IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="174a5-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="174a5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="174a5-110">PARAMETERS</span></span>

### <span data-ttu-id="174a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="174a5-111">-DefaultProfile</span></span>
<span data-ttu-id="174a5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="174a5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="174a5-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="174a5-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="174a5-114">Имя ConsumerGroup EventHub.</span><span class="sxs-lookup"><span data-stu-id="174a5-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="174a5-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="174a5-115">-Name</span></span>
<span data-ttu-id="174a5-116">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="174a5-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="174a5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="174a5-117">-ResourceGroupName</span></span>
<span data-ttu-id="174a5-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="174a5-118">Resource Group Name</span></span>

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

### <span data-ttu-id="174a5-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="174a5-119">-Confirm</span></span>
<span data-ttu-id="174a5-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="174a5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="174a5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="174a5-121">-WhatIf</span></span>
<span data-ttu-id="174a5-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="174a5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="174a5-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="174a5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="174a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="174a5-124">CommonParameters</span></span>
<span data-ttu-id="174a5-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="174a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="174a5-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="174a5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="174a5-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="174a5-127">INPUTS</span></span>

### <span data-ttu-id="174a5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="174a5-128">System.String</span></span>

## <span data-ttu-id="174a5-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="174a5-129">OUTPUTS</span></span>

### <span data-ttu-id="174a5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="174a5-130">System.String</span></span>

## <span data-ttu-id="174a5-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="174a5-131">NOTES</span></span>

## <span data-ttu-id="174a5-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="174a5-132">RELATED LINKS</span></span>
