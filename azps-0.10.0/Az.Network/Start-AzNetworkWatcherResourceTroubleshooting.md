---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: a72f494518b3a511eac3e4b1a92330f666bbca64
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910990"
---
# <span data-ttu-id="4ae38-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4ae38-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="4ae38-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ae38-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae38-103">Запуск устранения неполадок в сетевом ресурсе в Azure.</span><span class="sxs-lookup"><span data-stu-id="4ae38-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="4ae38-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ae38-104">SYNTAX</span></span>

### <span data-ttu-id="4ae38-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ae38-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ae38-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4ae38-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ae38-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ae38-107">DESCRIPTION</span></span>
<span data-ttu-id="4ae38-108">Командлет Start-AzNetworkWatcherResourceTroubleshooting запускает устранение неполадок для сетевых ресурсов в Azure и возвращает сведения о возможных проблемах и снижении риска.</span><span class="sxs-lookup"><span data-stu-id="4ae38-108">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="4ae38-109">В настоящее время поддерживаются шлюзы и соединения виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="4ae38-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="4ae38-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ae38-110">EXAMPLES</span></span>

### <span data-ttu-id="4ae38-111">---Пример 1: запуск устранения неполадок на шлюзе виртуальной сети---</span><span class="sxs-lookup"><span data-stu-id="4ae38-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="4ae38-112">В приведенном выше примере начинается устранение неполадок шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="4ae38-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="4ae38-113">Выполнение операции может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="4ae38-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="4ae38-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ae38-114">PARAMETERS</span></span>

### <span data-ttu-id="4ae38-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae38-115">-DefaultProfile</span></span>
<span data-ttu-id="4ae38-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ae38-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ae38-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4ae38-117">-NetworkWatcher</span></span>
<span data-ttu-id="4ae38-118">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="4ae38-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="4ae38-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4ae38-119">-NetworkWatcherName</span></span>
<span data-ttu-id="4ae38-120">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="4ae38-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="4ae38-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ae38-121">-ResourceGroupName</span></span>
<span data-ttu-id="4ae38-122">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="4ae38-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4ae38-123">-StorageId</span><span class="sxs-lookup"><span data-stu-id="4ae38-123">-StorageId</span></span>
<span data-ttu-id="4ae38-124">Идентификатор хранилища.</span><span class="sxs-lookup"><span data-stu-id="4ae38-124">The storage ID.</span></span>

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

### <span data-ttu-id="4ae38-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="4ae38-125">-StoragePath</span></span>
<span data-ttu-id="4ae38-126">Путь к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="4ae38-126">The storage path.</span></span>

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

### <span data-ttu-id="4ae38-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4ae38-127">-TargetResourceId</span></span>
<span data-ttu-id="4ae38-128">Указывает идентификатор ресурса для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="4ae38-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="4ae38-129">Пример формата: "/Subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="4ae38-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="4ae38-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae38-130">CommonParameters</span></span>
<span data-ttu-id="4ae38-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ae38-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae38-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ae38-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae38-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ae38-133">INPUTS</span></span>

### <span data-ttu-id="4ae38-134">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4ae38-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4ae38-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4ae38-135">System.String</span></span>

## <span data-ttu-id="4ae38-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ae38-136">OUTPUTS</span></span>

### <span data-ttu-id="4ae38-137">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="4ae38-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="4ae38-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ae38-138">NOTES</span></span>
<span data-ttu-id="4ae38-139">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, устранение неполадок, VPN, подключение</span><span class="sxs-lookup"><span data-stu-id="4ae38-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="4ae38-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ae38-140">RELATED LINKS</span></span>

[<span data-ttu-id="4ae38-141">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4ae38-141">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4ae38-142">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4ae38-142">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4ae38-143">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4ae38-143">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4ae38-144">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4ae38-144">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4ae38-145">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4ae38-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4ae38-146">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4ae38-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4ae38-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4ae38-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4ae38-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4ae38-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4ae38-149">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4ae38-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4ae38-150">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4ae38-150">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4ae38-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4ae38-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4ae38-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4ae38-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4ae38-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4ae38-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
