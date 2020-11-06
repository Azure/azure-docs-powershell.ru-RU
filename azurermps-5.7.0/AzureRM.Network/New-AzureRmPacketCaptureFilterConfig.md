---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
ms.openlocfilehash: a9f8570f1401387df8f26a9998c422e132f395e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568568"
---
# <span data-ttu-id="0589f-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0589f-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="0589f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0589f-102">SYNOPSIS</span></span>
<span data-ttu-id="0589f-103">Создание нового объекта фильтра захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="0589f-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0589f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0589f-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0589f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0589f-105">DESCRIPTION</span></span>
<span data-ttu-id="0589f-106">Командлет New-AzureRmPacketCaptureFilterConfig создает новый объект фильтра записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="0589f-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="0589f-107">Этот объект используется для ограничения типа пакетов, захваченных в течение сеанса захвата пакетов с использованием указанных условий.</span><span class="sxs-lookup"><span data-stu-id="0589f-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="0589f-108">Командлет New-AzureRmNetworkWatcherPacketCapture может допускать несколько объектов фильтра для включения сеансов захвата для композиции.</span><span class="sxs-lookup"><span data-stu-id="0589f-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="0589f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0589f-109">EXAMPLES</span></span>

### <span data-ttu-id="0589f-110">---Пример 1: создание захвата пакетов с несколькими фильтрами---</span><span class="sxs-lookup"><span data-stu-id="0589f-110">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="0589f-111">В этом примере мы создаем запись пакета с именем "PacketCaptureTest" с несколькими фильтрами и ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="0589f-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="0589f-112">После завершения сеанса он будет сохранен в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0589f-112">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="0589f-113">Примечание: для создания захваченных пакетов на целевой виртуальной машине должно быть установлено расширение сетевого наблюдателя Azure.</span><span class="sxs-lookup"><span data-stu-id="0589f-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="0589f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0589f-114">PARAMETERS</span></span>

### <span data-ttu-id="0589f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0589f-115">-DefaultProfile</span></span>
<span data-ttu-id="0589f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0589f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0589f-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="0589f-117">-LocalIPAddress</span></span>
<span data-ttu-id="0589f-118">Задает локальный IP-адрес, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="0589f-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="0589f-119">Пример ввода: "127.0.0.1" для записи с одним адресом.</span><span class="sxs-lookup"><span data-stu-id="0589f-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="0589f-120">"127.0.0.1-127.0.0.255" для диапазона.</span><span class="sxs-lookup"><span data-stu-id="0589f-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="0589f-121">"127.0.0.1; 127.0.0.5;" для нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="0589f-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0589f-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="0589f-122">-LocalPort</span></span>
<span data-ttu-id="0589f-123">Задает локальный IP-адрес, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="0589f-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="0589f-124">Пример ввода: "127.0.0.1" для записи с одним адресом.</span><span class="sxs-lookup"><span data-stu-id="0589f-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="0589f-125">"127.0.0.1-127.0.0.255" для диапазона.</span><span class="sxs-lookup"><span data-stu-id="0589f-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="0589f-126">"127.0.0.1; 127.0.0.5;" для нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="0589f-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0589f-127">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="0589f-127">-Protocol</span></span>
<span data-ttu-id="0589f-128">Указывает Procotol, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="0589f-128">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="0589f-129">Допустимые значения "TCP", "UDP", "Any"</span><span class="sxs-lookup"><span data-stu-id="0589f-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0589f-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="0589f-130">-RemoteIPAddress</span></span>
<span data-ttu-id="0589f-131">Задает удаленный IP-адрес, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="0589f-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="0589f-132">Пример ввода: "127.0.0.1" для записи с одним адресом.</span><span class="sxs-lookup"><span data-stu-id="0589f-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="0589f-133">"127.0.0.1-127.0.0.255" для диапазона.</span><span class="sxs-lookup"><span data-stu-id="0589f-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="0589f-134">"127.0.0.1; 127.0.0.5;" для нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="0589f-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0589f-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="0589f-135">-RemotePort</span></span>
<span data-ttu-id="0589f-136">Указывает удаленный порт, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="0589f-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="0589f-137">Пример удаленного порта входные данные: "80" для однопортового ввода.</span><span class="sxs-lookup"><span data-stu-id="0589f-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="0589f-138">"80-85" для диапазона.</span><span class="sxs-lookup"><span data-stu-id="0589f-138">"80-85" for range.</span></span>
<span data-ttu-id="0589f-139">"80; 443;" для нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="0589f-139">"80;443;" for multiple entries.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0589f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0589f-140">CommonParameters</span></span>
<span data-ttu-id="0589f-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0589f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0589f-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0589f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0589f-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0589f-143">INPUTS</span></span>

### <span data-ttu-id="0589f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0589f-144">System.String</span></span>

## <span data-ttu-id="0589f-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0589f-145">OUTPUTS</span></span>

### <span data-ttu-id="0589f-146">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="0589f-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="0589f-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="0589f-147">NOTES</span></span>
<span data-ttu-id="0589f-148">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель, пакет, захват, трафик, фильтр</span><span class="sxs-lookup"><span data-stu-id="0589f-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="0589f-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0589f-149">RELATED LINKS</span></span>

[<span data-ttu-id="0589f-150">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0589f-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0589f-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0589f-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0589f-152">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0589f-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0589f-153">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0589f-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0589f-154">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0589f-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0589f-155">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0589f-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0589f-156">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0589f-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0589f-157">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0589f-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="0589f-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0589f-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="0589f-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0589f-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0589f-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0589f-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="0589f-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0589f-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
