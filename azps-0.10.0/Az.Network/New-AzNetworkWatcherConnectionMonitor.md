---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: bfdcfbf57f44479ad35a2b9075590a0d40351ec9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909642"
---
# <span data-ttu-id="93990-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="93990-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="93990-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93990-102">SYNOPSIS</span></span>
<span data-ttu-id="93990-103">Создание монитора соединений.</span><span class="sxs-lookup"><span data-stu-id="93990-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="93990-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93990-104">SYNTAX</span></span>

### <span data-ttu-id="93990-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="93990-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="93990-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="93990-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="93990-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="93990-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="93990-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93990-108">DESCRIPTION</span></span>
<span data-ttu-id="93990-109">Командлет New-AzNetworkWatcherConnectionMonitor rcreates монитор подключений для определенного источника и места назначения.</span><span class="sxs-lookup"><span data-stu-id="93990-109">The New-AzNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="93990-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93990-110">EXAMPLES</span></span>

### <span data-ttu-id="93990-111">---------------Пример 1: Создание монитора подключений для виртуальной машины и назначения в Интернете---------------</span><span class="sxs-lookup"><span data-stu-id="93990-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
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

<span data-ttu-id="93990-112">Командлет New-AzNetworkWatcherConnectionMonitor создает монитор подключений для определенного источника и назначения.</span><span class="sxs-lookup"><span data-stu-id="93990-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="93990-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93990-113">PARAMETERS</span></span>

### <span data-ttu-id="93990-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93990-114">-AsJob</span></span>
<span data-ttu-id="93990-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="93990-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93990-116">-Автозагрузка</span><span class="sxs-lookup"><span data-stu-id="93990-116">-AutoStart</span></span>
<span data-ttu-id="93990-117">Автоматический запуск.</span><span class="sxs-lookup"><span data-stu-id="93990-117">Auto start.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93990-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93990-118">-Confirm</span></span>
<span data-ttu-id="93990-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="93990-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93990-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93990-120">-DefaultProfile</span></span>
<span data-ttu-id="93990-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93990-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93990-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="93990-122">-DestinationAddress</span></span>
<span data-ttu-id="93990-123">IP-адрес назначения монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="93990-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="93990-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="93990-124">-DestinationPort</span></span>
<span data-ttu-id="93990-125">Порт назначения.</span><span class="sxs-lookup"><span data-stu-id="93990-125">Destination port.</span></span>

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

### <span data-ttu-id="93990-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="93990-126">-DestinationResourceId</span></span>
<span data-ttu-id="93990-127">Идентификатор назначения монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="93990-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="93990-128">-Force</span><span class="sxs-lookup"><span data-stu-id="93990-128">-Force</span></span>
<span data-ttu-id="93990-129">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="93990-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="93990-130">-Location</span><span class="sxs-lookup"><span data-stu-id="93990-130">-Location</span></span>
<span data-ttu-id="93990-131">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="93990-131">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93990-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="93990-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="93990-133">Интервал наблюдения (в секундах).</span><span class="sxs-lookup"><span data-stu-id="93990-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="93990-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="93990-134">-Name</span></span>
<span data-ttu-id="93990-135">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="93990-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93990-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="93990-136">-NetworkWatcher</span></span>
<span data-ttu-id="93990-137">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="93990-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="93990-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="93990-138">-NetworkWatcherName</span></span>
<span data-ttu-id="93990-139">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="93990-139">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93990-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93990-140">-ResourceGroupName</span></span>
<span data-ttu-id="93990-141">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="93990-141">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93990-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="93990-142">-SourcePort</span></span>
<span data-ttu-id="93990-143">Порт источника.</span><span class="sxs-lookup"><span data-stu-id="93990-143">Source port.</span></span>

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

### <span data-ttu-id="93990-144">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="93990-144">-SourceResourceId</span></span>
<span data-ttu-id="93990-145">Идентификатор источника монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="93990-145">The ID of the connection monitor source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93990-146">-Тег</span><span class="sxs-lookup"><span data-stu-id="93990-146">-Tag</span></span>
<span data-ttu-id="93990-147">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93990-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="93990-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93990-148">-WhatIf</span></span>
<span data-ttu-id="93990-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="93990-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93990-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="93990-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="93990-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93990-151">INPUTS</span></span>

### <span data-ttu-id="93990-152">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="93990-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="93990-153">System. String</span><span class="sxs-lookup"><span data-stu-id="93990-153">System.String</span></span>


## <span data-ttu-id="93990-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93990-154">OUTPUTS</span></span>

### <span data-ttu-id="93990-155">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="93990-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="93990-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="93990-156">NOTES</span></span>
<span data-ttu-id="93990-157">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="93990-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="93990-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93990-158">RELATED LINKS</span></span>
<span data-ttu-id="93990-159">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="93990-159">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="93990-160">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="93990-160">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="93990-161">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Остановить-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="93990-161">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="93990-162">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="93990-162">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span></span>
