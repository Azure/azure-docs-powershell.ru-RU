---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b8dd04fa4727465ee9b3be3eaf5e5e06a2243338
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734435"
---
# <span data-ttu-id="2ceff-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ceff-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="2ceff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ceff-102">SYNOPSIS</span></span>
<span data-ttu-id="2ceff-103">Создание монитора соединений.</span><span class="sxs-lookup"><span data-stu-id="2ceff-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ceff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ceff-104">SYNTAX</span></span>

### <span data-ttu-id="2ceff-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ceff-105">SetByName (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ceff-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2ceff-106">SetByResource</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ceff-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2ceff-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ceff-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ceff-108">DESCRIPTION</span></span>
<span data-ttu-id="2ceff-109">Командлет New-AzureRmNetworkWatcherConnectionMonitor rcreates монитор подключений для определенного источника и места назначения.</span><span class="sxs-lookup"><span data-stu-id="2ceff-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="2ceff-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ceff-110">EXAMPLES</span></span>

### <span data-ttu-id="2ceff-111">Пример 1: Создание монитора подключений для виртуальной машины и адреса в Интернете</span><span class="sxs-lookup"><span data-stu-id="2ceff-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
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

<span data-ttu-id="2ceff-112">Командлет New-AzureRmNetworkWatcherConnectionMonitor создает монитор подключений для определенного источника и назначения.</span><span class="sxs-lookup"><span data-stu-id="2ceff-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="2ceff-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ceff-113">PARAMETERS</span></span>

### <span data-ttu-id="2ceff-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ceff-114">-AsJob</span></span>
<span data-ttu-id="2ceff-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2ceff-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ceff-116">-Confirm</span></span>
<span data-ttu-id="2ceff-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2ceff-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ceff-118">-DefaultProfile</span></span>
<span data-ttu-id="2ceff-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ceff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="2ceff-120">-DestinationAddress</span></span>
<span data-ttu-id="2ceff-121">IP-адрес назначения монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="2ceff-121">The Ip address of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="2ceff-122">-DestinationPort</span></span>
<span data-ttu-id="2ceff-123">Порт назначения.</span><span class="sxs-lookup"><span data-stu-id="2ceff-123">Destination port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="2ceff-124">-DestinationResourceId</span></span>
<span data-ttu-id="2ceff-125">Идентификатор назначения монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="2ceff-125">The ID of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-126">-Force</span><span class="sxs-lookup"><span data-stu-id="2ceff-126">-Force</span></span>
<span data-ttu-id="2ceff-127">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="2ceff-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-128">-Location</span><span class="sxs-lookup"><span data-stu-id="2ceff-128">-Location</span></span>
<span data-ttu-id="2ceff-129">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="2ceff-129">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="2ceff-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="2ceff-131">Интервал наблюдения (в секундах).</span><span class="sxs-lookup"><span data-stu-id="2ceff-131">Monitoring interval in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2ceff-132">-Name</span></span>
<span data-ttu-id="2ceff-133">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="2ceff-133">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ceff-134">-NetworkWatcher</span></span>
<span data-ttu-id="2ceff-135">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="2ceff-135">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2ceff-136">-NetworkWatcherName</span></span>
<span data-ttu-id="2ceff-137">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="2ceff-137">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ceff-138">-ResourceGroupName</span></span>
<span data-ttu-id="2ceff-139">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="2ceff-139">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="2ceff-140">-SourcePort</span></span>
<span data-ttu-id="2ceff-141">Порт источника.</span><span class="sxs-lookup"><span data-stu-id="2ceff-141">Source port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="2ceff-142">-SourceResourceId</span></span>
<span data-ttu-id="2ceff-143">Идентификатор источника монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="2ceff-143">The ID of the connection monitor source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="2ceff-144">-Tag</span></span>
<span data-ttu-id="2ceff-145">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ceff-145">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ceff-146">-WhatIf</span></span>
<span data-ttu-id="2ceff-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2ceff-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ceff-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2ceff-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-149">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="2ceff-149">-ConfigureOnly</span></span>
<span data-ttu-id="2ceff-150">Настройка монитора подключений, но не запуск</span><span class="sxs-lookup"><span data-stu-id="2ceff-150">Configure connection monitor, but do not start it</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ceff-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ceff-151">CommonParameters</span></span>
<span data-ttu-id="2ceff-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ceff-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2ceff-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ceff-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ceff-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ceff-154">INPUTS</span></span>

### <span data-ttu-id="2ceff-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ceff-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2ceff-156">System. String</span><span class="sxs-lookup"><span data-stu-id="2ceff-156">System.String</span></span>

## <span data-ttu-id="2ceff-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ceff-157">OUTPUTS</span></span>

### <span data-ttu-id="2ceff-158">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="2ceff-158">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="2ceff-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ceff-159">NOTES</span></span>
<span data-ttu-id="2ceff-160">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="2ceff-160">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="2ceff-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ceff-161">RELATED LINKS</span></span>

[<span data-ttu-id="2ceff-162">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ceff-162">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="2ceff-163">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ceff-163">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="2ceff-164">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ceff-164">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="2ceff-165">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2ceff-165">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="2ceff-166">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2ceff-166">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="2ceff-167">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2ceff-167">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="2ceff-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2ceff-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="2ceff-169">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2ceff-169">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="2ceff-170">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2ceff-170">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="2ceff-171">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2ceff-171">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="2ceff-172">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2ceff-172">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="2ceff-173">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2ceff-173">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="2ceff-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ceff-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="2ceff-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2ceff-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="2ceff-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ceff-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="2ceff-177">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ceff-177">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="2ceff-178">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ceff-178">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="2ceff-179">Остановить-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ceff-179">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
