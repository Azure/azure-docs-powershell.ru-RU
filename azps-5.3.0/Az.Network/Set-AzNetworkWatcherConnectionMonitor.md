---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517934"
---
# <span data-ttu-id="4be8f-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4be8f-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="4be8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4be8f-102">SYNOPSIS</span></span>
<span data-ttu-id="4be8f-103">Обновляет подключение к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="4be8f-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="4be8f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4be8f-104">SYNTAX</span></span>

### <span data-ttu-id="4be8f-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4be8f-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4be8f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4be8f-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4be8f-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="4be8f-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4be8f-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="4be8f-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4be8f-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4be8f-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4be8f-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="4be8f-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4be8f-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4be8f-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4be8f-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="4be8f-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4be8f-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="4be8f-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4be8f-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4be8f-114">DESCRIPTION</span></span>
<span data-ttu-id="4be8f-115">Для Set-AzNetworkWatcherConnectionMonitor ресурса обновляется подключение.</span><span class="sxs-lookup"><span data-stu-id="4be8f-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="4be8f-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4be8f-116">EXAMPLES</span></span>

### <span data-ttu-id="4be8f-117">Пример 1. Обновление монитора подключения</span><span class="sxs-lookup"><span data-stu-id="4be8f-117">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm
-DestinationAddress google.com -DestinationPort 80 -Tag @{"key1" = "value1"}

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"5b2b20e8-0ce0-417e-9607-76208149bb67"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMach
                                ines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="4be8f-118">В этом примере мы обновляем существующий монитор подключения, изменяя destinationAddress и добавляя теги.</span><span class="sxs-lookup"><span data-stu-id="4be8f-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="4be8f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4be8f-119">PARAMETERS</span></span>

### <span data-ttu-id="4be8f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4be8f-120">-AsJob</span></span>
<span data-ttu-id="4be8f-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4be8f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4be8f-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="4be8f-122">-ConfigureOnly</span></span>
<span data-ttu-id="4be8f-123">Настройка монитора подключения без его запуска</span><span class="sxs-lookup"><span data-stu-id="4be8f-123">Configure connection monitor, but do not start it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4be8f-124">-DefaultProfile</span></span>
<span data-ttu-id="4be8f-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4be8f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4be8f-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="4be8f-126">-DestinationAddress</span></span>
<span data-ttu-id="4be8f-127">Адрес назначения монитора подключения (IP или доменное имя).</span><span class="sxs-lookup"><span data-stu-id="4be8f-127">Address of the connection monitor destination (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="4be8f-128">-DestinationPort</span></span>
<span data-ttu-id="4be8f-129">Порт назначения, используемый монитором подключения.</span><span class="sxs-lookup"><span data-stu-id="4be8f-129">The destination port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="4be8f-130">-DestinationResourceId</span></span>
<span data-ttu-id="4be8f-131">ИД ресурса, используемого в качестве назначения с помощью монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="4be8f-131">The ID of the resource used as the destination by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-132">-Force</span><span class="sxs-lookup"><span data-stu-id="4be8f-132">-Force</span></span>
<span data-ttu-id="4be8f-133">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="4be8f-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4be8f-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4be8f-134">-InputObject</span></span>
<span data-ttu-id="4be8f-135">Объект монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="4be8f-135">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-136">-Location</span><span class="sxs-lookup"><span data-stu-id="4be8f-136">-Location</span></span>
<span data-ttu-id="4be8f-137">Расположение сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="4be8f-137">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation, SetByLocationV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="4be8f-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="4be8f-139">Интервал наблюдения за интервалом в секундах.</span><span class="sxs-lookup"><span data-stu-id="4be8f-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="4be8f-140">Значение по умолчанию — 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="4be8f-140">Default value is 60 seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-141">-Name</span><span class="sxs-lookup"><span data-stu-id="4be8f-141">-Name</span></span>
<span data-ttu-id="4be8f-142">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="4be8f-142">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4be8f-143">-NetworkWatcher</span></span>
<span data-ttu-id="4be8f-144">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="4be8f-144">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4be8f-145">-NetworkWatcherName</span></span>
<span data-ttu-id="4be8f-146">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="4be8f-146">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-147">-Note</span><span class="sxs-lookup"><span data-stu-id="4be8f-147">-Note</span></span>
<span data-ttu-id="4be8f-148">Заметки, связанные с монитором подключения.</span><span class="sxs-lookup"><span data-stu-id="4be8f-148">Notes associated with connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-149">-Output</span><span class="sxs-lookup"><span data-stu-id="4be8f-149">-Output</span></span>
<span data-ttu-id="4be8f-150">В статье описаны назначения выходных данных монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="4be8f-150">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4be8f-151">-ResourceGroupName</span></span>
<span data-ttu-id="4be8f-152">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="4be8f-152">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4be8f-153">-ResourceId</span></span>
<span data-ttu-id="4be8f-154">ИД ресурса ConnectionMonitor.</span><span class="sxs-lookup"><span data-stu-id="4be8f-154">ConnectionMonitor resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="4be8f-155">-SourcePort</span></span>
<span data-ttu-id="4be8f-156">Исходный порт, используемый монитором подключения.</span><span class="sxs-lookup"><span data-stu-id="4be8f-156">The source port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="4be8f-157">-SourceResourceId</span></span>
<span data-ttu-id="4be8f-158">Код ресурса, используемого в качестве источника монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="4be8f-158">The ID of the resource used as the source by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="4be8f-159">-Tag</span></span>
<span data-ttu-id="4be8f-160">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="4be8f-160">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-161">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="4be8f-161">-TestGroup</span></span>
<span data-ttu-id="4be8f-162">Список тестовых групп.</span><span class="sxs-lookup"><span data-stu-id="4be8f-162">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4be8f-163">-Confirm</span></span>
<span data-ttu-id="4be8f-164">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4be8f-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4be8f-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4be8f-165">-WhatIf</span></span>
<span data-ttu-id="4be8f-166">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4be8f-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4be8f-167">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4be8f-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4be8f-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be8f-168">CommonParameters</span></span>
<span data-ttu-id="4be8f-169">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4be8f-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be8f-170">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4be8f-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be8f-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4be8f-171">INPUTS</span></span>

### <span data-ttu-id="4be8f-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4be8f-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="4be8f-173">System.String</span><span class="sxs-lookup"><span data-stu-id="4be8f-173">System.String</span></span>

### <span data-ttu-id="4be8f-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="4be8f-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="4be8f-175">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4be8f-175">OUTPUTS</span></span>

### <span data-ttu-id="4be8f-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="4be8f-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="4be8f-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="4be8f-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="4be8f-178">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4be8f-178">NOTES</span></span>

## <span data-ttu-id="4be8f-179">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4be8f-179">RELATED LINKS</span></span>
