---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: f220f029b25963fa07d582b6ddd70b572791924a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568317"
---
# <span data-ttu-id="a8bb6-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a8bb6-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="a8bb6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="a8bb6-103">Запуск устранения неполадок в сетевом ресурсе в Azure.</span><span class="sxs-lookup"><span data-stu-id="a8bb6-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8bb6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8bb6-104">SYNTAX</span></span>

### <span data-ttu-id="a8bb6-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a8bb6-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8bb6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a8bb6-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8bb6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8bb6-107">DESCRIPTION</span></span>
<span data-ttu-id="a8bb6-108">Командлет Start-AzureRmNetworkWatcherResourceTroubleshooting запускает устранение неполадок для сетевых ресурсов в Azure и возвращает сведения о возможных проблемах и снижении риска.</span><span class="sxs-lookup"><span data-stu-id="a8bb6-108">The Start-AzureRmNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="a8bb6-109">В настоящее время поддерживаются шлюзы и соединения виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="a8bb6-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="a8bb6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8bb6-110">EXAMPLES</span></span>

### <span data-ttu-id="a8bb6-111">---Пример 1: запуск устранения неполадок на шлюзе виртуальной сети---</span><span class="sxs-lookup"><span data-stu-id="a8bb6-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="a8bb6-112">В приведенном выше примере начинается устранение неполадок шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a8bb6-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="a8bb6-113">Выполнение операции может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="a8bb6-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="a8bb6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8bb6-114">PARAMETERS</span></span>

### <span data-ttu-id="a8bb6-115">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a8bb6-115">-NetworkWatcher</span></span>
<span data-ttu-id="a8bb6-116">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="a8bb6-116">The network watcher resource.</span></span>

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

### <span data-ttu-id="a8bb6-117">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a8bb6-117">-NetworkWatcherName</span></span>
<span data-ttu-id="a8bb6-118">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="a8bb6-118">The name of network watcher.</span></span>

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

### <span data-ttu-id="a8bb6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8bb6-119">-ResourceGroupName</span></span>
<span data-ttu-id="a8bb6-120">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="a8bb6-120">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a8bb6-121">-StorageId</span><span class="sxs-lookup"><span data-stu-id="a8bb6-121">-StorageId</span></span>
<span data-ttu-id="a8bb6-122">Идентификатор хранилища.</span><span class="sxs-lookup"><span data-stu-id="a8bb6-122">The storage ID.</span></span>

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

### <span data-ttu-id="a8bb6-123">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="a8bb6-123">-StoragePath</span></span>
<span data-ttu-id="a8bb6-124">Путь к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="a8bb6-124">The storage path.</span></span>

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

### <span data-ttu-id="a8bb6-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a8bb6-125">-TargetResourceId</span></span>
<span data-ttu-id="a8bb6-126">Указывает идентификатор ресурса для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="a8bb6-126">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="a8bb6-127">Пример формата: "/Subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="a8bb6-127">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="a8bb6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8bb6-128">-DefaultProfile</span></span>
<span data-ttu-id="a8bb6-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8bb6-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8bb6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8bb6-130">CommonParameters</span></span>
<span data-ttu-id="a8bb6-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8bb6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8bb6-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8bb6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8bb6-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8bb6-133">INPUTS</span></span>

### <span data-ttu-id="a8bb6-134">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a8bb6-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a8bb6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a8bb6-135">System.String</span></span>

## <span data-ttu-id="a8bb6-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8bb6-136">OUTPUTS</span></span>

### <span data-ttu-id="a8bb6-137">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="a8bb6-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="a8bb6-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8bb6-138">NOTES</span></span>
<span data-ttu-id="a8bb6-139">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, устранение неполадок, VPN, подключение</span><span class="sxs-lookup"><span data-stu-id="a8bb6-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="a8bb6-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8bb6-140">RELATED LINKS</span></span>

[<span data-ttu-id="a8bb6-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a8bb6-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a8bb6-142">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a8bb6-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a8bb6-143">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a8bb6-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a8bb6-144">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a8bb6-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a8bb6-145">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a8bb6-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a8bb6-146">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a8bb6-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="a8bb6-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a8bb6-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a8bb6-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a8bb6-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a8bb6-149">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a8bb6-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a8bb6-150">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a8bb6-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="a8bb6-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a8bb6-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="a8bb6-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a8bb6-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a8bb6-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a8bb6-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
