---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 2ff36708ba9b8303c8b8763146c81ee4e4d8b209
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566725"
---
# <span data-ttu-id="d4e10-101">Set-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="d4e10-101">Set-AzureRmEventHub</span></span>

## <span data-ttu-id="d4e10-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4e10-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e10-103">Обновляет указанный центр событий.</span><span class="sxs-lookup"><span data-stu-id="d4e10-103">Updates the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4e10-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4e10-104">SYNTAX</span></span>

### <span data-ttu-id="d4e10-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d4e10-105">EventhubInputObjectSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d4e10-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="d4e10-106">EventhubPropertiesSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d4e10-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4e10-107">DESCRIPTION</span></span>
<span data-ttu-id="d4e10-108">Командлет Set-AzureRmEventHub обновляет свойства указанного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="d4e10-108">The Set-AzureRmEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="d4e10-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4e10-109">EXAMPLES</span></span>

### <span data-ttu-id="d4e10-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d4e10-110">Example 1</span></span>
<span data-ttu-id="d4e10-111">Чтобы обновить Eventhub с помощью свойств описания захвата, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="d4e10-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
PS C:\> $CreatedEventHub = Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.CaptureDescriptionAttributes
PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="d4e10-112">Обновляет MyEventHubName центра событий \` \` , представленный \` объектом MyCreatedEventHub \` , настроив срок хранения сообщений на 4 дня, число секций для 2 и CaptureDescription свойств.</span><span class="sxs-lookup"><span data-stu-id="d4e10-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="d4e10-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d4e10-113">Example 2</span></span>

```
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="d4e10-114">Обновляет MyEventHubName центра событий \` \` , представленный \` объектом MyCreatedEventHub \` , задавая срок хранения сообщения 4 дня и число секций равным 2.</span><span class="sxs-lookup"><span data-stu-id="d4e10-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="d4e10-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4e10-115">PARAMETERS</span></span>

### <span data-ttu-id="d4e10-116">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d4e10-116">-messageRetentionInDays</span></span>
<span data-ttu-id="d4e10-117">Срок хранения сообщений на концентраторе событий (в днях).</span><span class="sxs-lookup"><span data-stu-id="d4e10-117">Event Hub message retention period, in days.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e10-118">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="d4e10-118">-partitionCount</span></span>
<span data-ttu-id="d4e10-119">Количество разделов на этом концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="d4e10-119">Number of partitions on this Event Hub.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e10-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e10-120">-ResourceGroupName</span></span>
<span data-ttu-id="d4e10-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4e10-121">Resource group name.</span></span>

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

### <span data-ttu-id="d4e10-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4e10-122">-Confirm</span></span>
<span data-ttu-id="d4e10-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d4e10-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4e10-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e10-124">-WhatIf</span></span>
<span data-ttu-id="d4e10-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d4e10-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4e10-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d4e10-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4e10-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4e10-127">-InputObject</span></span>
<span data-ttu-id="d4e10-128">Объект EventHub.</span><span class="sxs-lookup"><span data-stu-id="d4e10-128">EventHub object.</span></span>

```yaml
Type: EventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e10-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d4e10-129">-Name</span></span>
<span data-ttu-id="d4e10-130">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d4e10-130">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e10-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d4e10-131">-Namespace</span></span>
<span data-ttu-id="d4e10-132">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d4e10-132">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="d4e10-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4e10-133">INPUTS</span></span>

### <span data-ttu-id="d4e10-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d4e10-134">System.String</span></span>

## <span data-ttu-id="d4e10-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4e10-135">OUTPUTS</span></span>

### <span data-ttu-id="d4e10-136">Microsoft. Azure. Commands. EventHub. Models. EventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="d4e10-136">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="d4e10-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4e10-137">NOTES</span></span>

## <span data-ttu-id="d4e10-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4e10-138">RELATED LINKS</span></span>

