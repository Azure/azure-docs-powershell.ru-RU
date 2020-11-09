---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: ef03af9c452496d198aaaa073ee9fd967d851bb4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248676"
---
# <span data-ttu-id="a6601-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a6601-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="a6601-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6601-102">SYNOPSIS</span></span>
<span data-ttu-id="a6601-103">Создает новую группу потребителей для определенного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="a6601-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="a6601-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6601-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6601-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6601-105">DESCRIPTION</span></span>
<span data-ttu-id="a6601-106">Создает новую группу потребителей для определенного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="a6601-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="a6601-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6601-107">EXAMPLES</span></span>

### <span data-ttu-id="a6601-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a6601-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="a6601-109">Создает группу потребителей \` MyConsumerGroupName \` в центре событий \` MyEventHubName \` , областью которого является пространство имен \` MyNamespaceName \` , с группировкой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a6601-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="a6601-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6601-110">PARAMETERS</span></span>

### <span data-ttu-id="a6601-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6601-111">-DefaultProfile</span></span>
<span data-ttu-id="a6601-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6601-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6601-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="a6601-113">-EventHub</span></span>
<span data-ttu-id="a6601-114">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="a6601-114">EventHub Name</span></span>

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

### <span data-ttu-id="a6601-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a6601-115">-Name</span></span>
<span data-ttu-id="a6601-116">Имя ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a6601-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="a6601-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a6601-117">-Namespace</span></span>
<span data-ttu-id="a6601-118">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="a6601-118">Namespace Name</span></span>

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

### <span data-ttu-id="a6601-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6601-119">-ResourceGroupName</span></span>
<span data-ttu-id="a6601-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a6601-120">Resource Group Name</span></span>

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

### <span data-ttu-id="a6601-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="a6601-121">-UserMetadata</span></span>
<span data-ttu-id="a6601-122">Метаданные пользователей для ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a6601-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="a6601-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6601-123">-Confirm</span></span>
<span data-ttu-id="a6601-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a6601-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6601-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6601-125">-WhatIf</span></span>
<span data-ttu-id="a6601-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a6601-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6601-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a6601-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6601-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6601-128">CommonParameters</span></span>
<span data-ttu-id="a6601-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6601-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6601-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6601-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6601-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6601-131">INPUTS</span></span>

### <span data-ttu-id="a6601-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a6601-132">System.String</span></span>

## <span data-ttu-id="a6601-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6601-133">OUTPUTS</span></span>

### <span data-ttu-id="a6601-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="a6601-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="a6601-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6601-135">NOTES</span></span>

## <span data-ttu-id="a6601-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6601-136">RELATED LINKS</span></span>