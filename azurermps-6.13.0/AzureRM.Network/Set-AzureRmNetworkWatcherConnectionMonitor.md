---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5c7709c234ba762e5b87418cc0e9b3fc4637ac11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732923"
---
# <span data-ttu-id="b1e61-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b1e61-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="b1e61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1e61-102">SYNOPSIS</span></span>
<span data-ttu-id="b1e61-103">Обновление монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="b1e61-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1e61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1e61-104">SYNTAX</span></span>

### <span data-ttu-id="b1e61-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b1e61-105">SetByName (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1e61-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b1e61-106">SetByResource</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1e61-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b1e61-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1e61-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b1e61-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1e61-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="b1e61-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1e61-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1e61-110">DESCRIPTION</span></span>
<span data-ttu-id="b1e61-111">Командлет Set-AzureRmNetworkWatcherConnectionMonitor обновляет указанный монитор подключения.</span><span class="sxs-lookup"><span data-stu-id="b1e61-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="b1e61-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1e61-112">EXAMPLES</span></span>

### <span data-ttu-id="b1e61-113">Пример 1: обновление монитора подключений</span><span class="sxs-lookup"><span data-stu-id="b1e61-113">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm 
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

<span data-ttu-id="b1e61-114">В этом примере мы обновляем существующий монитор соединения, изменяя destinationAddress и добавляя Теги.</span><span class="sxs-lookup"><span data-stu-id="b1e61-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="b1e61-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1e61-115">PARAMETERS</span></span>

### <span data-ttu-id="b1e61-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1e61-116">-AsJob</span></span>
<span data-ttu-id="b1e61-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b1e61-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1e61-118">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="b1e61-118">-ConfigureOnly</span></span>
<span data-ttu-id="b1e61-119">Настройка монитора подключений, но не запуск</span><span class="sxs-lookup"><span data-stu-id="b1e61-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="b1e61-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1e61-120">-DefaultProfile</span></span>
<span data-ttu-id="b1e61-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1e61-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1e61-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="b1e61-122">-DestinationAddress</span></span>
<span data-ttu-id="b1e61-123">IP-адрес назначения монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="b1e61-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="b1e61-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="b1e61-124">-DestinationPort</span></span>
<span data-ttu-id="b1e61-125">Порт назначения.</span><span class="sxs-lookup"><span data-stu-id="b1e61-125">Destination port.</span></span>

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

### <span data-ttu-id="b1e61-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="b1e61-126">-DestinationResourceId</span></span>
<span data-ttu-id="b1e61-127">Идентификатор назначения монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="b1e61-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="b1e61-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1e61-128">-InputObject</span></span>
<span data-ttu-id="b1e61-129">Объект монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="b1e61-129">Connection monitor object.</span></span>

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

### <span data-ttu-id="b1e61-130">-Location</span><span class="sxs-lookup"><span data-stu-id="b1e61-130">-Location</span></span>
<span data-ttu-id="b1e61-131">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="b1e61-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b1e61-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b1e61-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="b1e61-133">Интервал наблюдения (в секундах).</span><span class="sxs-lookup"><span data-stu-id="b1e61-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="b1e61-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b1e61-134">-Name</span></span>
<span data-ttu-id="b1e61-135">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="b1e61-135">The connection monitor name.</span></span>

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

### <span data-ttu-id="b1e61-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b1e61-136">-NetworkWatcher</span></span>
<span data-ttu-id="b1e61-137">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="b1e61-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="b1e61-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b1e61-138">-NetworkWatcherName</span></span>
<span data-ttu-id="b1e61-139">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="b1e61-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="b1e61-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1e61-140">-ResourceGroupName</span></span>
<span data-ttu-id="b1e61-141">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="b1e61-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b1e61-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1e61-142">-ResourceId</span></span>
<span data-ttu-id="b1e61-143">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b1e61-143">Resource ID.</span></span>

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

### <span data-ttu-id="b1e61-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="b1e61-144">-SourcePort</span></span>
<span data-ttu-id="b1e61-145">Порт источника.</span><span class="sxs-lookup"><span data-stu-id="b1e61-145">Source port.</span></span>

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

### <span data-ttu-id="b1e61-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="b1e61-146">-SourceResourceId</span></span>
<span data-ttu-id="b1e61-147">Идентификатор источника монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="b1e61-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="b1e61-148">-Тег</span><span class="sxs-lookup"><span data-stu-id="b1e61-148">-Tag</span></span>
<span data-ttu-id="b1e61-149">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b1e61-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b1e61-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1e61-150">-Confirm</span></span>
<span data-ttu-id="b1e61-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b1e61-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1e61-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1e61-152">-WhatIf</span></span>
<span data-ttu-id="b1e61-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b1e61-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1e61-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b1e61-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1e61-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1e61-155">CommonParameters</span></span>
<span data-ttu-id="b1e61-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1e61-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1e61-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1e61-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1e61-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1e61-158">INPUTS</span></span>

### <span data-ttu-id="b1e61-159">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b1e61-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="b1e61-160">Параметры: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b1e61-160">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="b1e61-161">System. String</span><span class="sxs-lookup"><span data-stu-id="b1e61-161">System.String</span></span>

### <span data-ttu-id="b1e61-162">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="b1e61-162">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="b1e61-163">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b1e61-163">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b1e61-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1e61-164">OUTPUTS</span></span>

### <span data-ttu-id="b1e61-165">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="b1e61-165">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="b1e61-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1e61-166">NOTES</span></span>
<span data-ttu-id="b1e61-167">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="b1e61-167">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="b1e61-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1e61-168">RELATED LINKS</span></span>

[<span data-ttu-id="b1e61-169">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b1e61-169">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="b1e61-170">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b1e61-170">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="b1e61-171">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b1e61-171">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="b1e61-172">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b1e61-172">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="b1e61-173">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b1e61-173">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="b1e61-174">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b1e61-174">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="b1e61-175">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b1e61-175">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="b1e61-176">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b1e61-176">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="b1e61-177">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b1e61-177">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="b1e61-178">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b1e61-178">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="b1e61-179">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b1e61-179">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="b1e61-180">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b1e61-180">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="b1e61-181">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b1e61-181">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b1e61-182">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b1e61-182">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="b1e61-183">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b1e61-183">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b1e61-184">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b1e61-184">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b1e61-185">Остановить-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b1e61-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b1e61-186">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b1e61-186">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b1e61-187">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1e61-187">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="b1e61-188">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b1e61-188">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="b1e61-189">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b1e61-189">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="b1e61-190">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b1e61-190">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="b1e61-191">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b1e61-191">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b1e61-192">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b1e61-192">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="b1e61-193">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b1e61-193">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="b1e61-194">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b1e61-194">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="b1e61-195">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b1e61-195">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
