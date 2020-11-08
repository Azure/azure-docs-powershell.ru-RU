---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
ms.openlocfilehash: 4fadb8a48b9886fe1c5a7c916d8f810abd8de6cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248993"
---
# <span data-ttu-id="c97b2-101">New-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="c97b2-101">New-AzKustoDataConnection</span></span>

## <span data-ttu-id="c97b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c97b2-102">SYNOPSIS</span></span>
<span data-ttu-id="c97b2-103">Создает или обновляет подключение к данным.</span><span class="sxs-lookup"><span data-stu-id="c97b2-103">Creates or updates a data connection.</span></span>

## <span data-ttu-id="c97b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c97b2-104">SYNTAX</span></span>

### <span data-ttu-id="c97b2-105">CreateExpandedEventHub (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c97b2-105">CreateExpandedEventHub (Default)</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c97b2-106">CreateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="c97b2-106">CreateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c97b2-107">CreateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="c97b2-107">CreateExpandedIotHub</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c97b2-108">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="c97b2-108">UpdateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c97b2-109">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="c97b2-109">UpdateViaIdentityExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c97b2-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c97b2-110">DESCRIPTION</span></span>
<span data-ttu-id="c97b2-111">Создает или обновляет подключение к данным.</span><span class="sxs-lookup"><span data-stu-id="c97b2-111">Creates or updates a data connection.</span></span>

## <span data-ttu-id="c97b2-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c97b2-112">EXAMPLES</span></span>

### <span data-ttu-id="c97b2-113">Пример 1: создание нового подключения к данным EventHub</span><span class="sxs-lookup"><span data-stu-id="c97b2-113">Example 1: Create a new EventHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "EventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="c97b2-114">В приведенной выше команде создается новое подключение к данным EventHub с именем "myeventhubdc" для базы данных "mykustodatabase" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="c97b2-114">The above command creates a new EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="c97b2-115">Пример 2: создание нового подключения к данным EventGrid</span><span class="sxs-lookup"><span data-stu-id="c97b2-115">Example 2: Create a new EventGrid data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping" -IgnoreFirstRecord "false" -BlobStorageEventType "Microsoft.Storage.BlobRenamed"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="c97b2-116">Вышеприведенная команда создает новое подключение к данным EventGrid с именем "myeventgriddc" для базы данных "mykustodatabase" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="c97b2-116">The above command creates a new EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="c97b2-117">Пример 3: создание нового подключения к данным IotHub</span><span class="sxs-lookup"><span data-stu-id="c97b2-117">Example 3: Create a new IotHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="c97b2-118">Вышеприведенная команда создает новое подключение к данным IotHub с именем "myiothubdc" для базы данных "mykustodatabase" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="c97b2-118">The above command creates a new IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="c97b2-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c97b2-119">PARAMETERS</span></span>

### <span data-ttu-id="c97b2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c97b2-120">-AsJob</span></span>
<span data-ttu-id="c97b2-121">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c97b2-121">Run the command as a job</span></span>

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

