---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7c32c58167336fc032e543261e237430de36653c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565842"
---
# <span data-ttu-id="65d66-101">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="65d66-101">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="65d66-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65d66-102">SYNOPSIS</span></span>
<span data-ttu-id="65d66-103">Запуск монитора подключений</span><span class="sxs-lookup"><span data-stu-id="65d66-103">Start a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65d66-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65d66-104">SYNTAX</span></span>

### <span data-ttu-id="65d66-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="65d66-105">SetByName (Default)</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65d66-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="65d66-106">SetByResource</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65d66-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="65d66-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65d66-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="65d66-108">SetByResourceId</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65d66-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="65d66-109">SetByInputObject</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65d66-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65d66-110">DESCRIPTION</span></span>
<span data-ttu-id="65d66-111">Командлет Start-AzureRmNetworkWatcherConnectionMonitor запускает указанный монитор подключения.</span><span class="sxs-lookup"><span data-stu-id="65d66-111">The Start-AzureRmNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="65d66-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65d66-112">EXAMPLES</span></span>

### <span data-ttu-id="65d66-113">Пример 1: Запуск монитора подключений</span><span class="sxs-lookup"><span data-stu-id="65d66-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="65d66-114">В этом примере мы запускаем монитор подключений, заданный по имени и наблюдателю сети.</span><span class="sxs-lookup"><span data-stu-id="65d66-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="65d66-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65d66-115">PARAMETERS</span></span>

### <span data-ttu-id="65d66-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65d66-116">-AsJob</span></span>
<span data-ttu-id="65d66-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="65d66-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d66-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d66-118">-DefaultProfile</span></span>
<span data-ttu-id="65d66-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65d66-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65d66-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65d66-120">-InputObject</span></span>
<span data-ttu-id="65d66-121">Объект монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="65d66-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65d66-122">-Location</span><span class="sxs-lookup"><span data-stu-id="65d66-122">-Location</span></span>
<span data-ttu-id="65d66-123">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="65d66-123">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d66-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="65d66-124">-Name</span></span>
<span data-ttu-id="65d66-125">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="65d66-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d66-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65d66-126">-NetworkWatcher</span></span>
<span data-ttu-id="65d66-127">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="65d66-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="65d66-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="65d66-128">-NetworkWatcherName</span></span>
<span data-ttu-id="65d66-129">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="65d66-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d66-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65d66-130">-PassThru</span></span>
<span data-ttu-id="65d66-131">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="65d66-131">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d66-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d66-132">-ResourceGroupName</span></span>
<span data-ttu-id="65d66-133">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="65d66-133">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d66-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65d66-134">-ResourceId</span></span>
<span data-ttu-id="65d66-135">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="65d66-135">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d66-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65d66-136">-Confirm</span></span>
<span data-ttu-id="65d66-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="65d66-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65d66-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65d66-138">-WhatIf</span></span>
<span data-ttu-id="65d66-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="65d66-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65d66-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="65d66-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65d66-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d66-141">CommonParameters</span></span>
<span data-ttu-id="65d66-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="65d66-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d66-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65d66-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d66-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65d66-144">INPUTS</span></span>

### <span data-ttu-id="65d66-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65d66-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="65d66-146">Параметры: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="65d66-146">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="65d66-147">System. String</span><span class="sxs-lookup"><span data-stu-id="65d66-147">System.String</span></span>

### <span data-ttu-id="65d66-148">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="65d66-148">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="65d66-149">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="65d66-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="65d66-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65d66-150">OUTPUTS</span></span>

### <span data-ttu-id="65d66-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65d66-151">System.Boolean</span></span>

## <span data-ttu-id="65d66-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="65d66-152">NOTES</span></span>
<span data-ttu-id="65d66-153">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="65d66-153">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="65d66-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65d66-154">RELATED LINKS</span></span>

[<span data-ttu-id="65d66-155">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65d66-155">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="65d66-156">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65d66-156">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="65d66-157">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65d66-157">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="65d66-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="65d66-158">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="65d66-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="65d66-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="65d66-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="65d66-160">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="65d66-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="65d66-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="65d66-162">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65d66-162">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="65d66-163">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="65d66-163">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="65d66-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65d66-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="65d66-165">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65d66-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="65d66-166">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65d66-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="65d66-167">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="65d66-167">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="65d66-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="65d66-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="65d66-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="65d66-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="65d66-170">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="65d66-170">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="65d66-171">Остановить-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="65d66-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="65d66-172">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="65d66-172">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="65d66-173">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="65d66-173">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="65d66-174">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="65d66-174">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="65d66-175">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="65d66-175">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="65d66-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="65d66-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="65d66-177">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="65d66-177">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="65d66-178">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="65d66-178">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="65d66-179">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="65d66-179">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="65d66-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="65d66-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="65d66-181">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="65d66-181">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
