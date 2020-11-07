---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: cf67e27a8f502a753cded74f0cb5bf48ceb2d4ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732366"
---
# <span data-ttu-id="22a1a-101">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22a1a-101">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="22a1a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="22a1a-103">Запуск монитора подключений</span><span class="sxs-lookup"><span data-stu-id="22a1a-103">Start a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22a1a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22a1a-104">SYNTAX</span></span>

### <span data-ttu-id="22a1a-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22a1a-105">SetByName (Default)</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22a1a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="22a1a-106">SetByResource</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22a1a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="22a1a-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22a1a-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="22a1a-108">SetByResourceId</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22a1a-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="22a1a-109">SetByInputObject</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22a1a-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22a1a-110">DESCRIPTION</span></span>
<span data-ttu-id="22a1a-111">Командлет Start-AzureRmNetworkWatcherConnectionMonitor запускает указанный монитор подключения.</span><span class="sxs-lookup"><span data-stu-id="22a1a-111">The Start-AzureRmNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="22a1a-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22a1a-112">EXAMPLES</span></span>

### <span data-ttu-id="22a1a-113">Пример 1: Запуск монитора подключений</span><span class="sxs-lookup"><span data-stu-id="22a1a-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="22a1a-114">В этом примере мы запускаем монитор подключений, заданный по имени и наблюдателю сети.</span><span class="sxs-lookup"><span data-stu-id="22a1a-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="22a1a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22a1a-115">PARAMETERS</span></span>

### <span data-ttu-id="22a1a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22a1a-116">-AsJob</span></span>
<span data-ttu-id="22a1a-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="22a1a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22a1a-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22a1a-118">-Confirm</span></span>
<span data-ttu-id="22a1a-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="22a1a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22a1a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22a1a-120">-DefaultProfile</span></span>
<span data-ttu-id="22a1a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22a1a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22a1a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22a1a-122">-InputObject</span></span>
<span data-ttu-id="22a1a-123">Объект монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="22a1a-123">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22a1a-124">-Location</span><span class="sxs-lookup"><span data-stu-id="22a1a-124">-Location</span></span>
<span data-ttu-id="22a1a-125">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="22a1a-125">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a1a-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="22a1a-126">-Name</span></span>
<span data-ttu-id="22a1a-127">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="22a1a-127">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a1a-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22a1a-128">-NetworkWatcher</span></span>
<span data-ttu-id="22a1a-129">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="22a1a-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="22a1a-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="22a1a-130">-NetworkWatcherName</span></span>
<span data-ttu-id="22a1a-131">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="22a1a-131">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a1a-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22a1a-132">-PassThru</span></span>
<span data-ttu-id="22a1a-133">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="22a1a-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="22a1a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22a1a-134">-ResourceGroupName</span></span>
<span data-ttu-id="22a1a-135">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="22a1a-135">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a1a-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22a1a-136">-ResourceId</span></span>
<span data-ttu-id="22a1a-137">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="22a1a-137">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22a1a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22a1a-138">-WhatIf</span></span>
<span data-ttu-id="22a1a-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="22a1a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22a1a-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="22a1a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22a1a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22a1a-141">CommonParameters</span></span>
<span data-ttu-id="22a1a-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="22a1a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="22a1a-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22a1a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22a1a-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22a1a-144">INPUTS</span></span>

### <span data-ttu-id="22a1a-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22a1a-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="22a1a-146">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="22a1a-146">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="22a1a-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22a1a-147">OUTPUTS</span></span>

### <span data-ttu-id="22a1a-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="22a1a-148">System.Boolean</span></span>

## <span data-ttu-id="22a1a-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="22a1a-149">NOTES</span></span>
<span data-ttu-id="22a1a-150">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="22a1a-150">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="22a1a-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22a1a-151">RELATED LINKS</span></span>

[<span data-ttu-id="22a1a-152">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22a1a-152">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="22a1a-153">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22a1a-153">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="22a1a-154">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22a1a-154">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="22a1a-155">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="22a1a-155">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="22a1a-156">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="22a1a-156">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="22a1a-157">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="22a1a-157">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="22a1a-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="22a1a-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="22a1a-159">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22a1a-159">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="22a1a-160">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="22a1a-160">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="22a1a-161">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22a1a-161">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="22a1a-162">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22a1a-162">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="22a1a-163">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22a1a-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="22a1a-164">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22a1a-164">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="22a1a-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="22a1a-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="22a1a-166">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22a1a-166">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="22a1a-167">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22a1a-167">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="22a1a-168">Остановить-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22a1a-168">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="22a1a-169">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22a1a-169">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
