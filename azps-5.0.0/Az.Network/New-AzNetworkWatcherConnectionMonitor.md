---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b84d11f259ffbf606bf0538a2ff71f6e9999db0a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316655"
---
# <span data-ttu-id="9153d-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9153d-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="9153d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9153d-102">SYNOPSIS</span></span>
<span data-ttu-id="9153d-103">Создание ресурса монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="9153d-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="9153d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9153d-104">SYNTAX</span></span>

### <span data-ttu-id="9153d-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9153d-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9153d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9153d-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9153d-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="9153d-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9153d-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="9153d-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9153d-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9153d-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9153d-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="9153d-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9153d-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="9153d-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9153d-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9153d-112">DESCRIPTION</span></span>
<span data-ttu-id="9153d-113">Командлет New-AzNetworkWatcherConnectionMonitor создает ресурс монитора подключений для определенного источника и назначения (монитор соединения SingleSourcedestination) или набор тестовых групп (MultiEndpointConnectionMonitor).</span><span class="sxs-lookup"><span data-stu-id="9153d-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="9153d-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9153d-114">EXAMPLES</span></span>

### <span data-ttu-id="9153d-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9153d-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="9153d-116">Имя: ИД диспетчера подключений:/subscriptions/00000000-0000-0000-0000-000000000000/resourceGro UPS/NetworkWatcherRG/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 ETag: W/"e86b28cf-B907-4475-a8b7-34d310367694" ProvisioningState: успешно источник: {"ResourceId": "/Subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft. Compute/virtualMachines/VM "," порт ": 0} назначение: {" адрес ":" bing.com ";" порт ": 80} MonitoringIntervalInSeconds: 60 Автозапуск: true StartTime: 1/12/2018 7:13:11 PM MonitoringStatus: выполнение расположения: centraluseuap Type: Microsoft. Network/networkWatchers/connectionMonitors. Теги: {}</span><span class="sxs-lookup"><span data-stu-id="9153d-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="9153d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9153d-117">PARAMETERS</span></span>

### <span data-ttu-id="9153d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9153d-118">-AsJob</span></span>
<span data-ttu-id="9153d-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9153d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9153d-120">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="9153d-120">-ConfigureOnly</span></span>
<span data-ttu-id="9153d-121">Настройка монитора подключений, но не запуск</span><span class="sxs-lookup"><span data-stu-id="9153d-121">Configure connection monitor, but do not start it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9153d-122">-ConnectionMonitor</span></span>
<span data-ttu-id="9153d-123">Объект монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="9153d-123">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject
Parameter Sets: SetByConnectionMonitorV2Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9153d-124">-DefaultProfile</span></span>
<span data-ttu-id="9153d-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9153d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="9153d-126">-DestinationAddress</span></span>
<span data-ttu-id="9153d-127">Адрес целевого монитора подключения (IP или доменное имя).</span><span class="sxs-lookup"><span data-stu-id="9153d-127">Address of the connection monitor destination (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="9153d-128">-DestinationPort</span></span>
<span data-ttu-id="9153d-129">Порт назначения, используемый монитором соединения.</span><span class="sxs-lookup"><span data-stu-id="9153d-129">The destination port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="9153d-130">-DestinationResourceId</span></span>
<span data-ttu-id="9153d-131">Идентификатор ресурса, используемого в качестве назначения монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="9153d-131">The ID of the resource used as the destination by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-132">-Force</span><span class="sxs-lookup"><span data-stu-id="9153d-132">-Force</span></span>
<span data-ttu-id="9153d-133">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="9153d-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9153d-134">-Location</span><span class="sxs-lookup"><span data-stu-id="9153d-134">-Location</span></span>
<span data-ttu-id="9153d-135">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="9153d-135">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation, SetByLocationV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9153d-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="9153d-137">Интервал наблюдения (в секундах).</span><span class="sxs-lookup"><span data-stu-id="9153d-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="9153d-138">Значение по умолчанию — 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="9153d-138">Default value is 60 seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9153d-139">-Name</span></span>
<span data-ttu-id="9153d-140">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="9153d-140">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9153d-141">-NetworkWatcher</span></span>
<span data-ttu-id="9153d-142">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="9153d-142">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9153d-143">-NetworkWatcherName</span></span>
<span data-ttu-id="9153d-144">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="9153d-144">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-145">-Примечание</span><span class="sxs-lookup"><span data-stu-id="9153d-145">-Note</span></span>
<span data-ttu-id="9153d-146">Заметки, связанные с монитором подключений.</span><span class="sxs-lookup"><span data-stu-id="9153d-146">Notes associated with connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-147">-Output</span><span class="sxs-lookup"><span data-stu-id="9153d-147">-Output</span></span>
<span data-ttu-id="9153d-148">Описание пунктов назначения выходных данных монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="9153d-148">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9153d-149">-ResourceGroupName</span></span>
<span data-ttu-id="9153d-150">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="9153d-150">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="9153d-151">-SourcePort</span></span>
<span data-ttu-id="9153d-152">Порт источника, используемый монитором соединения.</span><span class="sxs-lookup"><span data-stu-id="9153d-152">The source port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-153">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="9153d-153">-SourceResourceId</span></span>
<span data-ttu-id="9153d-154">Идентификатор ресурса, используемого в качестве источника монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="9153d-154">The ID of the resource used as the source by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-155">-Тег</span><span class="sxs-lookup"><span data-stu-id="9153d-155">-Tag</span></span>
<span data-ttu-id="9153d-156">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9153d-156">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-157">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="9153d-157">-TestGroup</span></span>
<span data-ttu-id="9153d-158">Список групп тестов.</span><span class="sxs-lookup"><span data-stu-id="9153d-158">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9153d-159">-Confirm</span></span>
<span data-ttu-id="9153d-160">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9153d-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9153d-161">-WhatIf</span></span>
<span data-ttu-id="9153d-162">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9153d-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9153d-163">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9153d-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9153d-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9153d-164">CommonParameters</span></span>
<span data-ttu-id="9153d-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9153d-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9153d-166">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9153d-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9153d-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9153d-167">INPUTS</span></span>

### <span data-ttu-id="9153d-168">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9153d-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="9153d-169">System. String</span><span class="sxs-lookup"><span data-stu-id="9153d-169">System.String</span></span>

### <span data-ttu-id="9153d-170">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft. Azure. PowerShell. командлеты. Network, Version = 2.2.2.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="9153d-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9153d-171">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorOutputObject, Microsoft. Azure. PowerShell. командлеты. Network, Version = 2.2.2.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="9153d-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9153d-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9153d-172">OUTPUTS</span></span>

### <span data-ttu-id="9153d-173">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="9153d-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="9153d-174">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="9153d-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="9153d-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="9153d-175">NOTES</span></span>

## <span data-ttu-id="9153d-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9153d-176">RELATED LINKS</span></span>
