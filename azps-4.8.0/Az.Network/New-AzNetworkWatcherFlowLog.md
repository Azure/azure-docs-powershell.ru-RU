---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 1fe3cb8227751553ac748fb99cf08baa044a6f0d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244366"
---
# <span data-ttu-id="6f94b-101">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="6f94b-101">New-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="6f94b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f94b-102">SYNOPSIS</span></span>
<span data-ttu-id="6f94b-103">Создание или обновление ресурса журнала потока для указанной группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="6f94b-103">Create or update a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="6f94b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f94b-104">SYNTAX</span></span>

### <span data-ttu-id="6f94b-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f94b-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f94b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6f94b-106">SetByResource</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f94b-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="6f94b-107">SetByResourceWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f94b-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="6f94b-108">SetByNameWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f94b-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6f94b-109">SetByLocation</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f94b-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="6f94b-110">SetByLocationWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f94b-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f94b-111">DESCRIPTION</span></span>
<span data-ttu-id="6f94b-112">Команда "New-AzNetworkWatcherFlowLog" создает или обновляет ресурс журнала потока для указанной группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="6f94b-112">New-AzNetworkWatcherFlowLog command creates or updates a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="6f94b-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f94b-113">EXAMPLES</span></span>

### <span data-ttu-id="6f94b-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6f94b-114">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $true -EnableRetention $true -RetentionPolicyDays 5 -FormatVersion 2 -EnableTrafficAnalytics -TrafficAnalyticsWorkspaceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace
```

<span data-ttu-id="6f94b-115">Name (имя): pstest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ERS/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETag: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: успешное расположение: eastus TargetResourceId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG StorageId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/MySTorage Enabled: true RetentionPolicy: {"дней": 5; {"тип": "JSON", "Version": 2} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"Enabled": true, "workspaceId": "BBBBBBBB-BBBB-BBBB-BBBB-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/Subscriptions/BBBBBBBB-BBBB-BBBB-BBBB-bbbbbbbbbbbb/resourcegr oups/FlowLogsV2Demo/providers/Microsoft. OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60}}</span><span class="sxs-lookup"><span data-stu-id="6f94b-115">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 } }</span></span>

### <span data-ttu-id="6f94b-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6f94b-116">Example 2</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $false -EnableTrafficAnalytics:$false
```

<span data-ttu-id="6f94b-117">Если вы хотите отключить ресурс flowLog, для которого настроен TrafficAnalytics, необходимо также отключить TrafficAnalytics.</span><span class="sxs-lookup"><span data-stu-id="6f94b-117">If you want to disable flowLog resource for which TrafficAnalytics is configured, it is necessary to disable TrafficAnalytics as well.</span></span> <span data-ttu-id="6f94b-118">Это можно сделать, как показано в примере 2.</span><span class="sxs-lookup"><span data-stu-id="6f94b-118">It can be done like in the example 2.</span></span>

<span data-ttu-id="6f94b-119">Name (имя): pstest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ERS/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETag: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: успешное расположение: eastus TargetResourceId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG StorageId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/MySTorage разрешено: false RetentionPolicy: {"дн.: 0," Enabled ": false} Format: {" тип ":" JSON "," Version ": 1} FlowAnalyticsConfiguration: {" networkWatcherFlowAnalyticsConfiguration ": {" Enabled ": false," trafficAnalyticsInterval ": 60}}</span><span class="sxs-lookup"><span data-stu-id="6f94b-119">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : False RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 1 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": false, "trafficAnalyticsInterval": 60 } }</span></span>

## <span data-ttu-id="6f94b-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f94b-120">PARAMETERS</span></span>

