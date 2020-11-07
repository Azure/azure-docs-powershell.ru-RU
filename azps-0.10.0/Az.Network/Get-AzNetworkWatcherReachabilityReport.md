---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 6da0a36ee5e394008ea1d1de4a16f7982227ca06
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909909"
---
# <span data-ttu-id="41872-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="41872-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="41872-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41872-102">SYNOPSIS</span></span>
<span data-ttu-id="41872-103">Возвращает относительную задержку для поставщиков услуг Интернета из указанного местоположения в регионы Azure.</span><span class="sxs-lookup"><span data-stu-id="41872-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="41872-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41872-104">SYNTAX</span></span>

### <span data-ttu-id="41872-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41872-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="41872-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="41872-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="41872-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="41872-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41872-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41872-108">DESCRIPTION</span></span>
<span data-ttu-id="41872-109">Get-AzNetworkWatcherReachabilityReport получает оценку относительной задержки для поставщиков услуг Интернета из указанного места в Azure regions.</span><span class="sxs-lookup"><span data-stu-id="41872-109">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="41872-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41872-110">EXAMPLES</span></span>

### <span data-ttu-id="41872-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41872-111">Example 1</span></span>
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

<span data-ttu-id="41872-112">Возвращает относительную задержку в центре обработки данных Azure на Запад США с 2017-10-10 до 2017-10-12 в США.</span><span class="sxs-lookup"><span data-stu-id="41872-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="41872-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41872-113">PARAMETERS</span></span>

### <span data-ttu-id="41872-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41872-114">-AsJob</span></span>
<span data-ttu-id="41872-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="41872-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41872-116">-Город</span><span class="sxs-lookup"><span data-stu-id="41872-116">-City</span></span>
<span data-ttu-id="41872-117">Название города.</span><span class="sxs-lookup"><span data-stu-id="41872-117">The name of the city.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41872-118">-Country</span><span class="sxs-lookup"><span data-stu-id="41872-118">-Country</span></span>
<span data-ttu-id="41872-119">Название страны.</span><span class="sxs-lookup"><span data-stu-id="41872-119">The name of the country.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41872-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41872-120">-DefaultProfile</span></span>
<span data-ttu-id="41872-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41872-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41872-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="41872-122">-EndTime</span></span>
<span data-ttu-id="41872-123">Время окончания отчета о достижимости Azure.</span><span class="sxs-lookup"><span data-stu-id="41872-123">The end time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41872-124">-Location</span><span class="sxs-lookup"><span data-stu-id="41872-124">-Location</span></span>
<span data-ttu-id="41872-125">Необязательные регионы Azure для определения области запроса.</span><span class="sxs-lookup"><span data-stu-id="41872-125">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41872-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41872-126">-NetworkWatcher</span></span>
<span data-ttu-id="41872-127">Ресурс «наблюдатель сети»</span><span class="sxs-lookup"><span data-stu-id="41872-127">The network watcher resource</span></span>

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

### <span data-ttu-id="41872-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="41872-128">-NetworkWatcherName</span></span>
<span data-ttu-id="41872-129">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="41872-129">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41872-130">-Provider</span><span class="sxs-lookup"><span data-stu-id="41872-130">-Provider</span></span>
<span data-ttu-id="41872-131">Список поставщиков услуг Интернета.</span><span class="sxs-lookup"><span data-stu-id="41872-131">List of Internet service providers.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41872-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41872-132">-ResourceGroupName</span></span>
<span data-ttu-id="41872-133">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="41872-133">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41872-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41872-134">-ResourceId</span></span>
<span data-ttu-id="41872-135">Идентификатор ресурса наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="41872-135">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="41872-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="41872-136">-StartTime</span></span>
<span data-ttu-id="41872-137">Время начала отчета о достижимости Azure.</span><span class="sxs-lookup"><span data-stu-id="41872-137">The start time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41872-138">-State</span><span class="sxs-lookup"><span data-stu-id="41872-138">-State</span></span>
<span data-ttu-id="41872-139">Имя состояния.</span><span class="sxs-lookup"><span data-stu-id="41872-139">The name of the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41872-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41872-140">CommonParameters</span></span>
<span data-ttu-id="41872-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41872-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41872-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41872-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41872-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41872-143">INPUTS</span></span>

### <span data-ttu-id="41872-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41872-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="41872-145">System. String</span><span class="sxs-lookup"><span data-stu-id="41872-145">System.String</span></span>

## <span data-ttu-id="41872-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41872-146">OUTPUTS</span></span>

### <span data-ttu-id="41872-147">Microsoft. Azure. Commands. Network. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="41872-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="41872-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="41872-148">NOTES</span></span>
<span data-ttu-id="41872-149">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, сетевое наблюдатель, достижимость, отчет</span><span class="sxs-lookup"><span data-stu-id="41872-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="41872-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41872-150">RELATED LINKS</span></span>

[<span data-ttu-id="41872-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41872-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="41872-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41872-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="41872-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41872-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="41872-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="41872-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="41872-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="41872-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="41872-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="41872-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="41872-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="41872-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="41872-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41872-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41872-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="41872-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="41872-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41872-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41872-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41872-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41872-162">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41872-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
