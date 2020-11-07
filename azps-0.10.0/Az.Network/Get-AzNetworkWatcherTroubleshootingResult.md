---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: c3d1e7e3a76a2561c77c8d580b7365f8fd2e6fee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909902"
---
# <span data-ttu-id="02be2-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="02be2-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="02be2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02be2-102">SYNOPSIS</span></span>
<span data-ttu-id="02be2-103">Возвращает результат устранения неполадок, описанных в операции, выполняемой ранее или в ходе устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="02be2-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="02be2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02be2-104">SYNTAX</span></span>

### <span data-ttu-id="02be2-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="02be2-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02be2-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="02be2-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02be2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02be2-107">DESCRIPTION</span></span>
<span data-ttu-id="02be2-108">Командлет Get-AzNetworkWatcherTroubleshootingResult получает результаты устранения неполадок, вызванных предыдущим запуском или выполнением Start-AzNetworkWatcherResourceTroubleshooting операции.</span><span class="sxs-lookup"><span data-stu-id="02be2-108">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="02be2-109">Если в данный момент выполняется операция устранения неполадок, выполнение этой операции может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="02be2-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="02be2-110">В настоящее время поддерживаются шлюзы и соединения виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="02be2-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="02be2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02be2-111">EXAMPLES</span></span>

### <span data-ttu-id="02be2-112">---Пример 1: запуск устранения неполадок на шлюзе виртуальной сети и получение результата---</span><span class="sxs-lookup"><span data-stu-id="02be2-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="02be2-113">В приведенном выше примере начинается устранение неполадок шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="02be2-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="02be2-114">Выполнение операции может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="02be2-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="02be2-115">После того как устранение неполадок будет запущено, для ресурса будет выполнен звонок Get-AzNetworkWatcherTroubleshootingResult, чтобы получить результат этого звонка.</span><span class="sxs-lookup"><span data-stu-id="02be2-115">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="02be2-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02be2-116">PARAMETERS</span></span>

### <span data-ttu-id="02be2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02be2-117">-DefaultProfile</span></span>
<span data-ttu-id="02be2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02be2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02be2-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="02be2-119">-NetworkWatcher</span></span>
<span data-ttu-id="02be2-120">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="02be2-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="02be2-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="02be2-121">-NetworkWatcherName</span></span>
<span data-ttu-id="02be2-122">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="02be2-122">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02be2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02be2-123">-ResourceGroupName</span></span>
<span data-ttu-id="02be2-124">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="02be2-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="02be2-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="02be2-125">-TargetResourceId</span></span>
<span data-ttu-id="02be2-126">Идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="02be2-126">The target resource ID.</span></span>

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

### <span data-ttu-id="02be2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02be2-127">CommonParameters</span></span>
<span data-ttu-id="02be2-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02be2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02be2-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02be2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02be2-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02be2-130">INPUTS</span></span>

### <span data-ttu-id="02be2-131">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="02be2-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="02be2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="02be2-132">System.String</span></span>

## <span data-ttu-id="02be2-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02be2-133">OUTPUTS</span></span>

### <span data-ttu-id="02be2-134">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="02be2-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="02be2-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="02be2-135">NOTES</span></span>
<span data-ttu-id="02be2-136">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, устранение неполадок, VPN, подключение</span><span class="sxs-lookup"><span data-stu-id="02be2-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="02be2-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02be2-137">RELATED LINKS</span></span>

[<span data-ttu-id="02be2-138">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="02be2-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="02be2-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="02be2-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="02be2-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="02be2-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="02be2-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="02be2-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="02be2-142">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="02be2-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="02be2-143">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="02be2-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="02be2-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="02be2-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="02be2-145">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="02be2-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="02be2-146">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="02be2-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="02be2-147">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="02be2-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="02be2-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="02be2-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="02be2-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="02be2-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="02be2-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="02be2-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
