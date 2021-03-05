---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/update-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
ms.openlocfilehash: 94a0764b61b32ce55ff4d9aca06a22d67b1edc96
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008984"
---
# <span data-ttu-id="30538-101">Update-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="30538-101">Update-AzKustoDataConnection</span></span>

## <span data-ttu-id="30538-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30538-102">SYNOPSIS</span></span>
<span data-ttu-id="30538-103">Обновляет подключение к данным.</span><span class="sxs-lookup"><span data-stu-id="30538-103">Updates a data connection.</span></span>

## <span data-ttu-id="30538-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="30538-104">SYNTAX</span></span>

### <span data-ttu-id="30538-105">UpdateExpandedEventHub (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="30538-105">UpdateExpandedEventHub (Default)</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="30538-106">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="30538-106">UpdateExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30538-107">UpdateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="30538-107">UpdateExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="30538-108">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="30538-108">UpdateViaIdentityExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> -StorageAccountResourceId <String>
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30538-109">UpdateViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="30538-109">UpdateViaIdentityExpandedEventHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="30538-110">UpdateViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="30538-110">UpdateViaIdentityExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>]
 [-EventSystemProperty <String[]>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="30538-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30538-111">DESCRIPTION</span></span>
<span data-ttu-id="30538-112">Обновляет подключение к данным.</span><span class="sxs-lookup"><span data-stu-id="30538-112">Updates a data connection.</span></span>

## <span data-ttu-id="30538-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="30538-113">EXAMPLES</span></span>

### <span data-ttu-id="30538-114">Пример 1. Обновление существующего подключения к данным EventHub</span><span class="sxs-lookup"><span data-stu-id="30538-114">Example 1: Update an existing EventHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="30538-115">Команда выше обновляет существующее подключение к данным EventHub с именем "myeventhubdc" для базы данных mykustodatabase в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="30538-115">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="30538-116">Пример 2. Обновление существующего подключения к данным EventGrid</span><span class="sxs-lookup"><span data-stu-id="30538-116">Example 2: Update an existing EventGrid data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="30538-117">Команда выше обновляет существующее подключение к данным EventGrid "myeventgriddc" для базы данных mykustodatabase в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="30538-117">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="30538-118">Пример 3. Обновление существующего подключения к данным IotHub</span><span class="sxs-lookup"><span data-stu-id="30538-118">Example 3: Update an existing IotHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="30538-119">С этой командой обновляется существующее подключение к данным IotHub с именем myiothubdc для базы данных mykustodatabase в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="30538-119">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="30538-120">Пример 4. Обновление существующего подключения к данным EventHub с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="30538-120">Example 4: Update an existing EventHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="30538-121">Команда выше обновляет существующее подключение к данным EventHub с именем "myeventhubdc" для базы данных mykustodatabase в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="30538-121">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="30538-122">Пример 5. Обновление существующего подключения к данным EventGrid с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="30538-122">Example 5: Update an existing EventGrid data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="30538-123">Команда выше обновляет существующее подключение к данным EventGrid "myeventgriddc" для базы данных mykustodatabase в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="30538-123">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="30538-124">Пример 6. Обновление существующего подключения к данным IotHub с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="30538-124">Example 6: Update an existing IotHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="30538-125">С этой командой обновляется существующее подключение к данным IotHub с именем myiothubdc для базы данных mykustodatabase в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="30538-125">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="30538-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30538-126">PARAMETERS</span></span>

### <span data-ttu-id="30538-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30538-127">-AsJob</span></span>
<span data-ttu-id="30538-128">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="30538-128">Run the command as a job</span></span>

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

### <span data-ttu-id="30538-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="30538-129">-BlobStorageEventType</span></span>
<span data-ttu-id="30538-130">Имя обработки события типа события хранилища BLOB-типов.</span><span class="sxs-lookup"><span data-stu-id="30538-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="30538-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="30538-131">-ClusterName</span></span>
<span data-ttu-id="30538-132">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="30538-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30538-133">-Сжатие</span><span class="sxs-lookup"><span data-stu-id="30538-133">-Compression</span></span>
<span data-ttu-id="30538-134">Центр событий сообщает о сжатии.</span><span class="sxs-lookup"><span data-stu-id="30538-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: UpdateExpandedEventHub, UpdateViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30538-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="30538-135">-ConsumerGroup</span></span>
<span data-ttu-id="30538-136">Группа потребительских событий/iot-концентратора.</span><span class="sxs-lookup"><span data-stu-id="30538-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="30538-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="30538-137">-DatabaseName</span></span>
<span data-ttu-id="30538-138">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="30538-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30538-139">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="30538-139">-DataFormat</span></span>
<span data-ttu-id="30538-140">Формат данных сообщения.</span><span class="sxs-lookup"><span data-stu-id="30538-140">The data format of the message.</span></span>
<span data-ttu-id="30538-141">При желании формат данных можно добавить в каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="30538-141">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="30538-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30538-142">-DefaultProfile</span></span>
<span data-ttu-id="30538-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30538-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30538-144">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="30538-144">-EventHubResourceId</span></span>
<span data-ttu-id="30538-145">ИД ресурса в центре событий, который используется для создания подключения к данным или сетки событий, настроен для отправки событий.</span><span class="sxs-lookup"><span data-stu-id="30538-145">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30538-146">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="30538-146">-EventSystemProperty</span></span>
<span data-ttu-id="30538-147">Системные свойства концентратора событий и iot.</span><span class="sxs-lookup"><span data-stu-id="30538-147">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpandedEventHub, UpdateExpandedIotHub, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30538-148">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="30538-148">-IgnoreFirstRecord</span></span>
<span data-ttu-id="30538-149">Если зафиксировать это, означает, что при чтении следует игнорировать первую запись каждого файла.</span><span class="sxs-lookup"><span data-stu-id="30538-149">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="30538-150">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30538-150">-InputObject</span></span>
<span data-ttu-id="30538-151">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="30538-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30538-152">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="30538-152">-IotHubResourceId</span></span>
<span data-ttu-id="30538-153">ИД ресурса концентратора IOT, который будет использоваться для создания подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="30538-153">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30538-154">-Kind</span><span class="sxs-lookup"><span data-stu-id="30538-154">-Kind</span></span>
<span data-ttu-id="30538-155">Тип конечной точки для подключения к данным</span><span class="sxs-lookup"><span data-stu-id="30538-155">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="30538-156">-Location</span><span class="sxs-lookup"><span data-stu-id="30538-156">-Location</span></span>
<span data-ttu-id="30538-157">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="30538-157">Resource location.</span></span>

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

### <span data-ttu-id="30538-158">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="30538-158">-MappingRuleName</span></span>
<span data-ttu-id="30538-159">Правило сопоставления, используемее для передачи данных.</span><span class="sxs-lookup"><span data-stu-id="30538-159">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="30538-160">При желании сведения о сопоставлении можно добавить в каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="30538-160">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="30538-161">-Name</span><span class="sxs-lookup"><span data-stu-id="30538-161">-Name</span></span>
<span data-ttu-id="30538-162">Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="30538-162">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30538-163">-NoWait</span><span class="sxs-lookup"><span data-stu-id="30538-163">-NoWait</span></span>
<span data-ttu-id="30538-164">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="30538-164">Run the command asynchronously</span></span>

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

### <span data-ttu-id="30538-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30538-165">-ResourceGroupName</span></span>
<span data-ttu-id="30538-166">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="30538-166">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30538-167">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="30538-167">-SharedAccessPolicyName</span></span>
<span data-ttu-id="30538-168">Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="30538-168">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30538-169">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="30538-169">-StorageAccountResourceId</span></span>
<span data-ttu-id="30538-170">ИД ресурса учетной записи хранения, в которой находятся данные.</span><span class="sxs-lookup"><span data-stu-id="30538-170">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30538-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30538-171">-SubscriptionId</span></span>
<span data-ttu-id="30538-172">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="30538-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="30538-173">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="30538-173">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30538-174">-TableName</span><span class="sxs-lookup"><span data-stu-id="30538-174">-TableName</span></span>
<span data-ttu-id="30538-175">Таблица, в которой нужно ввести данные.</span><span class="sxs-lookup"><span data-stu-id="30538-175">The table where the data should be ingested.</span></span>
<span data-ttu-id="30538-176">При желании в каждое сообщение можно добавить сведения из таблицы.</span><span class="sxs-lookup"><span data-stu-id="30538-176">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="30538-177">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30538-177">-Confirm</span></span>
<span data-ttu-id="30538-178">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30538-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30538-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30538-179">-WhatIf</span></span>
<span data-ttu-id="30538-180">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30538-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30538-181">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="30538-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30538-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30538-182">CommonParameters</span></span>
<span data-ttu-id="30538-183">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30538-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30538-184">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30538-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30538-185">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30538-185">INPUTS</span></span>

### <span data-ttu-id="30538-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="30538-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="30538-187">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="30538-187">OUTPUTS</span></span>

### <span data-ttu-id="30538-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="30538-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="30538-189">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="30538-189">NOTES</span></span>

<span data-ttu-id="30538-190">ALIASES</span><span class="sxs-lookup"><span data-stu-id="30538-190">ALIASES</span></span>

<span data-ttu-id="30538-191">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="30538-191">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="30538-192">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="30538-192">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="30538-193">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="30538-193">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="30538-194">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="30538-194">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="30538-195">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="30538-195">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="30538-196">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="30538-196">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="30538-197">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="30538-197">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="30538-198">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="30538-198">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="30538-199">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="30538-199">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="30538-200">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="30538-200">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="30538-201">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="30538-201">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="30538-202">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="30538-202">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="30538-203">`[SubscriptionId <String>]`: получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="30538-203">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="30538-204">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="30538-204">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="30538-205">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30538-205">RELATED LINKS</span></span>

