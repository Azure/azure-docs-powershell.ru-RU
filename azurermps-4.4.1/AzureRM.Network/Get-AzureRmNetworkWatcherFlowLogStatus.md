---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 1c7e67eacc52e995632a526514c84bf7a9f45425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567574"
---
# <span data-ttu-id="b1180-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b1180-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="b1180-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1180-102">SYNOPSIS</span></span>
<span data-ttu-id="b1180-103">Возвращает состояние регистрации потока для ресурса.</span><span class="sxs-lookup"><span data-stu-id="b1180-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1180-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1180-104">SYNTAX</span></span>

### <span data-ttu-id="b1180-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b1180-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1180-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b1180-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1180-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1180-107">DESCRIPTION</span></span>
<span data-ttu-id="b1180-108">Командлет Get-AzureRmNetworkWatcherFlowLogStatus возвращает состояние регистрации потока на ресурсе.</span><span class="sxs-lookup"><span data-stu-id="b1180-108">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="b1180-109">Состояние включает, включено ли ведение журнала потока для указанного ресурса, настроенной учетной записи хранения для отправки журналов и политики хранения для журналов.</span><span class="sxs-lookup"><span data-stu-id="b1180-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="b1180-110">Сетевые группы безопасности поддерживаются для ведения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="b1180-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="b1180-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1180-111">EXAMPLES</span></span>

### <span data-ttu-id="b1180-112">---Пример 1: получение состояния ведения журнала для указанной NSG---</span><span class="sxs-lookup"><span data-stu-id="b1180-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                   }
```

<span data-ttu-id="b1180-113">В этом примере мы получаем состояние ведения журнала потока для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="b1180-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="b1180-114">В указанном NSG включено ведение журнала потоков и не задана политика хранения.</span><span class="sxs-lookup"><span data-stu-id="b1180-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="b1180-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1180-115">PARAMETERS</span></span>

### <span data-ttu-id="b1180-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b1180-116">-NetworkWatcher</span></span>
<span data-ttu-id="b1180-117">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="b1180-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="b1180-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b1180-118">-NetworkWatcherName</span></span>
<span data-ttu-id="b1180-119">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="b1180-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="b1180-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1180-120">-ResourceGroupName</span></span>
<span data-ttu-id="b1180-121">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="b1180-121">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b1180-122">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b1180-122">-TargetResourceId</span></span>
<span data-ttu-id="b1180-123">Идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="b1180-123">The target resource ID.</span></span>

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

### <span data-ttu-id="b1180-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1180-124">-DefaultProfile</span></span>
<span data-ttu-id="b1180-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1180-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1180-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1180-126">CommonParameters</span></span>
<span data-ttu-id="b1180-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1180-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1180-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1180-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1180-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1180-129">INPUTS</span></span>

### <span data-ttu-id="b1180-130">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b1180-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="b1180-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b1180-131">System.String</span></span>

## <span data-ttu-id="b1180-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1180-132">OUTPUTS</span></span>

### <span data-ttu-id="b1180-133">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="b1180-133">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="b1180-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1180-134">NOTES</span></span>
<span data-ttu-id="b1180-135">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель, поток, журналы, flowlog, ведение журнала</span><span class="sxs-lookup"><span data-stu-id="b1180-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="b1180-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1180-136">RELATED LINKS</span></span>

[<span data-ttu-id="b1180-137">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b1180-137">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b1180-138">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b1180-138">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b1180-139">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b1180-139">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b1180-140">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b1180-140">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b1180-141">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b1180-141">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b1180-142">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b1180-142">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="b1180-143">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b1180-143">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b1180-144">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b1180-144">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b1180-145">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b1180-145">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b1180-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b1180-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="b1180-147">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b1180-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="b1180-148">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b1180-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b1180-149">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b1180-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="b1180-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b1180-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b1180-151">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b1180-151">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
