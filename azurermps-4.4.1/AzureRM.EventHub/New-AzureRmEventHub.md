---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 656e010a05ce1272355f689be8513ecadd330e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569483"
---
# <span data-ttu-id="97ba6-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="97ba6-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="97ba6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97ba6-102">SYNOPSIS</span></span>
<span data-ttu-id="97ba6-103">Создание нового концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="97ba6-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97ba6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97ba6-104">SYNTAX</span></span>

### <span data-ttu-id="97ba6-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="97ba6-105">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="97ba6-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="97ba6-106">EventhubPropertiesSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="97ba6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97ba6-107">DESCRIPTION</span></span>
<span data-ttu-id="97ba6-108">Командлет New-AzureRmEventHub создает новый центр событий Azure.</span><span class="sxs-lookup"><span data-stu-id="97ba6-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="97ba6-109">Чтобы создать Eventhub с помощью свойств описания захвата, сделайте следующее (примеры 2).</span><span class="sxs-lookup"><span data-stu-id="97ba6-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 


## <span data-ttu-id="97ba6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97ba6-110">EXAMPLES</span></span>

### <span data-ttu-id="97ba6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="97ba6-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2
```

<span data-ttu-id="97ba6-112">Создание концентратора событий с именем \` MyEventHubName \` с помощью 3-дневного срока хранения сообщений и двух секций \` в \` расположении WestUS с группой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="97ba6-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="97ba6-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="97ba6-113">Example 2</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

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

<span data-ttu-id="97ba6-114">Создание концентратора событий с именем \` MyEventHubName \` с помощью 3-дневного периода хранения сообщений, двух секций и свойств CaptureDescription в \` \` расположении WestUS с группой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="97ba6-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="97ba6-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97ba6-115">PARAMETERS</span></span>

### <span data-ttu-id="97ba6-116">-Location</span><span class="sxs-lookup"><span data-stu-id="97ba6-116">-Location</span></span>
<span data-ttu-id="97ba6-117">Пространство имен в географическом расположении.</span><span class="sxs-lookup"><span data-stu-id="97ba6-117">Namespace geographic location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97ba6-118">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="97ba6-118">-MessageRetentionInDays</span></span>
<span data-ttu-id="97ba6-119">Время хранения сообщений в концентраторах событий в днях.</span><span class="sxs-lookup"><span data-stu-id="97ba6-119">Event Hubs message retention time in days.</span></span>

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

### <span data-ttu-id="97ba6-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="97ba6-120">-PartitionCount</span></span>
<span data-ttu-id="97ba6-121">Количество секций в концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="97ba6-121">Number of partitions in the Event Hub.</span></span>

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

### <span data-ttu-id="97ba6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97ba6-122">-ResourceGroupName</span></span>
<span data-ttu-id="97ba6-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97ba6-123">Resource group name.</span></span>

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

### <span data-ttu-id="97ba6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97ba6-124">-Confirm</span></span>
<span data-ttu-id="97ba6-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="97ba6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97ba6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97ba6-126">-WhatIf</span></span>
<span data-ttu-id="97ba6-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="97ba6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97ba6-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="97ba6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97ba6-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97ba6-129">-InputObject</span></span>
<span data-ttu-id="97ba6-130">Объект ввода EventHub.</span><span class="sxs-lookup"><span data-stu-id="97ba6-130">EventHub Input object.</span></span>

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

### <span data-ttu-id="97ba6-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="97ba6-131">-Name</span></span>
<span data-ttu-id="97ba6-132">Имя Eventhub.</span><span class="sxs-lookup"><span data-stu-id="97ba6-132">Eventhub Name.</span></span>

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

### <span data-ttu-id="97ba6-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="97ba6-133">-Namespace</span></span>
<span data-ttu-id="97ba6-134">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="97ba6-134">Namespace Name.</span></span>

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

## <span data-ttu-id="97ba6-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97ba6-135">INPUTS</span></span>

### <span data-ttu-id="97ba6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="97ba6-136">System.String</span></span>

## <span data-ttu-id="97ba6-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97ba6-137">OUTPUTS</span></span>

### <span data-ttu-id="97ba6-138">Microsoft. Azure. Commands. EventHub. Models. EventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="97ba6-138">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="97ba6-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="97ba6-139">NOTES</span></span>

## <span data-ttu-id="97ba6-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97ba6-140">RELATED LINKS</span></span>

