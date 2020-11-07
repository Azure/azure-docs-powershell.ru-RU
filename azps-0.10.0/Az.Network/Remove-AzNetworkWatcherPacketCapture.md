---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: b3095aace7fa8e1959e51ef64aa92b6d2bcaffba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911123"
---
# <span data-ttu-id="da350-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da350-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="da350-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da350-102">SYNOPSIS</span></span>
<span data-ttu-id="da350-103">Удаляет ресурс захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="da350-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="da350-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da350-104">SYNTAX</span></span>

### <span data-ttu-id="da350-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da350-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da350-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="da350-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da350-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da350-107">DESCRIPTION</span></span>
<span data-ttu-id="da350-108">Remove-AzNetworkWatcherPacketCapture удаляет ресурс захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="da350-108">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="da350-109">Рекомендуется вызвать Stop-AzNetworkWatcherPacketCapture перед вызовом Remove-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="da350-109">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="da350-110">Если сеанс захвата пакетов выполняется при вызове Remove-AzNetworkWatcherPacketCapture, возможно, захват пакетов не сохранен.</span><span class="sxs-lookup"><span data-stu-id="da350-110">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="da350-111">Если сеанс остановлен до удаления файла. Cap, содержащего данные захвата, они не удаляются.</span><span class="sxs-lookup"><span data-stu-id="da350-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="da350-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da350-112">EXAMPLES</span></span>

### <span data-ttu-id="da350-113">---Пример 1: Удаление сеанса захвата пакетов--</span><span class="sxs-lookup"><span data-stu-id="da350-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="da350-114">В этом примере мы удалим существующий сеанс захвата пакетов с именем "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="da350-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="da350-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da350-115">PARAMETERS</span></span>

### <span data-ttu-id="da350-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da350-116">-AsJob</span></span>
<span data-ttu-id="da350-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="da350-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da350-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da350-118">-DefaultProfile</span></span>
<span data-ttu-id="da350-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da350-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da350-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da350-120">-NetworkWatcher</span></span>
<span data-ttu-id="da350-121">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="da350-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="da350-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="da350-122">-NetworkWatcherName</span></span>
<span data-ttu-id="da350-123">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="da350-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="da350-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="da350-124">-PacketCaptureName</span></span>
<span data-ttu-id="da350-125">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="da350-125">The packet capture name.</span></span>

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

### <span data-ttu-id="da350-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da350-126">-PassThru</span></span>
<span data-ttu-id="da350-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="da350-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="da350-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da350-128">-ResourceGroupName</span></span>
<span data-ttu-id="da350-129">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="da350-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="da350-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da350-130">-Confirm</span></span>
<span data-ttu-id="da350-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="da350-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da350-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da350-132">-WhatIf</span></span>
<span data-ttu-id="da350-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="da350-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da350-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="da350-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da350-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da350-135">CommonParameters</span></span>
<span data-ttu-id="da350-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da350-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da350-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da350-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da350-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da350-138">INPUTS</span></span>

### <span data-ttu-id="da350-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da350-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="da350-140">System. String</span><span class="sxs-lookup"><span data-stu-id="da350-140">System.String</span></span>

## <span data-ttu-id="da350-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da350-141">OUTPUTS</span></span>

### <span data-ttu-id="da350-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="da350-142">System.Object</span></span>

## <span data-ttu-id="da350-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="da350-143">NOTES</span></span>
<span data-ttu-id="da350-144">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик, удаление</span><span class="sxs-lookup"><span data-stu-id="da350-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="da350-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da350-145">RELATED LINKS</span></span>

[<span data-ttu-id="da350-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da350-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="da350-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="da350-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="da350-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da350-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="da350-149">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da350-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="da350-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da350-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="da350-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da350-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="da350-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da350-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="da350-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="da350-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="da350-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="da350-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="da350-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="da350-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="da350-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="da350-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="da350-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="da350-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
