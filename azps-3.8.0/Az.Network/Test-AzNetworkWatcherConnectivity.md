---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: b6c33809c1b738db47407ec65352adfcfb001957
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065566"
---
# <span data-ttu-id="b8a08-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b8a08-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="b8a08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8a08-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a08-103">Возвращает сведения о подключении для указанной исходной виртуальной машины и назначения.</span><span class="sxs-lookup"><span data-stu-id="b8a08-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="b8a08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8a08-104">SYNTAX</span></span>

### <span data-ttu-id="b8a08-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b8a08-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8a08-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b8a08-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8a08-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b8a08-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8a08-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8a08-108">DESCRIPTION</span></span>
<span data-ttu-id="b8a08-109">Командлет Test-AzNetworkWatcherConnectivity возвращает сведения о подключении для указанной исходной ВМ и назначения.</span><span class="sxs-lookup"><span data-stu-id="b8a08-109">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="b8a08-110">Если не удается установить связь между источником и пунктом назначения, командлет возвращает сведения о неполадке.</span><span class="sxs-lookup"><span data-stu-id="b8a08-110">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="b8a08-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8a08-111">EXAMPLES</span></span>

### <span data-ttu-id="b8a08-112">Пример 1: Проверка подключения к сетевому наблюдателю с виртуальной машины на веб-сайт</span><span class="sxs-lookup"><span data-stu-id="b8a08-112">Example 1: Test Network Watcher Connectivity from a VM to a website</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="b8a08-113">В этом примере мы проверяем подключение из виртуальной машины в Azure к www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="b8a08-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="b8a08-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8a08-114">PARAMETERS</span></span>

### <span data-ttu-id="b8a08-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8a08-115">-AsJob</span></span>
<span data-ttu-id="b8a08-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b8a08-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8a08-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a08-117">-DefaultProfile</span></span>
<span data-ttu-id="b8a08-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8a08-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8a08-119">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="b8a08-119">-DestinationAddress</span></span>
<span data-ttu-id="b8a08-120">IP-адрес или URI ресурса, на который будет выполнена попытка подключения.</span><span class="sxs-lookup"><span data-stu-id="b8a08-120">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="b8a08-121">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="b8a08-121">-DestinationId</span></span>
<span data-ttu-id="b8a08-122">Идентификатор ресурса, на который будет произведена попытка подключения.</span><span class="sxs-lookup"><span data-stu-id="b8a08-122">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="b8a08-123">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="b8a08-123">-DestinationPort</span></span>
<span data-ttu-id="b8a08-124">Порт, на котором будет проводиться проверка подключения.</span><span class="sxs-lookup"><span data-stu-id="b8a08-124">Port on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="b8a08-125">-Location</span><span class="sxs-lookup"><span data-stu-id="b8a08-125">-Location</span></span>
<span data-ttu-id="b8a08-126">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="b8a08-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b8a08-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8a08-127">-NetworkWatcher</span></span>
<span data-ttu-id="b8a08-128">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="b8a08-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="b8a08-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b8a08-129">-NetworkWatcherName</span></span>
<span data-ttu-id="b8a08-130">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="b8a08-130">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a08-131">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8a08-131">-ProtocolConfiguration</span></span>
<span data-ttu-id="b8a08-132">Конфигурация протокола, на которой будет проводиться проверка подключения.</span><span class="sxs-lookup"><span data-stu-id="b8a08-132">Protocol configuration on which check connectivity will be performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a08-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8a08-133">-ResourceGroupName</span></span>
<span data-ttu-id="b8a08-134">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="b8a08-134">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a08-135">-SourceId</span><span class="sxs-lookup"><span data-stu-id="b8a08-135">-SourceId</span></span>
<span data-ttu-id="b8a08-136">Идентификатор ресурса, из которого будет инициирована проверка подключения.</span><span class="sxs-lookup"><span data-stu-id="b8a08-136">The ID of the resource from which a connectivity check will be initiated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a08-137">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="b8a08-137">-SourcePort</span></span>
<span data-ttu-id="b8a08-138">Исходный порт, из которого будет проводиться проверка подключения.</span><span class="sxs-lookup"><span data-stu-id="b8a08-138">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a08-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a08-139">CommonParameters</span></span>
<span data-ttu-id="b8a08-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8a08-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a08-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8a08-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a08-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8a08-142">INPUTS</span></span>

### <span data-ttu-id="b8a08-143">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8a08-143">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b8a08-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b8a08-144">System.String</span></span>

### <span data-ttu-id="b8a08-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b8a08-145">System.Int32</span></span>

## <span data-ttu-id="b8a08-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8a08-146">OUTPUTS</span></span>

### <span data-ttu-id="b8a08-147">Microsoft. Azure. Commands. Network. Models. PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="b8a08-147">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="b8a08-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8a08-148">NOTES</span></span>
<span data-ttu-id="b8a08-149">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, руководитель, сеть, сеть, сетевое наблюдатель</span><span class="sxs-lookup"><span data-stu-id="b8a08-149">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="b8a08-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8a08-150">RELATED LINKS</span></span>

<span data-ttu-id="b8a08-151">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="b8a08-151">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="b8a08-152">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="b8a08-152">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="b8a08-153">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Остановить-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="b8a08-153">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>


<span data-ttu-id="b8a08-154">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md) 
 [New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md) 
 [Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md) 
 [Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md) 
 [Остановить-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md) 
 [Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md) 
 [Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span><span class="sxs-lookup"><span data-stu-id="b8a08-154">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)
[New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md)
[Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md)
[Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md)
[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md)
[Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md)
[Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span></span>