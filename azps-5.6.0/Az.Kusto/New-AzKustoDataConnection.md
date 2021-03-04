---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
ms.openlocfilehash: e9f221563f3d4d689e075f47a281620bc87d9011
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959528"
---
# <span data-ttu-id="e2649-101">New-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="e2649-101">New-AzKustoDataConnection</span></span>

## <span data-ttu-id="e2649-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2649-102">SYNOPSIS</span></span>
<span data-ttu-id="e2649-103">Создание или обновление подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="e2649-103">Creates or updates a data connection.</span></span>

## <span data-ttu-id="e2649-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e2649-104">SYNTAX</span></span>

### <span data-ttu-id="e2649-105">CreateExpandedEventHub (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2649-105">CreateExpandedEventHub (Default)</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e2649-106">CreateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="e2649-106">CreateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e2649-107">CreateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="e2649-107">CreateExpandedIotHub</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e2649-108">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="e2649-108">UpdateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e2649-109">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="e2649-109">UpdateViaIdentityExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e2649-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2649-110">DESCRIPTION</span></span>
<span data-ttu-id="e2649-111">Создание или обновление подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="e2649-111">Creates or updates a data connection.</span></span>

## <span data-ttu-id="e2649-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e2649-112">EXAMPLES</span></span>

### <span data-ttu-id="e2649-113">Пример 1. Создание подключения к данным EventHub</span><span class="sxs-lookup"><span data-stu-id="e2649-113">Example 1: Create a new EventHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "EventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="e2649-114">С этой командой создается новое подключение к данным EventHub с именем "myeventhubdc" для базы данных "mykustodatabase" в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="e2649-114">The above command creates a new EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="e2649-115">Пример 2. Создание подключения к данным EventGrid</span><span class="sxs-lookup"><span data-stu-id="e2649-115">Example 2: Create a new EventGrid data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping" -IgnoreFirstRecord "false" -BlobStorageEventType "Microsoft.Storage.BlobRenamed"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="e2649-116">С этой командой создается новое подключение к данным EventGrid с именем myeventgriddc для базы данных mykustodatabase в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="e2649-116">The above command creates a new EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="e2649-117">Пример 3. Создание подключения к данным IotHub</span><span class="sxs-lookup"><span data-stu-id="e2649-117">Example 3: Create a new IotHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="e2649-118">С этой командой создается новое подключение к данным IotHub с именем myiothubdc для базы данных mykustodatabase в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="e2649-118">The above command creates a new IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="e2649-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2649-119">PARAMETERS</span></span>

### <span data-ttu-id="e2649-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2649-120">-AsJob</span></span>
<span data-ttu-id="e2649-121">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="e2649-121">Run the command as a job</span></span>

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

