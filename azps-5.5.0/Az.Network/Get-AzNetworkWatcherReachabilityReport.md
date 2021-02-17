---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: f29ab593ffac847ec6b089efdc39bc594ad1d785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412849"
---
# <span data-ttu-id="f2def-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f2def-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="f2def-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2def-102">SYNOPSIS</span></span>
<span data-ttu-id="f2def-103">Возвращает относительную задержку для поставщиков услуг Интернета из указанного расположения в регионы Azure.</span><span class="sxs-lookup"><span data-stu-id="f2def-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="f2def-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f2def-104">SYNTAX</span></span>

### <span data-ttu-id="f2def-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f2def-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2def-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f2def-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2def-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f2def-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2def-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f2def-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2def-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2def-109">DESCRIPTION</span></span>
<span data-ttu-id="f2def-110">Служба Get-AzNetworkWatcherReachabilityReport получает относительную задержку для поставщиков услуг Интернета из указанного расположения в регионы Azure.</span><span class="sxs-lookup"><span data-stu-id="f2def-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="f2def-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f2def-111">EXAMPLES</span></span>

### <span data-ttu-id="f2def-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f2def-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="f2def-113">Позволяет получить относительные задержки в центре обработки данных Azure на западной части США с 2017-10 по 2017-10-12 в США.</span><span class="sxs-lookup"><span data-stu-id="f2def-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="f2def-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f2def-114">Example 2</span></span>

<span data-ttu-id="f2def-115">Возвращает относительную задержку для поставщиков услуг Интернета из указанного расположения в регионы Azure.</span><span class="sxs-lookup"><span data-stu-id="f2def-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="f2def-116">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="f2def-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="f2def-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2def-117">PARAMETERS</span></span>

### <span data-ttu-id="f2def-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2def-118">-AsJob</span></span>
<span data-ttu-id="f2def-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f2def-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2def-120">-Город</span><span class="sxs-lookup"><span data-stu-id="f2def-120">-City</span></span>
<span data-ttu-id="f2def-121">Название города.</span><span class="sxs-lookup"><span data-stu-id="f2def-121">The name of the city.</span></span>

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

### <span data-ttu-id="f2def-122">-Country</span><span class="sxs-lookup"><span data-stu-id="f2def-122">-Country</span></span>
<span data-ttu-id="f2def-123">Название страны.</span><span class="sxs-lookup"><span data-stu-id="f2def-123">The name of the country.</span></span>

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

### <span data-ttu-id="f2def-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2def-124">-DefaultProfile</span></span>
<span data-ttu-id="f2def-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2def-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2def-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f2def-126">-EndTime</span></span>
<span data-ttu-id="f2def-127">Время окончания отчета о доступности Azure.</span><span class="sxs-lookup"><span data-stu-id="f2def-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="f2def-128">-Location</span><span class="sxs-lookup"><span data-stu-id="f2def-128">-Location</span></span>
<span data-ttu-id="f2def-129">Необязательные регионы Azure для области действия запроса.</span><span class="sxs-lookup"><span data-stu-id="f2def-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="f2def-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2def-130">-NetworkWatcher</span></span>
<span data-ttu-id="f2def-131">Сетевой ресурс для просмотра</span><span class="sxs-lookup"><span data-stu-id="f2def-131">The network watcher resource</span></span>

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

### <span data-ttu-id="f2def-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="f2def-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="f2def-133">Расположение сетевого просмотра.</span><span class="sxs-lookup"><span data-stu-id="f2def-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f2def-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f2def-134">-NetworkWatcherName</span></span>
<span data-ttu-id="f2def-135">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="f2def-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="f2def-136">-Provider</span><span class="sxs-lookup"><span data-stu-id="f2def-136">-Provider</span></span>
<span data-ttu-id="f2def-137">Список поставщиков услуг Интернета.</span><span class="sxs-lookup"><span data-stu-id="f2def-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="f2def-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2def-138">-ResourceGroupName</span></span>
<span data-ttu-id="f2def-139">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="f2def-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f2def-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2def-140">-ResourceId</span></span>
<span data-ttu-id="f2def-141">ИД ресурса сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="f2def-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="f2def-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f2def-142">-StartTime</span></span>
<span data-ttu-id="f2def-143">Время начала отчета о доступности Azure.</span><span class="sxs-lookup"><span data-stu-id="f2def-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="f2def-144">-State</span><span class="sxs-lookup"><span data-stu-id="f2def-144">-State</span></span>
<span data-ttu-id="f2def-145">Название штата.</span><span class="sxs-lookup"><span data-stu-id="f2def-145">The name of the state.</span></span>

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

### <span data-ttu-id="f2def-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2def-146">CommonParameters</span></span>
<span data-ttu-id="f2def-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2def-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2def-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2def-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2def-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2def-149">INPUTS</span></span>

### <span data-ttu-id="f2def-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2def-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="f2def-151">System.String</span><span class="sxs-lookup"><span data-stu-id="f2def-151">System.String</span></span>

## <span data-ttu-id="f2def-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f2def-152">OUTPUTS</span></span>

### <span data-ttu-id="f2def-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f2def-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="f2def-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f2def-154">NOTES</span></span>
<span data-ttu-id="f2def-155">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, network, networking, network watcher, reachability, report</span><span class="sxs-lookup"><span data-stu-id="f2def-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="f2def-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2def-156">RELATED LINKS</span></span>

[<span data-ttu-id="f2def-157">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2def-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f2def-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2def-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f2def-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2def-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f2def-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f2def-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f2def-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f2def-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f2def-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f2def-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f2def-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f2def-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f2def-164">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2def-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2def-165">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f2def-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f2def-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2def-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2def-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2def-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2def-168">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2def-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2def-169">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2def-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f2def-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f2def-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f2def-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f2def-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f2def-172">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f2def-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f2def-173">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f2def-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f2def-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f2def-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f2def-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f2def-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f2def-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f2def-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f2def-177">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f2def-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f2def-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f2def-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f2def-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f2def-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f2def-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f2def-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f2def-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f2def-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f2def-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f2def-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="f2def-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f2def-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
