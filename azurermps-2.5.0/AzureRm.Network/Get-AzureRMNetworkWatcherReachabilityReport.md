---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityreport
schema: 2.0.0
ms.openlocfilehash: 75335fb09bb8f4187879ab69ab138952cc873993
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915233"
---
# <span data-ttu-id="66aaa-101">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="66aaa-101">Get-AzureRMNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="66aaa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="66aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="66aaa-103">Возвращает относительную задержку для поставщиков услуг Интернета из указанного местоположения в регионы Azure.</span><span class="sxs-lookup"><span data-stu-id="66aaa-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66aaa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="66aaa-104">SYNTAX</span></span>

### <span data-ttu-id="66aaa-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="66aaa-105">SetByName (Default)</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="66aaa-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="66aaa-106">SetByResource</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="66aaa-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="66aaa-107">SetByResourceId</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66aaa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66aaa-108">DESCRIPTION</span></span>
<span data-ttu-id="66aaa-109">Get-AzureRmNetworkWatcherReachabilityReport получает оценку относительной задержки для поставщиков услуг Интернета из указанного места в Azure regions.</span><span class="sxs-lookup"><span data-stu-id="66aaa-109">The Get-AzureRmNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="66aaa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="66aaa-110">EXAMPLES</span></span>

### <span data-ttu-id="66aaa-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="66aaa-111">Example 1</span></span>
```
$nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzureRmNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

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

<span data-ttu-id="66aaa-112">Возвращает относительную задержку в центре обработки данных Azure на Запад США с 2017-10-10 до 2017-10-12 в США.</span><span class="sxs-lookup"><span data-stu-id="66aaa-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="66aaa-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="66aaa-113">PARAMETERS</span></span>

### <span data-ttu-id="66aaa-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66aaa-114">-AsJob</span></span>
<span data-ttu-id="66aaa-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="66aaa-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66aaa-116">-Город</span><span class="sxs-lookup"><span data-stu-id="66aaa-116">-City</span></span>
<span data-ttu-id="66aaa-117">Название города.</span><span class="sxs-lookup"><span data-stu-id="66aaa-117">The name of the city.</span></span>

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

### <span data-ttu-id="66aaa-118">-Country</span><span class="sxs-lookup"><span data-stu-id="66aaa-118">-Country</span></span>
<span data-ttu-id="66aaa-119">Название страны.</span><span class="sxs-lookup"><span data-stu-id="66aaa-119">The name of the country.</span></span>

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

### <span data-ttu-id="66aaa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66aaa-120">-DefaultProfile</span></span>
<span data-ttu-id="66aaa-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66aaa-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66aaa-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="66aaa-122">-EndTime</span></span>
<span data-ttu-id="66aaa-123">Время окончания отчета о достижимости Azure.</span><span class="sxs-lookup"><span data-stu-id="66aaa-123">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="66aaa-124">-Location</span><span class="sxs-lookup"><span data-stu-id="66aaa-124">-Location</span></span>
<span data-ttu-id="66aaa-125">Необязательные регионы Azure для определения области запроса.</span><span class="sxs-lookup"><span data-stu-id="66aaa-125">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="66aaa-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="66aaa-126">-NetworkWatcher</span></span>
<span data-ttu-id="66aaa-127">Ресурс «наблюдатель сети»</span><span class="sxs-lookup"><span data-stu-id="66aaa-127">The network watcher resource</span></span>

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

### <span data-ttu-id="66aaa-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="66aaa-128">-NetworkWatcherName</span></span>
<span data-ttu-id="66aaa-129">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="66aaa-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="66aaa-130">-Provider</span><span class="sxs-lookup"><span data-stu-id="66aaa-130">-Provider</span></span>
<span data-ttu-id="66aaa-131">Список поставщиков услуг Интернета.</span><span class="sxs-lookup"><span data-stu-id="66aaa-131">List of Internet service providers.</span></span>

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

### <span data-ttu-id="66aaa-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66aaa-132">-ResourceGroupName</span></span>
<span data-ttu-id="66aaa-133">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="66aaa-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="66aaa-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66aaa-134">-ResourceId</span></span>
<span data-ttu-id="66aaa-135">Идентификатор ресурса наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="66aaa-135">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="66aaa-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="66aaa-136">-StartTime</span></span>
<span data-ttu-id="66aaa-137">Время начала отчета о достижимости Azure.</span><span class="sxs-lookup"><span data-stu-id="66aaa-137">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="66aaa-138">-State</span><span class="sxs-lookup"><span data-stu-id="66aaa-138">-State</span></span>
<span data-ttu-id="66aaa-139">Имя состояния.</span><span class="sxs-lookup"><span data-stu-id="66aaa-139">The name of the state.</span></span>

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

### <span data-ttu-id="66aaa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66aaa-140">CommonParameters</span></span>
<span data-ttu-id="66aaa-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="66aaa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66aaa-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66aaa-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66aaa-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="66aaa-143">INPUTS</span></span>

### <span data-ttu-id="66aaa-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="66aaa-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="66aaa-145">System. String</span><span class="sxs-lookup"><span data-stu-id="66aaa-145">System.String</span></span>

## <span data-ttu-id="66aaa-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="66aaa-146">OUTPUTS</span></span>

### <span data-ttu-id="66aaa-147">Microsoft. Azure. Commands. Network. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="66aaa-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="66aaa-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="66aaa-148">NOTES</span></span>
<span data-ttu-id="66aaa-149">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, сетевое наблюдатель, достижимость, отчет</span><span class="sxs-lookup"><span data-stu-id="66aaa-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="66aaa-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66aaa-150">RELATED LINKS</span></span>

[<span data-ttu-id="66aaa-151">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="66aaa-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="66aaa-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="66aaa-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="66aaa-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="66aaa-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="66aaa-154">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="66aaa-154">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="66aaa-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="66aaa-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="66aaa-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="66aaa-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="66aaa-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="66aaa-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="66aaa-158">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="66aaa-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="66aaa-159">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="66aaa-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="66aaa-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="66aaa-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="66aaa-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="66aaa-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="66aaa-162">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="66aaa-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