### <span data-ttu-id="e2649-122">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="e2649-122">-BlobStorageEventType</span></span>
<span data-ttu-id="e2649-123">Имя обработки события типа события хранилища BLOB-типов.</span><span class="sxs-lookup"><span data-stu-id="e2649-123">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="e2649-124">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e2649-124">-ClusterName</span></span>
<span data-ttu-id="e2649-125">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="e2649-125">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e2649-126">-Сжатие</span><span class="sxs-lookup"><span data-stu-id="e2649-126">-Compression</span></span>
<span data-ttu-id="e2649-127">Тип сжатия сообщений в центре событий.</span><span class="sxs-lookup"><span data-stu-id="e2649-127">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="e2649-128">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e2649-128">-ConsumerGroup</span></span>
<span data-ttu-id="e2649-129">Группа потребительских событий/iot-концентратора.</span><span class="sxs-lookup"><span data-stu-id="e2649-129">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="e2649-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e2649-130">-DatabaseName</span></span>
<span data-ttu-id="e2649-131">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="e2649-131">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="e2649-132">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="e2649-132">-DataFormat</span></span>
<span data-ttu-id="e2649-133">Формат данных сообщения.</span><span class="sxs-lookup"><span data-stu-id="e2649-133">The data format of the message.</span></span>
<span data-ttu-id="e2649-134">При желании формат данных можно добавить в каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="e2649-134">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="e2649-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2649-135">-DefaultProfile</span></span>
<span data-ttu-id="e2649-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2649-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2649-137">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="e2649-137">-EventHubResourceId</span></span>
<span data-ttu-id="e2649-138">ИД ресурса в центре событий, который будет использоваться для создания подключения к данным или сетки событий, настроен для отправки событий.</span><span class="sxs-lookup"><span data-stu-id="e2649-138">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="e2649-139">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="e2649-139">-EventSystemProperty</span></span>
<span data-ttu-id="e2649-140">Системные свойства концентратора событий и iot.</span><span class="sxs-lookup"><span data-stu-id="e2649-140">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="e2649-141">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="e2649-141">-IgnoreFirstRecord</span></span>
<span data-ttu-id="e2649-142">Если зафиксировать это, означает, что при чтении следует игнорировать первую запись каждого файла.</span><span class="sxs-lookup"><span data-stu-id="e2649-142">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="e2649-143">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="e2649-143">-IotHubResourceId</span></span>
<span data-ttu-id="e2649-144">ИД ресурса концентратора IOT, который будет использоваться для создания подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="e2649-144">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="e2649-145">-Kind</span><span class="sxs-lookup"><span data-stu-id="e2649-145">-Kind</span></span>
<span data-ttu-id="e2649-146">Тип конечной точки для подключения к данным</span><span class="sxs-lookup"><span data-stu-id="e2649-146">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="e2649-147">-Location</span><span class="sxs-lookup"><span data-stu-id="e2649-147">-Location</span></span>
<span data-ttu-id="e2649-148">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="e2649-148">Resource location.</span></span>

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

### <span data-ttu-id="e2649-149">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="e2649-149">-MappingRuleName</span></span>
<span data-ttu-id="e2649-150">Правило сопоставления, используемее для передачи данных.</span><span class="sxs-lookup"><span data-stu-id="e2649-150">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="e2649-151">При желании сведения о сопоставлении можно добавить в каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="e2649-151">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="e2649-152">-Name</span><span class="sxs-lookup"><span data-stu-id="e2649-152">-Name</span></span>
<span data-ttu-id="e2649-153">Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="e2649-153">The name of the data connection.</span></span>

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

### <span data-ttu-id="e2649-154">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e2649-154">-NoWait</span></span>
<span data-ttu-id="e2649-155">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="e2649-155">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e2649-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2649-156">-ResourceGroupName</span></span>
<span data-ttu-id="e2649-157">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="e2649-157">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e2649-158">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="e2649-158">-SharedAccessPolicyName</span></span>
<span data-ttu-id="e2649-159">Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="e2649-159">The name of the share access policy.</span></span>

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

### <span data-ttu-id="e2649-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="e2649-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="e2649-161">ИД ресурса учетной записи хранения, в которой находятся данные.</span><span class="sxs-lookup"><span data-stu-id="e2649-161">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="e2649-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2649-162">-SubscriptionId</span></span>
<span data-ttu-id="e2649-163">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e2649-163">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e2649-164">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="e2649-164">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e2649-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="e2649-165">-TableName</span></span>
<span data-ttu-id="e2649-166">Таблица, в которой нужно ввести данные.</span><span class="sxs-lookup"><span data-stu-id="e2649-166">The table where the data should be ingested.</span></span>
<span data-ttu-id="e2649-167">При желании в каждое сообщение можно добавить сведения из таблицы.</span><span class="sxs-lookup"><span data-stu-id="e2649-167">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="e2649-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2649-168">-Confirm</span></span>
<span data-ttu-id="e2649-169">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e2649-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2649-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2649-170">-WhatIf</span></span>
<span data-ttu-id="e2649-171">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2649-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2649-172">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e2649-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2649-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2649-173">CommonParameters</span></span>
<span data-ttu-id="e2649-174">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2649-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2649-175">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2649-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2649-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2649-176">INPUTS</span></span>

## <span data-ttu-id="e2649-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e2649-177">OUTPUTS</span></span>

### <span data-ttu-id="e2649-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="e2649-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="e2649-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e2649-179">NOTES</span></span>

<span data-ttu-id="e2649-180">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e2649-180">ALIASES</span></span>

## <span data-ttu-id="e2649-181">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2649-181">RELATED LINKS</span></span>

