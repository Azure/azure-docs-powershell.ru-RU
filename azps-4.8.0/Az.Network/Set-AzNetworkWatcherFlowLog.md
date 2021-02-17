---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: c59034dcd587c9fee3ce6a4a7699670c77ea372f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415382"
---
# <span data-ttu-id="c7b61-101">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c7b61-101">Set-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="c7b61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7b61-102">SYNOPSIS</span></span>
<span data-ttu-id="c7b61-103">Обновляет ресурс журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="c7b61-103">Updates flow log resource.</span></span>

## <span data-ttu-id="c7b61-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c7b61-104">SYNTAX</span></span>

### <span data-ttu-id="c7b61-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c7b61-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b61-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c7b61-106">SetByResource</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b61-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="c7b61-107">SetByResourceWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b61-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="c7b61-108">SetByNameWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b61-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c7b61-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b61-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="c7b61-110">SetByLocationWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b61-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c7b61-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b61-112">SetByResourceIdWithTA</span><span class="sxs-lookup"><span data-stu-id="c7b61-112">SetByResourceIdWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b61-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="c7b61-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7b61-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7b61-114">DESCRIPTION</span></span>
<span data-ttu-id="c7b61-115">Обновляет ресурс журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="c7b61-115">Updates flow log resource.</span></span>

## <span data-ttu-id="c7b61-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c7b61-116">EXAMPLES</span></span>

### <span data-ttu-id="c7b61-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c7b61-117">Example 1</span></span>
```powershell
PS C:\> $flowLog = Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
PS C:\> $flowLog.Enabled = $true
PS C:\> $flowLog.Format.Version = 2
PS C:\> $flowLog | Set-AzNetworkWatcherFlowLog -Force
```

<span data-ttu-id="c7b61-118">Name : pstest Id : /subscriptions/bbbbbb-bbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState : Succeeded Location : eastus TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbb-bbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId : /subscriptions/bbbbbb-bbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled: True RetentionPolicy : { "Days": 0, "Enabled": false } Format : { "Type": "JSON", "Версия": 2 } FlowAnalyticsConfiguration: {}</span><span class="sxs-lookup"><span data-stu-id="c7b61-118">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled                    : True RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : {}</span></span>

## <span data-ttu-id="c7b61-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7b61-119">PARAMETERS</span></span>

### <span data-ttu-id="c7b61-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7b61-120">-DefaultProfile</span></span>
<span data-ttu-id="c7b61-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7b61-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7b61-122">-Enabled</span><span class="sxs-lookup"><span data-stu-id="c7b61-122">-Enabled</span></span>
<span data-ttu-id="c7b61-123">Пометить, чтобы включить или отключить ведение журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="c7b61-123">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="c7b61-124">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="c7b61-124">-EnableRetention</span></span>
<span data-ttu-id="c7b61-125">Пометить, чтобы включить или отключить хранение.</span><span class="sxs-lookup"><span data-stu-id="c7b61-125">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="c7b61-126">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="c7b61-126">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="c7b61-127">Пометка для того, чтобы включить или отключить TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="c7b61-127">Flag to enable/disable TrafficAnalytics</span></span>

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

### <span data-ttu-id="c7b61-128">-Force</span><span class="sxs-lookup"><span data-stu-id="c7b61-128">-Force</span></span>
<span data-ttu-id="c7b61-129">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="c7b61-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c7b61-130">-FormatType</span><span class="sxs-lookup"><span data-stu-id="c7b61-130">-FormatType</span></span>
<span data-ttu-id="c7b61-131">Тип файла журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="c7b61-131">The file type of flow log.</span></span>
<span data-ttu-id="c7b61-132">Теперь поддерживается только значение JSON.</span><span class="sxs-lookup"><span data-stu-id="c7b61-132">The only supported value now is 'JSON'.</span></span>

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

### <span data-ttu-id="c7b61-133">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="c7b61-133">-FormatVersion</span></span>
<span data-ttu-id="c7b61-134">Версия (редакция) журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="c7b61-134">The version (revision) of the flow log.</span></span>

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

### <span data-ttu-id="c7b61-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7b61-135">-InputObject</span></span>
<span data-ttu-id="c7b61-136">Объект Flow lof.</span><span class="sxs-lookup"><span data-stu-id="c7b61-136">Flow lof object.</span></span>

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

