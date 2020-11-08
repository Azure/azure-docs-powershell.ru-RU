---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: 9eb3ff31873b23fc97f53fffecdbbb38367ac2b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236324"
---
# <span data-ttu-id="ebee4-101">Invoke-AzKustoDataConnectionValidation</span><span class="sxs-lookup"><span data-stu-id="ebee4-101">Invoke-AzKustoDataConnectionValidation</span></span>

## <span data-ttu-id="ebee4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebee4-102">SYNOPSIS</span></span>
<span data-ttu-id="ebee4-103">Проверка наличия допустимых параметров подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="ebee4-103">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="ebee4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebee4-104">SYNTAX</span></span>

### <span data-ttu-id="ebee4-105">DataExpandedEventHub (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ebee4-105">DataExpandedEventHub (Default)</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ebee4-106">DataExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="ebee4-106">DataExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ebee4-107">DataExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="ebee4-107">DataExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ebee4-108">DataViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="ebee4-108">DataViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ebee4-109">DataViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="ebee4-109">DataViaIdentityExpandedEventHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ebee4-110">DataViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="ebee4-110">DataViaIdentityExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ebee4-111">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="ebee4-111">UpdateExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ebee4-112">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="ebee4-112">UpdateViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ebee4-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebee4-113">DESCRIPTION</span></span>
<span data-ttu-id="ebee4-114">Проверка наличия допустимых параметров подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="ebee4-114">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="ebee4-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebee4-115">EXAMPLES</span></span>

### <span data-ttu-id="ebee4-116">Пример 1: Проверка параметров подключения к данным EventHub</span><span class="sxs-lookup"><span data-stu-id="ebee4-116">Example 1: Validate EventHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="ebee4-117">Описанная выше команда проверяет подключение к данным EventHub с именем "myeventhubdc" для базы данных "mykustodatabase" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ebee4-117">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ebee4-118">Пример 2: Проверка параметров подключения к данным EventGrid</span><span class="sxs-lookup"><span data-stu-id="ebee4-118">Example 2: Validate EventGrid data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="ebee4-119">Приведенная выше команда проверяет подключение к данным EventGrid с именем "myeventgriddc" для базы данных "mykustodatabase" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ebee4-119">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ebee4-120">Пример 3: Проверка параметров подключения к данным IotHub</span><span class="sxs-lookup"><span data-stu-id="ebee4-120">Example 3: Validate IotHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="ebee4-121">Приведенная выше команда проверяет подключение к данным IotHub с именем "myiothubdc" для базы данных "mykustodatabase" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ebee4-121">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ebee4-122">Пример 4: Проверка параметров подключения к данным EventHub с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="ebee4-122">Example 4: Validate EventHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="ebee4-123">Описанная выше команда проверяет подключение к данным EventHub с именем "myeventhubdc" для базы данных "mykustodatabase" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ebee4-123">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ebee4-124">Пример 5: Проверка параметров подключения к данным EventGrid с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="ebee4-124">Example 5: Validate EventGrid data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="ebee4-125">Приведенная выше команда проверяет подключение к данным EventGrid с именем "myeventgriddc" для базы данных "mykustodatabase" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ebee4-125">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ebee4-126">Пример 6: Проверка параметров подключения к данным IotHub с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="ebee4-126">Example 6: Validate IotHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="ebee4-127">Приведенная выше команда проверяет подключение к данным IotHub с именем "myiothubdc" для базы данных "mykustodatabase" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ebee4-127">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="ebee4-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebee4-128">PARAMETERS</span></span>

### <span data-ttu-id="ebee4-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="ebee4-129">-BlobStorageEventType</span></span>
<span data-ttu-id="ebee4-130">Имя типа события хранилища BLOB для обработки.</span><span class="sxs-lookup"><span data-stu-id="ebee4-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="ebee4-131">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="ebee4-131">-ClusterName</span></span>
<span data-ttu-id="ebee4-132">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="ebee4-132">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ebee4-133">-Сжатие</span><span class="sxs-lookup"><span data-stu-id="ebee4-133">-Compression</span></span>
<span data-ttu-id="ebee4-134">Тип сжатия сообщений центра событий.</span><span class="sxs-lookup"><span data-stu-id="ebee4-134">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="ebee4-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ebee4-135">-ConsumerGroup</span></span>
<span data-ttu-id="ebee4-136">Группа потребителей "событие/IOT центр Интернета".</span><span class="sxs-lookup"><span data-stu-id="ebee4-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="ebee4-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ebee4-137">-DatabaseName</span></span>
<span data-ttu-id="ebee4-138">Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="ebee4-138">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="ebee4-139">-DataConnectionName</span><span class="sxs-lookup"><span data-stu-id="ebee4-139">-DataConnectionName</span></span>
<span data-ttu-id="ebee4-140">Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="ebee4-140">The name of the data connection.</span></span>

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

