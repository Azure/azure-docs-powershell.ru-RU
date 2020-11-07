---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: 5f2b2bf738c4e83f8f8f3854e831601ea23c7d8e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913568"
---
# <span data-ttu-id="da010-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da010-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="da010-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da010-102">SYNOPSIS</span></span>
<span data-ttu-id="da010-103">Остановка сеанса сбора запущенных пакетов</span><span class="sxs-lookup"><span data-stu-id="da010-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da010-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da010-104">SYNTAX</span></span>

### <span data-ttu-id="da010-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da010-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da010-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="da010-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da010-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da010-107">DESCRIPTION</span></span>
<span data-ttu-id="da010-108">Stop-AzureRmNetworkWatcherPacketCapture останавливает выполнение сеанса захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="da010-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="da010-109">После остановки сеанса файл записи пакетов загружается в хранилище и (или) локально хранится на виртуальной машине в зависимости от ее конфигурации.</span><span class="sxs-lookup"><span data-stu-id="da010-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="da010-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da010-110">EXAMPLES</span></span>

### <span data-ttu-id="da010-111">---Пример 1: остановка сеанса захвата пакетов---</span><span class="sxs-lookup"><span data-stu-id="da010-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="da010-112">В этом примере мы прерывать сеанс захвата запущенных пакетов с именем "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="da010-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="da010-113">После остановки сеанса файл записи пакетов загружается в хранилище и (или) локально хранится на виртуальной машине в зависимости от ее конфигурации.</span><span class="sxs-lookup"><span data-stu-id="da010-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="da010-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da010-114">PARAMETERS</span></span>

### <span data-ttu-id="da010-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da010-115">-AsJob</span></span>
<span data-ttu-id="da010-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="da010-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da010-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da010-117">-DefaultProfile</span></span>
<span data-ttu-id="da010-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da010-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da010-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da010-119">-NetworkWatcher</span></span>
<span data-ttu-id="da010-120">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="da010-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="da010-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="da010-121">-NetworkWatcherName</span></span>
<span data-ttu-id="da010-122">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="da010-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="da010-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="da010-123">-PacketCaptureName</span></span>
<span data-ttu-id="da010-124">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="da010-124">The packet capture name.</span></span>

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

### <span data-ttu-id="da010-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da010-125">-PassThru</span></span>
<span data-ttu-id="da010-126">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="da010-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="da010-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da010-127">-ResourceGroupName</span></span>
<span data-ttu-id="da010-128">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="da010-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="da010-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da010-129">-Confirm</span></span>
<span data-ttu-id="da010-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="da010-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da010-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da010-131">-WhatIf</span></span>
<span data-ttu-id="da010-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="da010-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da010-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="da010-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da010-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da010-134">CommonParameters</span></span>
<span data-ttu-id="da010-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da010-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da010-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da010-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da010-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da010-137">INPUTS</span></span>

### <span data-ttu-id="da010-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da010-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="da010-139">System. String</span><span class="sxs-lookup"><span data-stu-id="da010-139">System.String</span></span>

## <span data-ttu-id="da010-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da010-140">OUTPUTS</span></span>

### <span data-ttu-id="da010-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da010-141">System.Boolean</span></span>

## <span data-ttu-id="da010-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="da010-142">NOTES</span></span>
<span data-ttu-id="da010-143">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик</span><span class="sxs-lookup"><span data-stu-id="da010-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="da010-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da010-144">RELATED LINKS</span></span>

[<span data-ttu-id="da010-145">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da010-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="da010-146">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="da010-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="da010-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da010-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="da010-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da010-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="da010-149">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da010-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="da010-150">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da010-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="da010-151">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da010-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="da010-152">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="da010-152">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="da010-153">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="da010-153">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="da010-154">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="da010-154">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="da010-155">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="da010-155">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="da010-156">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="da010-156">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
