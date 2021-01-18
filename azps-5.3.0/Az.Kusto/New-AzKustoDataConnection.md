---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
ms.openlocfilehash: ab58d679e9fc3ad62baeded8622b81a0cb8b2f95
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507162"
---
# <span data-ttu-id="490b1-101">New-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="490b1-101">New-AzKustoDataConnection</span></span>

## <span data-ttu-id="490b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="490b1-102">SYNOPSIS</span></span>
<span data-ttu-id="490b1-103">Создание или обновление подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="490b1-103">Creates or updates a data connection.</span></span>

## <span data-ttu-id="490b1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="490b1-104">SYNTAX</span></span>

### <span data-ttu-id="490b1-105">CreateExpandedEventHub (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="490b1-105">CreateExpandedEventHub (Default)</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="490b1-106">CreateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="490b1-106">CreateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="490b1-107">CreateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="490b1-107">CreateExpandedIotHub</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="490b1-108">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="490b1-108">UpdateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="490b1-109">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="490b1-109">UpdateViaIdentityExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="490b1-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="490b1-110">DESCRIPTION</span></span>
<span data-ttu-id="490b1-111">Создание или обновление подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="490b1-111">Creates or updates a data connection.</span></span>

## <span data-ttu-id="490b1-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="490b1-112">EXAMPLES</span></span>

### <span data-ttu-id="490b1-113">Пример 1. Создание подключения к данным EventHub</span><span class="sxs-lookup"><span data-stu-id="490b1-113">Example 1: Create a new EventHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "EventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="490b1-114">С этой командой создается новое подключение к данным EventHub с именем "myeventhubdc" для базы данных "mykustodatabase" в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="490b1-114">The above command creates a new EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="490b1-115">Пример 2. Создание подключения к данным EventGrid</span><span class="sxs-lookup"><span data-stu-id="490b1-115">Example 2: Create a new EventGrid data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping" -IgnoreFirstRecord "false" -BlobStorageEventType "Microsoft.Storage.BlobRenamed"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="490b1-116">С этой командой создается новое подключение к данным EventGrid с именем myeventgriddc для базы данных mykustodatabase в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="490b1-116">The above command creates a new EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="490b1-117">Пример 3. Создание подключения к данным IotHub</span><span class="sxs-lookup"><span data-stu-id="490b1-117">Example 3: Create a new IotHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="490b1-118">С этой командой создается новое подключение к данным IotHub с именем myiothubdc для базы данных mykustodatabase в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="490b1-118">The above command creates a new IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="490b1-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="490b1-119">PARAMETERS</span></span>

