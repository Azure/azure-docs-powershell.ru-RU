---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: 9eb3ff31873b23fc97f53fffecdbbb38367ac2b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392580"
---
# <span data-ttu-id="18158-101">Invoke-AzKustoDataConnectionValidation</span><span class="sxs-lookup"><span data-stu-id="18158-101">Invoke-AzKustoDataConnectionValidation</span></span>

## <span data-ttu-id="18158-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18158-102">SYNOPSIS</span></span>
<span data-ttu-id="18158-103">Проверяет, действительны ли параметры подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="18158-103">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="18158-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="18158-104">SYNTAX</span></span>

### <span data-ttu-id="18158-105">DataExpandedEventHub (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="18158-105">DataExpandedEventHub (Default)</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="18158-106">DataExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="18158-106">DataExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="18158-107">DataExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="18158-107">DataExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="18158-108">DataViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="18158-108">DataViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="18158-109">DataViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="18158-109">DataViaIdentityExpandedEventHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="18158-110">DataViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="18158-110">DataViaIdentityExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="18158-111">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="18158-111">UpdateExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="18158-112">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="18158-112">UpdateViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="18158-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18158-113">DESCRIPTION</span></span>
<span data-ttu-id="18158-114">Проверяет, действительны ли параметры подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="18158-114">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="18158-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="18158-115">EXAMPLES</span></span>

### <span data-ttu-id="18158-116">Пример 1. Проверка параметров подключения к данным EventHub</span><span class="sxs-lookup"><span data-stu-id="18158-116">Example 1: Validate EventHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="18158-117">Команда выше проверяет подключение к данным EventHub с именем "myeventhubdc" для базы данных mykustodatabase в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="18158-117">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="18158-118">Пример 2. Проверка параметров подключения к данным EventGrid</span><span class="sxs-lookup"><span data-stu-id="18158-118">Example 2: Validate EventGrid data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="18158-119">Команда выше проверяет подключение к данным EventGrid с именем myeventgriddc для базы данных mykustodatabase в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="18158-119">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="18158-120">Пример 3. Проверка параметров подключения к данным IotHub</span><span class="sxs-lookup"><span data-stu-id="18158-120">Example 3: Validate IotHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="18158-121">Команда выше проверяет подключение к данным IotHub с именем myiothubdc для базы данных mykustodatabase в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="18158-121">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="18158-122">Пример 4. Проверка параметров подключения к данным EventHub с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="18158-122">Example 4: Validate EventHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="18158-123">Команда выше проверяет подключение к данным EventHub с именем "myeventhubdc" для базы данных mykustodatabase в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="18158-123">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="18158-124">Пример 5. Проверка параметров подключения к данным EventGrid с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="18158-124">Example 5: Validate EventGrid data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="18158-125">Команда выше проверяет подключение к данным EventGrid с именем myeventgriddc для базы данных mykustodatabase в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="18158-125">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="18158-126">Пример 6. Проверка параметров подключения к данным IotHub с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="18158-126">Example 6: Validate IotHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="18158-127">Команда выше проверяет подключение к данным IotHub с именем myiothubdc для базы данных mykustodatabase в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="18158-127">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="18158-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18158-128">PARAMETERS</span></span>

### <span data-ttu-id="18158-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="18158-129">-BlobStorageEventType</span></span>
<span data-ttu-id="18158-130">Имя обработки события типа события хранилища BLOB-типов.</span><span class="sxs-lookup"><span data-stu-id="18158-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="18158-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="18158-131">-ClusterName</span></span>
<span data-ttu-id="18158-132">Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="18158-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18158-133">-Сжатие</span><span class="sxs-lookup"><span data-stu-id="18158-133">-Compression</span></span>
<span data-ttu-id="18158-134">Тип сжатия сообщений в центре событий.</span><span class="sxs-lookup"><span data-stu-id="18158-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: DataExpandedEventHub, DataViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18158-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="18158-135">-ConsumerGroup</span></span>
<span data-ttu-id="18158-136">Группа потребительских событий/iot-концентратора.</span><span class="sxs-lookup"><span data-stu-id="18158-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="18158-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="18158-137">-DatabaseName</span></span>
<span data-ttu-id="18158-138">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="18158-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18158-139">-DataConnectionName</span><span class="sxs-lookup"><span data-stu-id="18158-139">-DataConnectionName</span></span>
<span data-ttu-id="18158-140">Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="18158-140">The name of the data connection.</span></span>

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

