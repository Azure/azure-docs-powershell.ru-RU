---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: a5a1f0bbe0f353014047e795c467a645e244f125
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245459"
---
# <span data-ttu-id="11ccc-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="11ccc-101">Set-AzEventHub</span></span>

## <span data-ttu-id="11ccc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11ccc-102">SYNOPSIS</span></span>
<span data-ttu-id="11ccc-103">Обновляет указанный центр событий.</span><span class="sxs-lookup"><span data-stu-id="11ccc-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="11ccc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11ccc-104">SYNTAX</span></span>

### <span data-ttu-id="11ccc-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="11ccc-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11ccc-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="11ccc-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11ccc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11ccc-107">DESCRIPTION</span></span>
<span data-ttu-id="11ccc-108">Командлет Set-AzEventHub обновляет свойства указанного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="11ccc-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="11ccc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11ccc-109">EXAMPLES</span></span>

### <span data-ttu-id="11ccc-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="11ccc-110">Example 1</span></span>
<span data-ttu-id="11ccc-111">Чтобы обновить Eventhub с помощью свойств описания захвата, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="11ccc-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
PS C:\> $CreatedEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes
PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="11ccc-112">Обновляет MyEventHubName центра событий \` \` , представленный \` объектом MyCreatedEventHub \` , настроив срок хранения сообщений на 4 дня, число секций для 2 и CaptureDescription свойств.</span><span class="sxs-lookup"><span data-stu-id="11ccc-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="11ccc-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="11ccc-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="11ccc-114">Обновляет MyEventHubName центра событий \` \` , представленный \` объектом MyCreatedEventHub \` , задавая срок хранения сообщения 4 дня и число секций равным 2.</span><span class="sxs-lookup"><span data-stu-id="11ccc-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="11ccc-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11ccc-115">PARAMETERS</span></span>

### <span data-ttu-id="11ccc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ccc-116">-DefaultProfile</span></span>
<span data-ttu-id="11ccc-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11ccc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11ccc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11ccc-118">-InputObject</span></span>
<span data-ttu-id="11ccc-119">Объект EventHub</span><span class="sxs-lookup"><span data-stu-id="11ccc-119">EventHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ccc-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="11ccc-120">-messageRetentionInDays</span></span>
<span data-ttu-id="11ccc-121">Хранение сообщений Eventhub в днях</span><span class="sxs-lookup"><span data-stu-id="11ccc-121">Eventhub Message Retention In Days</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ccc-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="11ccc-122">-Name</span></span>
<span data-ttu-id="11ccc-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="11ccc-123">Namespace Name</span></span>

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

### <span data-ttu-id="11ccc-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="11ccc-124">-Namespace</span></span>
<span data-ttu-id="11ccc-125">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="11ccc-125">Namespace Name</span></span>

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

### <span data-ttu-id="11ccc-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="11ccc-126">-partitionCount</span></span>
<span data-ttu-id="11ccc-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="11ccc-127">Eventhub PartitionCount</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ccc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11ccc-128">-ResourceGroupName</span></span>
<span data-ttu-id="11ccc-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="11ccc-129">Resource Group Name</span></span>

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

### <span data-ttu-id="11ccc-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11ccc-130">-Confirm</span></span>
<span data-ttu-id="11ccc-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="11ccc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11ccc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11ccc-132">-WhatIf</span></span>
<span data-ttu-id="11ccc-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="11ccc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11ccc-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="11ccc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11ccc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ccc-135">CommonParameters</span></span>
<span data-ttu-id="11ccc-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11ccc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ccc-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11ccc-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ccc-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11ccc-138">INPUTS</span></span>

### <span data-ttu-id="11ccc-139">System. String</span><span class="sxs-lookup"><span data-stu-id="11ccc-139">System.String</span></span>

### <span data-ttu-id="11ccc-140">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="11ccc-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="11ccc-141">System. Nullable "1 [[System. Int64, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="11ccc-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="11ccc-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11ccc-142">OUTPUTS</span></span>

### <span data-ttu-id="11ccc-143">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="11ccc-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="11ccc-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="11ccc-144">NOTES</span></span>

## <span data-ttu-id="11ccc-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11ccc-145">RELATED LINKS</span></span>