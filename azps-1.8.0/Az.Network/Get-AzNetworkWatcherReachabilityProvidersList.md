---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: cf35292be5005a957e245370a5b15b78bb7d4fa6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730519"
---
# <span data-ttu-id="9dfaf-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9dfaf-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="9dfaf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9dfaf-102">SYNOPSIS</span></span>
<span data-ttu-id="9dfaf-103">Список всех поставщиков услуг Интернета для определенного региона Azure.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="9dfaf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9dfaf-104">SYNTAX</span></span>

### <span data-ttu-id="9dfaf-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9dfaf-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dfaf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9dfaf-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9dfaf-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9dfaf-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9dfaf-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9dfaf-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dfaf-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dfaf-109">DESCRIPTION</span></span>
<span data-ttu-id="9dfaf-110">В Get-AzNetworkWatcherReachabilityProvidersList перечислены все поставщики услуг Интернета, доступные в указанном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="9dfaf-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9dfaf-111">EXAMPLES</span></span>

### <span data-ttu-id="9dfaf-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9dfaf-112">Example 1</span></span>
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

<span data-ttu-id="9dfaf-113">Список всех доступных поставщиков в Сиэтле, WA для центра обработки данных Azure на Запад США.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="9dfaf-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9dfaf-114">PARAMETERS</span></span>

### <span data-ttu-id="9dfaf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dfaf-115">-AsJob</span></span>
<span data-ttu-id="9dfaf-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9dfaf-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9dfaf-117">-Город</span><span class="sxs-lookup"><span data-stu-id="9dfaf-117">-City</span></span>
<span data-ttu-id="9dfaf-118">Название города.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-118">The name of the city.</span></span>

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

### <span data-ttu-id="9dfaf-119">-Country</span><span class="sxs-lookup"><span data-stu-id="9dfaf-119">-Country</span></span>
<span data-ttu-id="9dfaf-120">Название страны.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-120">The name of the country.</span></span>

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

### <span data-ttu-id="9dfaf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dfaf-121">-DefaultProfile</span></span>
<span data-ttu-id="9dfaf-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9dfaf-123">-Location</span><span class="sxs-lookup"><span data-stu-id="9dfaf-123">-Location</span></span>
<span data-ttu-id="9dfaf-124">Необязательные регионы Azure для определения области запроса.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-124">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="9dfaf-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dfaf-125">-NetworkWatcher</span></span>
<span data-ttu-id="9dfaf-126">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="9dfaf-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="9dfaf-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="9dfaf-128">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9dfaf-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9dfaf-129">-NetworkWatcherName</span></span>
<span data-ttu-id="9dfaf-130">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="9dfaf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dfaf-131">-ResourceGroupName</span></span>
<span data-ttu-id="9dfaf-132">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9dfaf-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9dfaf-133">-ResourceId</span></span>
<span data-ttu-id="9dfaf-134">Идентификатор ресурса наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="9dfaf-135">-State</span><span class="sxs-lookup"><span data-stu-id="9dfaf-135">-State</span></span>
<span data-ttu-id="9dfaf-136">Имя состояния.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-136">The name of the state.</span></span>

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

### <span data-ttu-id="9dfaf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dfaf-137">CommonParameters</span></span>
<span data-ttu-id="9dfaf-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dfaf-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dfaf-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dfaf-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9dfaf-140">INPUTS</span></span>

### <span data-ttu-id="9dfaf-141">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dfaf-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="9dfaf-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9dfaf-142">System.String</span></span>

## <span data-ttu-id="9dfaf-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dfaf-143">OUTPUTS</span></span>

### <span data-ttu-id="9dfaf-144">Microsoft. Azure. Commands. Network. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="9dfaf-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="9dfaf-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="9dfaf-145">NOTES</span></span>
<span data-ttu-id="9dfaf-146">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, далее, прыжок</span><span class="sxs-lookup"><span data-stu-id="9dfaf-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="9dfaf-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9dfaf-147">RELATED LINKS</span></span>

[<span data-ttu-id="9dfaf-148">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dfaf-148">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="9dfaf-149">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dfaf-149">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="9dfaf-150">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dfaf-150">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="9dfaf-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9dfaf-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="9dfaf-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9dfaf-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9dfaf-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9dfaf-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="9dfaf-154">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9dfaf-154">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9dfaf-155">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9dfaf-155">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9dfaf-156">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9dfaf-156">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="9dfaf-157">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9dfaf-157">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9dfaf-158">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9dfaf-158">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9dfaf-159">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9dfaf-159">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9dfaf-160">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9dfaf-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="9dfaf-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9dfaf-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="9dfaf-162">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9dfaf-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="9dfaf-163">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dfaf-163">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9dfaf-164">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dfaf-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9dfaf-165">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dfaf-165">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9dfaf-166">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9dfaf-166">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9dfaf-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dfaf-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9dfaf-168">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dfaf-168">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9dfaf-169">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9dfaf-169">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="9dfaf-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9dfaf-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="9dfaf-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9dfaf-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="9dfaf-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9dfaf-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="9dfaf-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9dfaf-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="9dfaf-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dfaf-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
