---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7e3836f2c546c5ba3ad2ee4a2845e7c813601dda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904422"
---
# <span data-ttu-id="0c18d-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0c18d-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="0c18d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c18d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c18d-103">Обновление монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="0c18d-103">Update a connection monitor.</span></span>

## <span data-ttu-id="0c18d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c18d-104">SYNTAX</span></span>

### <span data-ttu-id="0c18d-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0c18d-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c18d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0c18d-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c18d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="0c18d-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c18d-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0c18d-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c18d-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="0c18d-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c18d-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c18d-110">DESCRIPTION</span></span>
<span data-ttu-id="0c18d-111">Командлет Set-AzNetworkWatcherConnectionMonitor обновляет указанный монитор подключения.</span><span class="sxs-lookup"><span data-stu-id="0c18d-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="0c18d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c18d-112">EXAMPLES</span></span>

### <span data-ttu-id="0c18d-113">Пример 1: обновление монитора подключений</span><span class="sxs-lookup"><span data-stu-id="0c18d-113">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="0c18d-114">В этом примере мы обновляем существующий монитор соединения, изменяя destinationAddress и добавляя Теги.</span><span class="sxs-lookup"><span data-stu-id="0c18d-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="0c18d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c18d-115">PARAMETERS</span></span>

### <span data-ttu-id="0c18d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c18d-116">-AsJob</span></span>
<span data-ttu-id="0c18d-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0c18d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c18d-118">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="0c18d-118">-ConfigureOnly</span></span>
<span data-ttu-id="0c18d-119">Настройка монитора подключений, но не запуск</span><span class="sxs-lookup"><span data-stu-id="0c18d-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="0c18d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c18d-120">-DefaultProfile</span></span>
<span data-ttu-id="0c18d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c18d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c18d-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="0c18d-122">-DestinationAddress</span></span>
<span data-ttu-id="0c18d-123">IP-адрес назначения монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="0c18d-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="0c18d-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="0c18d-124">-DestinationPort</span></span>
<span data-ttu-id="0c18d-125">Порт назначения.</span><span class="sxs-lookup"><span data-stu-id="0c18d-125">Destination port.</span></span>

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

### <span data-ttu-id="0c18d-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="0c18d-126">-DestinationResourceId</span></span>
<span data-ttu-id="0c18d-127">Идентификатор назначения монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="0c18d-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="0c18d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c18d-128">-InputObject</span></span>
<span data-ttu-id="0c18d-129">Объект монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="0c18d-129">Connection monitor object.</span></span>

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

### <span data-ttu-id="0c18d-130">-Location</span><span class="sxs-lookup"><span data-stu-id="0c18d-130">-Location</span></span>
<span data-ttu-id="0c18d-131">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="0c18d-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="0c18d-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0c18d-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="0c18d-133">Интервал наблюдения (в секундах).</span><span class="sxs-lookup"><span data-stu-id="0c18d-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="0c18d-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0c18d-134">-Name</span></span>
<span data-ttu-id="0c18d-135">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="0c18d-135">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c18d-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0c18d-136">-NetworkWatcher</span></span>
<span data-ttu-id="0c18d-137">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="0c18d-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="0c18d-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0c18d-138">-NetworkWatcherName</span></span>
<span data-ttu-id="0c18d-139">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="0c18d-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="0c18d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c18d-140">-ResourceGroupName</span></span>
<span data-ttu-id="0c18d-141">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="0c18d-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0c18d-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c18d-142">-ResourceId</span></span>
<span data-ttu-id="0c18d-143">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="0c18d-143">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c18d-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="0c18d-144">-SourcePort</span></span>
<span data-ttu-id="0c18d-145">Порт источника.</span><span class="sxs-lookup"><span data-stu-id="0c18d-145">Source port.</span></span>

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

### <span data-ttu-id="0c18d-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="0c18d-146">-SourceResourceId</span></span>
<span data-ttu-id="0c18d-147">Идентификатор источника монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="0c18d-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="0c18d-148">-Тег</span><span class="sxs-lookup"><span data-stu-id="0c18d-148">-Tag</span></span>
<span data-ttu-id="0c18d-149">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c18d-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="0c18d-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c18d-150">-Confirm</span></span>
<span data-ttu-id="0c18d-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0c18d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c18d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c18d-152">-WhatIf</span></span>
<span data-ttu-id="0c18d-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0c18d-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c18d-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0c18d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c18d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c18d-155">CommonParameters</span></span>
<span data-ttu-id="0c18d-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c18d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c18d-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c18d-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c18d-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c18d-158">INPUTS</span></span>

### <span data-ttu-id="0c18d-159">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0c18d-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="0c18d-160">System. String</span><span class="sxs-lookup"><span data-stu-id="0c18d-160">System.String</span></span>

### <span data-ttu-id="0c18d-161">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="0c18d-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="0c18d-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c18d-162">OUTPUTS</span></span>

### <span data-ttu-id="0c18d-163">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="0c18d-163">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="0c18d-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c18d-164">NOTES</span></span>
<span data-ttu-id="0c18d-165">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="0c18d-165">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="0c18d-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c18d-166">RELATED LINKS</span></span>

[<span data-ttu-id="0c18d-167">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0c18d-167">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0c18d-168">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0c18d-168">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0c18d-169">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0c18d-169">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0c18d-170">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0c18d-170">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0c18d-171">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0c18d-171">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0c18d-172">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0c18d-172">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0c18d-173">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0c18d-173">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0c18d-174">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0c18d-174">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0c18d-175">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0c18d-175">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0c18d-176">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0c18d-176">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0c18d-177">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0c18d-177">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0c18d-178">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0c18d-178">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0c18d-179">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0c18d-179">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0c18d-180">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0c18d-180">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="0c18d-181">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0c18d-181">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0c18d-182">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0c18d-182">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0c18d-183">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0c18d-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0c18d-184">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0c18d-184">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0c18d-185">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c18d-185">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0c18d-186">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0c18d-186">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0c18d-187">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0c18d-187">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0c18d-188">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0c18d-188">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0c18d-189">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0c18d-189">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0c18d-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0c18d-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0c18d-191">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0c18d-191">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0c18d-192">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0c18d-192">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0c18d-193">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0c18d-193">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