### <span data-ttu-id="490b1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="490b1-120">-AsJob</span></span>
<span data-ttu-id="490b1-121">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="490b1-121">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-122">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="490b1-122">-BlobStorageEventType</span></span>
<span data-ttu-id="490b1-123">Имя обработки события типа события хранилища BLOB-типов.</span><span class="sxs-lookup"><span data-stu-id="490b1-123">The name of blob storage event type to process.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.BlobStorageEventType
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-124">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="490b1-124">-ClusterName</span></span>
<span data-ttu-id="490b1-125">Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="490b1-125">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-126">-Сжатие</span><span class="sxs-lookup"><span data-stu-id="490b1-126">-Compression</span></span>
<span data-ttu-id="490b1-127">Центр событий сообщает о сжатии.</span><span class="sxs-lookup"><span data-stu-id="490b1-127">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: CreateExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-128">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="490b1-128">-ConsumerGroup</span></span>
<span data-ttu-id="490b1-129">Группа потребительских событий/iot-концентратора.</span><span class="sxs-lookup"><span data-stu-id="490b1-129">The event/iot hub consumer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="490b1-130">-DatabaseName</span></span>
<span data-ttu-id="490b1-131">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="490b1-131">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-132">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="490b1-132">-DataFormat</span></span>
<span data-ttu-id="490b1-133">Формат данных сообщения.</span><span class="sxs-lookup"><span data-stu-id="490b1-133">The data format of the message.</span></span>
<span data-ttu-id="490b1-134">При желании формат данных можно добавить в каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="490b1-134">Optionally the data format can be added to each message.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EventGridDataFormat
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="490b1-135">-DefaultProfile</span></span>
<span data-ttu-id="490b1-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="490b1-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-137">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="490b1-137">-EventHubResourceId</span></span>
<span data-ttu-id="490b1-138">ИД ресурса в центре событий, который будет использоваться для создания подключения к данным или сетки событий, настроен для отправки событий.</span><span class="sxs-lookup"><span data-stu-id="490b1-138">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid, CreateExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-139">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="490b1-139">-EventSystemProperty</span></span>
<span data-ttu-id="490b1-140">Системные свойства концентратора событий и iot.</span><span class="sxs-lookup"><span data-stu-id="490b1-140">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpandedEventHub, CreateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-141">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="490b1-141">-IgnoreFirstRecord</span></span>
<span data-ttu-id="490b1-142">Если установлено истинное, означает, что при чтении следует игнорировать первую запись каждого файла.</span><span class="sxs-lookup"><span data-stu-id="490b1-142">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-143">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="490b1-143">-IotHubResourceId</span></span>
<span data-ttu-id="490b1-144">ИД ресурса концентратора IOT, который будет использоваться для создания подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="490b1-144">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-145">-Kind</span><span class="sxs-lookup"><span data-stu-id="490b1-145">-Kind</span></span>
<span data-ttu-id="490b1-146">Тип конечной точки для подключения к данным</span><span class="sxs-lookup"><span data-stu-id="490b1-146">Kind of the endpoint for the data connection</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-147">-Location</span><span class="sxs-lookup"><span data-stu-id="490b1-147">-Location</span></span>
<span data-ttu-id="490b1-148">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="490b1-148">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-149">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="490b1-149">-MappingRuleName</span></span>
<span data-ttu-id="490b1-150">Правило сопоставления, используемее для передачи данных.</span><span class="sxs-lookup"><span data-stu-id="490b1-150">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="490b1-151">При желании сведения о сопоставлении можно добавить в каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="490b1-151">Optionally the mapping information can be added to each message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-152">-Name</span><span class="sxs-lookup"><span data-stu-id="490b1-152">-Name</span></span>
<span data-ttu-id="490b1-153">Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="490b1-153">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-154">-NoWait</span><span class="sxs-lookup"><span data-stu-id="490b1-154">-NoWait</span></span>
<span data-ttu-id="490b1-155">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="490b1-155">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="490b1-156">-ResourceGroupName</span></span>
<span data-ttu-id="490b1-157">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="490b1-157">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-158">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="490b1-158">-SharedAccessPolicyName</span></span>
<span data-ttu-id="490b1-159">Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="490b1-159">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="490b1-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="490b1-161">ИД ресурса учетной записи хранения, в которой находятся данные.</span><span class="sxs-lookup"><span data-stu-id="490b1-161">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="490b1-162">-SubscriptionId</span></span>
<span data-ttu-id="490b1-163">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="490b1-163">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="490b1-164">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="490b1-164">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="490b1-165">-TableName</span></span>
<span data-ttu-id="490b1-166">Таблица, в которой нужно ввести данные.</span><span class="sxs-lookup"><span data-stu-id="490b1-166">The table where the data should be ingested.</span></span>
<span data-ttu-id="490b1-167">При желании в каждое сообщение можно добавить сведения из таблицы.</span><span class="sxs-lookup"><span data-stu-id="490b1-167">Optionally the table information can be added to each message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490b1-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="490b1-168">-Confirm</span></span>
<span data-ttu-id="490b1-169">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="490b1-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="490b1-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="490b1-170">-WhatIf</span></span>
<span data-ttu-id="490b1-171">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="490b1-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="490b1-172">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="490b1-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="490b1-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="490b1-173">CommonParameters</span></span>
<span data-ttu-id="490b1-174">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="490b1-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="490b1-175">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="490b1-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="490b1-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="490b1-176">INPUTS</span></span>

## <span data-ttu-id="490b1-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="490b1-177">OUTPUTS</span></span>

### <span data-ttu-id="490b1-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="490b1-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="490b1-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="490b1-179">NOTES</span></span>

<span data-ttu-id="490b1-180">ALIASES</span><span class="sxs-lookup"><span data-stu-id="490b1-180">ALIASES</span></span>

## <span data-ttu-id="490b1-181">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="490b1-181">RELATED LINKS</span></span>

