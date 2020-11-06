---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 3f1206b79f8e80793106b1e294b591e21b9fb77d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559600"
---
# <span data-ttu-id="03554-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="03554-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="03554-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03554-102">SYNOPSIS</span></span>
<span data-ttu-id="03554-103">Остановка сеанса сбора запущенных пакетов</span><span class="sxs-lookup"><span data-stu-id="03554-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03554-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03554-104">SYNTAX</span></span>

### <span data-ttu-id="03554-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="03554-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03554-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="03554-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03554-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03554-107">DESCRIPTION</span></span>
<span data-ttu-id="03554-108">Stop-AzureRmNetworkWatcherPacketCapture останавливает выполнение сеанса захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="03554-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="03554-109">После остановки сеанса файл записи пакетов загружается в хранилище и (или) локально хранится на виртуальной машине в зависимости от ее конфигурации.</span><span class="sxs-lookup"><span data-stu-id="03554-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="03554-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03554-110">EXAMPLES</span></span>

### <span data-ttu-id="03554-111">---Пример 1: остановка сеанса захвата пакетов---</span><span class="sxs-lookup"><span data-stu-id="03554-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="03554-112">В этом примере мы прерывать сеанс захвата запущенных пакетов с именем "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="03554-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="03554-113">После остановки сеанса файл записи пакетов загружается в хранилище и (или) локально хранится на виртуальной машине в зависимости от ее конфигурации.</span><span class="sxs-lookup"><span data-stu-id="03554-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="03554-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03554-114">PARAMETERS</span></span>

### <span data-ttu-id="03554-115">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03554-115">-NetworkWatcher</span></span>
<span data-ttu-id="03554-116">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="03554-116">The network watcher resource.</span></span>

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

### <span data-ttu-id="03554-117">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="03554-117">-NetworkWatcherName</span></span>
<span data-ttu-id="03554-118">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="03554-118">The name of network watcher.</span></span>

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

### <span data-ttu-id="03554-119">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="03554-119">-PacketCaptureName</span></span>
<span data-ttu-id="03554-120">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="03554-120">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03554-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03554-121">-PassThru</span></span>
<span data-ttu-id="03554-122">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="03554-122">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03554-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03554-123">-ResourceGroupName</span></span>
<span data-ttu-id="03554-124">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="03554-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="03554-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03554-125">-Confirm</span></span>
<span data-ttu-id="03554-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="03554-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03554-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03554-127">-WhatIf</span></span>
<span data-ttu-id="03554-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="03554-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03554-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="03554-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03554-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03554-130">-DefaultProfile</span></span>
<span data-ttu-id="03554-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="03554-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03554-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03554-132">CommonParameters</span></span>
<span data-ttu-id="03554-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="03554-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03554-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03554-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03554-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03554-135">INPUTS</span></span>

### <span data-ttu-id="03554-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03554-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="03554-137">System. String</span><span class="sxs-lookup"><span data-stu-id="03554-137">System.String</span></span>

## <span data-ttu-id="03554-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03554-138">OUTPUTS</span></span>

### <span data-ttu-id="03554-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03554-139">System.Boolean</span></span>

## <span data-ttu-id="03554-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="03554-140">NOTES</span></span>
<span data-ttu-id="03554-141">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик</span><span class="sxs-lookup"><span data-stu-id="03554-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="03554-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03554-142">RELATED LINKS</span></span>

[<span data-ttu-id="03554-143">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="03554-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="03554-144">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="03554-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="03554-145">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="03554-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="03554-146">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="03554-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="03554-147">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03554-147">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="03554-148">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03554-148">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="03554-149">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03554-149">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="03554-150">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="03554-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="03554-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="03554-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="03554-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="03554-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="03554-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="03554-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="03554-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="03554-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
