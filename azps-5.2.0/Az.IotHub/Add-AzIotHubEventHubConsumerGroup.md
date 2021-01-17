---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 749bd1329537d165cb7c31850fd15ca23f38db2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399351"
---
# <span data-ttu-id="2fe34-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2fe34-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="2fe34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fe34-102">SYNOPSIS</span></span>
<span data-ttu-id="2fe34-103">Создает группу eventhub для потребителей.</span><span class="sxs-lookup"><span data-stu-id="2fe34-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="2fe34-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2fe34-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2fe34-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fe34-105">DESCRIPTION</span></span>
<span data-ttu-id="2fe34-106">Создает группу потребителей в Eventhub, связанном с указанным IotHub.</span><span class="sxs-lookup"><span data-stu-id="2fe34-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="2fe34-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2fe34-107">EXAMPLES</span></span>

### <span data-ttu-id="2fe34-108">Пример 1. Добавление группы потребителей в е eventhub телеметрии</span><span class="sxs-lookup"><span data-stu-id="2fe34-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="2fe34-109">Добавляет новую группу потребителей с именем myconsumergroup в еверху для событий телеметрии в iothub с именем myiothub.</span><span class="sxs-lookup"><span data-stu-id="2fe34-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="2fe34-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fe34-110">PARAMETERS</span></span>

### <span data-ttu-id="2fe34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fe34-111">-DefaultProfile</span></span>
<span data-ttu-id="2fe34-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2fe34-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fe34-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="2fe34-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="2fe34-114">Имя группы Потребителей EventHub, которую вы хотите добавить.</span><span class="sxs-lookup"><span data-stu-id="2fe34-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="2fe34-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2fe34-115">-Name</span></span>
<span data-ttu-id="2fe34-116">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="2fe34-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2fe34-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fe34-117">-ResourceGroupName</span></span>
<span data-ttu-id="2fe34-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2fe34-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="2fe34-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fe34-119">-Confirm</span></span>
<span data-ttu-id="2fe34-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2fe34-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fe34-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fe34-121">-WhatIf</span></span>
<span data-ttu-id="2fe34-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fe34-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fe34-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2fe34-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fe34-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fe34-124">CommonParameters</span></span>
<span data-ttu-id="2fe34-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fe34-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fe34-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fe34-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fe34-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2fe34-127">INPUTS</span></span>

### <span data-ttu-id="2fe34-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2fe34-128">System.String</span></span>

## <span data-ttu-id="2fe34-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2fe34-129">OUTPUTS</span></span>

### <span data-ttu-id="2fe34-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2fe34-130">System.String</span></span>

## <span data-ttu-id="2fe34-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2fe34-131">NOTES</span></span>

## <span data-ttu-id="2fe34-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fe34-132">RELATED LINKS</span></span>
