---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: a5a1f0bbe0f353014047e795c467a645e244f125
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426156"
---
# <span data-ttu-id="75008-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="75008-101">Set-AzEventHub</span></span>

## <span data-ttu-id="75008-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75008-102">SYNOPSIS</span></span>
<span data-ttu-id="75008-103">Обновляет указанный Центр событий.</span><span class="sxs-lookup"><span data-stu-id="75008-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="75008-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="75008-104">SYNTAX</span></span>

### <span data-ttu-id="75008-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="75008-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75008-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="75008-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75008-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75008-107">DESCRIPTION</span></span>
<span data-ttu-id="75008-108">Этот Set-AzEventHub обновляет свойства указанного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="75008-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="75008-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="75008-109">EXAMPLES</span></span>

### <span data-ttu-id="75008-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75008-110">Example 1</span></span>
<span data-ttu-id="75008-111">Чтобы обновить свойства описания Eventhub, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="75008-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

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

<span data-ttu-id="75008-112">Обновляет центр событий \` MyEventHubName, представленный объектом \` MyCreatedEventHub, устанавливая период хранения сообщения на 4 дня, количество разделов до 2 и свойства \` \` CaptureDescription.</span><span class="sxs-lookup"><span data-stu-id="75008-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="75008-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="75008-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="75008-114">Обновляет центр событий \` MyEventHubName, представленный объектом \` \` MyCreatedEventHub, устанавливая для периода хранения сообщений 4 дня и количество разделов \` — 2.</span><span class="sxs-lookup"><span data-stu-id="75008-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="75008-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75008-115">PARAMETERS</span></span>

### <span data-ttu-id="75008-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75008-116">-DefaultProfile</span></span>
<span data-ttu-id="75008-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75008-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75008-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75008-118">-InputObject</span></span>
<span data-ttu-id="75008-119">Объект EventHub</span><span class="sxs-lookup"><span data-stu-id="75008-119">EventHub object</span></span>

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

### <span data-ttu-id="75008-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="75008-120">-messageRetentionInDays</span></span>
<span data-ttu-id="75008-121">Хранение сообщений в Eventhub в днях</span><span class="sxs-lookup"><span data-stu-id="75008-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="75008-122">-Name</span><span class="sxs-lookup"><span data-stu-id="75008-122">-Name</span></span>
<span data-ttu-id="75008-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="75008-123">Namespace Name</span></span>

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

### <span data-ttu-id="75008-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="75008-124">-Namespace</span></span>
<span data-ttu-id="75008-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="75008-125">Namespace Name</span></span>

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

### <span data-ttu-id="75008-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="75008-126">-partitionCount</span></span>
<span data-ttu-id="75008-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="75008-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="75008-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75008-128">-ResourceGroupName</span></span>
<span data-ttu-id="75008-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="75008-129">Resource Group Name</span></span>

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

### <span data-ttu-id="75008-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75008-130">-Confirm</span></span>
<span data-ttu-id="75008-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="75008-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75008-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75008-132">-WhatIf</span></span>
<span data-ttu-id="75008-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75008-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75008-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="75008-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75008-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75008-135">CommonParameters</span></span>
<span data-ttu-id="75008-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75008-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75008-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75008-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75008-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75008-138">INPUTS</span></span>

### <span data-ttu-id="75008-139">System.String</span><span class="sxs-lookup"><span data-stu-id="75008-139">System.String</span></span>

### <span data-ttu-id="75008-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="75008-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="75008-141">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="75008-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="75008-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75008-142">OUTPUTS</span></span>

### <span data-ttu-id="75008-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="75008-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="75008-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="75008-144">NOTES</span></span>

## <span data-ttu-id="75008-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75008-145">RELATED LINKS</span></span>
