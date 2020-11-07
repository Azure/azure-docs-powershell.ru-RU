---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: a2c66f9e93a26c433c245f87c8506b71ad01c5e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912182"
---
# <span data-ttu-id="45368-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="45368-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="45368-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45368-102">SYNOPSIS</span></span>
<span data-ttu-id="45368-103">Список всех поставщиков услуг Интернета для определенного региона Azure.</span><span class="sxs-lookup"><span data-stu-id="45368-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="45368-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45368-104">SYNTAX</span></span>

### <span data-ttu-id="45368-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45368-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45368-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="45368-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45368-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="45368-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45368-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="45368-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45368-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45368-109">DESCRIPTION</span></span>
<span data-ttu-id="45368-110">В Get-AzNetworkWatcherReachabilityProvidersList перечислены все поставщики услуг Интернета, доступные в указанном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="45368-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="45368-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45368-111">EXAMPLES</span></span>

### <span data-ttu-id="45368-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="45368-112">Example 1</span></span>
```
PS C:\> $nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

"countries" : [
    {
        "countryName" : "United States",
        "states" : [
            {
                "stateName" : "washington",
                "cities" : [
                    {
                        "cityName" : "seattle",
                        "providers" : [
                            "Comcast Cable Communications, Inc. - ASN 7922",
                            "Comcast Cable Communications, LLC - ASN 7922",
                            "Level 3 Communications, Inc. (GBLX) - ASN 3549",
                            "Qwest Communications Company, LLC - ASN 209"
                        ]
                    }
                ]
            }
        ]
    }
]
```

<span data-ttu-id="45368-113">Список всех доступных поставщиков в Сиэтле, WA для центра обработки данных Azure на Запад США.</span><span class="sxs-lookup"><span data-stu-id="45368-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="45368-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45368-114">PARAMETERS</span></span>

### <span data-ttu-id="45368-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45368-115">-AsJob</span></span>
<span data-ttu-id="45368-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="45368-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45368-117">-Город</span><span class="sxs-lookup"><span data-stu-id="45368-117">-City</span></span>
<span data-ttu-id="45368-118">Название города.</span><span class="sxs-lookup"><span data-stu-id="45368-118">The name of the city.</span></span>

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

### <span data-ttu-id="45368-119">-Country</span><span class="sxs-lookup"><span data-stu-id="45368-119">-Country</span></span>
<span data-ttu-id="45368-120">Название страны.</span><span class="sxs-lookup"><span data-stu-id="45368-120">The name of the country.</span></span>

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

### <span data-ttu-id="45368-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45368-121">-DefaultProfile</span></span>
<span data-ttu-id="45368-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45368-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45368-123">-Location</span><span class="sxs-lookup"><span data-stu-id="45368-123">-Location</span></span>
<span data-ttu-id="45368-124">Необязательные регионы Azure для определения области запроса.</span><span class="sxs-lookup"><span data-stu-id="45368-124">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="45368-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="45368-125">-NetworkWatcher</span></span>
<span data-ttu-id="45368-126">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="45368-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="45368-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="45368-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="45368-128">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="45368-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="45368-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="45368-129">-NetworkWatcherName</span></span>
<span data-ttu-id="45368-130">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="45368-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="45368-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45368-131">-ResourceGroupName</span></span>
<span data-ttu-id="45368-132">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="45368-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="45368-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45368-133">-ResourceId</span></span>
<span data-ttu-id="45368-134">Идентификатор ресурса наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="45368-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="45368-135">-State</span><span class="sxs-lookup"><span data-stu-id="45368-135">-State</span></span>
<span data-ttu-id="45368-136">Имя состояния.</span><span class="sxs-lookup"><span data-stu-id="45368-136">The name of the state.</span></span>

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

### <span data-ttu-id="45368-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45368-137">CommonParameters</span></span>
<span data-ttu-id="45368-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45368-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45368-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45368-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45368-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45368-140">INPUTS</span></span>

### <span data-ttu-id="45368-141">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="45368-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="45368-142">System. String</span><span class="sxs-lookup"><span data-stu-id="45368-142">System.String</span></span>

## <span data-ttu-id="45368-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45368-143">OUTPUTS</span></span>

### <span data-ttu-id="45368-144">Microsoft. Azure. Commands. Network. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="45368-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="45368-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="45368-145">NOTES</span></span>
<span data-ttu-id="45368-146">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, далее, прыжок</span><span class="sxs-lookup"><span data-stu-id="45368-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="45368-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45368-147">RELATED LINKS</span></span>

[<span data-ttu-id="45368-148">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="45368-148">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="45368-149">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="45368-149">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="45368-150">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="45368-150">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="45368-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="45368-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="45368-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="45368-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="45368-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="45368-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="45368-154">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="45368-154">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="45368-155">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="45368-155">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="45368-156">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="45368-156">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="45368-157">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="45368-157">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="45368-158">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="45368-158">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="45368-159">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="45368-159">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="45368-160">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="45368-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="45368-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="45368-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="45368-162">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="45368-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="45368-163">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="45368-163">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="45368-164">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="45368-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="45368-165">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="45368-165">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="45368-166">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="45368-166">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="45368-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="45368-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="45368-168">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="45368-168">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="45368-169">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="45368-169">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="45368-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="45368-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="45368-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="45368-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="45368-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="45368-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="45368-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="45368-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="45368-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="45368-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
