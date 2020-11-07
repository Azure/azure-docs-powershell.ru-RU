---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: f69910140f2bd7b57a30bd413c74e6f26e646787
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910988"
---
# <span data-ttu-id="11d53-101">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="11d53-101">Stop-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="11d53-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11d53-102">SYNOPSIS</span></span>
<span data-ttu-id="11d53-103">Остановка монитора соединений</span><span class="sxs-lookup"><span data-stu-id="11d53-103">Stop a connection monitor</span></span>

## <span data-ttu-id="11d53-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11d53-104">SYNTAX</span></span>

### <span data-ttu-id="11d53-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11d53-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="11d53-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="11d53-106">SetByName</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="11d53-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="11d53-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="11d53-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="11d53-108">SetByResourceId</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="11d53-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="11d53-109">SetByInputObject</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="11d53-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11d53-110">DESCRIPTION</span></span>
<span data-ttu-id="11d53-111">Командлет Stop-AzNetworkWatcherConnectionMonitor останавливает указанный монитор подключений.</span><span class="sxs-lookup"><span data-stu-id="11d53-111">The Stop-AzNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="11d53-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11d53-112">EXAMPLES</span></span>

### <span data-ttu-id="11d53-113">---------------Пример 1: остановка монитора соединений---------------</span><span class="sxs-lookup"><span data-stu-id="11d53-113">---------------  Example 1: Stop a connection monitor ---------------</span></span>
```
PS C:\> Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="11d53-114">В этом примере показана остановка монитора подключений, указанного по имени и наблюдателю сети.</span><span class="sxs-lookup"><span data-stu-id="11d53-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="11d53-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11d53-115">PARAMETERS</span></span>

### <span data-ttu-id="11d53-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11d53-116">-AsJob</span></span>
<span data-ttu-id="11d53-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="11d53-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11d53-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11d53-118">-Confirm</span></span>
<span data-ttu-id="11d53-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="11d53-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11d53-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11d53-120">-DefaultProfile</span></span>
<span data-ttu-id="11d53-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11d53-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11d53-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11d53-122">-InputObject</span></span>
<span data-ttu-id="11d53-123">Объект монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="11d53-123">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11d53-124">-Location</span><span class="sxs-lookup"><span data-stu-id="11d53-124">-Location</span></span>
<span data-ttu-id="11d53-125">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="11d53-125">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11d53-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="11d53-126">-Name</span></span>
<span data-ttu-id="11d53-127">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="11d53-127">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11d53-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="11d53-128">-NetworkWatcher</span></span>
<span data-ttu-id="11d53-129">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="11d53-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="11d53-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="11d53-130">-NetworkWatcherName</span></span>
<span data-ttu-id="11d53-131">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="11d53-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="11d53-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11d53-132">-PassThru</span></span>
<span data-ttu-id="11d53-133">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="11d53-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="11d53-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11d53-134">-ResourceGroupName</span></span>
<span data-ttu-id="11d53-135">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="11d53-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="11d53-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11d53-136">-ResourceId</span></span>
<span data-ttu-id="11d53-137">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="11d53-137">Resource ID.</span></span>

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

### <span data-ttu-id="11d53-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11d53-138">-WhatIf</span></span>
<span data-ttu-id="11d53-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="11d53-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11d53-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="11d53-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="11d53-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11d53-141">INPUTS</span></span>

### <span data-ttu-id="11d53-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="11d53-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="11d53-143">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="11d53-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="11d53-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11d53-144">OUTPUTS</span></span>

### <span data-ttu-id="11d53-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="11d53-145">System.Boolean</span></span>


## <span data-ttu-id="11d53-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="11d53-146">NOTES</span></span>
<span data-ttu-id="11d53-147">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="11d53-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="11d53-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11d53-148">RELATED LINKS</span></span>
<span data-ttu-id="11d53-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="11d53-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="11d53-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="11d53-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="11d53-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Остановить-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="11d53-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="11d53-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="11d53-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span></span>