### <span data-ttu-id="18158-141">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="18158-141">-DataFormat</span></span>
<span data-ttu-id="18158-142">Формат данных сообщения.</span><span class="sxs-lookup"><span data-stu-id="18158-142">The data format of the message.</span></span>
<span data-ttu-id="18158-143">При желании формат данных можно добавить в каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="18158-143">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="18158-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18158-144">-DefaultProfile</span></span>
<span data-ttu-id="18158-145">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18158-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18158-146">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="18158-146">-EventHubResourceId</span></span>
<span data-ttu-id="18158-147">ИД ресурса в центре событий, который будет использоваться для создания подключения к данным или сетки событий, настроен для отправки событий.</span><span class="sxs-lookup"><span data-stu-id="18158-147">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18158-148">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="18158-148">-EventSystemProperty</span></span>
<span data-ttu-id="18158-149">Системные свойства концентратора событий и iot.</span><span class="sxs-lookup"><span data-stu-id="18158-149">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DataExpandedEventHub, DataExpandedIotHub, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18158-150">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="18158-150">-IgnoreFirstRecord</span></span>
<span data-ttu-id="18158-151">Если зафиксировать это, означает, что при чтении следует игнорировать первую запись каждого файла.</span><span class="sxs-lookup"><span data-stu-id="18158-151">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="18158-152">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18158-152">-InputObject</span></span>
<span data-ttu-id="18158-153">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="18158-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18158-154">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="18158-154">-IotHubResourceId</span></span>
<span data-ttu-id="18158-155">ИД ресурса концентратора IOT, который будет использоваться для создания подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="18158-155">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18158-156">-Kind</span><span class="sxs-lookup"><span data-stu-id="18158-156">-Kind</span></span>
<span data-ttu-id="18158-157">Тип конечной точки для подключения к данным</span><span class="sxs-lookup"><span data-stu-id="18158-157">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="18158-158">-Location</span><span class="sxs-lookup"><span data-stu-id="18158-158">-Location</span></span>
<span data-ttu-id="18158-159">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="18158-159">Resource location.</span></span>

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

### <span data-ttu-id="18158-160">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="18158-160">-MappingRuleName</span></span>
<span data-ttu-id="18158-161">Правило сопоставления, используемее для передачи данных.</span><span class="sxs-lookup"><span data-stu-id="18158-161">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="18158-162">При желании сведения о сопоставлении можно добавить в каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="18158-162">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="18158-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18158-163">-ResourceGroupName</span></span>
<span data-ttu-id="18158-164">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="18158-164">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18158-165">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="18158-165">-SharedAccessPolicyName</span></span>
<span data-ttu-id="18158-166">Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="18158-166">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18158-167">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="18158-167">-StorageAccountResourceId</span></span>
<span data-ttu-id="18158-168">ИД ресурса учетной записи хранения, в которой находятся данные.</span><span class="sxs-lookup"><span data-stu-id="18158-168">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18158-169">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18158-169">-SubscriptionId</span></span>
<span data-ttu-id="18158-170">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="18158-170">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="18158-171">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="18158-171">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18158-172">-TableName</span><span class="sxs-lookup"><span data-stu-id="18158-172">-TableName</span></span>
<span data-ttu-id="18158-173">Таблица, в которой нужно ввести данные.</span><span class="sxs-lookup"><span data-stu-id="18158-173">The table where the data should be ingested.</span></span>
<span data-ttu-id="18158-174">При желании в каждое сообщение можно добавить сведения из таблицы.</span><span class="sxs-lookup"><span data-stu-id="18158-174">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="18158-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18158-175">-Confirm</span></span>
<span data-ttu-id="18158-176">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18158-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18158-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18158-177">-WhatIf</span></span>
<span data-ttu-id="18158-178">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18158-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18158-179">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="18158-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18158-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18158-180">CommonParameters</span></span>
<span data-ttu-id="18158-181">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18158-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18158-182">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18158-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18158-183">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18158-183">INPUTS</span></span>

### <span data-ttu-id="18158-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="18158-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="18158-185">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="18158-185">OUTPUTS</span></span>

### <span data-ttu-id="18158-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnectionValidationResult</span><span class="sxs-lookup"><span data-stu-id="18158-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnectionValidationResult</span></span>

## <span data-ttu-id="18158-187">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="18158-187">NOTES</span></span>

<span data-ttu-id="18158-188">ALIASES</span><span class="sxs-lookup"><span data-stu-id="18158-188">ALIASES</span></span>

<span data-ttu-id="18158-189">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="18158-189">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="18158-190">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="18158-190">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="18158-191">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="18158-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="18158-192">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="18158-192">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="18158-193">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="18158-193">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="18158-194">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="18158-194">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="18158-195">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="18158-195">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="18158-196">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="18158-196">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="18158-197">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="18158-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="18158-198">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="18158-198">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="18158-199">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="18158-199">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="18158-200">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="18158-200">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="18158-201">`[SubscriptionId <String>]`: получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="18158-201">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="18158-202">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="18158-202">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="18158-203">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18158-203">RELATED LINKS</span></span>

