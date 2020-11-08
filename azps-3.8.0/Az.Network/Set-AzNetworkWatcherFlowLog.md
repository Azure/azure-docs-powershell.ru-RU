---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 284d88d4eb8dbe3a480911397790d5da35acb4a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073097"
---
# <span data-ttu-id="c30f3-101">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c30f3-101">Set-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="c30f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c30f3-102">SYNOPSIS</span></span>
<span data-ttu-id="c30f3-103">Обновляет ресурс журнала потока.</span><span class="sxs-lookup"><span data-stu-id="c30f3-103">Updates flow log resource.</span></span>

## <span data-ttu-id="c30f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c30f3-104">SYNTAX</span></span>

### <span data-ttu-id="c30f3-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c30f3-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c30f3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c30f3-106">SetByResource</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c30f3-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="c30f3-107">SetByResourceWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c30f3-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="c30f3-108">SetByNameWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c30f3-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c30f3-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c30f3-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="c30f3-110">SetByLocationWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c30f3-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c30f3-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c30f3-112">SetByResourceIdWithTA</span><span class="sxs-lookup"><span data-stu-id="c30f3-112">SetByResourceIdWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c30f3-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="c30f3-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c30f3-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c30f3-114">DESCRIPTION</span></span>
<span data-ttu-id="c30f3-115">Обновляет ресурс журнала потока.</span><span class="sxs-lookup"><span data-stu-id="c30f3-115">Updates flow log resource.</span></span>

## <span data-ttu-id="c30f3-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c30f3-116">EXAMPLES</span></span>

### <span data-ttu-id="c30f3-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c30f3-117">Example 1</span></span>
```powershell
PS C:\> $flowLog = Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
PS C:\> $flowLog.Enabled = $true
PS C:\> $flowLog.Format.Version = 2
PS C:\> $flowLog | Set-AzNetworkWatcherFlowLog -Force
```

