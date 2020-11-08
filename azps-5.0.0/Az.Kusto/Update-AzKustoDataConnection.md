---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
ms.openlocfilehash: 70862dee30fd03430d93de88e1e63f0f5acf5e6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247716"
---
# <span data-ttu-id="4da1f-101">Update-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="4da1f-101">Update-AzKustoDataConnection</span></span>

## <span data-ttu-id="4da1f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4da1f-102">SYNOPSIS</span></span>
<span data-ttu-id="4da1f-103">Обновляет подключение к данным.</span><span class="sxs-lookup"><span data-stu-id="4da1f-103">Updates a data connection.</span></span>

## <span data-ttu-id="4da1f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4da1f-104">SYNTAX</span></span>

### <span data-ttu-id="4da1f-105">UpdateExpandedEventHub (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4da1f-105">UpdateExpandedEventHub (Default)</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4da1f-106">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="4da1f-106">UpdateExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4da1f-107">UpdateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="4da1f-107">UpdateExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4da1f-108">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="4da1f-108">UpdateViaIdentityExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> -StorageAccountResourceId <String>
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4da1f-109">UpdateViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="4da1f-109">UpdateViaIdentityExpandedEventHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4da1f-110">UpdateViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="4da1f-110">UpdateViaIdentityExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>]
 [-EventSystemProperty <String[]>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4da1f-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4da1f-111">DESCRIPTION</span></span>
<span data-ttu-id="4da1f-112">Обновляет подключение к данным.</span><span class="sxs-lookup"><span data-stu-id="4da1f-112">Updates a data connection.</span></span>

## <span data-ttu-id="4da1f-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4da1f-113">EXAMPLES</span></span>

### <span data-ttu-id="4da1f-114">Пример 1: обновление существующего подключения к данным EventHub</span><span class="sxs-lookup"><span data-stu-id="4da1f-114">Example 1: Update an existing EventHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="4da1f-115">Эта команда обновляет существующее подключение к данным EventHub с именем "myeventhubdc" для базы данных "mykustodatabase" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="4da1f-115">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="4da1f-116">Пример 2: обновление существующего подключения к данным EventGrid</span><span class="sxs-lookup"><span data-stu-id="4da1f-116">Example 2: Update an existing EventGrid data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="4da1f-117">Приведенная выше команда обновляет существующее подключение к данным EventGrid с именем "myeventgriddc" для базы данных "mykustodatabase" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="4da1f-117">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="4da1f-118">Пример 3: обновление существующего подключения к данным IotHub</span><span class="sxs-lookup"><span data-stu-id="4da1f-118">Example 3: Update an existing IotHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="4da1f-119">Приведенная выше команда обновляет существующее подключение к данным IotHub с именем "myiothubdc" для базы данных "mykustodatabase" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="4da1f-119">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="4da1f-120">Пример 4: обновление существующего подключения к данным EventHub с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="4da1f-120">Example 4: Update an existing EventHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="4da1f-121">Эта команда обновляет существующее подключение к данным EventHub с именем "myeventhubdc" для базы данных "mykustodatabase" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="4da1f-121">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="4da1f-122">Пример 5: обновление существующего подключения к данным EventGrid с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="4da1f-122">Example 5: Update an existing EventGrid data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="4da1f-123">Приведенная выше команда обновляет существующее подключение к данным EventGrid с именем "myeventgriddc" для базы данных "mykustodatabase" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="4da1f-123">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="4da1f-124">Пример 6: обновление существующего подключения к данным IotHub с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="4da1f-124">Example 6: Update an existing IotHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="4da1f-125">Приведенная выше команда обновляет существующее подключение к данным IotHub с именем "myiothubdc" для базы данных "mykustodatabase" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="4da1f-125">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="4da1f-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4da1f-126">PARAMETERS</span></span>

### <span data-ttu-id="4da1f-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4da1f-127">-AsJob</span></span>
<span data-ttu-id="4da1f-128">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="4da1f-128">Run the command as a job</span></span>

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

### <span data-ttu-id="4da1f-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="4da1f-129">-BlobStorageEventType</span></span>
<span data-ttu-id="4da1f-130">Имя типа события хранилища BLOB для обработки.</span><span class="sxs-lookup"><span data-stu-id="4da1f-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="4da1f-131">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="4da1f-131">-ClusterName</span></span>
<span data-ttu-id="4da1f-132">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="4da1f-132">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="4da1f-133">-Сжатие</span><span class="sxs-lookup"><span data-stu-id="4da1f-133">-Compression</span></span>
<span data-ttu-id="4da1f-134">Тип сжатия сообщений центра событий.</span><span class="sxs-lookup"><span data-stu-id="4da1f-134">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="4da1f-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="4da1f-135">-ConsumerGroup</span></span>
<span data-ttu-id="4da1f-136">Группа потребителей "событие/IOT центр Интернета".</span><span class="sxs-lookup"><span data-stu-id="4da1f-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="4da1f-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4da1f-137">-DatabaseName</span></span>
<span data-ttu-id="4da1f-138">Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="4da1f-138">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="4da1f-139">-Формат.</span><span class="sxs-lookup"><span data-stu-id="4da1f-139">-DataFormat</span></span>
<span data-ttu-id="4da1f-140">Формат данных сообщения.</span><span class="sxs-lookup"><span data-stu-id="4da1f-140">The data format of the message.</span></span>
<span data-ttu-id="4da1f-141">При необходимости можно добавить в каждое сообщение формат данных.</span><span class="sxs-lookup"><span data-stu-id="4da1f-141">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="4da1f-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da1f-142">-DefaultProfile</span></span>
<span data-ttu-id="4da1f-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4da1f-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4da1f-144">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="4da1f-144">-EventHubResourceId</span></span>
<span data-ttu-id="4da1f-145">Идентификатор ресурса для концентратора событий, который будет использоваться для создания подключения к данным или сетки событий, настроен для отправки событий.</span><span class="sxs-lookup"><span data-stu-id="4da1f-145">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="4da1f-146">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="4da1f-146">-EventSystemProperty</span></span>
<span data-ttu-id="4da1f-147">Свойства системы для центра событий и Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="4da1f-147">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="4da1f-148">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="4da1f-148">-IgnoreFirstRecord</span></span>
<span data-ttu-id="4da1f-149">Если установлено значение true, это означает, что при приеме будет игнорироваться первая запись каждого файла.</span><span class="sxs-lookup"><span data-stu-id="4da1f-149">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="4da1f-150">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4da1f-150">-InputObject</span></span>
<span data-ttu-id="4da1f-151">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="4da1f-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4da1f-152">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="4da1f-152">-IotHubResourceId</span></span>
<span data-ttu-id="4da1f-153">Идентификатор ресурса центра Интернета вещей, который будет использоваться для создания подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="4da1f-153">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="4da1f-154">-Видах</span><span class="sxs-lookup"><span data-stu-id="4da1f-154">-Kind</span></span>
<span data-ttu-id="4da1f-155">Вариант конечной точки подключения к данным</span><span class="sxs-lookup"><span data-stu-id="4da1f-155">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="4da1f-156">-Location</span><span class="sxs-lookup"><span data-stu-id="4da1f-156">-Location</span></span>
<span data-ttu-id="4da1f-157">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="4da1f-157">Resource location.</span></span>

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

### <span data-ttu-id="4da1f-158">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="4da1f-158">-MappingRuleName</span></span>
<span data-ttu-id="4da1f-159">Правило сопоставления, которое будет использоваться для приема данных.</span><span class="sxs-lookup"><span data-stu-id="4da1f-159">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="4da1f-160">Кроме того, можно добавить сведения о сопоставлении в каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="4da1f-160">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="4da1f-161">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4da1f-161">-Name</span></span>
<span data-ttu-id="4da1f-162">Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="4da1f-162">The name of the data connection.</span></span>

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

### <span data-ttu-id="4da1f-163">-Wait</span><span class="sxs-lookup"><span data-stu-id="4da1f-163">-NoWait</span></span>
<span data-ttu-id="4da1f-164">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="4da1f-164">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4da1f-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4da1f-165">-ResourceGroupName</span></span>
<span data-ttu-id="4da1f-166">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="4da1f-166">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="4da1f-167">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="4da1f-167">-SharedAccessPolicyName</span></span>
<span data-ttu-id="4da1f-168">Имя политики общего доступа.</span><span class="sxs-lookup"><span data-stu-id="4da1f-168">The name of the share access policy.</span></span>

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

### <span data-ttu-id="4da1f-169">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="4da1f-169">-StorageAccountResourceId</span></span>
<span data-ttu-id="4da1f-170">Идентификатор ресурса учетной записи хранения, в которой хранятся данные.</span><span class="sxs-lookup"><span data-stu-id="4da1f-170">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="4da1f-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4da1f-171">-SubscriptionId</span></span>
<span data-ttu-id="4da1f-172">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4da1f-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4da1f-173">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="4da1f-173">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4da1f-174">-TableName</span><span class="sxs-lookup"><span data-stu-id="4da1f-174">-TableName</span></span>
<span data-ttu-id="4da1f-175">Таблица, в которой должны быть выдаваться данные.</span><span class="sxs-lookup"><span data-stu-id="4da1f-175">The table where the data should be ingested.</span></span>
<span data-ttu-id="4da1f-176">При необходимости в каждое сообщение можно добавить сведения о таблице.</span><span class="sxs-lookup"><span data-stu-id="4da1f-176">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="4da1f-177">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4da1f-177">-Confirm</span></span>
<span data-ttu-id="4da1f-178">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4da1f-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4da1f-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4da1f-179">-WhatIf</span></span>
<span data-ttu-id="4da1f-180">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4da1f-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4da1f-181">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4da1f-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4da1f-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da1f-182">CommonParameters</span></span>
<span data-ttu-id="4da1f-183">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4da1f-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da1f-184">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4da1f-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da1f-185">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4da1f-185">INPUTS</span></span>

### <span data-ttu-id="4da1f-186">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="4da1f-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="4da1f-187">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4da1f-187">OUTPUTS</span></span>

### <span data-ttu-id="4da1f-188">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="4da1f-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="4da1f-189">Пуск</span><span class="sxs-lookup"><span data-stu-id="4da1f-189">NOTES</span></span>

<span data-ttu-id="4da1f-190">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="4da1f-190">ALIASES</span></span>

<span data-ttu-id="4da1f-191">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4da1f-191">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4da1f-192">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4da1f-192">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4da1f-193">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4da1f-193">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4da1f-194">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="4da1f-194">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4da1f-195">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="4da1f-195">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="4da1f-196">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="4da1f-196">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="4da1f-197">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="4da1f-197">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="4da1f-198">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="4da1f-198">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="4da1f-199">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="4da1f-199">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4da1f-200">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="4da1f-200">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="4da1f-201">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="4da1f-201">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="4da1f-202">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="4da1f-202">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="4da1f-203">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4da1f-203">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4da1f-204">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="4da1f-204">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4da1f-205">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4da1f-205">RELATED LINKS</span></span>

