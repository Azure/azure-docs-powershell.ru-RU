---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
ms.openlocfilehash: 2c5bf49245da7ecac0f9d4351f5a66a39a663b98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567990"
---
# <span data-ttu-id="35921-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="35921-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="35921-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35921-102">SYNOPSIS</span></span>
<span data-ttu-id="35921-103">Создание нового концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="35921-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35921-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35921-104">SYNTAX</span></span>

### <span data-ttu-id="35921-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="35921-105">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35921-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="35921-106">EventhubPropertiesSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35921-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35921-107">DESCRIPTION</span></span>
<span data-ttu-id="35921-108">Командлет New-AzureRmEventHub создает новый центр событий Azure.</span><span class="sxs-lookup"><span data-stu-id="35921-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="35921-109">Чтобы создать Eventhub с помощью свойств описания захвата, сделайте следующее (примеры 2).</span><span class="sxs-lookup"><span data-stu-id="35921-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="35921-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35921-110">EXAMPLES</span></span>

### <span data-ttu-id="35921-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35921-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2
```

<span data-ttu-id="35921-112">Создание концентратора событий с именем \` MyEventHubName \` с помощью 3-дневного срока хранения сообщений и двух секций \` в \` расположении WestUS с группой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="35921-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="35921-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="35921-113">Example 2</span></span>
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

<span data-ttu-id="35921-114">Создание концентратора событий с именем \` MyEventHubName \` с помощью 3-дневного периода хранения сообщений, двух секций и свойств CaptureDescription в \` \` расположении WestUS с группой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="35921-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="35921-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35921-115">PARAMETERS</span></span>

### <span data-ttu-id="35921-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35921-116">-DefaultProfile</span></span>
<span data-ttu-id="35921-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35921-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35921-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35921-118">-InputObject</span></span>
<span data-ttu-id="35921-119">Объект ввода EventHub</span><span class="sxs-lookup"><span data-stu-id="35921-119">EventHub Input object</span></span>

```yaml
Type: PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35921-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="35921-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="35921-121">Хранение сообщений Eventhub в днях</span><span class="sxs-lookup"><span data-stu-id="35921-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="35921-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="35921-122">-Name</span></span>
<span data-ttu-id="35921-123">Имя Eventhub</span><span class="sxs-lookup"><span data-stu-id="35921-123">Eventhub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35921-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="35921-124">-Namespace</span></span>
<span data-ttu-id="35921-125">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="35921-125">Namespace Name</span></span>

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

### <span data-ttu-id="35921-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="35921-126">-PartitionCount</span></span>
<span data-ttu-id="35921-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="35921-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="35921-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35921-128">-ResourceGroupName</span></span>
<span data-ttu-id="35921-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="35921-129">Resource Group Name</span></span>

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

### <span data-ttu-id="35921-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35921-130">-Confirm</span></span>
<span data-ttu-id="35921-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="35921-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35921-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35921-132">-WhatIf</span></span>
<span data-ttu-id="35921-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="35921-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35921-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="35921-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35921-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35921-135">CommonParameters</span></span>
<span data-ttu-id="35921-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35921-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="35921-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35921-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35921-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35921-138">INPUTS</span></span>

### <span data-ttu-id="35921-139">System. String</span><span class="sxs-lookup"><span data-stu-id="35921-139">System.String</span></span>
<span data-ttu-id="35921-140">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes System. Nullable "1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="35921-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="35921-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35921-141">OUTPUTS</span></span>

### <span data-ttu-id="35921-142">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="35921-142">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>


## <span data-ttu-id="35921-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="35921-143">NOTES</span></span>

## <span data-ttu-id="35921-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35921-144">RELATED LINKS</span></span>
