---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 034cca094bf6dd7d3911e3e705e03888f0ea10ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568236"
---
# <span data-ttu-id="27647-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="27647-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="27647-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27647-102">SYNOPSIS</span></span>
<span data-ttu-id="27647-103">Удаляет ресурс захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="27647-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27647-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27647-104">SYNTAX</span></span>

### <span data-ttu-id="27647-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27647-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27647-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="27647-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27647-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27647-107">DESCRIPTION</span></span>
<span data-ttu-id="27647-108">Remove-AzureRmNetworkWatcherPacketCapture удаляет ресурс захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="27647-108">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="27647-109">Рекомендуется вызвать Stop-AzureRmNetworkWatcherPacketCapture перед вызовом Remove-AzureRmNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="27647-109">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="27647-110">Если сеанс захвата пакетов выполняется при вызове Remove-AzureRmNetworkWatcherPacketCapture, возможно, захват пакетов не сохранен.</span><span class="sxs-lookup"><span data-stu-id="27647-110">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="27647-111">Если сеанс остановлен до удаления файла. Cap, содержащего данные захвата, они не удаляются.</span><span class="sxs-lookup"><span data-stu-id="27647-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="27647-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27647-112">EXAMPLES</span></span>

### <span data-ttu-id="27647-113">---Пример 1: Удаление сеанса захвата пакетов--</span><span class="sxs-lookup"><span data-stu-id="27647-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="27647-114">В этом примере мы удалим существующий сеанс захвата пакетов с именем "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="27647-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="27647-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27647-115">PARAMETERS</span></span>

### <span data-ttu-id="27647-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27647-116">-AsJob</span></span>
<span data-ttu-id="27647-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="27647-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27647-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27647-118">-DefaultProfile</span></span>
<span data-ttu-id="27647-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27647-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27647-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="27647-120">-NetworkWatcher</span></span>
<span data-ttu-id="27647-121">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="27647-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="27647-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="27647-122">-NetworkWatcherName</span></span>
<span data-ttu-id="27647-123">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="27647-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="27647-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="27647-124">-PacketCaptureName</span></span>
<span data-ttu-id="27647-125">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="27647-125">The packet capture name.</span></span>

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

### <span data-ttu-id="27647-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27647-126">-PassThru</span></span>
<span data-ttu-id="27647-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="27647-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27647-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27647-128">-ResourceGroupName</span></span>
<span data-ttu-id="27647-129">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="27647-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="27647-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27647-130">-Confirm</span></span>
<span data-ttu-id="27647-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="27647-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27647-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27647-132">-WhatIf</span></span>
<span data-ttu-id="27647-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="27647-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27647-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="27647-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27647-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27647-135">CommonParameters</span></span>
<span data-ttu-id="27647-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27647-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27647-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27647-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27647-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27647-138">INPUTS</span></span>

### <span data-ttu-id="27647-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="27647-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="27647-140">System. String</span><span class="sxs-lookup"><span data-stu-id="27647-140">System.String</span></span>

## <span data-ttu-id="27647-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27647-141">OUTPUTS</span></span>

### <span data-ttu-id="27647-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="27647-142">System.Object</span></span>

## <span data-ttu-id="27647-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="27647-143">NOTES</span></span>
<span data-ttu-id="27647-144">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик, удаление</span><span class="sxs-lookup"><span data-stu-id="27647-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="27647-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27647-145">RELATED LINKS</span></span>

[<span data-ttu-id="27647-146">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="27647-146">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="27647-147">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="27647-147">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="27647-148">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="27647-148">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="27647-149">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="27647-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="27647-150">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="27647-150">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="27647-151">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="27647-151">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="27647-152">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="27647-152">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="27647-153">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="27647-153">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="27647-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="27647-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="27647-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="27647-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="27647-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="27647-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="27647-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="27647-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
