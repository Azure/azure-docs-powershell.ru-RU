---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 55e98b23f4da1adf641bcf2a3ce7ced95cf5befd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402683"
---
# <span data-ttu-id="34ea6-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="34ea6-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="34ea6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="34ea6-103">Настраивает ведение журнала потоков для целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="34ea6-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="34ea6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="34ea6-104">SYNTAX</span></span>

### <span data-ttu-id="34ea6-105">SetFlowlogByResourceWithoutTA (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="34ea6-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34ea6-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="34ea6-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34ea6-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="34ea6-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34ea6-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="34ea6-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34ea6-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="34ea6-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34ea6-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="34ea6-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34ea6-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="34ea6-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34ea6-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="34ea6-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34ea6-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="34ea6-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34ea6-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34ea6-114">DESCRIPTION</span></span>
<span data-ttu-id="34ea6-115">В Set-AzNetworkWatcherConfigFlowLog настраивается ведение журнала потоков для целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="34ea6-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="34ea6-116">Настраиваемые свойства включают в себя: включено ли ведение журнала потоков для предоставленного ресурса, настроенная учетная запись хранения для отправки журналов, формат ведения журнала потоков и политика хранения журналов.</span><span class="sxs-lookup"><span data-stu-id="34ea6-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="34ea6-117">В настоящее время сетевые группы безопасности поддерживают ведение журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="34ea6-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="34ea6-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="34ea6-118">EXAMPLES</span></span>

### <span data-ttu-id="34ea6-119">Пример 1. Настройка ведения журнала потока для указанного NSG</span><span class="sxs-lookup"><span data-stu-id="34ea6-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
```

<span data-ttu-id="34ea6-120">В этом примере мы настроим состояние ведения журнала потоков для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="34ea6-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="34ea6-121">В ответе мы видим, что в NSG включено ведение журнала потоков, формат по умолчанию, а политика хранения не настроена.</span><span class="sxs-lookup"><span data-stu-id="34ea6-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="34ea6-122">Пример 2. Настройте ведение журнала потока для указанного NSG-журнала и установите для версии ведения журнала потоков 2.</span><span class="sxs-lookup"><span data-stu-id="34ea6-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -FormatVersion 2

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 2
                   }
```

<span data-ttu-id="34ea6-123">В этом примере мы настраиваем ведение журнала потока в группе безопасности сети (NSG) с помощью журналов версии 2.</span><span class="sxs-lookup"><span data-stu-id="34ea6-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="34ea6-124">В ответе мы видим, что в NSG включено ведение журнала потоков, задан формат и политика хранения не настроена.</span><span class="sxs-lookup"><span data-stu-id="34ea6-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="34ea6-125">Если регион не поддерживает указанную версию, Network Watcher напишет в нем поддерживаемую по умолчанию версию.</span><span class="sxs-lookup"><span data-stu-id="34ea6-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="34ea6-126">Пример 3. Настройка журнала потоков и аналитики трафика для указанного NSG</span><span class="sxs-lookup"><span data-stu-id="34ea6-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="34ea6-127">В этом примере мы настроим состояние ведения журнала потоков и аналитику трафика для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="34ea6-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="34ea6-128">В ответе мы видим, что в NSG включено ведение журнала потоков и включена аналитика трафика, формат по умолчанию, а политика хранения не настроена.</span><span class="sxs-lookup"><span data-stu-id="34ea6-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

## <span data-ttu-id="34ea6-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34ea6-129">PARAMETERS</span></span>

