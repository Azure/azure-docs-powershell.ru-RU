---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 046a2ee4591eb345efd71163d27140799cb229e2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914025"
---
# <span data-ttu-id="9fda4-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9fda4-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="9fda4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9fda4-102">SYNOPSIS</span></span>
<span data-ttu-id="9fda4-103">Удаление монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="9fda4-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fda4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9fda4-104">SYNTAX</span></span>

### <span data-ttu-id="9fda4-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9fda4-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9fda4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="9fda4-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9fda4-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9fda4-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9fda4-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9fda4-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9fda4-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="9fda4-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="9fda4-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fda4-110">DESCRIPTION</span></span>
<span data-ttu-id="9fda4-111">Командлет Remove-AzureRmNetworkWatcherConnectionMonitor удаляет указанный монитор подключения.</span><span class="sxs-lookup"><span data-stu-id="9fda4-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="9fda4-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9fda4-112">EXAMPLES</span></span>

### <span data-ttu-id="9fda4-113">---------------Пример 1: Удаление указанного монитора подключений---------------</span><span class="sxs-lookup"><span data-stu-id="9fda4-113">---------------  Example 1: Remove the specified connection monitor ---------------</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="9fda4-114">В этом примере мы удалим монитор подключений, заданный по местоположению и названию.</span><span class="sxs-lookup"><span data-stu-id="9fda4-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="9fda4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9fda4-115">PARAMETERS</span></span>

### <span data-ttu-id="9fda4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9fda4-116">-AsJob</span></span>
<span data-ttu-id="9fda4-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9fda4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9fda4-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fda4-118">-Confirm</span></span>
<span data-ttu-id="9fda4-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9fda4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fda4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fda4-120">-DefaultProfile</span></span>
<span data-ttu-id="9fda4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9fda4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fda4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fda4-122">-InputObject</span></span>
<span data-ttu-id="9fda4-123">Объект монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="9fda4-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="9fda4-124">-Location</span><span class="sxs-lookup"><span data-stu-id="9fda4-124">-Location</span></span>
<span data-ttu-id="9fda4-125">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="9fda4-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9fda4-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9fda4-126">-Name</span></span>
<span data-ttu-id="9fda4-127">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="9fda4-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="9fda4-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9fda4-128">-NetworkWatcher</span></span>
<span data-ttu-id="9fda4-129">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="9fda4-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="9fda4-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9fda4-130">-NetworkWatcherName</span></span>
<span data-ttu-id="9fda4-131">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="9fda4-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="9fda4-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9fda4-132">-PassThru</span></span>
<span data-ttu-id="9fda4-133">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="9fda4-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9fda4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fda4-134">-ResourceGroupName</span></span>
<span data-ttu-id="9fda4-135">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="9fda4-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9fda4-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fda4-136">-ResourceId</span></span>
<span data-ttu-id="9fda4-137">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="9fda4-137">Resource ID.</span></span>

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

### <span data-ttu-id="9fda4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fda4-138">-WhatIf</span></span>
<span data-ttu-id="9fda4-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9fda4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fda4-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9fda4-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="9fda4-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9fda4-141">INPUTS</span></span>

### <span data-ttu-id="9fda4-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9fda4-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="9fda4-143">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="9fda4-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="9fda4-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fda4-144">OUTPUTS</span></span>

### <span data-ttu-id="9fda4-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9fda4-145">System.Boolean</span></span>


## <span data-ttu-id="9fda4-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="9fda4-146">NOTES</span></span>
<span data-ttu-id="9fda4-147">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="9fda4-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="9fda4-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9fda4-148">RELATED LINKS</span></span>
<span data-ttu-id="9fda4-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="9fda4-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="9fda4-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="9fda4-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="9fda4-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Остановить-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="9fda4-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="9fda4-152">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="9fda4-152">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span></span>