### <span data-ttu-id="c97b2-122">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="c97b2-122">-BlobStorageEventType</span></span>
<span data-ttu-id="c97b2-123">Имя типа события хранилища BLOB для обработки.</span><span class="sxs-lookup"><span data-stu-id="c97b2-123">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="c97b2-124">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="c97b2-124">-ClusterName</span></span>
<span data-ttu-id="c97b2-125">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="c97b2-125">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c97b2-126">-Сжатие</span><span class="sxs-lookup"><span data-stu-id="c97b2-126">-Compression</span></span>
<span data-ttu-id="c97b2-127">Тип сжатия сообщений центра событий.</span><span class="sxs-lookup"><span data-stu-id="c97b2-127">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="c97b2-128">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c97b2-128">-ConsumerGroup</span></span>
<span data-ttu-id="c97b2-129">Группа потребителей "событие/IOT центр Интернета".</span><span class="sxs-lookup"><span data-stu-id="c97b2-129">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="c97b2-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c97b2-130">-DatabaseName</span></span>
<span data-ttu-id="c97b2-131">Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="c97b2-131">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="c97b2-132">-Формат.</span><span class="sxs-lookup"><span data-stu-id="c97b2-132">-DataFormat</span></span>
<span data-ttu-id="c97b2-133">Формат данных сообщения.</span><span class="sxs-lookup"><span data-stu-id="c97b2-133">The data format of the message.</span></span>
<span data-ttu-id="c97b2-134">При необходимости можно добавить в каждое сообщение формат данных.</span><span class="sxs-lookup"><span data-stu-id="c97b2-134">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="c97b2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c97b2-135">-DefaultProfile</span></span>
<span data-ttu-id="c97b2-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c97b2-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c97b2-137">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="c97b2-137">-EventHubResourceId</span></span>
<span data-ttu-id="c97b2-138">Идентификатор ресурса для концентратора событий, который будет использоваться для создания подключения к данным или сетки событий, настроен для отправки событий.</span><span class="sxs-lookup"><span data-stu-id="c97b2-138">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="c97b2-139">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="c97b2-139">-EventSystemProperty</span></span>
<span data-ttu-id="c97b2-140">Свойства системы для центра событий и Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="c97b2-140">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="c97b2-141">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="c97b2-141">-IgnoreFirstRecord</span></span>
<span data-ttu-id="c97b2-142">Если установлено значение true, это означает, что при приеме будет игнорироваться первая запись каждого файла.</span><span class="sxs-lookup"><span data-stu-id="c97b2-142">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="c97b2-143">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="c97b2-143">-IotHubResourceId</span></span>
<span data-ttu-id="c97b2-144">Идентификатор ресурса центра Интернета вещей, который будет использоваться для создания подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="c97b2-144">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="c97b2-145">-Видах</span><span class="sxs-lookup"><span data-stu-id="c97b2-145">-Kind</span></span>
<span data-ttu-id="c97b2-146">Вариант конечной точки подключения к данным</span><span class="sxs-lookup"><span data-stu-id="c97b2-146">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="c97b2-147">-Location</span><span class="sxs-lookup"><span data-stu-id="c97b2-147">-Location</span></span>
<span data-ttu-id="c97b2-148">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="c97b2-148">Resource location.</span></span>

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

### <span data-ttu-id="c97b2-149">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="c97b2-149">-MappingRuleName</span></span>
<span data-ttu-id="c97b2-150">Правило сопоставления, которое будет использоваться для приема данных.</span><span class="sxs-lookup"><span data-stu-id="c97b2-150">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="c97b2-151">Кроме того, можно добавить сведения о сопоставлении в каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="c97b2-151">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="c97b2-152">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c97b2-152">-Name</span></span>
<span data-ttu-id="c97b2-153">Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="c97b2-153">The name of the data connection.</span></span>

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

### <span data-ttu-id="c97b2-154">-Wait</span><span class="sxs-lookup"><span data-stu-id="c97b2-154">-NoWait</span></span>
<span data-ttu-id="c97b2-155">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="c97b2-155">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c97b2-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c97b2-156">-ResourceGroupName</span></span>
<span data-ttu-id="c97b2-157">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="c97b2-157">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c97b2-158">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="c97b2-158">-SharedAccessPolicyName</span></span>
<span data-ttu-id="c97b2-159">Имя политики общего доступа.</span><span class="sxs-lookup"><span data-stu-id="c97b2-159">The name of the share access policy.</span></span>

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

### <span data-ttu-id="c97b2-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c97b2-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="c97b2-161">Идентификатор ресурса учетной записи хранения, в которой хранятся данные.</span><span class="sxs-lookup"><span data-stu-id="c97b2-161">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="c97b2-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c97b2-162">-SubscriptionId</span></span>
<span data-ttu-id="c97b2-163">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c97b2-163">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c97b2-164">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="c97b2-164">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c97b2-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="c97b2-165">-TableName</span></span>
<span data-ttu-id="c97b2-166">Таблица, в которой должны быть выдаваться данные.</span><span class="sxs-lookup"><span data-stu-id="c97b2-166">The table where the data should be ingested.</span></span>
<span data-ttu-id="c97b2-167">При необходимости в каждое сообщение можно добавить сведения о таблице.</span><span class="sxs-lookup"><span data-stu-id="c97b2-167">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="c97b2-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c97b2-168">-Confirm</span></span>
<span data-ttu-id="c97b2-169">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c97b2-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c97b2-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c97b2-170">-WhatIf</span></span>
<span data-ttu-id="c97b2-171">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c97b2-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c97b2-172">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c97b2-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c97b2-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97b2-173">CommonParameters</span></span>
<span data-ttu-id="c97b2-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c97b2-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97b2-175">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c97b2-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97b2-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c97b2-176">INPUTS</span></span>

## <span data-ttu-id="c97b2-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c97b2-177">OUTPUTS</span></span>

### <span data-ttu-id="c97b2-178">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="c97b2-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="c97b2-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="c97b2-179">NOTES</span></span>

<span data-ttu-id="c97b2-180">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="c97b2-180">ALIASES</span></span>

## <span data-ttu-id="c97b2-181">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c97b2-181">RELATED LINKS</span></span>

