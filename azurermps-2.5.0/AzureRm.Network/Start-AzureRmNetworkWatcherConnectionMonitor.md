---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: c8464183646ee9a78bad4f8f94a8e2093ad6b21d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913575"
---
# <span data-ttu-id="520e0-101">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="520e0-101">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="520e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="520e0-102">SYNOPSIS</span></span>
<span data-ttu-id="520e0-103">Запуск монитора подключений</span><span class="sxs-lookup"><span data-stu-id="520e0-103">Start a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="520e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="520e0-104">SYNTAX</span></span>

### <span data-ttu-id="520e0-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="520e0-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="520e0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="520e0-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="520e0-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="520e0-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="520e0-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="520e0-108">SetByResourceId</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="520e0-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="520e0-109">SetByInputObject</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="520e0-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="520e0-110">DESCRIPTION</span></span>
<span data-ttu-id="520e0-111">Командлет Start-AzureRmNetworkWatcherConnectionMonitor запускает указанный монитор подключения.</span><span class="sxs-lookup"><span data-stu-id="520e0-111">The Start-AzureRmNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="520e0-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="520e0-112">EXAMPLES</span></span>

### <span data-ttu-id="520e0-113">---------------Пример 1: Запуск монитора подключений---------------</span><span class="sxs-lookup"><span data-stu-id="520e0-113">---------------  Example 1: Start a connection monitor ---------------</span></span>
```
PS C:\> Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="520e0-114">В этом примере мы запускаем монитор подключений, заданный по имени и наблюдателю сети.</span><span class="sxs-lookup"><span data-stu-id="520e0-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="520e0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="520e0-115">PARAMETERS</span></span>

### <span data-ttu-id="520e0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="520e0-116">-AsJob</span></span>
<span data-ttu-id="520e0-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="520e0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="520e0-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="520e0-118">-Confirm</span></span>
<span data-ttu-id="520e0-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="520e0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="520e0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="520e0-120">-DefaultProfile</span></span>
<span data-ttu-id="520e0-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="520e0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="520e0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="520e0-122">-InputObject</span></span>
<span data-ttu-id="520e0-123">Объект монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="520e0-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="520e0-124">-Location</span><span class="sxs-lookup"><span data-stu-id="520e0-124">-Location</span></span>
<span data-ttu-id="520e0-125">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="520e0-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="520e0-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="520e0-126">-Name</span></span>
<span data-ttu-id="520e0-127">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="520e0-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="520e0-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="520e0-128">-NetworkWatcher</span></span>
<span data-ttu-id="520e0-129">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="520e0-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="520e0-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="520e0-130">-NetworkWatcherName</span></span>
<span data-ttu-id="520e0-131">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="520e0-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="520e0-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="520e0-132">-PassThru</span></span>
<span data-ttu-id="520e0-133">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="520e0-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="520e0-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="520e0-134">-ResourceGroupName</span></span>
<span data-ttu-id="520e0-135">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="520e0-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="520e0-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="520e0-136">-ResourceId</span></span>
<span data-ttu-id="520e0-137">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="520e0-137">Resource ID.</span></span>

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

### <span data-ttu-id="520e0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="520e0-138">-WhatIf</span></span>
<span data-ttu-id="520e0-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="520e0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="520e0-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="520e0-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="520e0-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="520e0-141">INPUTS</span></span>

### <span data-ttu-id="520e0-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="520e0-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="520e0-143">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="520e0-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="520e0-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="520e0-144">OUTPUTS</span></span>

### <span data-ttu-id="520e0-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="520e0-145">System.Boolean</span></span>


## <span data-ttu-id="520e0-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="520e0-146">NOTES</span></span>
<span data-ttu-id="520e0-147">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="520e0-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="520e0-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="520e0-148">RELATED LINKS</span></span>
<span data-ttu-id="520e0-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="520e0-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="520e0-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="520e0-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="520e0-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Остановить-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="520e0-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="520e0-152">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Остановить-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="520e0-152">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md)
[Stop-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
