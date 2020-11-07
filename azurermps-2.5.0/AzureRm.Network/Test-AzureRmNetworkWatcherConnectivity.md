---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcherconnectivity
schema: 2.0.0
ms.openlocfilehash: 55dc2682c4c3e62b42a6a23ac12f93991e4873fc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913559"
---
# <span data-ttu-id="1a087-101">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1a087-101">Test-AzureRmNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="1a087-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a087-102">SYNOPSIS</span></span>
<span data-ttu-id="1a087-103">Возвращает сведения о подключении для указанной исходной виртуальной машины и назначения.</span><span class="sxs-lookup"><span data-stu-id="1a087-103">Returns connectivity information for a specified source VM and a destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a087-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a087-104">SYNTAX</span></span>

### <span data-ttu-id="1a087-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1a087-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a087-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1a087-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a087-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a087-107">DESCRIPTION</span></span>
<span data-ttu-id="1a087-108">Командлет Test-AzureRmNetworkWatcherConnectivity возвращает сведения о подключении для указанной исходной ВМ и назначения.</span><span class="sxs-lookup"><span data-stu-id="1a087-108">The Test-AzureRmNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="1a087-109">Если не удается установить связь между источником и пунктом назначения, командлет возвращает сведения о неполадке.</span><span class="sxs-lookup"><span data-stu-id="1a087-109">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="1a087-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a087-110">EXAMPLES</span></span>

### <span data-ttu-id="1a087-111">---------------Пример 1: Проверка подключения к сетевому наблюдателю с виртуальной машины на веб-сайт---------------</span><span class="sxs-lookup"><span data-stu-id="1a087-111">---------------  Example 1: Test Network Watcher Connectivity from a VM to a website  ---------------</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


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

<span data-ttu-id="1a087-112">В этом примере мы проверяем подключение из виртуальной машины в Azure к www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="1a087-112">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="1a087-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a087-113">PARAMETERS</span></span>

### <span data-ttu-id="1a087-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a087-114">-AsJob</span></span>
<span data-ttu-id="1a087-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1a087-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a087-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a087-116">-DefaultProfile</span></span>
<span data-ttu-id="1a087-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a087-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a087-118">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="1a087-118">-DestinationAddress</span></span>
<span data-ttu-id="1a087-119">IP-адрес или URI ресурса, на который будет выполнена попытка подключения.</span><span class="sxs-lookup"><span data-stu-id="1a087-119">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="1a087-120">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="1a087-120">-DestinationId</span></span>
<span data-ttu-id="1a087-121">Идентификатор ресурса, на который будет произведена попытка подключения.</span><span class="sxs-lookup"><span data-stu-id="1a087-121">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="1a087-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="1a087-122">-DestinationPort</span></span>
<span data-ttu-id="1a087-123">Порт, на котором будет проводиться проверка подключения.</span><span class="sxs-lookup"><span data-stu-id="1a087-123">Port on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="1a087-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1a087-124">-NetworkWatcher</span></span>
<span data-ttu-id="1a087-125">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="1a087-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="1a087-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1a087-126">-NetworkWatcherName</span></span>
<span data-ttu-id="1a087-127">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="1a087-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="1a087-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a087-128">-ResourceGroupName</span></span>
<span data-ttu-id="1a087-129">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="1a087-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1a087-130">-SourceId</span><span class="sxs-lookup"><span data-stu-id="1a087-130">-SourceId</span></span>
<span data-ttu-id="1a087-131">Идентификатор ресурса, из которого будет инициирована проверка подключения.</span><span class="sxs-lookup"><span data-stu-id="1a087-131">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="1a087-132">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="1a087-132">-SourcePort</span></span>
<span data-ttu-id="1a087-133">Исходный порт, из которого будет проводиться проверка подключения.</span><span class="sxs-lookup"><span data-stu-id="1a087-133">The source port from which a connectivity check will be performed.</span></span>

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

### <span data-ttu-id="1a087-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a087-134">CommonParameters</span></span>
<span data-ttu-id="1a087-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a087-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a087-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a087-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a087-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a087-137">INPUTS</span></span>

### <span data-ttu-id="1a087-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1a087-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="1a087-139">System. String System. Int32</span><span class="sxs-lookup"><span data-stu-id="1a087-139">System.String System.Int32</span></span>

## <span data-ttu-id="1a087-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a087-140">OUTPUTS</span></span>

### <span data-ttu-id="1a087-141">Microsoft. Azure. Commands. Network. Models. PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="1a087-141">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="1a087-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a087-142">NOTES</span></span>
<span data-ttu-id="1a087-143">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, руководитель, сеть, сеть, сетевое наблюдатель</span><span class="sxs-lookup"><span data-stu-id="1a087-143">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="1a087-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a087-144">RELATED LINKS</span></span>

<span data-ttu-id="1a087-145">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="1a087-145">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="1a087-146">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="1a087-146">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="1a087-147">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Остановить-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="1a087-147">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>
