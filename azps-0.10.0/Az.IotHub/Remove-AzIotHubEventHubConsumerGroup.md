---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: e2b6bb4c58be90b205fc4a50ddab9c84c0d1ee20
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910329"
---
# <span data-ttu-id="c9d71-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c9d71-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="c9d71-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9d71-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d71-103">Удаляет consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="c9d71-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="c9d71-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9d71-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9d71-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9d71-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d71-106">Удаляет consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="c9d71-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="c9d71-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9d71-107">EXAMPLES</span></span>

### <span data-ttu-id="c9d71-108">Пример 1. Удаление eventhub consumergroup из eventhub для телеметрии</span><span class="sxs-lookup"><span data-stu-id="c9d71-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="c9d71-109">Удаляет consumergroup с именем myconsumergroup из IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="c9d71-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="c9d71-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9d71-110">PARAMETERS</span></span>

### <span data-ttu-id="c9d71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d71-111">-DefaultProfile</span></span>
<span data-ttu-id="c9d71-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c9d71-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9d71-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="c9d71-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="c9d71-114">Имя ConsumerGroup EventHub.</span><span class="sxs-lookup"><span data-stu-id="c9d71-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="c9d71-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c9d71-115">-Name</span></span>
<span data-ttu-id="c9d71-116">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="c9d71-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="c9d71-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9d71-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9d71-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c9d71-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c9d71-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9d71-119">-Confirm</span></span>
<span data-ttu-id="c9d71-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c9d71-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9d71-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9d71-121">-WhatIf</span></span>
<span data-ttu-id="c9d71-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c9d71-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9d71-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c9d71-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9d71-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d71-124">CommonParameters</span></span>
<span data-ttu-id="c9d71-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9d71-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d71-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d71-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d71-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9d71-127">INPUTS</span></span>

### <span data-ttu-id="c9d71-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c9d71-128">System.String</span></span>

## <span data-ttu-id="c9d71-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9d71-129">OUTPUTS</span></span>

### <span data-ttu-id="c9d71-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c9d71-130">System.String</span></span>

## <span data-ttu-id="c9d71-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9d71-131">NOTES</span></span>

## <span data-ttu-id="c9d71-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9d71-132">RELATED LINKS</span></span>
