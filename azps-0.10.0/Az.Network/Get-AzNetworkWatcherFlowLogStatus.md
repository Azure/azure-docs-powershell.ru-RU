---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 2f855175065f743bdfec5fb8dc9c917af262b05b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909917"
---
# <span data-ttu-id="01a66-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="01a66-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="01a66-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01a66-102">SYNOPSIS</span></span>
<span data-ttu-id="01a66-103">Возвращает состояние регистрации потока для ресурса.</span><span class="sxs-lookup"><span data-stu-id="01a66-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="01a66-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01a66-104">SYNTAX</span></span>

### <span data-ttu-id="01a66-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="01a66-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01a66-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="01a66-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01a66-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01a66-107">DESCRIPTION</span></span>
<span data-ttu-id="01a66-108">Командлет Get-AzNetworkWatcherFlowLogStatus возвращает состояние регистрации потока на ресурсе.</span><span class="sxs-lookup"><span data-stu-id="01a66-108">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="01a66-109">Состояние включает, включено ли ведение журнала потока для указанного ресурса, настроенной учетной записи хранения для отправки журналов и политики хранения для журналов.</span><span class="sxs-lookup"><span data-stu-id="01a66-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="01a66-110">Сетевые группы безопасности поддерживаются для ведения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="01a66-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="01a66-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01a66-111">EXAMPLES</span></span>

### <span data-ttu-id="01a66-112">---Пример 1: получение состояния ведения журнала для указанной NSG---</span><span class="sxs-lookup"><span data-stu-id="01a66-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

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

<span data-ttu-id="01a66-113">В этом примере мы получаем состояние ведения журнала потока для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="01a66-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="01a66-114">В указанном NSG включено ведение журнала потоков и не задана политика хранения.</span><span class="sxs-lookup"><span data-stu-id="01a66-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="01a66-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01a66-115">PARAMETERS</span></span>

### <span data-ttu-id="01a66-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01a66-116">-AsJob</span></span>
<span data-ttu-id="01a66-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="01a66-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01a66-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a66-118">-DefaultProfile</span></span>
<span data-ttu-id="01a66-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01a66-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01a66-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="01a66-120">-NetworkWatcher</span></span>
<span data-ttu-id="01a66-121">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="01a66-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="01a66-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="01a66-122">-NetworkWatcherName</span></span>
<span data-ttu-id="01a66-123">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="01a66-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="01a66-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01a66-124">-ResourceGroupName</span></span>
<span data-ttu-id="01a66-125">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="01a66-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="01a66-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="01a66-126">-TargetResourceId</span></span>
<span data-ttu-id="01a66-127">Идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="01a66-127">The target resource ID.</span></span>

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

### <span data-ttu-id="01a66-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01a66-128">CommonParameters</span></span>
<span data-ttu-id="01a66-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01a66-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01a66-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01a66-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01a66-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01a66-131">INPUTS</span></span>

### <span data-ttu-id="01a66-132">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="01a66-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="01a66-133">System. String</span><span class="sxs-lookup"><span data-stu-id="01a66-133">System.String</span></span>

## <span data-ttu-id="01a66-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01a66-134">OUTPUTS</span></span>

### <span data-ttu-id="01a66-135">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="01a66-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="01a66-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="01a66-136">NOTES</span></span>
<span data-ttu-id="01a66-137">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель, поток, журналы, flowlog, ведение журнала</span><span class="sxs-lookup"><span data-stu-id="01a66-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="01a66-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01a66-138">RELATED LINKS</span></span>

[<span data-ttu-id="01a66-139">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="01a66-139">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="01a66-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="01a66-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="01a66-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="01a66-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="01a66-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="01a66-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="01a66-143">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="01a66-143">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="01a66-144">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="01a66-144">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="01a66-145">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="01a66-145">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="01a66-146">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="01a66-146">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="01a66-147">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="01a66-147">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="01a66-148">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="01a66-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="01a66-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="01a66-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="01a66-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="01a66-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="01a66-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="01a66-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="01a66-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="01a66-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="01a66-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="01a66-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