<span data-ttu-id="c30f3-118">Name (имя): pstest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ERS/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETag: W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState: успешное расположение: eastus TargetResourceId:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG StorageId:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/MyStorage Enabled: true RetentionPolicy: {"Days": 0, "Enabled": false} Format: {"тип": "JSON", "Version": "2}". {}</span><span class="sxs-lookup"><span data-stu-id="c30f3-118">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled                    : True RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : {}</span></span>

## <span data-ttu-id="c30f3-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c30f3-119">PARAMETERS</span></span>

### <span data-ttu-id="c30f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c30f3-120">-DefaultProfile</span></span>
<span data-ttu-id="c30f3-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c30f3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c30f3-122">-Включено</span><span class="sxs-lookup"><span data-stu-id="c30f3-122">-Enabled</span></span>
<span data-ttu-id="c30f3-123">Пометка для включения и отключения ведения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="c30f3-123">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30f3-124">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="c30f3-124">-EnableRetention</span></span>
<span data-ttu-id="c30f3-125">Пометка для включения и отключения хранения.</span><span class="sxs-lookup"><span data-stu-id="c30f3-125">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30f3-126">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="c30f3-126">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="c30f3-127">Пометка для включения и отключения TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="c30f3-127">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30f3-128">-Force</span><span class="sxs-lookup"><span data-stu-id="c30f3-128">-Force</span></span>
<span data-ttu-id="c30f3-129">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="c30f3-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c30f3-130">-FormatType</span><span class="sxs-lookup"><span data-stu-id="c30f3-130">-FormatType</span></span>
<span data-ttu-id="c30f3-131">Тип файла журнала потока.</span><span class="sxs-lookup"><span data-stu-id="c30f3-131">The file type of flow log.</span></span>
<span data-ttu-id="c30f3-132">Теперь единственным поддерживаемым значением является "JSON".</span><span class="sxs-lookup"><span data-stu-id="c30f3-132">The only supported value now is 'JSON'.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30f3-133">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="c30f3-133">-FormatVersion</span></span>
<span data-ttu-id="c30f3-134">Версия журнала потока (редакция).</span><span class="sxs-lookup"><span data-stu-id="c30f3-134">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30f3-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c30f3-135">-InputObject</span></span>
<span data-ttu-id="c30f3-136">Объект "поток LOF".</span><span class="sxs-lookup"><span data-stu-id="c30f3-136">Flow lof object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c30f3-137">-Location</span><span class="sxs-lookup"><span data-stu-id="c30f3-137">-Location</span></span>
<span data-ttu-id="c30f3-138">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="c30f3-138">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c30f3-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c30f3-139">-Name</span></span>
<span data-ttu-id="c30f3-140">Имя журнала потока.</span><span class="sxs-lookup"><span data-stu-id="c30f3-140">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30f3-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c30f3-141">-NetworkWatcher</span></span>
<span data-ttu-id="c30f3-142">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="c30f3-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="c30f3-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c30f3-143">-NetworkWatcherName</span></span>
<span data-ttu-id="c30f3-144">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="c30f3-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="c30f3-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c30f3-145">-ResourceGroupName</span></span>
<span data-ttu-id="c30f3-146">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="c30f3-146">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c30f3-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c30f3-147">-ResourceId</span></span>
<span data-ttu-id="c30f3-148">Идентификатор ресурса FlowLog.</span><span class="sxs-lookup"><span data-stu-id="c30f3-148">FlowLog resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c30f3-149">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="c30f3-149">-RetentionPolicyDays</span></span>
<span data-ttu-id="c30f3-150">Количество дней для хранения записей журнала потока.</span><span class="sxs-lookup"><span data-stu-id="c30f3-150">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30f3-151">-StorageId</span><span class="sxs-lookup"><span data-stu-id="c30f3-151">-StorageId</span></span>
<span data-ttu-id="c30f3-152">Идентификатор учетной записи хранения, которая используется для хранения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="c30f3-152">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30f3-153">-Тег</span><span class="sxs-lookup"><span data-stu-id="c30f3-153">-Tag</span></span>
<span data-ttu-id="c30f3-154">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c30f3-154">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30f3-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c30f3-155">-TargetResourceId</span></span>
<span data-ttu-id="c30f3-156">Идентификатор группы безопасности сети, к которой будет применен журнал потока.</span><span class="sxs-lookup"><span data-stu-id="c30f3-156">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30f3-157">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="c30f3-157">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="c30f3-158">Интервал (в минутах), по истечении которого служба TA должна выполнять анализ потока.</span><span class="sxs-lookup"><span data-stu-id="c30f3-158">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30f3-159">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="c30f3-159">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="c30f3-160">Код ресурса присоединенной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c30f3-160">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30f3-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c30f3-161">-Confirm</span></span>
<span data-ttu-id="c30f3-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c30f3-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c30f3-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c30f3-163">-WhatIf</span></span>
<span data-ttu-id="c30f3-164">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c30f3-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c30f3-165">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c30f3-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c30f3-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c30f3-166">CommonParameters</span></span>
<span data-ttu-id="c30f3-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c30f3-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c30f3-168">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c30f3-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c30f3-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c30f3-169">INPUTS</span></span>

### <span data-ttu-id="c30f3-170">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c30f3-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c30f3-171">System. String</span><span class="sxs-lookup"><span data-stu-id="c30f3-171">System.String</span></span>

### <span data-ttu-id="c30f3-172">Microsoft. Azure. Commands. Network. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="c30f3-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="c30f3-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c30f3-173">OUTPUTS</span></span>

### <span data-ttu-id="c30f3-174">Microsoft. Azure. Commands. Network. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="c30f3-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="c30f3-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="c30f3-175">NOTES</span></span>

## <span data-ttu-id="c30f3-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c30f3-176">RELATED LINKS</span></span>

[<span data-ttu-id="c30f3-177">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c30f3-177">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c30f3-178">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c30f3-178">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c30f3-179">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c30f3-179">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c30f3-180">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c30f3-180">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c30f3-181">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c30f3-181">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c30f3-182">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c30f3-182">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c30f3-183">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c30f3-183">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c30f3-184">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c30f3-184">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c30f3-185">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c30f3-185">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c30f3-186">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c30f3-186">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c30f3-187">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c30f3-187">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c30f3-188">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c30f3-188">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c30f3-189">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c30f3-189">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c30f3-190">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c30f3-190">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c30f3-191">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c30f3-191">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c30f3-192">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c30f3-192">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c30f3-193">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c30f3-193">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c30f3-194">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c30f3-194">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c30f3-195">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c30f3-195">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c30f3-196">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c30f3-196">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c30f3-197">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c30f3-197">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c30f3-198">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c30f3-198">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c30f3-199">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c30f3-199">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c30f3-200">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c30f3-200">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c30f3-201">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c30f3-201">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c30f3-202">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c30f3-202">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="c30f3-203">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c30f3-203">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="c30f3-204">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c30f3-204">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog)

[<span data-ttu-id="c30f3-205">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c30f3-205">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="c30f3-206">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c30f3-206">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog)