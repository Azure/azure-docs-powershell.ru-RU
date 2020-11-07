---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: a67dde4b1e8f3f97038304086b63d02d75ff8fec
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913571"
---
# <span data-ttu-id="7307d-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7307d-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="7307d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7307d-102">SYNOPSIS</span></span>
<span data-ttu-id="7307d-103">Остановка монитора соединений</span><span class="sxs-lookup"><span data-stu-id="7307d-103">Stop a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7307d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7307d-104">SYNTAX</span></span>

### <span data-ttu-id="7307d-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7307d-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7307d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7307d-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7307d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7307d-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7307d-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7307d-108">SetByResourceId</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7307d-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="7307d-109">SetByInputObject</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="7307d-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7307d-110">DESCRIPTION</span></span>
<span data-ttu-id="7307d-111">Командлет Stop-AzureRmNetworkWatcherConnectionMonitor останавливает указанный монитор подключений.</span><span class="sxs-lookup"><span data-stu-id="7307d-111">The Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="7307d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7307d-112">EXAMPLES</span></span>

### <span data-ttu-id="7307d-113">---------------Пример 1: остановка монитора соединений---------------</span><span class="sxs-lookup"><span data-stu-id="7307d-113">---------------  Example 1: Stop a connection monitor ---------------</span></span>
```
PS C:\> Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="7307d-114">В этом примере показана остановка монитора подключений, указанного по имени и наблюдателю сети.</span><span class="sxs-lookup"><span data-stu-id="7307d-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="7307d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7307d-115">PARAMETERS</span></span>

### <span data-ttu-id="7307d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7307d-116">-AsJob</span></span>
<span data-ttu-id="7307d-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7307d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7307d-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7307d-118">-Confirm</span></span>
<span data-ttu-id="7307d-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7307d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7307d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7307d-120">-DefaultProfile</span></span>
<span data-ttu-id="7307d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7307d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7307d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7307d-122">-InputObject</span></span>
<span data-ttu-id="7307d-123">Объект монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="7307d-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="7307d-124">-Location</span><span class="sxs-lookup"><span data-stu-id="7307d-124">-Location</span></span>
<span data-ttu-id="7307d-125">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="7307d-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7307d-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7307d-126">-Name</span></span>
<span data-ttu-id="7307d-127">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="7307d-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="7307d-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7307d-128">-NetworkWatcher</span></span>
<span data-ttu-id="7307d-129">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="7307d-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="7307d-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7307d-130">-NetworkWatcherName</span></span>
<span data-ttu-id="7307d-131">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="7307d-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="7307d-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7307d-132">-PassThru</span></span>
<span data-ttu-id="7307d-133">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="7307d-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7307d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7307d-134">-ResourceGroupName</span></span>
<span data-ttu-id="7307d-135">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="7307d-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7307d-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7307d-136">-ResourceId</span></span>
<span data-ttu-id="7307d-137">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="7307d-137">Resource ID.</span></span>

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

### <span data-ttu-id="7307d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7307d-138">-WhatIf</span></span>
<span data-ttu-id="7307d-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7307d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7307d-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7307d-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="7307d-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7307d-141">INPUTS</span></span>

### <span data-ttu-id="7307d-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7307d-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7307d-143">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="7307d-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="7307d-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7307d-144">OUTPUTS</span></span>

### <span data-ttu-id="7307d-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7307d-145">System.Boolean</span></span>


## <span data-ttu-id="7307d-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="7307d-146">NOTES</span></span>
<span data-ttu-id="7307d-147">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="7307d-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="7307d-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7307d-148">RELATED LINKS</span></span>
<span data-ttu-id="7307d-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="7307d-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="7307d-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="7307d-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="7307d-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Остановить-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="7307d-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="7307d-152">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="7307d-152">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md)
[Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
