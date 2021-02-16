---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: e717c32b817dc86de2bfa1b9de09b95121609f28
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100416164"
---
# <span data-ttu-id="2687d-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2687d-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="2687d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2687d-102">SYNOPSIS</span></span>
<span data-ttu-id="2687d-103">Возвращает сведения о подключениях для указанного источника VM и назначения.</span><span class="sxs-lookup"><span data-stu-id="2687d-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="2687d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2687d-104">SYNTAX</span></span>

### <span data-ttu-id="2687d-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2687d-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2687d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2687d-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2687d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2687d-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2687d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2687d-108">DESCRIPTION</span></span>
<span data-ttu-id="2687d-109">Этот Test-AzNetworkWatcherConnectivity возвращает сведения о подключениях для указанного источника VM и назначения.</span><span class="sxs-lookup"><span data-stu-id="2687d-109">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="2687d-110">Если не удается установить связь между источником и пунктом назначения, cmdlet возвращает сведения о проблеме.</span><span class="sxs-lookup"><span data-stu-id="2687d-110">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="2687d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2687d-111">EXAMPLES</span></span>

### <span data-ttu-id="2687d-112">Пример 1. Проверка подключения КВВ с VM к веб-сайту</span><span class="sxs-lookup"><span data-stu-id="2687d-112">Example 1: Test Network Watcher Connectivity from a VM to a website</span></span>
```powershell
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

<span data-ttu-id="2687d-113">В этом примере мы протестировали подключение из VM-службы Azure к www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="2687d-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

### <span data-ttu-id="2687d-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2687d-114">Example 2</span></span>

<span data-ttu-id="2687d-115">Возвращает сведения о подключениях для указанного источника VM и назначения.</span><span class="sxs-lookup"><span data-stu-id="2687d-115">Returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="2687d-116">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="2687d-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Test-AzNetworkWatcherConnectivity -DestinationAddress 'bing.com' -DestinationPort 80 -NetworkWatcher <PSNetworkWatcher> -SourceId '/subscriptions/00000000-0000-0000-0000-00000000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0'
```

## <span data-ttu-id="2687d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2687d-117">PARAMETERS</span></span>

### <span data-ttu-id="2687d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2687d-118">-AsJob</span></span>
<span data-ttu-id="2687d-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2687d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2687d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2687d-120">-DefaultProfile</span></span>
<span data-ttu-id="2687d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2687d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2687d-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="2687d-122">-DestinationAddress</span></span>
<span data-ttu-id="2687d-123">IP-адрес или URI ресурса, к которому будет выполнена попытка подключения.</span><span class="sxs-lookup"><span data-stu-id="2687d-123">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="2687d-124">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="2687d-124">-DestinationId</span></span>
<span data-ttu-id="2687d-125">ИД ресурса, к которому будет выполнена попытка подключения.</span><span class="sxs-lookup"><span data-stu-id="2687d-125">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="2687d-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="2687d-126">-DestinationPort</span></span>
<span data-ttu-id="2687d-127">Порт, для которого будет выполнена проверка подключения.</span><span class="sxs-lookup"><span data-stu-id="2687d-127">Port on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="2687d-128">-Location</span><span class="sxs-lookup"><span data-stu-id="2687d-128">-Location</span></span>
<span data-ttu-id="2687d-129">Расположение сетевого просмотра.</span><span class="sxs-lookup"><span data-stu-id="2687d-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2687d-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2687d-130">-NetworkWatcher</span></span>
<span data-ttu-id="2687d-131">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="2687d-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="2687d-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2687d-132">-NetworkWatcherName</span></span>
<span data-ttu-id="2687d-133">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="2687d-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="2687d-134">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2687d-134">-ProtocolConfiguration</span></span>
<span data-ttu-id="2687d-135">Конфигурация протокола, на которой будет выполняться проверка подключения.</span><span class="sxs-lookup"><span data-stu-id="2687d-135">Protocol configuration on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="2687d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2687d-136">-ResourceGroupName</span></span>
<span data-ttu-id="2687d-137">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="2687d-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2687d-138">-SourceId</span><span class="sxs-lookup"><span data-stu-id="2687d-138">-SourceId</span></span>
<span data-ttu-id="2687d-139">ИД ресурса, с которого будет инициировалась проверка подключения.</span><span class="sxs-lookup"><span data-stu-id="2687d-139">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="2687d-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="2687d-140">-SourcePort</span></span>
<span data-ttu-id="2687d-141">Исходный порт, с которого будет выполняться проверка подключения.</span><span class="sxs-lookup"><span data-stu-id="2687d-141">The source port from which a connectivity check will be performed.</span></span>

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

### <span data-ttu-id="2687d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2687d-142">CommonParameters</span></span>
<span data-ttu-id="2687d-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2687d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2687d-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2687d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2687d-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2687d-145">INPUTS</span></span>

### <span data-ttu-id="2687d-146">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2687d-146">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2687d-147">System.String</span><span class="sxs-lookup"><span data-stu-id="2687d-147">System.String</span></span>

### <span data-ttu-id="2687d-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2687d-148">System.Int32</span></span>

## <span data-ttu-id="2687d-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2687d-149">OUTPUTS</span></span>

### <span data-ttu-id="2687d-150">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="2687d-150">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="2687d-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2687d-151">NOTES</span></span>
<span data-ttu-id="2687d-152">Ключевые слова: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span><span class="sxs-lookup"><span data-stu-id="2687d-152">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="2687d-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2687d-153">RELATED LINKS</span></span>

<span data-ttu-id="2687d-154">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="2687d-154">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="2687d-155">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="2687d-155">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="2687d-156">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="2687d-156">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>


<span data-ttu-id="2687d-157">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md) 
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
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="2687d-157">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)
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
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)</span></span>
