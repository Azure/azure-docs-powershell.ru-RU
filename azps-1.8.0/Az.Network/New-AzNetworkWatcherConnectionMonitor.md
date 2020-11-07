---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7c6ad774c7b260424821b37837882bab0b47bd53
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730299"
---
# <span data-ttu-id="a277b-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a277b-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="a277b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a277b-102">SYNOPSIS</span></span>
<span data-ttu-id="a277b-103">Создание монитора соединений.</span><span class="sxs-lookup"><span data-stu-id="a277b-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="a277b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a277b-104">SYNTAX</span></span>

### <span data-ttu-id="a277b-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a277b-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a277b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a277b-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a277b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a277b-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a277b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a277b-108">DESCRIPTION</span></span>
<span data-ttu-id="a277b-109">Командлет New-AzNetworkWatcherConnectionMonitor rcreates монитор подключений для определенного источника и места назначения.</span><span class="sxs-lookup"><span data-stu-id="a277b-109">The New-AzNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="a277b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a277b-110">EXAMPLES</span></span>

### <span data-ttu-id="a277b-111">Пример 1: Создание монитора подключений для виртуальной машины и адреса в Интернете</span><span class="sxs-lookup"><span data-stu-id="a277b-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/t1
Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft
                                .Compute/virtualMachines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "bing.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:13:11 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {}
```

<span data-ttu-id="a277b-112">Командлет New-AzNetworkWatcherConnectionMonitor создает монитор подключений для определенного источника и назначения.</span><span class="sxs-lookup"><span data-stu-id="a277b-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="a277b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a277b-113">PARAMETERS</span></span>

### <span data-ttu-id="a277b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a277b-114">-AsJob</span></span>
<span data-ttu-id="a277b-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a277b-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a277b-116">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="a277b-116">-ConfigureOnly</span></span>
<span data-ttu-id="a277b-117">Настройка монитора подключений, но не запуск</span><span class="sxs-lookup"><span data-stu-id="a277b-117">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="a277b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a277b-118">-DefaultProfile</span></span>
<span data-ttu-id="a277b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a277b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a277b-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="a277b-120">-DestinationAddress</span></span>
<span data-ttu-id="a277b-121">IP-адрес назначения монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="a277b-121">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="a277b-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="a277b-122">-DestinationPort</span></span>
<span data-ttu-id="a277b-123">Порт назначения.</span><span class="sxs-lookup"><span data-stu-id="a277b-123">Destination port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a277b-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="a277b-124">-DestinationResourceId</span></span>
<span data-ttu-id="a277b-125">Идентификатор назначения монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="a277b-125">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="a277b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="a277b-126">-Force</span></span>
<span data-ttu-id="a277b-127">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="a277b-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a277b-128">-Location</span><span class="sxs-lookup"><span data-stu-id="a277b-128">-Location</span></span>
<span data-ttu-id="a277b-129">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="a277b-129">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a277b-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a277b-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="a277b-131">Интервал наблюдения (в секундах).</span><span class="sxs-lookup"><span data-stu-id="a277b-131">Monitoring interval in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a277b-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a277b-132">-Name</span></span>
<span data-ttu-id="a277b-133">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="a277b-133">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a277b-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a277b-134">-NetworkWatcher</span></span>
<span data-ttu-id="a277b-135">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="a277b-135">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a277b-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a277b-136">-NetworkWatcherName</span></span>
<span data-ttu-id="a277b-137">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="a277b-137">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a277b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a277b-138">-ResourceGroupName</span></span>
<span data-ttu-id="a277b-139">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="a277b-139">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a277b-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="a277b-140">-SourcePort</span></span>
<span data-ttu-id="a277b-141">Порт источника.</span><span class="sxs-lookup"><span data-stu-id="a277b-141">Source port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a277b-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="a277b-142">-SourceResourceId</span></span>
<span data-ttu-id="a277b-143">Идентификатор источника монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="a277b-143">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="a277b-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="a277b-144">-Tag</span></span>
<span data-ttu-id="a277b-145">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a277b-145">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a277b-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a277b-146">-Confirm</span></span>
<span data-ttu-id="a277b-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a277b-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a277b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a277b-148">-WhatIf</span></span>
<span data-ttu-id="a277b-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a277b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a277b-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a277b-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a277b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a277b-151">CommonParameters</span></span>
<span data-ttu-id="a277b-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a277b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a277b-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a277b-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a277b-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a277b-154">INPUTS</span></span>

### <span data-ttu-id="a277b-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a277b-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="a277b-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a277b-156">OUTPUTS</span></span>

### <span data-ttu-id="a277b-157">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="a277b-157">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="a277b-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="a277b-158">NOTES</span></span>
<span data-ttu-id="a277b-159">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="a277b-159">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="a277b-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a277b-160">RELATED LINKS</span></span>

[<span data-ttu-id="a277b-161">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a277b-161">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a277b-162">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a277b-162">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a277b-163">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a277b-163">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a277b-164">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a277b-164">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a277b-165">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a277b-165">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a277b-166">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a277b-166">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a277b-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a277b-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a277b-168">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a277b-168">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a277b-169">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a277b-169">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a277b-170">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a277b-170">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a277b-171">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a277b-171">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a277b-172">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a277b-172">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a277b-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a277b-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a277b-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a277b-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a277b-175">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a277b-175">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a277b-176">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a277b-176">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a277b-177">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a277b-177">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a277b-178">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a277b-178">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a277b-179">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a277b-179">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a277b-180">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a277b-180">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a277b-181">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a277b-181">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a277b-182">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a277b-182">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a277b-183">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a277b-183">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a277b-184">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a277b-184">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a277b-185">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a277b-185">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a277b-186">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a277b-186">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a277b-187">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a277b-187">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
