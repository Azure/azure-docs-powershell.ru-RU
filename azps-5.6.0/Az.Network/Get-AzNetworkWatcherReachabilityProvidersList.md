---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 0d9d5867007c25db64cf8232ec9b66591362eef4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954387"
---
# <span data-ttu-id="b8357-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b8357-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="b8357-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8357-102">SYNOPSIS</span></span>
<span data-ttu-id="b8357-103">Список всех поставщиков услуг Интернета для указанного региона Azure.</span><span class="sxs-lookup"><span data-stu-id="b8357-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="b8357-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b8357-104">SYNTAX</span></span>

### <span data-ttu-id="b8357-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b8357-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8357-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b8357-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8357-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b8357-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8357-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b8357-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8357-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8357-109">DESCRIPTION</span></span>
<span data-ttu-id="b8357-110">В Get-AzNetworkWatcherReachabilityProvidersList перечислены все доступные поставщики услуг Интернета для указанного региона Azure.</span><span class="sxs-lookup"><span data-stu-id="b8357-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="b8357-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b8357-111">EXAMPLES</span></span>

### <span data-ttu-id="b8357-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b8357-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="b8357-113">Список всех доступных поставщиков в Москве и Москве для Центра обработки данных Azure на западном сайте США.</span><span class="sxs-lookup"><span data-stu-id="b8357-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

### <span data-ttu-id="b8357-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b8357-114">Example 2</span></span>

<span data-ttu-id="b8357-115">Список всех поставщиков услуг Интернета для указанного региона Azure.</span><span class="sxs-lookup"><span data-stu-id="b8357-115">Lists all available internet service providers for a specified Azure region.</span></span> <span data-ttu-id="b8357-116">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="b8357-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="b8357-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8357-117">PARAMETERS</span></span>

### <span data-ttu-id="b8357-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8357-118">-AsJob</span></span>
<span data-ttu-id="b8357-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b8357-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8357-120">-Город</span><span class="sxs-lookup"><span data-stu-id="b8357-120">-City</span></span>
<span data-ttu-id="b8357-121">Название города.</span><span class="sxs-lookup"><span data-stu-id="b8357-121">The name of the city.</span></span>

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

### <span data-ttu-id="b8357-122">-Country</span><span class="sxs-lookup"><span data-stu-id="b8357-122">-Country</span></span>
<span data-ttu-id="b8357-123">Название страны.</span><span class="sxs-lookup"><span data-stu-id="b8357-123">The name of the country.</span></span>

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

### <span data-ttu-id="b8357-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8357-124">-DefaultProfile</span></span>
<span data-ttu-id="b8357-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8357-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8357-126">-Location</span><span class="sxs-lookup"><span data-stu-id="b8357-126">-Location</span></span>
<span data-ttu-id="b8357-127">Необязательные регионы Azure для области действия запроса.</span><span class="sxs-lookup"><span data-stu-id="b8357-127">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="b8357-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8357-128">-NetworkWatcher</span></span>
<span data-ttu-id="b8357-129">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="b8357-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="b8357-130">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="b8357-130">-NetworkWatcherLocation</span></span>
<span data-ttu-id="b8357-131">Расположение сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="b8357-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b8357-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b8357-132">-NetworkWatcherName</span></span>
<span data-ttu-id="b8357-133">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="b8357-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="b8357-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8357-134">-ResourceGroupName</span></span>
<span data-ttu-id="b8357-135">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="b8357-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b8357-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8357-136">-ResourceId</span></span>
<span data-ttu-id="b8357-137">ИД ресурса сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="b8357-137">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="b8357-138">-State</span><span class="sxs-lookup"><span data-stu-id="b8357-138">-State</span></span>
<span data-ttu-id="b8357-139">Название штата.</span><span class="sxs-lookup"><span data-stu-id="b8357-139">The name of the state.</span></span>

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

### <span data-ttu-id="b8357-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8357-140">CommonParameters</span></span>
<span data-ttu-id="b8357-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8357-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8357-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8357-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8357-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8357-143">INPUTS</span></span>

### <span data-ttu-id="b8357-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8357-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b8357-145">System.String</span><span class="sxs-lookup"><span data-stu-id="b8357-145">System.String</span></span>

## <span data-ttu-id="b8357-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b8357-146">OUTPUTS</span></span>

### <span data-ttu-id="b8357-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="b8357-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="b8357-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b8357-148">NOTES</span></span>
<span data-ttu-id="b8357-149">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span><span class="sxs-lookup"><span data-stu-id="b8357-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="b8357-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8357-150">RELATED LINKS</span></span>

[<span data-ttu-id="b8357-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8357-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b8357-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8357-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b8357-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8357-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b8357-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b8357-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b8357-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b8357-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b8357-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b8357-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b8357-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b8357-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b8357-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8357-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8357-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b8357-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b8357-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8357-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8357-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8357-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8357-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8357-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8357-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8357-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b8357-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b8357-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b8357-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b8357-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b8357-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8357-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8357-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8357-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8357-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8357-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8357-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b8357-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b8357-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8357-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8357-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8357-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8357-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b8357-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b8357-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b8357-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b8357-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b8357-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b8357-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b8357-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b8357-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b8357-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="b8357-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8357-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