### <span data-ttu-id="ebee4-141">-Формат.</span><span class="sxs-lookup"><span data-stu-id="ebee4-141">-DataFormat</span></span>
<span data-ttu-id="ebee4-142">Формат данных сообщения.</span><span class="sxs-lookup"><span data-stu-id="ebee4-142">The data format of the message.</span></span>
<span data-ttu-id="ebee4-143">При необходимости можно добавить в каждое сообщение формат данных.</span><span class="sxs-lookup"><span data-stu-id="ebee4-143">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="ebee4-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebee4-144">-DefaultProfile</span></span>
<span data-ttu-id="ebee4-145">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebee4-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebee4-146">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="ebee4-146">-EventHubResourceId</span></span>
<span data-ttu-id="ebee4-147">Идентификатор ресурса для концентратора событий, который будет использоваться для создания подключения к данным или сетки событий, настроен для отправки событий.</span><span class="sxs-lookup"><span data-stu-id="ebee4-147">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="ebee4-148">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="ebee4-148">-EventSystemProperty</span></span>
<span data-ttu-id="ebee4-149">Свойства системы для центра событий и Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="ebee4-149">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="ebee4-150">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="ebee4-150">-IgnoreFirstRecord</span></span>
<span data-ttu-id="ebee4-151">Если установлено значение true, это означает, что при приеме будет игнорироваться первая запись каждого файла.</span><span class="sxs-lookup"><span data-stu-id="ebee4-151">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="ebee4-152">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebee4-152">-InputObject</span></span>
<span data-ttu-id="ebee4-153">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="ebee4-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ebee4-154">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="ebee4-154">-IotHubResourceId</span></span>
<span data-ttu-id="ebee4-155">Идентификатор ресурса центра Интернета вещей, который будет использоваться для создания подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="ebee4-155">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="ebee4-156">-Видах</span><span class="sxs-lookup"><span data-stu-id="ebee4-156">-Kind</span></span>
<span data-ttu-id="ebee4-157">Вариант конечной точки подключения к данным</span><span class="sxs-lookup"><span data-stu-id="ebee4-157">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="ebee4-158">-Location</span><span class="sxs-lookup"><span data-stu-id="ebee4-158">-Location</span></span>
<span data-ttu-id="ebee4-159">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="ebee4-159">Resource location.</span></span>

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

### <span data-ttu-id="ebee4-160">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="ebee4-160">-MappingRuleName</span></span>
<span data-ttu-id="ebee4-161">Правило сопоставления, которое будет использоваться для приема данных.</span><span class="sxs-lookup"><span data-stu-id="ebee4-161">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="ebee4-162">Кроме того, можно добавить сведения о сопоставлении в каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="ebee4-162">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="ebee4-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebee4-163">-ResourceGroupName</span></span>
<span data-ttu-id="ebee4-164">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="ebee4-164">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ebee4-165">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="ebee4-165">-SharedAccessPolicyName</span></span>
<span data-ttu-id="ebee4-166">Имя политики общего доступа.</span><span class="sxs-lookup"><span data-stu-id="ebee4-166">The name of the share access policy.</span></span>

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

### <span data-ttu-id="ebee4-167">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="ebee4-167">-StorageAccountResourceId</span></span>
<span data-ttu-id="ebee4-168">Идентификатор ресурса учетной записи хранения, в которой хранятся данные.</span><span class="sxs-lookup"><span data-stu-id="ebee4-168">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="ebee4-169">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ebee4-169">-SubscriptionId</span></span>
<span data-ttu-id="ebee4-170">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ebee4-170">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ebee4-171">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="ebee4-171">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ebee4-172">-TableName</span><span class="sxs-lookup"><span data-stu-id="ebee4-172">-TableName</span></span>
<span data-ttu-id="ebee4-173">Таблица, в которой должны быть выдаваться данные.</span><span class="sxs-lookup"><span data-stu-id="ebee4-173">The table where the data should be ingested.</span></span>
<span data-ttu-id="ebee4-174">При необходимости в каждое сообщение можно добавить сведения о таблице.</span><span class="sxs-lookup"><span data-stu-id="ebee4-174">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="ebee4-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebee4-175">-Confirm</span></span>
<span data-ttu-id="ebee4-176">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ebee4-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebee4-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebee4-177">-WhatIf</span></span>
<span data-ttu-id="ebee4-178">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ebee4-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebee4-179">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ebee4-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebee4-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebee4-180">CommonParameters</span></span>
<span data-ttu-id="ebee4-181">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebee4-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebee4-182">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebee4-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebee4-183">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebee4-183">INPUTS</span></span>

### <span data-ttu-id="ebee4-184">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ebee4-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ebee4-185">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebee4-185">OUTPUTS</span></span>

### <span data-ttu-id="ebee4-186">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IDataConnectionValidationResult</span><span class="sxs-lookup"><span data-stu-id="ebee4-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnectionValidationResult</span></span>

## <span data-ttu-id="ebee4-187">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebee4-187">NOTES</span></span>

<span data-ttu-id="ebee4-188">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="ebee4-188">ALIASES</span></span>

<span data-ttu-id="ebee4-189">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ebee4-189">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ebee4-190">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ebee4-190">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ebee4-191">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ebee4-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ebee4-192">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="ebee4-192">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ebee4-193">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="ebee4-193">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ebee4-194">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="ebee4-194">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ebee4-195">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="ebee4-195">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ebee4-196">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="ebee4-196">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ebee4-197">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="ebee4-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ebee4-198">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="ebee4-198">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ebee4-199">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="ebee4-199">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ebee4-200">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="ebee4-200">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ebee4-201">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ebee4-201">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ebee4-202">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="ebee4-202">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ebee4-203">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebee4-203">RELATED LINKS</span></span>

