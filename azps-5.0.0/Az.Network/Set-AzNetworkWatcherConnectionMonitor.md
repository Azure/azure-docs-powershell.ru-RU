---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249190"
---
# <span data-ttu-id="80c8e-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="80c8e-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="80c8e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="80c8e-103">Обновляет ресурс монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="80c8e-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="80c8e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80c8e-104">SYNTAX</span></span>

### <span data-ttu-id="80c8e-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="80c8e-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80c8e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="80c8e-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80c8e-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="80c8e-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80c8e-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="80c8e-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80c8e-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="80c8e-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80c8e-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="80c8e-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80c8e-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="80c8e-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80c8e-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="80c8e-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80c8e-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="80c8e-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80c8e-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80c8e-114">DESCRIPTION</span></span>
<span data-ttu-id="80c8e-115">Командлет Set-AzNetworkWatcherConnectionMonitor обновляет ресурс монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="80c8e-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="80c8e-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80c8e-116">EXAMPLES</span></span>

### <span data-ttu-id="80c8e-117">Пример 1: обновление монитора подключений</span><span class="sxs-lookup"><span data-stu-id="80c8e-117">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="80c8e-118">В этом примере мы обновляем существующий монитор соединения, изменяя destinationAddress и добавляя Теги.</span><span class="sxs-lookup"><span data-stu-id="80c8e-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="80c8e-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80c8e-119">PARAMETERS</span></span>

### <span data-ttu-id="80c8e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80c8e-120">-AsJob</span></span>
<span data-ttu-id="80c8e-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="80c8e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80c8e-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="80c8e-122">-ConfigureOnly</span></span>
<span data-ttu-id="80c8e-123">Настройка монитора подключений, но не запуск</span><span class="sxs-lookup"><span data-stu-id="80c8e-123">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="80c8e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c8e-124">-DefaultProfile</span></span>
<span data-ttu-id="80c8e-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80c8e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80c8e-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="80c8e-126">-DestinationAddress</span></span>
<span data-ttu-id="80c8e-127">Адрес целевого монитора подключения (IP или доменное имя).</span><span class="sxs-lookup"><span data-stu-id="80c8e-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="80c8e-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="80c8e-128">-DestinationPort</span></span>
<span data-ttu-id="80c8e-129">Порт назначения, используемый монитором соединения.</span><span class="sxs-lookup"><span data-stu-id="80c8e-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="80c8e-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="80c8e-130">-DestinationResourceId</span></span>
<span data-ttu-id="80c8e-131">Идентификатор ресурса, используемого в качестве назначения монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="80c8e-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="80c8e-132">-Force</span><span class="sxs-lookup"><span data-stu-id="80c8e-132">-Force</span></span>
<span data-ttu-id="80c8e-133">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="80c8e-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="80c8e-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80c8e-134">-InputObject</span></span>
<span data-ttu-id="80c8e-135">Объект монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="80c8e-135">Connection monitor object.</span></span>

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

### <span data-ttu-id="80c8e-136">-Location</span><span class="sxs-lookup"><span data-stu-id="80c8e-136">-Location</span></span>
<span data-ttu-id="80c8e-137">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="80c8e-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="80c8e-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="80c8e-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="80c8e-139">Интервал наблюдения (в секундах).</span><span class="sxs-lookup"><span data-stu-id="80c8e-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="80c8e-140">Значение по умолчанию — 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="80c8e-140">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="80c8e-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="80c8e-141">-Name</span></span>
<span data-ttu-id="80c8e-142">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="80c8e-142">The connection monitor name.</span></span>

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

### <span data-ttu-id="80c8e-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="80c8e-143">-NetworkWatcher</span></span>
<span data-ttu-id="80c8e-144">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="80c8e-144">The network watcher resource.</span></span>

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

### <span data-ttu-id="80c8e-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="80c8e-145">-NetworkWatcherName</span></span>
<span data-ttu-id="80c8e-146">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="80c8e-146">The name of network watcher.</span></span>

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

### <span data-ttu-id="80c8e-147">-Примечание</span><span class="sxs-lookup"><span data-stu-id="80c8e-147">-Note</span></span>
<span data-ttu-id="80c8e-148">Заметки, связанные с монитором подключений.</span><span class="sxs-lookup"><span data-stu-id="80c8e-148">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="80c8e-149">-Output</span><span class="sxs-lookup"><span data-stu-id="80c8e-149">-Output</span></span>
<span data-ttu-id="80c8e-150">Описание пунктов назначения выходных данных монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="80c8e-150">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="80c8e-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80c8e-151">-ResourceGroupName</span></span>
<span data-ttu-id="80c8e-152">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="80c8e-152">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="80c8e-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80c8e-153">-ResourceId</span></span>
<span data-ttu-id="80c8e-154">Идентификатор ресурса ConnectionMonitor.</span><span class="sxs-lookup"><span data-stu-id="80c8e-154">ConnectionMonitor resource ID.</span></span>

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

### <span data-ttu-id="80c8e-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="80c8e-155">-SourcePort</span></span>
<span data-ttu-id="80c8e-156">Порт источника, используемый монитором соединения.</span><span class="sxs-lookup"><span data-stu-id="80c8e-156">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="80c8e-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="80c8e-157">-SourceResourceId</span></span>
<span data-ttu-id="80c8e-158">Идентификатор ресурса, используемого в качестве источника монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="80c8e-158">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="80c8e-159">-Тег</span><span class="sxs-lookup"><span data-stu-id="80c8e-159">-Tag</span></span>
<span data-ttu-id="80c8e-160">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80c8e-160">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="80c8e-161">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="80c8e-161">-TestGroup</span></span>
<span data-ttu-id="80c8e-162">Список групп тестов.</span><span class="sxs-lookup"><span data-stu-id="80c8e-162">The list of test groups.</span></span>

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

### <span data-ttu-id="80c8e-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80c8e-163">-Confirm</span></span>
<span data-ttu-id="80c8e-164">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="80c8e-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80c8e-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80c8e-165">-WhatIf</span></span>
<span data-ttu-id="80c8e-166">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="80c8e-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80c8e-167">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="80c8e-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80c8e-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c8e-168">CommonParameters</span></span>
<span data-ttu-id="80c8e-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80c8e-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c8e-170">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80c8e-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c8e-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80c8e-171">INPUTS</span></span>

### <span data-ttu-id="80c8e-172">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="80c8e-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="80c8e-173">System. String</span><span class="sxs-lookup"><span data-stu-id="80c8e-173">System.String</span></span>

### <span data-ttu-id="80c8e-174">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="80c8e-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="80c8e-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80c8e-175">OUTPUTS</span></span>

### <span data-ttu-id="80c8e-176">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="80c8e-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="80c8e-177">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="80c8e-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="80c8e-178">Пуск</span><span class="sxs-lookup"><span data-stu-id="80c8e-178">NOTES</span></span>

## <span data-ttu-id="80c8e-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80c8e-179">RELATED LINKS</span></span>