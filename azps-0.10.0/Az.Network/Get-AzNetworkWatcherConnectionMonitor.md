---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: d8ab2ce24db9c6ab07989dc5a4a45b8bfca8fc78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909921"
---
# <span data-ttu-id="aa0bf-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aa0bf-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="aa0bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa0bf-102">SYNOPSIS</span></span>
<span data-ttu-id="aa0bf-103">Возвращает монитор подключений с указанным именем или списком мониторов соединения.</span><span class="sxs-lookup"><span data-stu-id="aa0bf-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="aa0bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa0bf-104">SYNTAX</span></span>

### <span data-ttu-id="aa0bf-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa0bf-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="aa0bf-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="aa0bf-106">SetByName</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="aa0bf-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="aa0bf-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="aa0bf-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="aa0bf-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="aa0bf-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa0bf-109">DESCRIPTION</span></span>
<span data-ttu-id="aa0bf-110">Командлет Get-AzNetworkWatcherConnectionMonitor возвращает монитор подключений с указанным именем/resourceId или списком мониторов соединений, соответствующих указанному сетевому ресурсу или расположению.</span><span class="sxs-lookup"><span data-stu-id="aa0bf-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="aa0bf-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa0bf-111">EXAMPLES</span></span>

### <span data-ttu-id="aa0bf-112">---------------Пример 1: получение монитора подключений по имени в указанном расположении---------------</span><span class="sxs-lookup"><span data-stu-id="aa0bf-112">---------------  Example 1: Get connection monitor by name in the specified location ---------------</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="aa0bf-113">В этом примере монитор соединения получается по имени в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="aa0bf-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="aa0bf-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa0bf-114">PARAMETERS</span></span>

### <span data-ttu-id="aa0bf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa0bf-115">-AsJob</span></span>
<span data-ttu-id="aa0bf-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="aa0bf-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa0bf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa0bf-117">-DefaultProfile</span></span>
<span data-ttu-id="aa0bf-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa0bf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa0bf-119">-Location</span><span class="sxs-lookup"><span data-stu-id="aa0bf-119">-Location</span></span>
<span data-ttu-id="aa0bf-120">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="aa0bf-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="aa0bf-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aa0bf-121">-Name</span></span>
<span data-ttu-id="aa0bf-122">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="aa0bf-122">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa0bf-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aa0bf-123">-NetworkWatcher</span></span>
<span data-ttu-id="aa0bf-124">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="aa0bf-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="aa0bf-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="aa0bf-125">-NetworkWatcherName</span></span>
<span data-ttu-id="aa0bf-126">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="aa0bf-126">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa0bf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa0bf-127">-ResourceGroupName</span></span>
<span data-ttu-id="aa0bf-128">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="aa0bf-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="aa0bf-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa0bf-129">-ResourceId</span></span>
<span data-ttu-id="aa0bf-130">Идентификатор ресурса для монитора соединений.</span><span class="sxs-lookup"><span data-stu-id="aa0bf-130">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="aa0bf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa0bf-131">CommonParameters</span></span>
<span data-ttu-id="aa0bf-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa0bf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa0bf-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa0bf-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa0bf-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa0bf-134">INPUTS</span></span>

### <span data-ttu-id="aa0bf-135">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aa0bf-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="aa0bf-136">System. String</span><span class="sxs-lookup"><span data-stu-id="aa0bf-136">System.String</span></span>


## <span data-ttu-id="aa0bf-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa0bf-137">OUTPUTS</span></span>

### <span data-ttu-id="aa0bf-138">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="aa0bf-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="aa0bf-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa0bf-139">NOTES</span></span>
<span data-ttu-id="aa0bf-140">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="aa0bf-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="aa0bf-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa0bf-141">RELATED LINKS</span></span>
<span data-ttu-id="aa0bf-142">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="aa0bf-142">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="aa0bf-143">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="aa0bf-143">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="aa0bf-144">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Остановить-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="aa0bf-144">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="aa0bf-145">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="aa0bf-145">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span></span>