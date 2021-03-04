---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcherconnectionmonitorreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitorReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitorReport.md
ms.openlocfilehash: 139bfb7836ca8b92a1459df25675483adfd35231
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954419"
---
# <span data-ttu-id="04b52-101">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="04b52-101">Get-AzNetworkWatcherConnectionMonitorReport</span></span>

## <span data-ttu-id="04b52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04b52-102">SYNOPSIS</span></span>
<span data-ttu-id="04b52-103">Запрос на моментальный снимок последних штатов подключения.</span><span class="sxs-lookup"><span data-stu-id="04b52-103">Query a snapshot of the most recent connection states.</span></span>

## <span data-ttu-id="04b52-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="04b52-104">SYNTAX</span></span>

### <span data-ttu-id="04b52-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="04b52-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitorReport -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04b52-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="04b52-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitorReport -NetworkWatcher <PSNetworkWatcher> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04b52-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="04b52-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitorReport -Location <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04b52-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="04b52-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitorReport -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04b52-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="04b52-109">SetByInputObject</span></span>
```
Get-AzNetworkWatcherConnectionMonitorReport -InputObject <PSConnectionMonitorResult> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04b52-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04b52-110">DESCRIPTION</span></span>
<span data-ttu-id="04b52-111">Этот Get-AzNetworkWatcherConnectionMonitorReport возвращает отчет о последних состояниях подключения.</span><span class="sxs-lookup"><span data-stu-id="04b52-111">The Get-AzNetworkWatcherConnectionMonitorReport cmdlet returns the report on the most recent connection states.</span></span>

## <span data-ttu-id="04b52-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="04b52-112">EXAMPLES</span></span>

### <span data-ttu-id="04b52-113">Пример 1. Получить последний снимок подключения монитора подключения по имени в указанном расположении</span><span class="sxs-lookup"><span data-stu-id="04b52-113">Example 1: Get the most recent connection snapshot of the connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitorReport -Location centraluseuap -Name cm


States : [
           {
             "ConnectionState": "Reachable",
             "StartTime": "2018-01-12T01:18:20Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "1530e0f2-c9b7-4bc0-a205-cf7332cd8983",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "b19b74b1-423d-4f0b-99cd-bcaed4d0b8a2"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "b19b74b1-423d-4f0b-99cd-bcaed4d0b8a2",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "80e46c56-2cf9-4106-8602-608a74832d41"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "80e46c56-2cf9-4106-8602-608a74832d41",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "e17cf884-69db-43b8-9cd5-f920770a0dbe"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "e17cf884-69db-43b8-9cd5-f920770a0dbe",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           },
           {
             "ConnectionState": "Unreachable",
             "StartTime": "2018-01-12T01:14:11Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "b6251ff8-3d07-4fdf-98f8-04b168e1cf90",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "de6d463b-47fb-4beb-afc4-d77782755313"
                 ],
                 "Issues": [
                   {
                     "Origin": "Local",
                     "Severity": "Error",
                     "Type": "NetworkError",
                     "Context": []
                   }
                 ]
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "de6d463b-47fb-4beb-afc4-d77782755313",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "0cbadb7e-cd99-4fa9-a832-eb4e0d112293"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "0cbadb7e-cd99-4fa9-a832-eb4e0d112293",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "538005d1-994a-4350-9866-6985385beecf"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "538005d1-994a-4350-9866-6985385beecf",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           },
           {
             "ConnectionState": "Reachable",
             "StartTime": "2018-01-11T23:54:05Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "3dbec7e8-a37f-4acd-bc5f-86918fffba0e",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "1a87cf61-1be6-4add-bba7-f84afbcf3726"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "1a87cf61-1be6-4add-bba7-f84afbcf3726",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "070c0740-308e-43ba-b72f-5d8d5a6537ec"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "070c0740-308e-43ba-b72f-5d8d5a6537ec",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "760182e1-c88d-4cfc-a711-65e7e622a67a"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "760182e1-c88d-4cfc-a711-65e7e622a67a",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           }
         ]
```

<span data-ttu-id="04b52-114">В этом примере мы запрашиваем последние состояния подключения указанного монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="04b52-114">In this example we query the most recent connection states of the specified connection monitor.</span></span>

## <span data-ttu-id="04b52-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04b52-115">PARAMETERS</span></span>

### <span data-ttu-id="04b52-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04b52-116">-AsJob</span></span>
<span data-ttu-id="04b52-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="04b52-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04b52-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04b52-118">-DefaultProfile</span></span>
<span data-ttu-id="04b52-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04b52-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04b52-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04b52-120">-InputObject</span></span>
<span data-ttu-id="04b52-121">Объект монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="04b52-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="04b52-122">-Location</span><span class="sxs-lookup"><span data-stu-id="04b52-122">-Location</span></span>
<span data-ttu-id="04b52-123">Расположение сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="04b52-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="04b52-124">-Name</span><span class="sxs-lookup"><span data-stu-id="04b52-124">-Name</span></span>
<span data-ttu-id="04b52-125">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="04b52-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="04b52-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="04b52-126">-NetworkWatcher</span></span>
<span data-ttu-id="04b52-127">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="04b52-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="04b52-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="04b52-128">-NetworkWatcherName</span></span>
<span data-ttu-id="04b52-129">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="04b52-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="04b52-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04b52-130">-ResourceGroupName</span></span>
<span data-ttu-id="04b52-131">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="04b52-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="04b52-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04b52-132">-ResourceId</span></span>
<span data-ttu-id="04b52-133">ИД ресурса монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="04b52-133">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="04b52-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b52-134">CommonParameters</span></span>
<span data-ttu-id="04b52-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04b52-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b52-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04b52-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b52-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04b52-137">INPUTS</span></span>

### <span data-ttu-id="04b52-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="04b52-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="04b52-139">System.String</span><span class="sxs-lookup"><span data-stu-id="04b52-139">System.String</span></span>

### <span data-ttu-id="04b52-140">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="04b52-140">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="04b52-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="04b52-141">OUTPUTS</span></span>

### <span data-ttu-id="04b52-142">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorQueryResult</span><span class="sxs-lookup"><span data-stu-id="04b52-142">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorQueryResult</span></span>

## <span data-ttu-id="04b52-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="04b52-143">NOTES</span></span>
<span data-ttu-id="04b52-144">Ключевые слова: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span><span class="sxs-lookup"><span data-stu-id="04b52-144">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="04b52-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04b52-145">RELATED LINKS</span></span>

[<span data-ttu-id="04b52-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="04b52-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="04b52-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="04b52-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="04b52-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="04b52-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="04b52-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="04b52-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="04b52-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="04b52-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="04b52-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="04b52-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="04b52-152">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="04b52-152">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="04b52-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="04b52-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="04b52-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="04b52-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="04b52-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="04b52-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="04b52-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="04b52-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="04b52-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="04b52-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="04b52-158">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="04b52-158">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="04b52-159">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="04b52-159">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="04b52-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="04b52-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="04b52-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="04b52-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="04b52-162">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="04b52-162">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="04b52-163">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="04b52-163">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="04b52-164">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="04b52-164">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="04b52-165">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="04b52-165">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="04b52-166">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="04b52-166">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="04b52-167">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="04b52-167">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="04b52-168">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="04b52-168">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="04b52-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="04b52-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="04b52-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="04b52-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="04b52-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="04b52-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="04b52-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="04b52-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
