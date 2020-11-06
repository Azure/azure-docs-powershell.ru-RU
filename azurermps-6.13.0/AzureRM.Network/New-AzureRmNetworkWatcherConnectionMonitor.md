---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7554183d52b263f4eed470295a2574a3d1f487b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569791"
---
# <span data-ttu-id="d6db6-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6db6-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="d6db6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6db6-102">SYNOPSIS</span></span>
<span data-ttu-id="d6db6-103">Создание монитора соединений.</span><span class="sxs-lookup"><span data-stu-id="d6db6-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6db6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6db6-104">SYNTAX</span></span>

### <span data-ttu-id="d6db6-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d6db6-105">SetByName (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6db6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d6db6-106">SetByResource</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6db6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d6db6-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6db6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6db6-108">DESCRIPTION</span></span>
<span data-ttu-id="d6db6-109">Командлет New-AzureRmNetworkWatcherConnectionMonitor rcreates монитор подключений для определенного источника и места назначения.</span><span class="sxs-lookup"><span data-stu-id="d6db6-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="d6db6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6db6-110">EXAMPLES</span></span>

### <span data-ttu-id="d6db6-111">Пример 1: Создание монитора подключений для виртуальной машины и адреса в Интернете</span><span class="sxs-lookup"><span data-stu-id="d6db6-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

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

<span data-ttu-id="d6db6-112">Командлет New-AzureRmNetworkWatcherConnectionMonitor создает монитор подключений для определенного источника и назначения.</span><span class="sxs-lookup"><span data-stu-id="d6db6-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="d6db6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6db6-113">PARAMETERS</span></span>

### <span data-ttu-id="d6db6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6db6-114">-AsJob</span></span>
<span data-ttu-id="d6db6-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d6db6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6db6-116">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="d6db6-116">-ConfigureOnly</span></span>
<span data-ttu-id="d6db6-117">Настройка монитора подключений, но не запуск</span><span class="sxs-lookup"><span data-stu-id="d6db6-117">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="d6db6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6db6-118">-DefaultProfile</span></span>
<span data-ttu-id="d6db6-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6db6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6db6-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="d6db6-120">-DestinationAddress</span></span>
<span data-ttu-id="d6db6-121">IP-адрес назначения монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="d6db6-121">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="d6db6-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="d6db6-122">-DestinationPort</span></span>
<span data-ttu-id="d6db6-123">Порт назначения.</span><span class="sxs-lookup"><span data-stu-id="d6db6-123">Destination port.</span></span>

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

### <span data-ttu-id="d6db6-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="d6db6-124">-DestinationResourceId</span></span>
<span data-ttu-id="d6db6-125">Идентификатор назначения монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="d6db6-125">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="d6db6-126">-Force</span><span class="sxs-lookup"><span data-stu-id="d6db6-126">-Force</span></span>
<span data-ttu-id="d6db6-127">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="d6db6-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d6db6-128">-Location</span><span class="sxs-lookup"><span data-stu-id="d6db6-128">-Location</span></span>
<span data-ttu-id="d6db6-129">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="d6db6-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d6db6-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d6db6-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="d6db6-131">Интервал наблюдения (в секундах).</span><span class="sxs-lookup"><span data-stu-id="d6db6-131">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="d6db6-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d6db6-132">-Name</span></span>
<span data-ttu-id="d6db6-133">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="d6db6-133">The connection monitor name.</span></span>

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

### <span data-ttu-id="d6db6-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6db6-134">-NetworkWatcher</span></span>
<span data-ttu-id="d6db6-135">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="d6db6-135">The network watcher resource.</span></span>

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

### <span data-ttu-id="d6db6-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d6db6-136">-NetworkWatcherName</span></span>
<span data-ttu-id="d6db6-137">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="d6db6-137">The name of network watcher.</span></span>

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

### <span data-ttu-id="d6db6-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6db6-138">-ResourceGroupName</span></span>
<span data-ttu-id="d6db6-139">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="d6db6-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d6db6-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="d6db6-140">-SourcePort</span></span>
<span data-ttu-id="d6db6-141">Порт источника.</span><span class="sxs-lookup"><span data-stu-id="d6db6-141">Source port.</span></span>

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

### <span data-ttu-id="d6db6-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="d6db6-142">-SourceResourceId</span></span>
<span data-ttu-id="d6db6-143">Идентификатор источника монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="d6db6-143">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="d6db6-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="d6db6-144">-Tag</span></span>
<span data-ttu-id="d6db6-145">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6db6-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d6db6-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6db6-146">-Confirm</span></span>
<span data-ttu-id="d6db6-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d6db6-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6db6-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6db6-148">-WhatIf</span></span>
<span data-ttu-id="d6db6-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d6db6-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6db6-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d6db6-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6db6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6db6-151">CommonParameters</span></span>
<span data-ttu-id="d6db6-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6db6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6db6-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6db6-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6db6-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6db6-154">INPUTS</span></span>

### <span data-ttu-id="d6db6-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6db6-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d6db6-156">Параметры: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d6db6-156">Parameters: NetworkWatcher (ByValue)</span></span>

## <span data-ttu-id="d6db6-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6db6-157">OUTPUTS</span></span>

### <span data-ttu-id="d6db6-158">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="d6db6-158">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="d6db6-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6db6-159">NOTES</span></span>
<span data-ttu-id="d6db6-160">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="d6db6-160">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="d6db6-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6db6-161">RELATED LINKS</span></span>

[<span data-ttu-id="d6db6-162">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6db6-162">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="d6db6-163">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6db6-163">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="d6db6-164">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6db6-164">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="d6db6-165">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d6db6-165">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="d6db6-166">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d6db6-166">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="d6db6-167">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d6db6-167">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="d6db6-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d6db6-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="d6db6-169">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6db6-169">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="d6db6-170">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d6db6-170">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="d6db6-171">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6db6-171">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="d6db6-172">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6db6-172">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="d6db6-173">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6db6-173">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="d6db6-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6db6-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d6db6-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d6db6-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="d6db6-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6db6-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d6db6-177">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6db6-177">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d6db6-178">Остановить-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6db6-178">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d6db6-179">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6db6-179">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d6db6-180">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6db6-180">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="d6db6-181">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d6db6-181">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="d6db6-182">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d6db6-182">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="d6db6-183">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d6db6-183">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="d6db6-184">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6db6-184">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d6db6-185">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d6db6-185">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="d6db6-186">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d6db6-186">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="d6db6-187">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d6db6-187">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="d6db6-188">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d6db6-188">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
