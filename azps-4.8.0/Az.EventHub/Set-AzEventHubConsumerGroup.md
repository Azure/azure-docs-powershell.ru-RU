---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: cb898921b7fdfddddc95fc88d49dade4654c7ad2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077770"
---
# <span data-ttu-id="3d46e-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="3d46e-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="3d46e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d46e-102">SYNOPSIS</span></span>
<span data-ttu-id="3d46e-103">Обновляет указанную группу потребителей концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="3d46e-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="3d46e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d46e-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d46e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d46e-105">DESCRIPTION</span></span>
<span data-ttu-id="3d46e-106">Командлет Set-AzEventHubConsumerGroup обновляет указанную группу потребителей концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="3d46e-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="3d46e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d46e-107">EXAMPLES</span></span>

### <span data-ttu-id="3d46e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3d46e-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="3d46e-109">Задает пользовательские метаданные группы потребителей \` MyConsumerGroupName \` для "тестирование".</span><span class="sxs-lookup"><span data-stu-id="3d46e-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="3d46e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d46e-110">PARAMETERS</span></span>

### <span data-ttu-id="3d46e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d46e-111">-DefaultProfile</span></span>
<span data-ttu-id="3d46e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d46e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d46e-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="3d46e-113">-EventHub</span></span>
<span data-ttu-id="3d46e-114">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="3d46e-114">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d46e-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d46e-115">-Name</span></span>
<span data-ttu-id="3d46e-116">Имя ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="3d46e-116">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d46e-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3d46e-117">-Namespace</span></span>
<span data-ttu-id="3d46e-118">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="3d46e-118">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d46e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d46e-119">-ResourceGroupName</span></span>
<span data-ttu-id="3d46e-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3d46e-120">Resource Group Name</span></span>

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

### <span data-ttu-id="3d46e-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="3d46e-121">-UserMetadata</span></span>
<span data-ttu-id="3d46e-122">Метаданные пользователей для ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="3d46e-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d46e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d46e-123">-Confirm</span></span>
<span data-ttu-id="3d46e-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3d46e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d46e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d46e-125">-WhatIf</span></span>
<span data-ttu-id="3d46e-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3d46e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d46e-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3d46e-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d46e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d46e-128">CommonParameters</span></span>
<span data-ttu-id="3d46e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d46e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d46e-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d46e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d46e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d46e-131">INPUTS</span></span>

### <span data-ttu-id="3d46e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3d46e-132">System.String</span></span>

## <span data-ttu-id="3d46e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d46e-133">OUTPUTS</span></span>

### <span data-ttu-id="3d46e-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="3d46e-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="3d46e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d46e-135">NOTES</span></span>

## <span data-ttu-id="3d46e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d46e-136">RELATED LINKS</span></span>
