---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 20d59fb2a112b32c95b380c114ebc1b365569235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560852"
---
# <span data-ttu-id="be4ad-101">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="be4ad-101">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="be4ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be4ad-102">SYNOPSIS</span></span>
<span data-ttu-id="be4ad-103">Настраивает ведение журнала потока для целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="be4ad-103">Configures flow logging for a target resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be4ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be4ad-104">SYNTAX</span></span>

### <span data-ttu-id="be4ad-105">SetFlowlogByResourceWithoutTA (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="be4ad-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be4ad-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="be4ad-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be4ad-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="be4ad-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String> -WorkspaceGUID <String>
 -WorkspaceLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be4ad-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="be4ad-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be4ad-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="be4ad-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be4ad-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="be4ad-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be4ad-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="be4ad-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-AsJob]
 [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be4ad-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="be4ad-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-AsJob]
 [-EnableTrafficAnalytics] -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be4ad-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="be4ad-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be4ad-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be4ad-114">DESCRIPTION</span></span>
<span data-ttu-id="be4ad-115">Set-AzureRmNetworkWatcherConfigFlowLog настраивает ведение журнала потока для целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="be4ad-115">The Set-AzureRmNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="be4ad-116">Свойства для настройки включают, включено ли ведение журнала потока для указанного ресурса, настроенной учетной записи хранения для отправки журналов и политики хранения для журналов.</span><span class="sxs-lookup"><span data-stu-id="be4ad-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="be4ad-117">Сетевые группы безопасности поддерживаются для ведения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="be4ad-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="be4ad-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be4ad-118">EXAMPLES</span></span>

### <span data-ttu-id="be4ad-119">Пример 1: Настройка ведения журнала потока для указанного NSG</span><span class="sxs-lookup"><span data-stu-id="be4ad-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="be4ad-120">В этом примере мы настраиваем состояние ведения журнала для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="be4ad-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="be4ad-121">В ответе мы видим, что в указанном NSG включено ведение журнала потока, а политика хранения не задана.</span><span class="sxs-lookup"><span data-stu-id="be4ad-121">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

### <span data-ttu-id="be4ad-122">Пример 2: Настройка ведения журнала потока и анализа трафика для указанной NSG</span><span class="sxs-lookup"><span data-stu-id="be4ad-122">Example 2: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzureRmOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg


PS C:\> Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName"
            }
          }
