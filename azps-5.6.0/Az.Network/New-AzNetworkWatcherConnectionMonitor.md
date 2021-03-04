---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 18db8d01bd9c6c54b1fdf3957f25e12848e309ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958536"
---
# <span data-ttu-id="7594d-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7594d-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="7594d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7594d-102">SYNOPSIS</span></span>
<span data-ttu-id="7594d-103">Создает ресурс монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="7594d-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="7594d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7594d-104">SYNTAX</span></span>

### <span data-ttu-id="7594d-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7594d-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7594d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7594d-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7594d-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="7594d-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7594d-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="7594d-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7594d-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7594d-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7594d-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="7594d-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7594d-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="7594d-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7594d-112">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7594d-112">DESCRIPTION</span></span>
<span data-ttu-id="7594d-113">С New-AzNetworkWatcherConnectionMonitor создается ресурс монитора подключения для указанного источника и назначения (монитор подключения SingleSourcedestination) или группы тестирования (MultiEndpointConnectionMonitor).</span><span class="sxs-lookup"><span data-stu-id="7594d-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="7594d-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7594d-114">EXAMPLES</span></span>

### <span data-ttu-id="7594d-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7594d-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="7594d-116">Name : cm Id : /subscriptions/00000000-0000-0000-0000-0000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState : Succeeded Source: { "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft . Compute/virtualMaоes/vm", "Port": 0 } Destination: { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart : True StartTime : 12.01.2018 7:13:11 MonitoringStatus : Running Location : centraluseuap Type : Microsoft.Network/networkWatchers/connectionMonitors Tags: {}</span><span class="sxs-lookup"><span data-stu-id="7594d-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="7594d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7594d-117">PARAMETERS</span></span>

### <span data-ttu-id="7594d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7594d-118">-AsJob</span></span>
<span data-ttu-id="7594d-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7594d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7594d-120">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="7594d-120">-ConfigureOnly</span></span>
<span data-ttu-id="7594d-121">Настройка монитора подключения без его запуска</span><span class="sxs-lookup"><span data-stu-id="7594d-121">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="7594d-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7594d-122">-ConnectionMonitor</span></span>
<span data-ttu-id="7594d-123">Объект монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="7594d-123">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject
Parameter Sets: SetByConnectionMonitorV2Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7594d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7594d-124">-DefaultProfile</span></span>
<span data-ttu-id="7594d-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7594d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7594d-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="7594d-126">-DestinationAddress</span></span>
<span data-ttu-id="7594d-127">Адрес назначения монитора подключения (IP или доменное имя).</span><span class="sxs-lookup"><span data-stu-id="7594d-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="7594d-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="7594d-128">-DestinationPort</span></span>
<span data-ttu-id="7594d-129">Порт назначения, используемый монитором подключения.</span><span class="sxs-lookup"><span data-stu-id="7594d-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="7594d-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="7594d-130">-DestinationResourceId</span></span>
<span data-ttu-id="7594d-131">ИД ресурса, используемого в качестве назначения с помощью монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="7594d-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="7594d-132">-Force</span><span class="sxs-lookup"><span data-stu-id="7594d-132">-Force</span></span>
<span data-ttu-id="7594d-133">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="7594d-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7594d-134">-Location</span><span class="sxs-lookup"><span data-stu-id="7594d-134">-Location</span></span>
<span data-ttu-id="7594d-135">Расположение сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="7594d-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7594d-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="7594d-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="7594d-137">Интервал наблюдения за секундами.</span><span class="sxs-lookup"><span data-stu-id="7594d-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="7594d-138">Значение по умолчанию — 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="7594d-138">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="7594d-139">-Name</span><span class="sxs-lookup"><span data-stu-id="7594d-139">-Name</span></span>
<span data-ttu-id="7594d-140">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="7594d-140">The connection monitor name.</span></span>

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

### <span data-ttu-id="7594d-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7594d-141">-NetworkWatcher</span></span>
<span data-ttu-id="7594d-142">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="7594d-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="7594d-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7594d-143">-NetworkWatcherName</span></span>
<span data-ttu-id="7594d-144">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="7594d-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="7594d-145">-Note</span><span class="sxs-lookup"><span data-stu-id="7594d-145">-Note</span></span>
<span data-ttu-id="7594d-146">Заметки, связанные с монитором подключения.</span><span class="sxs-lookup"><span data-stu-id="7594d-146">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="7594d-147">-Output</span><span class="sxs-lookup"><span data-stu-id="7594d-147">-Output</span></span>
<span data-ttu-id="7594d-148">В статье описаны назначения выходных данных монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="7594d-148">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="7594d-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7594d-149">-ResourceGroupName</span></span>
<span data-ttu-id="7594d-150">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="7594d-150">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7594d-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="7594d-151">-SourcePort</span></span>
<span data-ttu-id="7594d-152">Исходный порт, используемый монитором подключения.</span><span class="sxs-lookup"><span data-stu-id="7594d-152">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="7594d-153">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="7594d-153">-SourceResourceId</span></span>
<span data-ttu-id="7594d-154">Код ресурса, используемого в качестве источника монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="7594d-154">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="7594d-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="7594d-155">-Tag</span></span>
<span data-ttu-id="7594d-156">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="7594d-156">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7594d-157">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="7594d-157">-TestGroup</span></span>
<span data-ttu-id="7594d-158">Список тестовых групп.</span><span class="sxs-lookup"><span data-stu-id="7594d-158">The list of test groups.</span></span>

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

### <span data-ttu-id="7594d-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7594d-159">-Confirm</span></span>
<span data-ttu-id="7594d-160">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7594d-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7594d-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7594d-161">-WhatIf</span></span>
<span data-ttu-id="7594d-162">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7594d-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7594d-163">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7594d-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7594d-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7594d-164">CommonParameters</span></span>
<span data-ttu-id="7594d-165">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7594d-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7594d-166">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7594d-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7594d-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7594d-167">INPUTS</span></span>

### <span data-ttu-id="7594d-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7594d-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="7594d-169">System.String</span><span class="sxs-lookup"><span data-stu-id="7594d-169">System.String</span></span>

### <span data-ttu-id="7594d-170">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="7594d-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7594d-171">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="7594d-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7594d-172">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7594d-172">OUTPUTS</span></span>

### <span data-ttu-id="7594d-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="7594d-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="7594d-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="7594d-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="7594d-175">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7594d-175">NOTES</span></span>

## <span data-ttu-id="7594d-176">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7594d-176">RELATED LINKS</span></span>