### <span data-ttu-id="34ea6-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34ea6-130">-AsJob</span></span>
<span data-ttu-id="34ea6-131">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="34ea6-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34ea6-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ea6-132">-DefaultProfile</span></span>
<span data-ttu-id="34ea6-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34ea6-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-134">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="34ea6-134">-EnableFlowLog</span></span>
<span data-ttu-id="34ea6-135">Пометить, чтобы включить или отключить ведение журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="34ea6-135">Flag to enable/disable flow logging.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-136">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="34ea6-136">-EnableRetention</span></span>
<span data-ttu-id="34ea6-137">Пометить, чтобы включить или отключить хранение.</span><span class="sxs-lookup"><span data-stu-id="34ea6-137">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-138">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="34ea6-138">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="34ea6-139">Пометить, чтобы включить или отключить хранение.</span><span class="sxs-lookup"><span data-stu-id="34ea6-139">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases: EnableTA

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-140">-FormatType</span><span class="sxs-lookup"><span data-stu-id="34ea6-140">-FormatType</span></span>
<span data-ttu-id="34ea6-141">Тип формата журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="34ea6-141">Type of flow log format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-142">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="34ea6-142">-FormatVersion</span></span>
<span data-ttu-id="34ea6-143">Версия формата журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="34ea6-143">Version of flow log format.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-144">-Location</span><span class="sxs-lookup"><span data-stu-id="34ea6-144">-Location</span></span>
<span data-ttu-id="34ea6-145">Расположение сетевого просмотра.</span><span class="sxs-lookup"><span data-stu-id="34ea6-145">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails, SetFlowlogByLocationWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-146">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="34ea6-146">-NetworkWatcher</span></span>
<span data-ttu-id="34ea6-147">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="34ea6-147">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetFlowlogByResourceWithoutTA, SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-148">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="34ea6-148">-NetworkWatcherName</span></span>
<span data-ttu-id="34ea6-149">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="34ea6-149">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34ea6-150">-ResourceGroupName</span></span>
<span data-ttu-id="34ea6-151">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="34ea6-151">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="34ea6-152">-RetentionInDays</span></span>
<span data-ttu-id="34ea6-153">Количество дней для сохранения записей журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="34ea6-153">Number of days to retain flow log records.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="34ea6-154">-StorageAccountId</span></span>
<span data-ttu-id="34ea6-155">ИД учетной записи хранения, которая используется для хранения журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="34ea6-155">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-156">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="34ea6-156">-TargetResourceId</span></span>
<span data-ttu-id="34ea6-157">ИД целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="34ea6-157">The target resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-158">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="34ea6-158">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="34ea6-159">Возвращает или задает интервал (в минутах), который определяет, как часто служба tas должна делать аналитические данные.</span><span class="sxs-lookup"><span data-stu-id="34ea6-159">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-160">-Workspace</span><span class="sxs-lookup"><span data-stu-id="34ea6-160">-Workspace</span></span>
<span data-ttu-id="34ea6-161">Объект WS, который используется для хранения аналитических данных о трафике.</span><span class="sxs-lookup"><span data-stu-id="34ea6-161">The WS object which is used to store the traffic analytics data.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByResourceWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByLocationWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-162">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="34ea6-162">-WorkspaceGUID</span></span>
<span data-ttu-id="34ea6-163">GUID WS, используемого для хранения данных аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="34ea6-163">GUID of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-164">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="34ea6-164">-WorkspaceLocation</span></span>
<span data-ttu-id="34ea6-165">Регион Azure службы WS, которая используется для хранения данных аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="34ea6-165">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-166">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="34ea6-166">-WorkspaceResourceId</span></span>
<span data-ttu-id="34ea6-167">Подписка на службу WS, которая используется для хранения аналитических данных о трафике.</span><span class="sxs-lookup"><span data-stu-id="34ea6-167">Subscription of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea6-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34ea6-168">-Confirm</span></span>
<span data-ttu-id="34ea6-169">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="34ea6-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34ea6-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34ea6-170">-WhatIf</span></span>
<span data-ttu-id="34ea6-171">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34ea6-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34ea6-172">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="34ea6-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34ea6-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ea6-173">CommonParameters</span></span>
<span data-ttu-id="34ea6-174">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34ea6-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ea6-175">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34ea6-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ea6-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34ea6-176">INPUTS</span></span>

### <span data-ttu-id="34ea6-177">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="34ea6-177">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="34ea6-178">System.String</span><span class="sxs-lookup"><span data-stu-id="34ea6-178">System.String</span></span>

### <span data-ttu-id="34ea6-179">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="34ea6-179">System.Boolean</span></span>

### <span data-ttu-id="34ea6-180">System.Int32</span><span class="sxs-lookup"><span data-stu-id="34ea6-180">System.Int32</span></span>

### <span data-ttu-id="34ea6-181">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="34ea6-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="34ea6-182">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="34ea6-182">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="34ea6-183">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="34ea6-183">OUTPUTS</span></span>

### <span data-ttu-id="34ea6-184">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="34ea6-184">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="34ea6-185">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="34ea6-185">NOTES</span></span>
<span data-ttu-id="34ea6-186">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking, networking, watcher, flow, logs, flowlog, logging</span><span class="sxs-lookup"><span data-stu-id="34ea6-186">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="34ea6-187">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34ea6-187">RELATED LINKS</span></span>

[<span data-ttu-id="34ea6-188">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="34ea6-188">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="34ea6-189">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="34ea6-189">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="34ea6-190">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="34ea6-190">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="34ea6-191">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="34ea6-191">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="34ea6-192">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="34ea6-192">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="34ea6-193">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="34ea6-193">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="34ea6-194">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="34ea6-194">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="34ea6-195">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="34ea6-195">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="34ea6-196">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="34ea6-196">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="34ea6-197">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="34ea6-197">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="34ea6-198">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="34ea6-198">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="34ea6-199">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="34ea6-199">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="34ea6-200">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="34ea6-200">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="34ea6-201">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="34ea6-201">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="34ea6-202">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="34ea6-202">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="34ea6-203">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="34ea6-203">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="34ea6-204">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="34ea6-204">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="34ea6-205">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="34ea6-205">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="34ea6-206">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="34ea6-206">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="34ea6-207">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="34ea6-207">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="34ea6-208">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="34ea6-208">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="34ea6-209">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="34ea6-209">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="34ea6-210">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="34ea6-210">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="34ea6-211">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="34ea6-211">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="34ea6-212">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="34ea6-212">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="34ea6-213">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="34ea6-213">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="34ea6-214">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="34ea6-214">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
