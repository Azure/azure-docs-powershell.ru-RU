---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 20d350bec1e344ed359a62f0026c490361140fcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563895"
---
# <span data-ttu-id="f7dda-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f7dda-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="f7dda-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7dda-102">SYNOPSIS</span></span>
<span data-ttu-id="f7dda-103">Возвращает результат устранения неполадок, описанных в операции, выполняемой ранее или в ходе устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="f7dda-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7dda-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7dda-104">SYNTAX</span></span>

### <span data-ttu-id="f7dda-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7dda-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7dda-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f7dda-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7dda-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7dda-107">DESCRIPTION</span></span>
<span data-ttu-id="f7dda-108">Командлет Get-AzureRmNetworkWatcherTroubleshootingResult получает результаты устранения неполадок, вызванных предыдущим запуском или выполнением Start-AzureRmNetworkWatcherResourceTroubleshooting операции.</span><span class="sxs-lookup"><span data-stu-id="f7dda-108">The Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzureRmNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="f7dda-109">Если в данный момент выполняется операция устранения неполадок, выполнение этой операции может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="f7dda-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="f7dda-110">В настоящее время поддерживаются шлюзы и соединения виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="f7dda-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="f7dda-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7dda-111">EXAMPLES</span></span>

### <span data-ttu-id="f7dda-112">---Пример 1: запуск устранения неполадок на шлюзе виртуальной сети и получение результата---</span><span class="sxs-lookup"><span data-stu-id="f7dda-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="f7dda-113">В приведенном выше примере начинается устранение неполадок шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f7dda-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="f7dda-114">Выполнение операции может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="f7dda-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="f7dda-115">После того как устранение неполадок будет запущено, для ресурса будет выполнен звонок Get-AzureRmNetworkWatcherTroubleshootingResult, чтобы получить результат этого звонка.</span><span class="sxs-lookup"><span data-stu-id="f7dda-115">After troubleshooting has started, a Get-AzureRmNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="f7dda-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7dda-116">PARAMETERS</span></span>

### <span data-ttu-id="f7dda-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7dda-117">-NetworkWatcher</span></span>
<span data-ttu-id="f7dda-118">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="f7dda-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="f7dda-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f7dda-119">-NetworkWatcherName</span></span>
<span data-ttu-id="f7dda-120">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="f7dda-120">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7dda-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7dda-121">-ResourceGroupName</span></span>
<span data-ttu-id="f7dda-122">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="f7dda-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f7dda-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f7dda-123">-TargetResourceId</span></span>
<span data-ttu-id="f7dda-124">Идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="f7dda-124">The target resource ID.</span></span>

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

### <span data-ttu-id="f7dda-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7dda-125">-DefaultProfile</span></span>
<span data-ttu-id="f7dda-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7dda-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7dda-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7dda-127">CommonParameters</span></span>
<span data-ttu-id="f7dda-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7dda-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7dda-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7dda-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7dda-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7dda-130">INPUTS</span></span>

### <span data-ttu-id="f7dda-131">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7dda-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f7dda-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f7dda-132">System.String</span></span>

## <span data-ttu-id="f7dda-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7dda-133">OUTPUTS</span></span>

### <span data-ttu-id="f7dda-134">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="f7dda-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="f7dda-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7dda-135">NOTES</span></span>
<span data-ttu-id="f7dda-136">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, устранение неполадок, VPN, подключение</span><span class="sxs-lookup"><span data-stu-id="f7dda-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="f7dda-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7dda-137">RELATED LINKS</span></span>

[<span data-ttu-id="f7dda-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f7dda-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f7dda-139">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7dda-139">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f7dda-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7dda-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f7dda-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7dda-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f7dda-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f7dda-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f7dda-143">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f7dda-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="f7dda-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f7dda-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f7dda-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f7dda-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f7dda-146">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f7dda-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f7dda-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f7dda-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="f7dda-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f7dda-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="f7dda-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f7dda-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f7dda-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f7dda-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
