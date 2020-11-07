---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherflowlogstatus
schema: 2.0.0
ms.openlocfilehash: 96d3bea781b0c595b54387a9b07b085f173d7b0a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913617"
---
# <span data-ttu-id="5274f-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5274f-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="5274f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5274f-102">SYNOPSIS</span></span>
<span data-ttu-id="5274f-103">Возвращает состояние регистрации потока для ресурса.</span><span class="sxs-lookup"><span data-stu-id="5274f-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5274f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5274f-104">SYNTAX</span></span>

### <span data-ttu-id="5274f-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5274f-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5274f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5274f-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5274f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5274f-107">DESCRIPTION</span></span>
<span data-ttu-id="5274f-108">Командлет Get-AzureRmNetworkWatcherFlowLogStatus возвращает состояние регистрации потока на ресурсе.</span><span class="sxs-lookup"><span data-stu-id="5274f-108">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="5274f-109">Состояние включает, включено ли ведение журнала потока для указанного ресурса, настроенной учетной записи хранения для отправки журналов и политики хранения для журналов.</span><span class="sxs-lookup"><span data-stu-id="5274f-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="5274f-110">Сетевые группы безопасности поддерживаются для ведения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="5274f-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="5274f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5274f-111">EXAMPLES</span></span>

### <span data-ttu-id="5274f-112">---Пример 1: получение состояния ведения журнала для указанной NSG---</span><span class="sxs-lookup"><span data-stu-id="5274f-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
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

<span data-ttu-id="5274f-113">В этом примере мы получаем состояние ведения журнала потока для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="5274f-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="5274f-114">В указанном NSG включено ведение журнала потоков и не задана политика хранения.</span><span class="sxs-lookup"><span data-stu-id="5274f-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="5274f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5274f-115">PARAMETERS</span></span>

### <span data-ttu-id="5274f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5274f-116">-AsJob</span></span>
<span data-ttu-id="5274f-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5274f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5274f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5274f-118">-DefaultProfile</span></span>
<span data-ttu-id="5274f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5274f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5274f-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5274f-120">-NetworkWatcher</span></span>
<span data-ttu-id="5274f-121">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="5274f-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="5274f-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5274f-122">-NetworkWatcherName</span></span>
<span data-ttu-id="5274f-123">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="5274f-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="5274f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5274f-124">-ResourceGroupName</span></span>
<span data-ttu-id="5274f-125">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="5274f-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5274f-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="5274f-126">-TargetResourceId</span></span>
<span data-ttu-id="5274f-127">Идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="5274f-127">The target resource ID.</span></span>

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

### <span data-ttu-id="5274f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5274f-128">CommonParameters</span></span>
<span data-ttu-id="5274f-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5274f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5274f-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5274f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5274f-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5274f-131">INPUTS</span></span>

### <span data-ttu-id="5274f-132">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5274f-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5274f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5274f-133">System.String</span></span>

## <span data-ttu-id="5274f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5274f-134">OUTPUTS</span></span>

### <span data-ttu-id="5274f-135">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="5274f-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="5274f-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="5274f-136">NOTES</span></span>
<span data-ttu-id="5274f-137">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель, поток, журналы, flowlog, ведение журнала</span><span class="sxs-lookup"><span data-stu-id="5274f-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="5274f-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5274f-138">RELATED LINKS</span></span>

[<span data-ttu-id="5274f-139">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5274f-139">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5274f-140">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5274f-140">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5274f-141">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5274f-141">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5274f-142">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5274f-142">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5274f-143">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5274f-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5274f-144">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5274f-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="5274f-145">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5274f-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5274f-146">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5274f-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5274f-147">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5274f-147">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5274f-148">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5274f-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="5274f-149">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5274f-149">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="5274f-150">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5274f-150">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5274f-151">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5274f-151">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="5274f-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5274f-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5274f-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5274f-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
