---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: e8ce107453a447ef2da4cb8528b2f3e1f24a3ebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562404"
---
# <span data-ttu-id="3950b-101">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3950b-101">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="3950b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3950b-102">SYNOPSIS</span></span>
<span data-ttu-id="3950b-103">Настраивает ведение журнала потока для целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="3950b-103">Configures flow logging for a target resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3950b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3950b-104">SYNTAX</span></span>

### <span data-ttu-id="3950b-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3950b-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3950b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3950b-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3950b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3950b-107">DESCRIPTION</span></span>
<span data-ttu-id="3950b-108">Set-AzureRmNetworkWatcherConfigFlowLog настраивает ведение журнала потока для целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="3950b-108">The Set-AzureRmNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="3950b-109">Свойства для настройки включают, включено ли ведение журнала потока для указанного ресурса, настроенной учетной записи хранения для отправки журналов и политики хранения для журналов.</span><span class="sxs-lookup"><span data-stu-id="3950b-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="3950b-110">Сетевые группы безопасности поддерживаются для ведения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="3950b-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="3950b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3950b-111">EXAMPLES</span></span>

### <span data-ttu-id="3950b-112">---Пример 1: Настройка ведения журнала потока для указанной NSG---</span><span class="sxs-lookup"><span data-stu-id="3950b-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
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

<span data-ttu-id="3950b-113">В этом примере мы настраиваем состояние ведения журнала для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="3950b-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="3950b-114">В ответе мы видим, что в указанном NSG включено ведение журнала потока, а политика хранения не задана.</span><span class="sxs-lookup"><span data-stu-id="3950b-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="3950b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3950b-115">PARAMETERS</span></span>

### <span data-ttu-id="3950b-116">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="3950b-116">-EnableFlowLog</span></span>
<span data-ttu-id="3950b-117">Пометка для включения и отключения ведения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="3950b-117">Flag to enable/disable flow logging.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3950b-118">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="3950b-118">-EnableRetention</span></span>
<span data-ttu-id="3950b-119">Пометка для включения и отключения хранения.</span><span class="sxs-lookup"><span data-stu-id="3950b-119">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3950b-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3950b-120">-NetworkWatcher</span></span>
<span data-ttu-id="3950b-121">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="3950b-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="3950b-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3950b-122">-NetworkWatcherName</span></span>
<span data-ttu-id="3950b-123">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="3950b-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="3950b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3950b-124">-ResourceGroupName</span></span>
<span data-ttu-id="3950b-125">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="3950b-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3950b-126">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="3950b-126">-RetentionInDays</span></span>
<span data-ttu-id="3950b-127">Количество дней для хранения записей журнала потока.</span><span class="sxs-lookup"><span data-stu-id="3950b-127">Number of days to retain flow log records.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3950b-128">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3950b-128">-StorageAccountId</span></span>
<span data-ttu-id="3950b-129">Идентификатор учетной записи хранения, которая используется для хранения журнала потока.</span><span class="sxs-lookup"><span data-stu-id="3950b-129">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="3950b-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="3950b-130">-TargetResourceId</span></span>
<span data-ttu-id="3950b-131">Идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="3950b-131">The target resource ID.</span></span>

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

### <span data-ttu-id="3950b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3950b-132">-Confirm</span></span>
<span data-ttu-id="3950b-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3950b-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3950b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3950b-134">-WhatIf</span></span>
<span data-ttu-id="3950b-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3950b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3950b-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3950b-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3950b-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3950b-137">-DefaultProfile</span></span>
<span data-ttu-id="3950b-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3950b-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3950b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3950b-139">CommonParameters</span></span>
<span data-ttu-id="3950b-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3950b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3950b-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3950b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3950b-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3950b-142">INPUTS</span></span>

### <span data-ttu-id="3950b-143">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3950b-143">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3950b-144">System. String System. Boolean System. Int32</span><span class="sxs-lookup"><span data-stu-id="3950b-144">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="3950b-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3950b-145">OUTPUTS</span></span>

### <span data-ttu-id="3950b-146">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="3950b-146">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="3950b-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="3950b-147">NOTES</span></span>
<span data-ttu-id="3950b-148">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель, поток, журналы, flowlog, ведение журнала</span><span class="sxs-lookup"><span data-stu-id="3950b-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="3950b-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3950b-149">RELATED LINKS</span></span>

[<span data-ttu-id="3950b-150">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3950b-150">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3950b-151">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3950b-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3950b-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3950b-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3950b-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3950b-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3950b-154">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3950b-154">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3950b-155">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3950b-155">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="3950b-156">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3950b-156">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3950b-157">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3950b-157">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3950b-158">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3950b-158">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3950b-159">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3950b-159">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="3950b-160">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3950b-160">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="3950b-161">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3950b-161">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3950b-162">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3950b-162">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="3950b-163">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3950b-163">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3950b-164">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3950b-164">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
