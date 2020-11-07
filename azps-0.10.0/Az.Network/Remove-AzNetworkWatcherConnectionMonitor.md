---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 2f2ca6c4b9174248074cb3863c7be7de45c170c6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911128"
---
# <span data-ttu-id="4023f-101">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4023f-101">Remove-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="4023f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4023f-102">SYNOPSIS</span></span>
<span data-ttu-id="4023f-103">Удаление монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="4023f-103">Remove connection monitor.</span></span>

## <span data-ttu-id="4023f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4023f-104">SYNTAX</span></span>

### <span data-ttu-id="4023f-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4023f-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4023f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4023f-106">SetByName</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4023f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4023f-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4023f-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4023f-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4023f-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="4023f-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4023f-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4023f-110">DESCRIPTION</span></span>
<span data-ttu-id="4023f-111">Командлет Remove-AzNetworkWatcherConnectionMonitor удаляет указанный монитор подключения.</span><span class="sxs-lookup"><span data-stu-id="4023f-111">The remove-AzNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="4023f-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4023f-112">EXAMPLES</span></span>

### <span data-ttu-id="4023f-113">---------------Пример 1: Удаление указанного монитора подключений---------------</span><span class="sxs-lookup"><span data-stu-id="4023f-113">---------------  Example 1: Remove the specified connection monitor ---------------</span></span>
```
PS C:\> Remove-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="4023f-114">В этом примере мы удалим монитор подключений, заданный по местоположению и названию.</span><span class="sxs-lookup"><span data-stu-id="4023f-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="4023f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4023f-115">PARAMETERS</span></span>

### <span data-ttu-id="4023f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4023f-116">-AsJob</span></span>
<span data-ttu-id="4023f-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4023f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4023f-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4023f-118">-Confirm</span></span>
<span data-ttu-id="4023f-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4023f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4023f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4023f-120">-DefaultProfile</span></span>
<span data-ttu-id="4023f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4023f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4023f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4023f-122">-InputObject</span></span>
<span data-ttu-id="4023f-123">Объект монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="4023f-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="4023f-124">-Location</span><span class="sxs-lookup"><span data-stu-id="4023f-124">-Location</span></span>
<span data-ttu-id="4023f-125">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="4023f-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="4023f-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4023f-126">-Name</span></span>
<span data-ttu-id="4023f-127">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="4023f-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="4023f-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4023f-128">-NetworkWatcher</span></span>
<span data-ttu-id="4023f-129">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="4023f-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="4023f-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4023f-130">-NetworkWatcherName</span></span>
<span data-ttu-id="4023f-131">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="4023f-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="4023f-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4023f-132">-PassThru</span></span>
<span data-ttu-id="4023f-133">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="4023f-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4023f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4023f-134">-ResourceGroupName</span></span>
<span data-ttu-id="4023f-135">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="4023f-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4023f-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4023f-136">-ResourceId</span></span>
<span data-ttu-id="4023f-137">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="4023f-137">Resource ID.</span></span>

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

### <span data-ttu-id="4023f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4023f-138">-WhatIf</span></span>
<span data-ttu-id="4023f-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4023f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4023f-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4023f-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="4023f-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4023f-141">INPUTS</span></span>

### <span data-ttu-id="4023f-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4023f-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4023f-143">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="4023f-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="4023f-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4023f-144">OUTPUTS</span></span>

### <span data-ttu-id="4023f-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4023f-145">System.Boolean</span></span>


## <span data-ttu-id="4023f-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="4023f-146">NOTES</span></span>
<span data-ttu-id="4023f-147">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="4023f-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="4023f-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4023f-148">RELATED LINKS</span></span>
<span data-ttu-id="4023f-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="4023f-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="4023f-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="4023f-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="4023f-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Остановить-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="4023f-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="4023f-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="4023f-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span></span>

