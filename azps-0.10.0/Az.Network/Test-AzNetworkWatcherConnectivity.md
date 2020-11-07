---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: f6c25d58588d0b75f67163c50cfa91a6f8e982da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910980"
---
# <span data-ttu-id="c03a6-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c03a6-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="c03a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c03a6-102">SYNOPSIS</span></span>
<span data-ttu-id="c03a6-103">Возвращает сведения о подключении для указанной исходной виртуальной машины и назначения.</span><span class="sxs-lookup"><span data-stu-id="c03a6-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="c03a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c03a6-104">SYNTAX</span></span>

### <span data-ttu-id="c03a6-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c03a6-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c03a6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c03a6-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c03a6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c03a6-107">DESCRIPTION</span></span>
<span data-ttu-id="c03a6-108">Командлет Test-AzNetworkWatcherConnectivity возвращает сведения о подключении для указанной исходной ВМ и назначения.</span><span class="sxs-lookup"><span data-stu-id="c03a6-108">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="c03a6-109">Если не удается установить связь между источником и пунктом назначения, командлет возвращает сведения о неполадке.</span><span class="sxs-lookup"><span data-stu-id="c03a6-109">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="c03a6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c03a6-110">EXAMPLES</span></span>

### <span data-ttu-id="c03a6-111">---------------Пример 1: Проверка подключения к сетевому наблюдателю с виртуальной машины на веб-сайт---------------</span><span class="sxs-lookup"><span data-stu-id="c03a6-111">---------------  Example 1: Test Network Watcher Connectivity from a VM to a website  ---------------</span></span>
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

<span data-ttu-id="c03a6-112">В этом примере мы проверяем подключение из виртуальной машины в Azure к www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="c03a6-112">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="c03a6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c03a6-113">PARAMETERS</span></span>

### <span data-ttu-id="c03a6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c03a6-114">-AsJob</span></span>
<span data-ttu-id="c03a6-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c03a6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c03a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c03a6-116">-DefaultProfile</span></span>
<span data-ttu-id="c03a6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c03a6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c03a6-118">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="c03a6-118">-DestinationAddress</span></span>
<span data-ttu-id="c03a6-119">IP-адрес или URI ресурса, на который будет выполнена попытка подключения.</span><span class="sxs-lookup"><span data-stu-id="c03a6-119">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="c03a6-120">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="c03a6-120">-DestinationId</span></span>
<span data-ttu-id="c03a6-121">Идентификатор ресурса, на который будет произведена попытка подключения.</span><span class="sxs-lookup"><span data-stu-id="c03a6-121">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="c03a6-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="c03a6-122">-DestinationPort</span></span>
<span data-ttu-id="c03a6-123">Порт, на котором будет проводиться проверка подключения.</span><span class="sxs-lookup"><span data-stu-id="c03a6-123">Port on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="c03a6-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c03a6-124">-NetworkWatcher</span></span>
<span data-ttu-id="c03a6-125">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="c03a6-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="c03a6-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c03a6-126">-NetworkWatcherName</span></span>
<span data-ttu-id="c03a6-127">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="c03a6-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c03a6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c03a6-128">-ResourceGroupName</span></span>
<span data-ttu-id="c03a6-129">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="c03a6-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c03a6-130">-SourceId</span><span class="sxs-lookup"><span data-stu-id="c03a6-130">-SourceId</span></span>
<span data-ttu-id="c03a6-131">Идентификатор ресурса, из которого будет инициирована проверка подключения.</span><span class="sxs-lookup"><span data-stu-id="c03a6-131">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="c03a6-132">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="c03a6-132">-SourcePort</span></span>
<span data-ttu-id="c03a6-133">Исходный порт, из которого будет проводиться проверка подключения.</span><span class="sxs-lookup"><span data-stu-id="c03a6-133">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c03a6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c03a6-134">CommonParameters</span></span>
<span data-ttu-id="c03a6-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c03a6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c03a6-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c03a6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c03a6-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c03a6-137">INPUTS</span></span>

### <span data-ttu-id="c03a6-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c03a6-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c03a6-139">System. String System. Int32</span><span class="sxs-lookup"><span data-stu-id="c03a6-139">System.String System.Int32</span></span>

## <span data-ttu-id="c03a6-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c03a6-140">OUTPUTS</span></span>

### <span data-ttu-id="c03a6-141">Microsoft. Azure. Commands. Network. Models. PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="c03a6-141">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="c03a6-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="c03a6-142">NOTES</span></span>
<span data-ttu-id="c03a6-143">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, руководитель, сеть, сеть, сетевое наблюдатель</span><span class="sxs-lookup"><span data-stu-id="c03a6-143">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="c03a6-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c03a6-144">RELATED LINKS</span></span>

<span data-ttu-id="c03a6-145">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="c03a6-145">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="c03a6-146">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="c03a6-146">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="c03a6-147">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Остановить-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="c03a6-147">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>