### <span data-ttu-id="c7b61-137">-Location</span><span class="sxs-lookup"><span data-stu-id="c7b61-137">-Location</span></span>
<span data-ttu-id="c7b61-138">Расположение сетевого просмотра.</span><span class="sxs-lookup"><span data-stu-id="c7b61-138">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c7b61-139">-Name</span><span class="sxs-lookup"><span data-stu-id="c7b61-139">-Name</span></span>
<span data-ttu-id="c7b61-140">Имя журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="c7b61-140">The flow log name.</span></span>

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

### <span data-ttu-id="c7b61-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7b61-141">-NetworkWatcher</span></span>
<span data-ttu-id="c7b61-142">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="c7b61-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="c7b61-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c7b61-143">-NetworkWatcherName</span></span>
<span data-ttu-id="c7b61-144">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="c7b61-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="c7b61-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7b61-145">-ResourceGroupName</span></span>
<span data-ttu-id="c7b61-146">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="c7b61-146">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c7b61-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7b61-147">-ResourceId</span></span>
<span data-ttu-id="c7b61-148">ИД ресурса FlowLog.</span><span class="sxs-lookup"><span data-stu-id="c7b61-148">FlowLog resource ID.</span></span>

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

### <span data-ttu-id="c7b61-149">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="c7b61-149">-RetentionPolicyDays</span></span>
<span data-ttu-id="c7b61-150">Количество дней для сохранения записей журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="c7b61-150">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="c7b61-151">-StorageId</span><span class="sxs-lookup"><span data-stu-id="c7b61-151">-StorageId</span></span>
<span data-ttu-id="c7b61-152">ИД учетной записи хранения, которая используется для хранения журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="c7b61-152">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="c7b61-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="c7b61-153">-Tag</span></span>
<span data-ttu-id="c7b61-154">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="c7b61-154">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c7b61-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c7b61-155">-TargetResourceId</span></span>
<span data-ttu-id="c7b61-156">ИД группы безопасности сети, к которой будет применен журнал потоков.</span><span class="sxs-lookup"><span data-stu-id="c7b61-156">ID of network security group to which flow log will be applied.</span></span>

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

### <span data-ttu-id="c7b61-157">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="c7b61-157">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="c7b61-158">Интервал в минутах, который определяет, как часто служба tas должна делать анализ потока.</span><span class="sxs-lookup"><span data-stu-id="c7b61-158">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

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

### <span data-ttu-id="c7b61-159">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="c7b61-159">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="c7b61-160">ИД ресурса вложенной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c7b61-160">Resource Id of the attached workspace.</span></span>

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

### <span data-ttu-id="c7b61-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7b61-161">-Confirm</span></span>
<span data-ttu-id="c7b61-162">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c7b61-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7b61-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7b61-163">-WhatIf</span></span>
<span data-ttu-id="c7b61-164">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7b61-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7b61-165">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c7b61-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7b61-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7b61-166">CommonParameters</span></span>
<span data-ttu-id="c7b61-167">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7b61-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7b61-168">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7b61-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7b61-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7b61-169">INPUTS</span></span>

### <span data-ttu-id="c7b61-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7b61-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c7b61-171">System.String</span><span class="sxs-lookup"><span data-stu-id="c7b61-171">System.String</span></span>

### <span data-ttu-id="c7b61-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="c7b61-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="c7b61-173">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c7b61-173">OUTPUTS</span></span>

### <span data-ttu-id="c7b61-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="c7b61-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="c7b61-175">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c7b61-175">NOTES</span></span>

## <span data-ttu-id="c7b61-176">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7b61-176">RELATED LINKS</span></span>

[<span data-ttu-id="c7b61-177">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7b61-177">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c7b61-178">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7b61-178">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c7b61-179">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7b61-179">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c7b61-180">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c7b61-180">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c7b61-181">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c7b61-181">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c7b61-182">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c7b61-182">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c7b61-183">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c7b61-183">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c7b61-184">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7b61-184">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7b61-185">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c7b61-185">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c7b61-186">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7b61-186">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7b61-187">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7b61-187">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7b61-188">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7b61-188">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7b61-189">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7b61-189">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c7b61-190">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c7b61-190">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c7b61-191">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c7b61-191">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c7b61-192">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7b61-192">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7b61-193">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7b61-193">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7b61-194">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7b61-194">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7b61-195">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c7b61-195">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c7b61-196">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7b61-196">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7b61-197">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7b61-197">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7b61-198">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c7b61-198">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c7b61-199">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c7b61-199">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c7b61-200">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c7b61-200">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c7b61-201">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c7b61-201">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c7b61-202">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c7b61-202">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c7b61-203">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7b61-203">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7b61-204">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c7b61-204">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="c7b61-205">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c7b61-205">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="c7b61-206">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c7b61-206">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