### <span data-ttu-id="6f94b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f94b-121">-DefaultProfile</span></span>
<span data-ttu-id="6f94b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f94b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-123">-Включено</span><span class="sxs-lookup"><span data-stu-id="6f94b-123">-Enabled</span></span>
<span data-ttu-id="6f94b-124">Пометка для включения и отключения ведения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="6f94b-124">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-125">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="6f94b-125">-EnableRetention</span></span>
<span data-ttu-id="6f94b-126">Пометка для включения и отключения хранения.</span><span class="sxs-lookup"><span data-stu-id="6f94b-126">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-127">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="6f94b-127">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="6f94b-128">Пометка для включения и отключения TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="6f94b-128">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-129">-Force</span><span class="sxs-lookup"><span data-stu-id="6f94b-129">-Force</span></span>
<span data-ttu-id="6f94b-130">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="6f94b-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-131">-FormatType</span><span class="sxs-lookup"><span data-stu-id="6f94b-131">-FormatType</span></span>
<span data-ttu-id="6f94b-132">Тип файла журнала потока.</span><span class="sxs-lookup"><span data-stu-id="6f94b-132">The file type of flow log.</span></span>
<span data-ttu-id="6f94b-133">Теперь единственным поддерживаемым значением является "JSON".</span><span class="sxs-lookup"><span data-stu-id="6f94b-133">The only supported value now is 'JSON'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-134">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="6f94b-134">-FormatVersion</span></span>
<span data-ttu-id="6f94b-135">Версия журнала потока (редакция).</span><span class="sxs-lookup"><span data-stu-id="6f94b-135">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-136">-Location</span><span class="sxs-lookup"><span data-stu-id="6f94b-136">-Location</span></span>
<span data-ttu-id="6f94b-137">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="6f94b-137">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6f94b-138">-Name</span></span>
<span data-ttu-id="6f94b-139">Имя журнала потока.</span><span class="sxs-lookup"><span data-stu-id="6f94b-139">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6f94b-140">-NetworkWatcher</span></span>
<span data-ttu-id="6f94b-141">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="6f94b-141">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6f94b-142">-NetworkWatcherName</span></span>
<span data-ttu-id="6f94b-143">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="6f94b-143">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f94b-144">-ResourceGroupName</span></span>
<span data-ttu-id="6f94b-145">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="6f94b-145">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-146">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="6f94b-146">-RetentionPolicyDays</span></span>
<span data-ttu-id="6f94b-147">Количество дней для хранения записей журнала потока.</span><span class="sxs-lookup"><span data-stu-id="6f94b-147">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-148">-StorageId</span><span class="sxs-lookup"><span data-stu-id="6f94b-148">-StorageId</span></span>
<span data-ttu-id="6f94b-149">Идентификатор учетной записи хранения, которая используется для хранения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="6f94b-149">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-150">-Тег</span><span class="sxs-lookup"><span data-stu-id="6f94b-150">-Tag</span></span>
<span data-ttu-id="6f94b-151">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6f94b-151">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-152">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6f94b-152">-TargetResourceId</span></span>
<span data-ttu-id="6f94b-153">Идентификатор группы безопасности сети, к которой будет применен журнал потока.</span><span class="sxs-lookup"><span data-stu-id="6f94b-153">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-154">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="6f94b-154">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="6f94b-155">Интервал (в минутах), по истечении которого служба TA должна выполнять анализ потока.</span><span class="sxs-lookup"><span data-stu-id="6f94b-155">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-156">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="6f94b-156">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="6f94b-157">Код ресурса присоединенной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6f94b-157">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f94b-158">-Confirm</span></span>
<span data-ttu-id="6f94b-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6f94b-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f94b-160">-WhatIf</span></span>
<span data-ttu-id="6f94b-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6f94b-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f94b-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6f94b-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f94b-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f94b-163">CommonParameters</span></span>
<span data-ttu-id="6f94b-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f94b-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f94b-165">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f94b-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f94b-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f94b-166">INPUTS</span></span>

### <span data-ttu-id="6f94b-167">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6f94b-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="6f94b-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f94b-168">OUTPUTS</span></span>

### <span data-ttu-id="6f94b-169">Microsoft. Azure. Commands. Network. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="6f94b-169">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="6f94b-170">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f94b-170">NOTES</span></span>

## <span data-ttu-id="6f94b-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f94b-171">RELATED LINKS</span></span>

[<span data-ttu-id="6f94b-172">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6f94b-172">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="6f94b-173">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6f94b-173">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="6f94b-174">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6f94b-174">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="6f94b-175">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6f94b-175">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="6f94b-176">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6f94b-176">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6f94b-177">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6f94b-177">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="6f94b-178">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6f94b-178">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6f94b-179">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6f94b-179">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6f94b-180">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6f94b-180">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="6f94b-181">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6f94b-181">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6f94b-182">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6f94b-182">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6f94b-183">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6f94b-183">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6f94b-184">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f94b-184">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="6f94b-185">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6f94b-185">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="6f94b-186">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6f94b-186">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="6f94b-187">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6f94b-187">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6f94b-188">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6f94b-188">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6f94b-189">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6f94b-189">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6f94b-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6f94b-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="6f94b-191">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6f94b-191">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6f94b-192">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6f94b-192">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6f94b-193">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6f94b-193">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="6f94b-194">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6f94b-194">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="6f94b-195">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6f94b-195">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="6f94b-196">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6f94b-196">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="6f94b-197">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6f94b-197">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="6f94b-198">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6f94b-198">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="6f94b-199">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="6f94b-199">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="6f94b-200">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="6f94b-200">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="6f94b-201">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="6f94b-201">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
