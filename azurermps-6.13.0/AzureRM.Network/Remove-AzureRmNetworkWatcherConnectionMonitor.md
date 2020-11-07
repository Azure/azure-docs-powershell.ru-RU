---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 01e8a41c8d8854527037c447545f3d0601d4daf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734332"
---
# <span data-ttu-id="6de1b-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6de1b-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="6de1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6de1b-102">SYNOPSIS</span></span>
<span data-ttu-id="6de1b-103">Удаление монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="6de1b-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6de1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6de1b-104">SYNTAX</span></span>

### <span data-ttu-id="6de1b-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6de1b-105">SetByName (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6de1b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6de1b-106">SetByResource</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6de1b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6de1b-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6de1b-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6de1b-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6de1b-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="6de1b-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6de1b-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6de1b-110">DESCRIPTION</span></span>
<span data-ttu-id="6de1b-111">Командлет Remove-AzureRmNetworkWatcherConnectionMonitor удаляет указанный монитор подключения.</span><span class="sxs-lookup"><span data-stu-id="6de1b-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="6de1b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6de1b-112">EXAMPLES</span></span>

### <span data-ttu-id="6de1b-113">Пример 1: Удаление указанного монитора подключений</span><span class="sxs-lookup"><span data-stu-id="6de1b-113">Example 1: Remove the specified connection monitor</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="6de1b-114">В этом примере мы удалим монитор подключений, заданный по местоположению и названию.</span><span class="sxs-lookup"><span data-stu-id="6de1b-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="6de1b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6de1b-115">PARAMETERS</span></span>

### <span data-ttu-id="6de1b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6de1b-116">-AsJob</span></span>
<span data-ttu-id="6de1b-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6de1b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6de1b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de1b-118">-DefaultProfile</span></span>
<span data-ttu-id="6de1b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6de1b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6de1b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6de1b-120">-InputObject</span></span>
<span data-ttu-id="6de1b-121">Объект монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="6de1b-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="6de1b-122">-Location</span><span class="sxs-lookup"><span data-stu-id="6de1b-122">-Location</span></span>
<span data-ttu-id="6de1b-123">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="6de1b-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="6de1b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6de1b-124">-Name</span></span>
<span data-ttu-id="6de1b-125">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="6de1b-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="6de1b-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6de1b-126">-NetworkWatcher</span></span>
<span data-ttu-id="6de1b-127">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="6de1b-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="6de1b-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6de1b-128">-NetworkWatcherName</span></span>
<span data-ttu-id="6de1b-129">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="6de1b-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="6de1b-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6de1b-130">-PassThru</span></span>
<span data-ttu-id="6de1b-131">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="6de1b-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6de1b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6de1b-132">-ResourceGroupName</span></span>
<span data-ttu-id="6de1b-133">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="6de1b-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6de1b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6de1b-134">-ResourceId</span></span>
<span data-ttu-id="6de1b-135">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="6de1b-135">Resource ID.</span></span>

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

### <span data-ttu-id="6de1b-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6de1b-136">-Confirm</span></span>
<span data-ttu-id="6de1b-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6de1b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6de1b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6de1b-138">-WhatIf</span></span>
<span data-ttu-id="6de1b-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6de1b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6de1b-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6de1b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6de1b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de1b-141">CommonParameters</span></span>
<span data-ttu-id="6de1b-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6de1b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de1b-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6de1b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de1b-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6de1b-144">INPUTS</span></span>

### <span data-ttu-id="6de1b-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6de1b-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6de1b-146">Параметры: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6de1b-146">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="6de1b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="6de1b-147">System.String</span></span>

### <span data-ttu-id="6de1b-148">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="6de1b-148">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="6de1b-149">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6de1b-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6de1b-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6de1b-150">OUTPUTS</span></span>

### <span data-ttu-id="6de1b-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6de1b-151">System.Boolean</span></span>

## <span data-ttu-id="6de1b-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="6de1b-152">NOTES</span></span>
<span data-ttu-id="6de1b-153">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="6de1b-153">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="6de1b-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6de1b-154">RELATED LINKS</span></span>

[<span data-ttu-id="6de1b-155">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6de1b-155">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="6de1b-156">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6de1b-156">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="6de1b-157">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6de1b-157">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="6de1b-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6de1b-158">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="6de1b-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6de1b-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="6de1b-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6de1b-160">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="6de1b-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6de1b-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="6de1b-162">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6de1b-162">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="6de1b-163">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6de1b-163">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="6de1b-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6de1b-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="6de1b-165">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6de1b-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="6de1b-166">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6de1b-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="6de1b-167">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6de1b-167">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6de1b-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6de1b-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="6de1b-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6de1b-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6de1b-170">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6de1b-170">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6de1b-171">Остановить-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6de1b-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6de1b-172">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6de1b-172">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6de1b-173">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6de1b-173">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="6de1b-174">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6de1b-174">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="6de1b-175">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6de1b-175">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="6de1b-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6de1b-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="6de1b-177">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6de1b-177">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6de1b-178">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6de1b-178">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="6de1b-179">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6de1b-179">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="6de1b-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6de1b-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="6de1b-181">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6de1b-181">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
