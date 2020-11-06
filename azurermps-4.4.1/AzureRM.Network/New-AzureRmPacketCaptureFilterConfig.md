---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
ms.openlocfilehash: ad6d2baaccdc17ec6ca414ae4b0cee84db20c94b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562459"
---
# <span data-ttu-id="99fed-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="99fed-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="99fed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99fed-102">SYNOPSIS</span></span>
<span data-ttu-id="99fed-103">Создание нового объекта фильтра захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="99fed-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99fed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99fed-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99fed-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99fed-105">DESCRIPTION</span></span>
<span data-ttu-id="99fed-106">Командлет New-AzureRmPacketCaptureFilterConfig создает новый объект фильтра записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="99fed-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="99fed-107">Этот объект используется для ограничения типа пакетов, захваченных в течение сеанса захвата пакетов с использованием указанных условий.</span><span class="sxs-lookup"><span data-stu-id="99fed-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="99fed-108">Командлет New-AzureRmNetworkWatcherPacketCapture может допускать несколько объектов фильтра для включения сеансов захвата для композиции.</span><span class="sxs-lookup"><span data-stu-id="99fed-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="99fed-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99fed-109">EXAMPLES</span></span>

### <span data-ttu-id="99fed-110">---Пример 1: создание захвата пакетов с несколькими фильтрами---</span><span class="sxs-lookup"><span data-stu-id="99fed-110">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="99fed-111">В этом примере мы создаем запись пакета с именем "PacketCaptureTest" с несколькими фильтрами и ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="99fed-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="99fed-112">После завершения сеанса он будет сохранен в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="99fed-112">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="99fed-113">Примечание: для создания захваченных пакетов на целевой виртуальной машине должно быть установлено расширение сетевого наблюдателя Azure.</span><span class="sxs-lookup"><span data-stu-id="99fed-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="99fed-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99fed-114">PARAMETERS</span></span>

### <span data-ttu-id="99fed-115">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="99fed-115">-LocalIPAddress</span></span>
<span data-ttu-id="99fed-116">Задает локальный IP-адрес, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="99fed-116">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="99fed-117">Пример ввода: "127.0.0.1" для записи с одним адресом.</span><span class="sxs-lookup"><span data-stu-id="99fed-117">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="99fed-118">"127.0.0.1-127.0.0.255" для диапазона.</span><span class="sxs-lookup"><span data-stu-id="99fed-118">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="99fed-119">"127.0.0.1; 127.0.0.5;" для нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="99fed-119">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99fed-120">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="99fed-120">-LocalPort</span></span>
<span data-ttu-id="99fed-121">Задает локальный IP-адрес, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="99fed-121">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="99fed-122">Пример ввода: "127.0.0.1" для записи с одним адресом.</span><span class="sxs-lookup"><span data-stu-id="99fed-122">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="99fed-123">"127.0.0.1-127.0.0.255" для диапазона.</span><span class="sxs-lookup"><span data-stu-id="99fed-123">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="99fed-124">"127.0.0.1; 127.0.0.5;" для нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="99fed-124">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99fed-125">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="99fed-125">-Protocol</span></span>
<span data-ttu-id="99fed-126">Указывает Procotol, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="99fed-126">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="99fed-127">Допустимые значения "TCP", "UDP", "Any"</span><span class="sxs-lookup"><span data-stu-id="99fed-127">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99fed-128">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="99fed-128">-RemoteIPAddress</span></span>
<span data-ttu-id="99fed-129">Задает удаленный IP-адрес, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="99fed-129">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="99fed-130">Пример ввода: "127.0.0.1" для записи с одним адресом.</span><span class="sxs-lookup"><span data-stu-id="99fed-130">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="99fed-131">"127.0.0.1-127.0.0.255" для диапазона.</span><span class="sxs-lookup"><span data-stu-id="99fed-131">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="99fed-132">"127.0.0.1; 127.0.0.5;" для нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="99fed-132">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99fed-133">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="99fed-133">-RemotePort</span></span>
<span data-ttu-id="99fed-134">Указывает удаленный порт, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="99fed-134">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="99fed-135">Пример удаленного порта входные данные: "80" для однопортового ввода.</span><span class="sxs-lookup"><span data-stu-id="99fed-135">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="99fed-136">"80-85" для диапазона.</span><span class="sxs-lookup"><span data-stu-id="99fed-136">"80-85" for range.</span></span>
<span data-ttu-id="99fed-137">"80; 443;" для нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="99fed-137">"80;443;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99fed-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99fed-138">-DefaultProfile</span></span>
<span data-ttu-id="99fed-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99fed-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99fed-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99fed-140">CommonParameters</span></span>
<span data-ttu-id="99fed-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99fed-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99fed-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99fed-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99fed-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99fed-143">INPUTS</span></span>

### <span data-ttu-id="99fed-144">System. String</span><span class="sxs-lookup"><span data-stu-id="99fed-144">System.String</span></span>

## <span data-ttu-id="99fed-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99fed-145">OUTPUTS</span></span>

### <span data-ttu-id="99fed-146">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="99fed-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="99fed-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="99fed-147">NOTES</span></span>
<span data-ttu-id="99fed-148">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель, пакет, захват, трафик, фильтр</span><span class="sxs-lookup"><span data-stu-id="99fed-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="99fed-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99fed-149">RELATED LINKS</span></span>

[<span data-ttu-id="99fed-150">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="99fed-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="99fed-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="99fed-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="99fed-152">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="99fed-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="99fed-153">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="99fed-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="99fed-154">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="99fed-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="99fed-155">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="99fed-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="99fed-156">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="99fed-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="99fed-157">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="99fed-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="99fed-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="99fed-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="99fed-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="99fed-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="99fed-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="99fed-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="99fed-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="99fed-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
