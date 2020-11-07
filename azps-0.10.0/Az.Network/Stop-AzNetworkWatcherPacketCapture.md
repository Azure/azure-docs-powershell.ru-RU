---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: c4d31de526132974defc6b3d28542e1ec8de4c67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910984"
---
# <span data-ttu-id="05dff-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="05dff-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="05dff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05dff-102">SYNOPSIS</span></span>
<span data-ttu-id="05dff-103">Остановка сеанса сбора запущенных пакетов</span><span class="sxs-lookup"><span data-stu-id="05dff-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="05dff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05dff-104">SYNTAX</span></span>

### <span data-ttu-id="05dff-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="05dff-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05dff-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="05dff-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05dff-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05dff-107">DESCRIPTION</span></span>
<span data-ttu-id="05dff-108">Stop-AzNetworkWatcherPacketCapture останавливает выполнение сеанса захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="05dff-108">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="05dff-109">После остановки сеанса файл записи пакетов загружается в хранилище и (или) локально хранится на виртуальной машине в зависимости от ее конфигурации.</span><span class="sxs-lookup"><span data-stu-id="05dff-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="05dff-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05dff-110">EXAMPLES</span></span>

### <span data-ttu-id="05dff-111">---Пример 1: остановка сеанса захвата пакетов---</span><span class="sxs-lookup"><span data-stu-id="05dff-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="05dff-112">В этом примере мы прерывать сеанс захвата запущенных пакетов с именем "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="05dff-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="05dff-113">После остановки сеанса файл записи пакетов загружается в хранилище и (или) локально хранится на виртуальной машине в зависимости от ее конфигурации.</span><span class="sxs-lookup"><span data-stu-id="05dff-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="05dff-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05dff-114">PARAMETERS</span></span>

### <span data-ttu-id="05dff-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05dff-115">-AsJob</span></span>
<span data-ttu-id="05dff-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="05dff-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05dff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05dff-117">-DefaultProfile</span></span>
<span data-ttu-id="05dff-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05dff-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05dff-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="05dff-119">-NetworkWatcher</span></span>
<span data-ttu-id="05dff-120">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="05dff-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="05dff-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="05dff-121">-NetworkWatcherName</span></span>
<span data-ttu-id="05dff-122">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="05dff-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="05dff-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="05dff-123">-PacketCaptureName</span></span>
<span data-ttu-id="05dff-124">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="05dff-124">The packet capture name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05dff-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05dff-125">-PassThru</span></span>
<span data-ttu-id="05dff-126">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="05dff-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="05dff-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05dff-127">-ResourceGroupName</span></span>
<span data-ttu-id="05dff-128">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="05dff-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="05dff-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05dff-129">-Confirm</span></span>
<span data-ttu-id="05dff-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="05dff-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05dff-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05dff-131">-WhatIf</span></span>
<span data-ttu-id="05dff-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="05dff-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05dff-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="05dff-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05dff-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05dff-134">CommonParameters</span></span>
<span data-ttu-id="05dff-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05dff-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05dff-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05dff-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05dff-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05dff-137">INPUTS</span></span>

### <span data-ttu-id="05dff-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="05dff-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="05dff-139">System. String</span><span class="sxs-lookup"><span data-stu-id="05dff-139">System.String</span></span>

## <span data-ttu-id="05dff-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05dff-140">OUTPUTS</span></span>

### <span data-ttu-id="05dff-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="05dff-141">System.Boolean</span></span>

## <span data-ttu-id="05dff-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="05dff-142">NOTES</span></span>
<span data-ttu-id="05dff-143">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик</span><span class="sxs-lookup"><span data-stu-id="05dff-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="05dff-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05dff-144">RELATED LINKS</span></span>

[<span data-ttu-id="05dff-145">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="05dff-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="05dff-146">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="05dff-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="05dff-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="05dff-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="05dff-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="05dff-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="05dff-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="05dff-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="05dff-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="05dff-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="05dff-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="05dff-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="05dff-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="05dff-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="05dff-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="05dff-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="05dff-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="05dff-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="05dff-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="05dff-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="05dff-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="05dff-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
