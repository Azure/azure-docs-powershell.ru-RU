---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 71227c2e351e12381a857dcf9cd66767f00265cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902885"
---
# <span data-ttu-id="b3b26-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b3b26-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="b3b26-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3b26-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b26-103">Возвращает относительную задержку для поставщиков услуг Интернета из указанного местоположения в регионы Azure.</span><span class="sxs-lookup"><span data-stu-id="b3b26-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="b3b26-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3b26-104">SYNTAX</span></span>

### <span data-ttu-id="b3b26-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3b26-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b26-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b3b26-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b26-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b3b26-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b26-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b3b26-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3b26-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3b26-109">DESCRIPTION</span></span>
<span data-ttu-id="b3b26-110">Get-AzNetworkWatcherReachabilityReport получает оценку относительной задержки для поставщиков услуг Интернета из указанного места в Azure regions.</span><span class="sxs-lookup"><span data-stu-id="b3b26-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="b3b26-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3b26-111">EXAMPLES</span></span>

### <span data-ttu-id="b3b26-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b3b26-112">Example 1</span></span>
```
$nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

"aggregationLevel" : "Country",
"providerLocation" : {
    "country" : "United States"
},
"reachabilityReport" : [
    {
        "provider" : "Frontier Communications of America, Inc. - ASN 5650",
        "azureLocation": "West US",
        "latencies": [
            {
                "timeStamp": "2017-10-10T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-11T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-12T00:00:00Z",
                "score": 94    
            }
        ]  
    }
]
```

<span data-ttu-id="b3b26-113">Возвращает относительную задержку в центре обработки данных Azure на Запад США с 2017-10-10 до 2017-10-12 в США.</span><span class="sxs-lookup"><span data-stu-id="b3b26-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="b3b26-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3b26-114">PARAMETERS</span></span>

### <span data-ttu-id="b3b26-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3b26-115">-AsJob</span></span>
<span data-ttu-id="b3b26-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b3b26-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b3b26-117">-Город</span><span class="sxs-lookup"><span data-stu-id="b3b26-117">-City</span></span>
<span data-ttu-id="b3b26-118">Название города.</span><span class="sxs-lookup"><span data-stu-id="b3b26-118">The name of the city.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b26-119">-Country</span><span class="sxs-lookup"><span data-stu-id="b3b26-119">-Country</span></span>
<span data-ttu-id="b3b26-120">Название страны.</span><span class="sxs-lookup"><span data-stu-id="b3b26-120">The name of the country.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b26-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b26-121">-DefaultProfile</span></span>
<span data-ttu-id="b3b26-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3b26-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3b26-123">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b3b26-123">-EndTime</span></span>
<span data-ttu-id="b3b26-124">Время окончания отчета о достижимости Azure.</span><span class="sxs-lookup"><span data-stu-id="b3b26-124">The end time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b26-125">-Location</span><span class="sxs-lookup"><span data-stu-id="b3b26-125">-Location</span></span>
<span data-ttu-id="b3b26-126">Необязательные регионы Azure для определения области запроса.</span><span class="sxs-lookup"><span data-stu-id="b3b26-126">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b26-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b3b26-127">-NetworkWatcher</span></span>
<span data-ttu-id="b3b26-128">Ресурс «наблюдатель сети»</span><span class="sxs-lookup"><span data-stu-id="b3b26-128">The network watcher resource</span></span>

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

### <span data-ttu-id="b3b26-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="b3b26-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="b3b26-130">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="b3b26-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b3b26-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b3b26-131">-NetworkWatcherName</span></span>
<span data-ttu-id="b3b26-132">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="b3b26-132">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b26-133">-Provider</span><span class="sxs-lookup"><span data-stu-id="b3b26-133">-Provider</span></span>
<span data-ttu-id="b3b26-134">Список поставщиков услуг Интернета.</span><span class="sxs-lookup"><span data-stu-id="b3b26-134">List of Internet service providers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b26-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3b26-135">-ResourceGroupName</span></span>
<span data-ttu-id="b3b26-136">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="b3b26-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b3b26-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3b26-137">-ResourceId</span></span>
<span data-ttu-id="b3b26-138">Идентификатор ресурса наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="b3b26-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="b3b26-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b3b26-139">-StartTime</span></span>
<span data-ttu-id="b3b26-140">Время начала отчета о достижимости Azure.</span><span class="sxs-lookup"><span data-stu-id="b3b26-140">The start time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b26-141">-State</span><span class="sxs-lookup"><span data-stu-id="b3b26-141">-State</span></span>
<span data-ttu-id="b3b26-142">Имя состояния.</span><span class="sxs-lookup"><span data-stu-id="b3b26-142">The name of the state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b26-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b26-143">CommonParameters</span></span>
<span data-ttu-id="b3b26-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3b26-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b26-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3b26-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b26-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3b26-146">INPUTS</span></span>

### <span data-ttu-id="b3b26-147">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b3b26-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b3b26-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b3b26-148">System.String</span></span>

## <span data-ttu-id="b3b26-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3b26-149">OUTPUTS</span></span>

### <span data-ttu-id="b3b26-150">Microsoft. Azure. Commands. Network. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b3b26-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="b3b26-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3b26-151">NOTES</span></span>
<span data-ttu-id="b3b26-152">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, сетевое наблюдатель, достижимость, отчет</span><span class="sxs-lookup"><span data-stu-id="b3b26-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="b3b26-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3b26-153">RELATED LINKS</span></span>

[<span data-ttu-id="b3b26-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b3b26-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b3b26-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b3b26-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b3b26-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b3b26-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b3b26-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b3b26-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b3b26-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b3b26-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b3b26-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b3b26-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b3b26-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b3b26-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b3b26-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b3b26-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b3b26-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b3b26-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b3b26-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b3b26-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b3b26-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b3b26-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b3b26-165">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b3b26-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b3b26-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3b26-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b3b26-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b3b26-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b3b26-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b3b26-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b3b26-169">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b3b26-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b3b26-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b3b26-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b3b26-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b3b26-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b3b26-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b3b26-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b3b26-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b3b26-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b3b26-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b3b26-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b3b26-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b3b26-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b3b26-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b3b26-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b3b26-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b3b26-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b3b26-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b3b26-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b3b26-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b3b26-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="b3b26-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b3b26-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)