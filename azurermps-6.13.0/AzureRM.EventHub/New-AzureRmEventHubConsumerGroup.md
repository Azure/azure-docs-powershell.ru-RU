---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 34a59f0530ed036397523e3810d68175e7ee2d3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558419"
---
# <span data-ttu-id="2794c-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2794c-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="2794c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2794c-102">SYNOPSIS</span></span>
<span data-ttu-id="2794c-103">Создает новую группу потребителей для определенного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="2794c-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2794c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2794c-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2794c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2794c-105">DESCRIPTION</span></span>
<span data-ttu-id="2794c-106">Создает новую группу потребителей для определенного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="2794c-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="2794c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2794c-107">EXAMPLES</span></span>

### <span data-ttu-id="2794c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2794c-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="2794c-109">Создает группу потребителей \` MyConsumerGroupName \` в центре событий \` MyEventHubName \` , областью которого является пространство имен \` MyNamespaceName \` , с группировкой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="2794c-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="2794c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2794c-110">PARAMETERS</span></span>

### <span data-ttu-id="2794c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2794c-111">-DefaultProfile</span></span>
<span data-ttu-id="2794c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2794c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2794c-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="2794c-113">-EventHub</span></span>
<span data-ttu-id="2794c-114">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="2794c-114">EventHub Name</span></span>

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

### <span data-ttu-id="2794c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2794c-115">-Name</span></span>
<span data-ttu-id="2794c-116">Имя ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2794c-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="2794c-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2794c-117">-Namespace</span></span>
<span data-ttu-id="2794c-118">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="2794c-118">Namespace Name</span></span>

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

### <span data-ttu-id="2794c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2794c-119">-ResourceGroupName</span></span>
<span data-ttu-id="2794c-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2794c-120">Resource Group Name</span></span>

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

### <span data-ttu-id="2794c-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="2794c-121">-UserMetadata</span></span>
<span data-ttu-id="2794c-122">Метаданные пользователей для ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2794c-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="2794c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2794c-123">-Confirm</span></span>
<span data-ttu-id="2794c-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2794c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2794c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2794c-125">-WhatIf</span></span>
<span data-ttu-id="2794c-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2794c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2794c-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2794c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2794c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2794c-128">CommonParameters</span></span>
<span data-ttu-id="2794c-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2794c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2794c-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2794c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2794c-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2794c-131">INPUTS</span></span>

### <span data-ttu-id="2794c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2794c-132">System.String</span></span>

## <span data-ttu-id="2794c-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2794c-133">OUTPUTS</span></span>

### <span data-ttu-id="2794c-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="2794c-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="2794c-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="2794c-135">NOTES</span></span>

## <span data-ttu-id="2794c-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2794c-136">RELATED LINKS</span></span>
