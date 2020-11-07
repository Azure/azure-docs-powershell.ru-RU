---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: f250615837f4953f63a4c5ff5f0a0ea965691856
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911026"
---
# <span data-ttu-id="3a20f-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3a20f-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="3a20f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a20f-102">SYNOPSIS</span></span>
<span data-ttu-id="3a20f-103">Настраивает ведение журнала потока для целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="3a20f-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="3a20f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a20f-104">SYNTAX</span></span>

### <span data-ttu-id="3a20f-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3a20f-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a20f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3a20f-106">SetByName</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a20f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a20f-107">DESCRIPTION</span></span>
<span data-ttu-id="3a20f-108">Set-AzNetworkWatcherConfigFlowLog настраивает ведение журнала потока для целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="3a20f-108">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="3a20f-109">Свойства для настройки включают, включено ли ведение журнала потока для указанного ресурса, настроенной учетной записи хранения для отправки журналов и политики хранения для журналов.</span><span class="sxs-lookup"><span data-stu-id="3a20f-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="3a20f-110">Сетевые группы безопасности поддерживаются для ведения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="3a20f-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="3a20f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a20f-111">EXAMPLES</span></span>

### <span data-ttu-id="3a20f-112">---Пример 1: Настройка ведения журнала потока для указанной NSG---</span><span class="sxs-lookup"><span data-stu-id="3a20f-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="3a20f-113">В этом примере мы настраиваем состояние ведения журнала для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="3a20f-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="3a20f-114">В ответе мы видим, что в указанном NSG включено ведение журнала потока, а политика хранения не задана.</span><span class="sxs-lookup"><span data-stu-id="3a20f-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="3a20f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a20f-115">PARAMETERS</span></span>

### <span data-ttu-id="3a20f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a20f-116">-AsJob</span></span>
<span data-ttu-id="3a20f-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3a20f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a20f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a20f-118">-DefaultProfile</span></span>
<span data-ttu-id="3a20f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a20f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a20f-120">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="3a20f-120">-EnableFlowLog</span></span>
<span data-ttu-id="3a20f-121">Пометка для включения и отключения ведения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="3a20f-121">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a20f-122">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="3a20f-122">-EnableRetention</span></span>
<span data-ttu-id="3a20f-123">Пометка для включения и отключения хранения.</span><span class="sxs-lookup"><span data-stu-id="3a20f-123">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a20f-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3a20f-124">-NetworkWatcher</span></span>
<span data-ttu-id="3a20f-125">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="3a20f-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="3a20f-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3a20f-126">-NetworkWatcherName</span></span>
<span data-ttu-id="3a20f-127">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="3a20f-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="3a20f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a20f-128">-ResourceGroupName</span></span>
<span data-ttu-id="3a20f-129">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="3a20f-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3a20f-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="3a20f-130">-RetentionInDays</span></span>
<span data-ttu-id="3a20f-131">Количество дней для хранения записей журнала потока.</span><span class="sxs-lookup"><span data-stu-id="3a20f-131">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="3a20f-132">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3a20f-132">-StorageAccountId</span></span>
<span data-ttu-id="3a20f-133">Идентификатор учетной записи хранения, которая используется для хранения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="3a20f-133">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="3a20f-134">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="3a20f-134">-TargetResourceId</span></span>
<span data-ttu-id="3a20f-135">Идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="3a20f-135">The target resource ID.</span></span>

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

### <span data-ttu-id="3a20f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a20f-136">-Confirm</span></span>
<span data-ttu-id="3a20f-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3a20f-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a20f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a20f-138">-WhatIf</span></span>
<span data-ttu-id="3a20f-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3a20f-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a20f-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3a20f-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a20f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a20f-141">CommonParameters</span></span>
<span data-ttu-id="3a20f-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a20f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a20f-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a20f-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a20f-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a20f-144">INPUTS</span></span>

### <span data-ttu-id="3a20f-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3a20f-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3a20f-146">System. String System. Boolean System. Int32</span><span class="sxs-lookup"><span data-stu-id="3a20f-146">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="3a20f-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a20f-147">OUTPUTS</span></span>

### <span data-ttu-id="3a20f-148">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="3a20f-148">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="3a20f-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a20f-149">NOTES</span></span>
<span data-ttu-id="3a20f-150">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель, поток, журналы, flowlog, ведение журнала</span><span class="sxs-lookup"><span data-stu-id="3a20f-150">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="3a20f-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a20f-151">RELATED LINKS</span></span>

[<span data-ttu-id="3a20f-152">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3a20f-152">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3a20f-153">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3a20f-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3a20f-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3a20f-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3a20f-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3a20f-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3a20f-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3a20f-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3a20f-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3a20f-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3a20f-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3a20f-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3a20f-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3a20f-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3a20f-160">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3a20f-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3a20f-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3a20f-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3a20f-162">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3a20f-162">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3a20f-163">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3a20f-163">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3a20f-164">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3a20f-164">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3a20f-165">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3a20f-165">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3a20f-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3a20f-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
