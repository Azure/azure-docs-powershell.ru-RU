---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: ef03af9c452496d198aaaa073ee9fd967d851bb4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214748"
---
# <span data-ttu-id="660a9-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="660a9-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="660a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="660a9-102">SYNOPSIS</span></span>
<span data-ttu-id="660a9-103">Создает группу для указанного центра событий.</span><span class="sxs-lookup"><span data-stu-id="660a9-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="660a9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="660a9-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="660a9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="660a9-105">DESCRIPTION</span></span>
<span data-ttu-id="660a9-106">Создает группу для указанного центра событий.</span><span class="sxs-lookup"><span data-stu-id="660a9-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="660a9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="660a9-107">EXAMPLES</span></span>

### <span data-ttu-id="660a9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="660a9-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="660a9-109">Создает группу для потребителей MyConsumerGroupName в Центре событий MyEventHubName, область действия которого состоит из пространства имен \` \` \` \` \` MyNamespaceName и группы ресурсов \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="660a9-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="660a9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="660a9-110">PARAMETERS</span></span>

### <span data-ttu-id="660a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="660a9-111">-DefaultProfile</span></span>
<span data-ttu-id="660a9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="660a9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="660a9-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="660a9-113">-EventHub</span></span>
<span data-ttu-id="660a9-114">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="660a9-114">EventHub Name</span></span>

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

### <span data-ttu-id="660a9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="660a9-115">-Name</span></span>
<span data-ttu-id="660a9-116">Имя группы потребителей</span><span class="sxs-lookup"><span data-stu-id="660a9-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="660a9-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="660a9-117">-Namespace</span></span>
<span data-ttu-id="660a9-118">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="660a9-118">Namespace Name</span></span>

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

### <span data-ttu-id="660a9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="660a9-119">-ResourceGroupName</span></span>
<span data-ttu-id="660a9-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="660a9-120">Resource Group Name</span></span>

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

### <span data-ttu-id="660a9-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="660a9-121">-UserMetadata</span></span>
<span data-ttu-id="660a9-122">Метаданные пользователя для ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="660a9-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="660a9-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="660a9-123">-Confirm</span></span>
<span data-ttu-id="660a9-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="660a9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="660a9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="660a9-125">-WhatIf</span></span>
<span data-ttu-id="660a9-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="660a9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="660a9-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="660a9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="660a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="660a9-128">CommonParameters</span></span>
<span data-ttu-id="660a9-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="660a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="660a9-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="660a9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="660a9-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="660a9-131">INPUTS</span></span>

### <span data-ttu-id="660a9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="660a9-132">System.String</span></span>

## <span data-ttu-id="660a9-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="660a9-133">OUTPUTS</span></span>

### <span data-ttu-id="660a9-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="660a9-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="660a9-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="660a9-135">NOTES</span></span>

## <span data-ttu-id="660a9-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="660a9-136">RELATED LINKS</span></span>
