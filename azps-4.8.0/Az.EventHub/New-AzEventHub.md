---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
ms.openlocfilehash: eec7294a15217be85b4c2248dac6506d54c2e6aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244971"
---
# <span data-ttu-id="ca4bd-101">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="ca4bd-101">New-AzEventHub</span></span>

## <span data-ttu-id="ca4bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ca4bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ca4bd-103">Создание нового концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-103">Creates a new Event Hub.</span></span>

## <span data-ttu-id="ca4bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ca4bd-104">SYNTAX</span></span>

### <span data-ttu-id="ca4bd-105">EventhubPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ca4bd-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca4bd-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ca4bd-106">EventhubInputObjectSet</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca4bd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca4bd-107">DESCRIPTION</span></span>
<span data-ttu-id="ca4bd-108">Командлет New-AzEventHub создает новый центр событий Azure.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-108">The New-AzEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="ca4bd-109">Чтобы создать Eventhub с помощью свойств описания захвата, сделайте следующее (примеры 2).</span><span class="sxs-lookup"><span data-stu-id="ca4bd-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="ca4bd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ca4bd-110">EXAMPLES</span></span>

### <span data-ttu-id="ca4bd-111">Пример 1:-создание нового EventHub</span><span class="sxs-lookup"><span data-stu-id="ca4bd-111">Example 1: - Create new EventHub</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="ca4bd-112">Создание концентратора событий с именем \` MyEventHubName \` с помощью 3-дневного срока хранения сообщений и двух секций \` в \` расположении WestUS с группой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ca4bd-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ca4bd-113">Пример 2: обновление Eventhub с помощью "CaptureDescription"</span><span class="sxs-lookup"><span data-stu-id="ca4bd-113">Example 2: Update Eventhub with 'CaptureDescription'</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

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

<span data-ttu-id="ca4bd-114">Создание концентратора событий с именем \` MyEventHubName \` с помощью 3-дневного периода хранения сообщений, двух секций и свойств CaptureDescription в \` \` расположении WestUS с группой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ca4bd-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ca4bd-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ca4bd-115">PARAMETERS</span></span>

### <span data-ttu-id="ca4bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca4bd-116">-DefaultProfile</span></span>
<span data-ttu-id="ca4bd-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca4bd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca4bd-118">-InputObject</span></span>
<span data-ttu-id="ca4bd-119">Объект ввода EventHub</span><span class="sxs-lookup"><span data-stu-id="ca4bd-119">EventHub Input object</span></span>

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

### <span data-ttu-id="ca4bd-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ca4bd-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="ca4bd-121">Хранение сообщений Eventhub в днях</span><span class="sxs-lookup"><span data-stu-id="ca4bd-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="ca4bd-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ca4bd-122">-Name</span></span>
<span data-ttu-id="ca4bd-123">Имя Eventhub</span><span class="sxs-lookup"><span data-stu-id="ca4bd-123">Eventhub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4bd-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ca4bd-124">-Namespace</span></span>
<span data-ttu-id="ca4bd-125">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="ca4bd-125">Namespace Name</span></span>

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

### <span data-ttu-id="ca4bd-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="ca4bd-126">-PartitionCount</span></span>
<span data-ttu-id="ca4bd-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="ca4bd-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="ca4bd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca4bd-128">-ResourceGroupName</span></span>
<span data-ttu-id="ca4bd-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ca4bd-129">Resource Group Name</span></span>

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

### <span data-ttu-id="ca4bd-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca4bd-130">-Confirm</span></span>
<span data-ttu-id="ca4bd-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca4bd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca4bd-132">-WhatIf</span></span>
<span data-ttu-id="ca4bd-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca4bd-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca4bd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca4bd-135">CommonParameters</span></span>
<span data-ttu-id="ca4bd-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca4bd-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca4bd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca4bd-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ca4bd-138">INPUTS</span></span>

### <span data-ttu-id="ca4bd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ca4bd-139">System.String</span></span>

### <span data-ttu-id="ca4bd-140">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="ca4bd-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="ca4bd-141">System. Nullable "1 [[System. Int64, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ca4bd-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ca4bd-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca4bd-142">OUTPUTS</span></span>

### <span data-ttu-id="ca4bd-143">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="ca4bd-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="ca4bd-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="ca4bd-144">NOTES</span></span>

## <span data-ttu-id="ca4bd-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca4bd-145">RELATED LINKS</span></span>