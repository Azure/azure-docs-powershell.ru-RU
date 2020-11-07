---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 014942f38abf0caae01463d07343b5ad473a24d7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913618"
---
# <span data-ttu-id="874c3-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="874c3-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="874c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="874c3-102">SYNOPSIS</span></span>
<span data-ttu-id="874c3-103">Возвращает монитор подключений с указанным именем или списком мониторов соединения.</span><span class="sxs-lookup"><span data-stu-id="874c3-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="874c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="874c3-104">SYNTAX</span></span>

### <span data-ttu-id="874c3-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="874c3-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="874c3-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="874c3-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="874c3-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="874c3-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="874c3-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="874c3-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="874c3-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="874c3-109">DESCRIPTION</span></span>
<span data-ttu-id="874c3-110">Командлет Get-AzureRmNetworkWatcherConnectionMonitor возвращает монитор подключений с указанным именем/resourceId или списком мониторов соединений, соответствующих указанному сетевому ресурсу или расположению.</span><span class="sxs-lookup"><span data-stu-id="874c3-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="874c3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="874c3-111">EXAMPLES</span></span>

### <span data-ttu-id="874c3-112">---------------Пример 1: получение монитора подключений по имени в указанном расположении---------------</span><span class="sxs-lookup"><span data-stu-id="874c3-112">---------------  Example 1: Get connection monitor by name in the specified location ---------------</span></span>
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


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

<span data-ttu-id="874c3-113">В этом примере монитор соединения получается по имени в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="874c3-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="874c3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="874c3-114">PARAMETERS</span></span>

### <span data-ttu-id="874c3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="874c3-115">-AsJob</span></span>
<span data-ttu-id="874c3-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="874c3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="874c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="874c3-117">-DefaultProfile</span></span>
<span data-ttu-id="874c3-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="874c3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="874c3-119">-Location</span><span class="sxs-lookup"><span data-stu-id="874c3-119">-Location</span></span>
<span data-ttu-id="874c3-120">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="874c3-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="874c3-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="874c3-121">-Name</span></span>
<span data-ttu-id="874c3-122">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="874c3-122">The connection monitor name.</span></span>

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

### <span data-ttu-id="874c3-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="874c3-123">-NetworkWatcher</span></span>
<span data-ttu-id="874c3-124">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="874c3-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="874c3-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="874c3-125">-NetworkWatcherName</span></span>
<span data-ttu-id="874c3-126">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="874c3-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="874c3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="874c3-127">-ResourceGroupName</span></span>
<span data-ttu-id="874c3-128">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="874c3-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="874c3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="874c3-129">-ResourceId</span></span>
<span data-ttu-id="874c3-130">Идентификатор ресурса для монитора соединений.</span><span class="sxs-lookup"><span data-stu-id="874c3-130">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="874c3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="874c3-131">CommonParameters</span></span>
<span data-ttu-id="874c3-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="874c3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="874c3-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="874c3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="874c3-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="874c3-134">INPUTS</span></span>

### <span data-ttu-id="874c3-135">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="874c3-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="874c3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="874c3-136">System.String</span></span>


## <span data-ttu-id="874c3-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="874c3-137">OUTPUTS</span></span>

### <span data-ttu-id="874c3-138">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="874c3-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="874c3-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="874c3-139">NOTES</span></span>
<span data-ttu-id="874c3-140">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="874c3-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="874c3-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="874c3-141">RELATED LINKS</span></span>
<span data-ttu-id="874c3-142">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="874c3-142">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="874c3-143">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="874c3-143">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="874c3-144">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Остановить-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="874c3-144">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="874c3-145">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="874c3-145">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span></span>
