---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 2b6ad73e3a054ee01c2200ea47098fe3c3f206fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244771"
---
# <span data-ttu-id="3cf3e-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3cf3e-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="3cf3e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3cf3e-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf3e-103">Настраивает ведение журнала потока для целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="3cf3e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3cf3e-104">SYNTAX</span></span>

### <span data-ttu-id="3cf3e-105">SetFlowlogByResourceWithoutTA (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3cf3e-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf3e-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="3cf3e-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf3e-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="3cf3e-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cf3e-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="3cf3e-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf3e-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="3cf3e-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cf3e-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="3cf3e-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf3e-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="3cf3e-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cf3e-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="3cf3e-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf3e-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="3cf3e-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cf3e-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cf3e-114">DESCRIPTION</span></span>
<span data-ttu-id="3cf3e-115">Set-AzNetworkWatcherConfigFlowLog настраивает ведение журнала потока для целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="3cf3e-116">Свойства для настройки включают, включено ли ведение журнала потока для указанного ресурса, настроенной учетной записи хранения для отправки журналов, формата ведения журнала потока и политики хранения для журналов.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="3cf3e-117">Сетевые группы безопасности поддерживаются для ведения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="3cf3e-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3cf3e-118">EXAMPLES</span></span>

### <span data-ttu-id="3cf3e-119">Пример 1: Настройка ведения журнала потока для указанного NSG</span><span class="sxs-lookup"><span data-stu-id="3cf3e-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
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

<span data-ttu-id="3cf3e-120">В этом примере мы настраиваем состояние ведения журнала для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="3cf3e-121">В ответе мы видим, что в указанном NSG включено ведение журнала потока, формат по умолчанию, а политика хранения не задана.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="3cf3e-122">Пример 2: Настройка ведения журнала потока для указанной NSG и установка для функции ведения журнала потока значения 2.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
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

<span data-ttu-id="3cf3e-123">В этом примере мы настраиваем ведение журнала для потока в сетевой группе безопасности (NSG) с указанными журналами версии 2.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="3cf3e-124">В ответе мы видим, что в указанном NSG включено ведение журнала потока, задан формат и не настроена политика хранения.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="3cf3e-125">Если регион не поддерживает указанную вами версию, наблюдатель сети будет записывать поддерживаемую версию по умолчанию в регионе.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="3cf3e-126">Пример 3: Настройка ведения журнала потока и анализа трафика для указанной NSG</span><span class="sxs-lookup"><span data-stu-id="3cf3e-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
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

<span data-ttu-id="3cf3e-127">В этом примере мы настраиваем состояние ведения журнала и анализ трафика для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="3cf3e-128">В ответе мы видим, что в указанном NSG есть ведение журнала потока и включена аналитическая трафик, формат по умолчанию и политика хранения.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="3cf3e-129">Пример 4: Отключение анализа трафика для указанной NSG с ведением журнала и настройкой Analytics трафик</span><span class="sxs-lookup"><span data-stu-id="3cf3e-129">Example 4: Disable Traffic Analytics for a Specified NSG with Flow Logging and Traffic Analytics configured</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg
PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics:$false -Workspace $workspace

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
              "enabled": false,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
          "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="3cf3e-130">В этом примере мы отключили аналитический трафик для группы безопасности сети, в которой есть ведение журнала потока и анализ трафика, настроенный ранее.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-130">In this example we disable Traffic Analytics for a Network Security Group which has flow logging and Traffic Analytics configured earlier.</span></span> <span data-ttu-id="3cf3e-131">В ответе мы видим, что в указанном NSG включено ведение журнала потока, но анализ трафика отключен.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-131">In the response, we see the specified NSG has flow logging enabled but Traffic Analytics disabled.</span></span>

## <span data-ttu-id="3cf3e-132">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3cf3e-132">PARAMETERS</span></span>

### <span data-ttu-id="3cf3e-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cf3e-133">-AsJob</span></span>
<span data-ttu-id="3cf3e-134">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3cf3e-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cf3e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf3e-135">-DefaultProfile</span></span>
<span data-ttu-id="3cf3e-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cf3e-137">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="3cf3e-137">-EnableFlowLog</span></span>
<span data-ttu-id="3cf3e-138">Пометка для включения и отключения ведения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-138">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="3cf3e-139">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="3cf3e-139">-EnableRetention</span></span>
<span data-ttu-id="3cf3e-140">Пометка для включения и отключения хранения.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-140">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="3cf3e-141">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="3cf3e-141">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="3cf3e-142">Пометка для включения и отключения хранения.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-142">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="3cf3e-143">-FormatType</span><span class="sxs-lookup"><span data-stu-id="3cf3e-143">-FormatType</span></span>
<span data-ttu-id="3cf3e-144">Тип формата журнала потока.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-144">Type of flow log format.</span></span>

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

### <span data-ttu-id="3cf3e-145">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="3cf3e-145">-FormatVersion</span></span>
<span data-ttu-id="3cf3e-146">Версия формата журнала потока.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-146">Version of flow log format.</span></span>

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

