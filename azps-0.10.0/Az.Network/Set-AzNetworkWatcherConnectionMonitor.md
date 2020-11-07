---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 93c54df5cb0976aa0bd8f73881208c1966bbe9d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911025"
---
# <span data-ttu-id="6e5f8-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6e5f8-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="6e5f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e5f8-102">SYNOPSIS</span></span>
<span data-ttu-id="6e5f8-103">Обновление монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-103">Update a connection monitor.</span></span>

## <span data-ttu-id="6e5f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e5f8-104">SYNTAX</span></span>

### <span data-ttu-id="6e5f8-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6e5f8-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6e5f8-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6e5f8-106">SetByName</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6e5f8-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6e5f8-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6e5f8-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6e5f8-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6e5f8-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="6e5f8-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="6e5f8-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e5f8-110">DESCRIPTION</span></span>
<span data-ttu-id="6e5f8-111">Командлет Set-AzNetworkWatcherConnectionMonitor обновляет указанный монитор подключения.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="6e5f8-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e5f8-112">EXAMPLES</span></span>

### <span data-ttu-id="6e5f8-113">---------------Пример 1: обновление монитора подключений---------------</span><span class="sxs-lookup"><span data-stu-id="6e5f8-113">---------------  Example 1: Update a connection monitor ---------------</span></span>
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

<span data-ttu-id="6e5f8-114">В этом примере мы обновляем существующий монитор соединения, изменяя destinationAddress и добавляя Теги.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="6e5f8-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e5f8-115">PARAMETERS</span></span>

### <span data-ttu-id="6e5f8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e5f8-116">-AsJob</span></span>
<span data-ttu-id="6e5f8-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6e5f8-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e5f8-118">-Автозагрузка</span><span class="sxs-lookup"><span data-stu-id="6e5f8-118">-AutoStart</span></span>
<span data-ttu-id="6e5f8-119">Автоматический запуск.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-119">Auto start.</span></span>

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

### <span data-ttu-id="6e5f8-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e5f8-120">-Confirm</span></span>
<span data-ttu-id="6e5f8-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e5f8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e5f8-122">-DefaultProfile</span></span>
<span data-ttu-id="6e5f8-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e5f8-124">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="6e5f8-124">-DestinationAddress</span></span>
<span data-ttu-id="6e5f8-125">IP-адрес назначения монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-125">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="6e5f8-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="6e5f8-126">-DestinationPort</span></span>
<span data-ttu-id="6e5f8-127">Порт назначения.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-127">Destination port.</span></span>

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

### <span data-ttu-id="6e5f8-128">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="6e5f8-128">-DestinationResourceId</span></span>
<span data-ttu-id="6e5f8-129">Идентификатор назначения монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-129">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="6e5f8-130">-Force</span><span class="sxs-lookup"><span data-stu-id="6e5f8-130">-Force</span></span>
<span data-ttu-id="6e5f8-131">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="6e5f8-131">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6e5f8-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e5f8-132">-InputObject</span></span>
<span data-ttu-id="6e5f8-133">Объект монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-133">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e5f8-134">-Location</span><span class="sxs-lookup"><span data-stu-id="6e5f8-134">-Location</span></span>
<span data-ttu-id="6e5f8-135">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="6e5f8-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="6e5f8-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="6e5f8-137">Интервал наблюдения (в секундах).</span><span class="sxs-lookup"><span data-stu-id="6e5f8-137">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="6e5f8-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6e5f8-138">-Name</span></span>
<span data-ttu-id="6e5f8-139">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-139">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e5f8-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6e5f8-140">-NetworkWatcher</span></span>
<span data-ttu-id="6e5f8-141">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="6e5f8-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6e5f8-142">-NetworkWatcherName</span></span>
<span data-ttu-id="6e5f8-143">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="6e5f8-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e5f8-144">-ResourceGroupName</span></span>
<span data-ttu-id="6e5f8-145">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6e5f8-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e5f8-146">-ResourceId</span></span>
<span data-ttu-id="6e5f8-147">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-147">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e5f8-148">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="6e5f8-148">-SourcePort</span></span>
<span data-ttu-id="6e5f8-149">Порт источника.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-149">Source port.</span></span>

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

### <span data-ttu-id="6e5f8-150">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="6e5f8-150">-SourceResourceId</span></span>
<span data-ttu-id="6e5f8-151">Идентификатор источника монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-151">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="6e5f8-152">-Тег</span><span class="sxs-lookup"><span data-stu-id="6e5f8-152">-Tag</span></span>
<span data-ttu-id="6e5f8-153">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-153">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6e5f8-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e5f8-154">-WhatIf</span></span>
<span data-ttu-id="6e5f8-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e5f8-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6e5f8-156">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="6e5f8-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e5f8-157">INPUTS</span></span>

### <span data-ttu-id="6e5f8-158">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6e5f8-158">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6e5f8-159">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="6e5f8-159">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="6e5f8-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e5f8-160">OUTPUTS</span></span>

### <span data-ttu-id="6e5f8-161">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="6e5f8-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="6e5f8-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e5f8-162">NOTES</span></span>
<span data-ttu-id="6e5f8-163">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="6e5f8-163">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="6e5f8-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e5f8-164">RELATED LINKS</span></span>
<span data-ttu-id="6e5f8-165">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="6e5f8-165">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="6e5f8-166">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="6e5f8-166">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="6e5f8-167">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Остановить-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="6e5f8-167">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="6e5f8-168">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="6e5f8-168">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span></span>