```

<span data-ttu-id="be4ad-123">В этом примере мы настраиваем состояние ведения журнала и анализ трафика для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="be4ad-123">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="be4ad-124">В ответе мы видим, что в указанном NSG есть ведение журнала потока и включена аналитическая трафик, и не задана политика хранения.</span><span class="sxs-lookup"><span data-stu-id="be4ad-124">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, and no retention policy set.</span></span>

## <span data-ttu-id="be4ad-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be4ad-125">PARAMETERS</span></span>

### <span data-ttu-id="be4ad-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be4ad-126">-AsJob</span></span>
<span data-ttu-id="be4ad-127">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="be4ad-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="be4ad-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be4ad-128">-DefaultProfile</span></span>
<span data-ttu-id="be4ad-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be4ad-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be4ad-130">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="be4ad-130">-EnableFlowLog</span></span>
<span data-ttu-id="be4ad-131">Пометка для включения и отключения ведения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="be4ad-131">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="be4ad-132">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="be4ad-132">-EnableRetention</span></span>
<span data-ttu-id="be4ad-133">Пометка для включения и отключения хранения.</span><span class="sxs-lookup"><span data-stu-id="be4ad-133">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="be4ad-134">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="be4ad-134">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="be4ad-135">Пометка для включения и отключения хранения.</span><span class="sxs-lookup"><span data-stu-id="be4ad-135">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="be4ad-136">-Location</span><span class="sxs-lookup"><span data-stu-id="be4ad-136">-Location</span></span>
<span data-ttu-id="be4ad-137">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="be4ad-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="be4ad-138">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="be4ad-138">-NetworkWatcher</span></span>
<span data-ttu-id="be4ad-139">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="be4ad-139">The network watcher resource.</span></span>

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

### <span data-ttu-id="be4ad-140">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="be4ad-140">-NetworkWatcherName</span></span>
<span data-ttu-id="be4ad-141">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="be4ad-141">The name of network watcher.</span></span>

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

### <span data-ttu-id="be4ad-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be4ad-142">-ResourceGroupName</span></span>
<span data-ttu-id="be4ad-143">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="be4ad-143">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="be4ad-144">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="be4ad-144">-RetentionInDays</span></span>
<span data-ttu-id="be4ad-145">Количество дней для хранения записей журнала потока.</span><span class="sxs-lookup"><span data-stu-id="be4ad-145">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="be4ad-146">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="be4ad-146">-StorageAccountId</span></span>
<span data-ttu-id="be4ad-147">Идентификатор учетной записи хранения, которая используется для хранения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="be4ad-147">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="be4ad-148">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="be4ad-148">-TargetResourceId</span></span>
<span data-ttu-id="be4ad-149">Идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="be4ad-149">The target resource ID.</span></span>

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

### <span data-ttu-id="be4ad-150">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="be4ad-150">-Workspace</span></span>
<span data-ttu-id="be4ad-151">Объект WS, который используется для хранения данных аналитического трафика.</span><span class="sxs-lookup"><span data-stu-id="be4ad-151">The WS object which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="be4ad-152">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="be4ad-152">-WorkspaceGUID</span></span>
<span data-ttu-id="be4ad-153">GUID элемента WS, который используется для хранения данных аналитического трафика.</span><span class="sxs-lookup"><span data-stu-id="be4ad-153">GUID of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="be4ad-154">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="be4ad-154">-WorkspaceLocation</span></span>
<span data-ttu-id="be4ad-155">Регион Azure в службе WS, которая используется для хранения данных анализа трафика.</span><span class="sxs-lookup"><span data-stu-id="be4ad-155">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="be4ad-156">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="be4ad-156">-WorkspaceResourceId</span></span>
<span data-ttu-id="be4ad-157">Подписка на протокол WS, которая используется для хранения данных анализа трафика.</span><span class="sxs-lookup"><span data-stu-id="be4ad-157">Subscription of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="be4ad-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be4ad-158">-Confirm</span></span>
<span data-ttu-id="be4ad-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be4ad-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be4ad-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be4ad-160">-WhatIf</span></span>
<span data-ttu-id="be4ad-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be4ad-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be4ad-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be4ad-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be4ad-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be4ad-163">CommonParameters</span></span>
<span data-ttu-id="be4ad-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be4ad-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be4ad-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be4ad-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be4ad-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be4ad-166">INPUTS</span></span>

### <span data-ttu-id="be4ad-167">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="be4ad-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="be4ad-168">Параметры: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="be4ad-168">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="be4ad-169">System. String</span><span class="sxs-lookup"><span data-stu-id="be4ad-169">System.String</span></span>
<span data-ttu-id="be4ad-170">Параметры: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="be4ad-170">Parameters: NetworkWatcherName (ByValue)</span></span>

### <span data-ttu-id="be4ad-171">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="be4ad-171">System.Boolean</span></span>

### <span data-ttu-id="be4ad-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="be4ad-172">System.Int32</span></span>

### <span data-ttu-id="be4ad-173">Microsoft. Azure. Management. internal. Network. Common. IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="be4ad-173">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="be4ad-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be4ad-174">OUTPUTS</span></span>

### <span data-ttu-id="be4ad-175">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="be4ad-175">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="be4ad-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="be4ad-176">NOTES</span></span>
<span data-ttu-id="be4ad-177">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель, поток, журналы, flowlog, ведение журнала</span><span class="sxs-lookup"><span data-stu-id="be4ad-177">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="be4ad-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be4ad-178">RELATED LINKS</span></span>

[<span data-ttu-id="be4ad-179">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="be4ad-179">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="be4ad-180">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="be4ad-180">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="be4ad-181">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="be4ad-181">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="be4ad-182">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="be4ad-182">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="be4ad-183">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="be4ad-183">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="be4ad-184">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="be4ad-184">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="be4ad-185">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="be4ad-185">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="be4ad-186">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="be4ad-186">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="be4ad-187">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="be4ad-187">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="be4ad-188">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="be4ad-188">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="be4ad-189">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="be4ad-189">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="be4ad-190">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="be4ad-190">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="be4ad-191">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="be4ad-191">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="be4ad-192">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="be4ad-192">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="be4ad-193">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="be4ad-193">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="be4ad-194">Остановить-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="be4ad-194">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="be4ad-195">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="be4ad-195">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="be4ad-196">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="be4ad-196">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="be4ad-197">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="be4ad-197">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="be4ad-198">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="be4ad-198">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="be4ad-199">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="be4ad-199">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="be4ad-200">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="be4ad-200">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="be4ad-201">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="be4ad-201">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="be4ad-202">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="be4ad-202">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="be4ad-203">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="be4ad-203">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="be4ad-204">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="be4ad-204">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="be4ad-205">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="be4ad-205">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