### <span data-ttu-id="3cf3e-147">-Location</span><span class="sxs-lookup"><span data-stu-id="3cf3e-147">-Location</span></span>
<span data-ttu-id="3cf3e-148">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-148">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3cf3e-149">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3cf3e-149">-NetworkWatcher</span></span>
<span data-ttu-id="3cf3e-150">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-150">The network watcher resource.</span></span>

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

### <span data-ttu-id="3cf3e-151">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3cf3e-151">-NetworkWatcherName</span></span>
<span data-ttu-id="3cf3e-152">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-152">The name of network watcher.</span></span>

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

### <span data-ttu-id="3cf3e-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf3e-153">-ResourceGroupName</span></span>
<span data-ttu-id="3cf3e-154">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-154">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3cf3e-155">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="3cf3e-155">-RetentionInDays</span></span>
<span data-ttu-id="3cf3e-156">Количество дней для хранения записей журнала потока.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-156">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="3cf3e-157">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3cf3e-157">-StorageAccountId</span></span>
<span data-ttu-id="3cf3e-158">Идентификатор учетной записи хранения, которая используется для хранения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-158">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="3cf3e-159">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="3cf3e-159">-TargetResourceId</span></span>
<span data-ttu-id="3cf3e-160">Идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-160">The target resource ID.</span></span>

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

### <span data-ttu-id="3cf3e-161">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="3cf3e-161">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="3cf3e-162">Возвращает или задает интервал (в минутах), который может решить, как часто служба TA должна выполнять анализ потока.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-162">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span>

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

### <span data-ttu-id="3cf3e-163">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="3cf3e-163">-Workspace</span></span>
<span data-ttu-id="3cf3e-164">Объект WS, который используется для хранения данных аналитического трафика.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-164">The WS object which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="3cf3e-165">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="3cf3e-165">-WorkspaceGUID</span></span>
<span data-ttu-id="3cf3e-166">GUID элемента WS, который используется для хранения данных аналитического трафика.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-166">GUID of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="3cf3e-167">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="3cf3e-167">-WorkspaceLocation</span></span>
<span data-ttu-id="3cf3e-168">Регион Azure в службе WS, которая используется для хранения данных анализа трафика.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-168">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="3cf3e-169">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="3cf3e-169">-WorkspaceResourceId</span></span>
<span data-ttu-id="3cf3e-170">Подписка на протокол WS, которая используется для хранения данных анализа трафика.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-170">Subscription of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="3cf3e-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cf3e-171">-Confirm</span></span>
<span data-ttu-id="3cf3e-172">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cf3e-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf3e-173">-WhatIf</span></span>
<span data-ttu-id="3cf3e-174">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cf3e-175">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cf3e-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf3e-176">CommonParameters</span></span>
<span data-ttu-id="3cf3e-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3cf3e-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf3e-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cf3e-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf3e-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3cf3e-179">INPUTS</span></span>

### <span data-ttu-id="3cf3e-180">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3cf3e-180">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3cf3e-181">System. String</span><span class="sxs-lookup"><span data-stu-id="3cf3e-181">System.String</span></span>

### <span data-ttu-id="3cf3e-182">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3cf3e-182">System.Boolean</span></span>

### <span data-ttu-id="3cf3e-183">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3cf3e-183">System.Int32</span></span>

### <span data-ttu-id="3cf3e-184">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3cf3e-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3cf3e-185">Microsoft. Azure. Management. internal. Network. Common. IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="3cf3e-185">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="3cf3e-186">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cf3e-186">OUTPUTS</span></span>

### <span data-ttu-id="3cf3e-187">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="3cf3e-187">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="3cf3e-188">Пуск</span><span class="sxs-lookup"><span data-stu-id="3cf3e-188">NOTES</span></span>
<span data-ttu-id="3cf3e-189">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель, поток, журналы, flowlog, ведение журнала</span><span class="sxs-lookup"><span data-stu-id="3cf3e-189">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="3cf3e-190">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3cf3e-190">RELATED LINKS</span></span>

[<span data-ttu-id="3cf3e-191">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3cf3e-191">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3cf3e-192">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3cf3e-192">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3cf3e-193">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3cf3e-193">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3cf3e-194">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3cf3e-194">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3cf3e-195">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3cf3e-195">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3cf3e-196">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3cf3e-196">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3cf3e-197">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3cf3e-197">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3cf3e-198">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3cf3e-198">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3cf3e-199">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3cf3e-199">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3cf3e-200">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3cf3e-200">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3cf3e-201">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3cf3e-201">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3cf3e-202">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3cf3e-202">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3cf3e-203">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3cf3e-203">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3cf3e-204">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3cf3e-204">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3cf3e-205">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3cf3e-205">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="3cf3e-206">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3cf3e-206">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3cf3e-207">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3cf3e-207">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3cf3e-208">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3cf3e-208">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3cf3e-209">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3cf3e-209">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3cf3e-210">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3cf3e-210">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3cf3e-211">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3cf3e-211">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3cf3e-212">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3cf3e-212">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3cf3e-213">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3cf3e-213">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3cf3e-214">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3cf3e-214">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3cf3e-215">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3cf3e-215">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3cf3e-216">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3cf3e-216">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="3cf3e-217">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3cf3e-217">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
