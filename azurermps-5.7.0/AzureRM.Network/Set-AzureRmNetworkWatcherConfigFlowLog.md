---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 3c918b36bf851d34f8f10541de5cbf0de1a595cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568231"
---
# <span data-ttu-id="eaeed-101">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="eaeed-101">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="eaeed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eaeed-102">SYNOPSIS</span></span>
<span data-ttu-id="eaeed-103">Настраивает ведение журнала потока для целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="eaeed-103">Configures flow logging for a target resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaeed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eaeed-104">SYNTAX</span></span>

### <span data-ttu-id="eaeed-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eaeed-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaeed-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="eaeed-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eaeed-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eaeed-107">DESCRIPTION</span></span>
<span data-ttu-id="eaeed-108">Set-AzureRmNetworkWatcherConfigFlowLog настраивает ведение журнала потока для целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="eaeed-108">The Set-AzureRmNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="eaeed-109">Свойства для настройки включают, включено ли ведение журнала потока для указанного ресурса, настроенной учетной записи хранения для отправки журналов и политики хранения для журналов.</span><span class="sxs-lookup"><span data-stu-id="eaeed-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="eaeed-110">Сетевые группы безопасности поддерживаются для ведения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="eaeed-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="eaeed-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eaeed-111">EXAMPLES</span></span>

### <span data-ttu-id="eaeed-112">---Пример 1: Настройка ведения журнала потока для указанной NSG---</span><span class="sxs-lookup"><span data-stu-id="eaeed-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="eaeed-113">В этом примере мы настраиваем состояние ведения журнала для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="eaeed-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="eaeed-114">В ответе мы видим, что в указанном NSG включено ведение журнала потока, а политика хранения не задана.</span><span class="sxs-lookup"><span data-stu-id="eaeed-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="eaeed-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eaeed-115">PARAMETERS</span></span>

### <span data-ttu-id="eaeed-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eaeed-116">-AsJob</span></span>
<span data-ttu-id="eaeed-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="eaeed-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eaeed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaeed-118">-DefaultProfile</span></span>
<span data-ttu-id="eaeed-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eaeed-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaeed-120">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="eaeed-120">-EnableFlowLog</span></span>
<span data-ttu-id="eaeed-121">Пометка для включения и отключения ведения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="eaeed-121">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="eaeed-122">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="eaeed-122">-EnableRetention</span></span>
<span data-ttu-id="eaeed-123">Пометка для включения и отключения хранения.</span><span class="sxs-lookup"><span data-stu-id="eaeed-123">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="eaeed-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eaeed-124">-NetworkWatcher</span></span>
<span data-ttu-id="eaeed-125">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="eaeed-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="eaeed-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="eaeed-126">-NetworkWatcherName</span></span>
<span data-ttu-id="eaeed-127">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="eaeed-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="eaeed-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaeed-128">-ResourceGroupName</span></span>
<span data-ttu-id="eaeed-129">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="eaeed-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="eaeed-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="eaeed-130">-RetentionInDays</span></span>
<span data-ttu-id="eaeed-131">Количество дней для хранения записей журнала потока.</span><span class="sxs-lookup"><span data-stu-id="eaeed-131">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="eaeed-132">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="eaeed-132">-StorageAccountId</span></span>
<span data-ttu-id="eaeed-133">Идентификатор учетной записи хранения, которая используется для хранения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="eaeed-133">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="eaeed-134">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="eaeed-134">-TargetResourceId</span></span>
<span data-ttu-id="eaeed-135">Идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="eaeed-135">The target resource ID.</span></span>

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

### <span data-ttu-id="eaeed-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eaeed-136">-Confirm</span></span>
<span data-ttu-id="eaeed-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eaeed-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaeed-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaeed-138">-WhatIf</span></span>
<span data-ttu-id="eaeed-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eaeed-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eaeed-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eaeed-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaeed-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaeed-141">CommonParameters</span></span>
<span data-ttu-id="eaeed-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eaeed-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaeed-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaeed-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaeed-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eaeed-144">INPUTS</span></span>

### <span data-ttu-id="eaeed-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eaeed-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="eaeed-146">System. String System. Boolean System. Int32</span><span class="sxs-lookup"><span data-stu-id="eaeed-146">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="eaeed-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eaeed-147">OUTPUTS</span></span>

### <span data-ttu-id="eaeed-148">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="eaeed-148">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="eaeed-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="eaeed-149">NOTES</span></span>
<span data-ttu-id="eaeed-150">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель, поток, журналы, flowlog, ведение журнала</span><span class="sxs-lookup"><span data-stu-id="eaeed-150">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="eaeed-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eaeed-151">RELATED LINKS</span></span>

[<span data-ttu-id="eaeed-152">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="eaeed-152">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="eaeed-153">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eaeed-153">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="eaeed-154">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eaeed-154">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="eaeed-155">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eaeed-155">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="eaeed-156">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="eaeed-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="eaeed-157">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="eaeed-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="eaeed-158">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="eaeed-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="eaeed-159">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="eaeed-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="eaeed-160">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="eaeed-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="eaeed-161">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="eaeed-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="eaeed-162">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="eaeed-162">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="eaeed-163">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="eaeed-163">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="eaeed-164">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="eaeed-164">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="eaeed-165">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="eaeed-165">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="eaeed-166">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="eaeed-166">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
