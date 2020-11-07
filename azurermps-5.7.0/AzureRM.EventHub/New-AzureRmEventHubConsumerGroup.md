---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: a9447c745ddf60c4a2adcb2a55c824b65d96efd8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734024"
---
# <span data-ttu-id="3868c-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="3868c-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="3868c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3868c-102">SYNOPSIS</span></span>
<span data-ttu-id="3868c-103">Создает новую группу потребителей для определенного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="3868c-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3868c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3868c-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3868c-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3868c-105">EXAMPLES</span></span>

### <span data-ttu-id="3868c-106">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3868c-106">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="3868c-107">Создает группу потребителей \` MyConsumerGroupName \` в центре событий \` MyEventHubName \` , областью которого является пространство имен \` MyNamespaceName \` , с группировкой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="3868c-107">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="3868c-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3868c-108">PARAMETERS</span></span>

### <span data-ttu-id="3868c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3868c-109">-DefaultProfile</span></span>
<span data-ttu-id="3868c-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3868c-110">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3868c-111">-EventHub</span><span class="sxs-lookup"><span data-stu-id="3868c-111">-EventHub</span></span>
<span data-ttu-id="3868c-112">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="3868c-112">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3868c-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3868c-113">-Name</span></span>
<span data-ttu-id="3868c-114">Имя ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="3868c-114">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3868c-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3868c-115">-Namespace</span></span>
<span data-ttu-id="3868c-116">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="3868c-116">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3868c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3868c-117">-ResourceGroupName</span></span>
<span data-ttu-id="3868c-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3868c-118">Resource Group Name</span></span>

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

### <span data-ttu-id="3868c-119">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="3868c-119">-UserMetadata</span></span>
<span data-ttu-id="3868c-120">Метаданные пользователей для ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="3868c-120">User Metadata for ConsumerGroup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3868c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3868c-121">-Confirm</span></span>
<span data-ttu-id="3868c-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3868c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3868c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3868c-123">-WhatIf</span></span>
<span data-ttu-id="3868c-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3868c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3868c-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3868c-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3868c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3868c-126">CommonParameters</span></span>
<span data-ttu-id="3868c-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3868c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3868c-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3868c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3868c-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3868c-129">INPUTS</span></span>

### <span data-ttu-id="3868c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3868c-130">System.String</span></span>


## <span data-ttu-id="3868c-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3868c-131">OUTPUTS</span></span>

### <span data-ttu-id="3868c-132">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="3868c-132">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>


## <span data-ttu-id="3868c-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3868c-133">NOTES</span></span>

## <span data-ttu-id="3868c-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3868c-134">RELATED LINKS</span></span>
