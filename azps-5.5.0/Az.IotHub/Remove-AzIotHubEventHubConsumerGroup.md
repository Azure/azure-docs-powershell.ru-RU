---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 9fa0a9d85dc9c7b1a6cc56c3c329b1810cceaa18
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222252"
---
# <span data-ttu-id="54aec-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="54aec-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="54aec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54aec-102">SYNOPSIS</span></span>
<span data-ttu-id="54aec-103">Удаляет группу потребителей eventhub.</span><span class="sxs-lookup"><span data-stu-id="54aec-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="54aec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="54aec-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54aec-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54aec-105">DESCRIPTION</span></span>
<span data-ttu-id="54aec-106">Удаляет группу потребителей eventhub.</span><span class="sxs-lookup"><span data-stu-id="54aec-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="54aec-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="54aec-107">EXAMPLES</span></span>

### <span data-ttu-id="54aec-108">Пример 1. Удаление группы потребителей Eventhub из естройки телеметрии</span><span class="sxs-lookup"><span data-stu-id="54aec-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="54aec-109">Удаляет группу потребителей myconsumergroup из IotHub с именем myiothub.</span><span class="sxs-lookup"><span data-stu-id="54aec-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="54aec-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54aec-110">PARAMETERS</span></span>

### <span data-ttu-id="54aec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54aec-111">-DefaultProfile</span></span>
<span data-ttu-id="54aec-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="54aec-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54aec-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="54aec-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="54aec-114">EventHub ConsumerGroup Name.</span><span class="sxs-lookup"><span data-stu-id="54aec-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="54aec-115">-Name</span><span class="sxs-lookup"><span data-stu-id="54aec-115">-Name</span></span>
<span data-ttu-id="54aec-116">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="54aec-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="54aec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54aec-117">-ResourceGroupName</span></span>
<span data-ttu-id="54aec-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="54aec-118">Resource Group Name</span></span>

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

### <span data-ttu-id="54aec-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54aec-119">-Confirm</span></span>
<span data-ttu-id="54aec-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="54aec-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54aec-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54aec-121">-WhatIf</span></span>
<span data-ttu-id="54aec-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54aec-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54aec-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="54aec-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54aec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54aec-124">CommonParameters</span></span>
<span data-ttu-id="54aec-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54aec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54aec-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54aec-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54aec-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54aec-127">INPUTS</span></span>

### <span data-ttu-id="54aec-128">System.String</span><span class="sxs-lookup"><span data-stu-id="54aec-128">System.String</span></span>

## <span data-ttu-id="54aec-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="54aec-129">OUTPUTS</span></span>

### <span data-ttu-id="54aec-130">System.String</span><span class="sxs-lookup"><span data-stu-id="54aec-130">System.String</span></span>

## <span data-ttu-id="54aec-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="54aec-131">NOTES</span></span>

## <span data-ttu-id="54aec-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54aec-132">RELATED LINKS</span></span>
