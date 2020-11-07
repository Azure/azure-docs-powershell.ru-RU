---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityproviderslist
schema: 2.0.0
ms.openlocfilehash: c5a681f8be210e76ecbf3bc965e7e9e9c108a94a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913453"
---
# <span data-ttu-id="5d66c-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5d66c-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="5d66c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d66c-102">SYNOPSIS</span></span>
<span data-ttu-id="5d66c-103">Список всех поставщиков услуг Интернета для определенного региона Azure.</span><span class="sxs-lookup"><span data-stu-id="5d66c-103">Lists all available internet service providers for a specified Azure region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d66c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d66c-104">SYNTAX</span></span>

### <span data-ttu-id="5d66c-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d66c-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d66c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5d66c-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d66c-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5d66c-107">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d66c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d66c-108">DESCRIPTION</span></span>
<span data-ttu-id="5d66c-109">В Get-AzureRmNetworkWatcherReachabilityProvidersList перечислены все поставщики услуг Интернета, доступные в указанном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="5d66c-109">The Get-AzureRmNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="5d66c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d66c-110">EXAMPLES</span></span>

### <span data-ttu-id="5d66c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5d66c-111">Example 1</span></span>
```
PS C:\> $nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

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

<span data-ttu-id="5d66c-112">Список всех доступных поставщиков в Сиэтле, WA для центра обработки данных Azure на Запад США.</span><span class="sxs-lookup"><span data-stu-id="5d66c-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="5d66c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d66c-113">PARAMETERS</span></span>

### <span data-ttu-id="5d66c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d66c-114">-AsJob</span></span>
<span data-ttu-id="5d66c-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5d66c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d66c-116">-Город</span><span class="sxs-lookup"><span data-stu-id="5d66c-116">-City</span></span>
<span data-ttu-id="5d66c-117">Название города.</span><span class="sxs-lookup"><span data-stu-id="5d66c-117">The name of the city.</span></span>

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

### <span data-ttu-id="5d66c-118">-Country</span><span class="sxs-lookup"><span data-stu-id="5d66c-118">-Country</span></span>
<span data-ttu-id="5d66c-119">Название страны.</span><span class="sxs-lookup"><span data-stu-id="5d66c-119">The name of the country.</span></span>

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

### <span data-ttu-id="5d66c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d66c-120">-DefaultProfile</span></span>
<span data-ttu-id="5d66c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d66c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d66c-122">-Location</span><span class="sxs-lookup"><span data-stu-id="5d66c-122">-Location</span></span>
<span data-ttu-id="5d66c-123">Необязательные регионы Azure для определения области запроса.</span><span class="sxs-lookup"><span data-stu-id="5d66c-123">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="5d66c-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d66c-124">-NetworkWatcher</span></span>
<span data-ttu-id="5d66c-125">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="5d66c-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="5d66c-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5d66c-126">-NetworkWatcherName</span></span>
<span data-ttu-id="5d66c-127">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="5d66c-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="5d66c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d66c-128">-ResourceGroupName</span></span>
<span data-ttu-id="5d66c-129">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="5d66c-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5d66c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d66c-130">-ResourceId</span></span>
<span data-ttu-id="5d66c-131">Идентификатор ресурса наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="5d66c-131">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="5d66c-132">-State</span><span class="sxs-lookup"><span data-stu-id="5d66c-132">-State</span></span>
<span data-ttu-id="5d66c-133">Имя состояния.</span><span class="sxs-lookup"><span data-stu-id="5d66c-133">The name of the state.</span></span>

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

### <span data-ttu-id="5d66c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d66c-134">CommonParameters</span></span>
<span data-ttu-id="5d66c-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d66c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d66c-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d66c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d66c-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d66c-137">INPUTS</span></span>

### <span data-ttu-id="5d66c-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d66c-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5d66c-139">System. String System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5d66c-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="5d66c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d66c-140">OUTPUTS</span></span>

### <span data-ttu-id="5d66c-141">Microsoft. Azure. Commands. Network. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="5d66c-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="5d66c-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d66c-142">NOTES</span></span>
<span data-ttu-id="5d66c-143">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, далее, прыжок</span><span class="sxs-lookup"><span data-stu-id="5d66c-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="5d66c-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d66c-144">RELATED LINKS</span></span>

[<span data-ttu-id="5d66c-145">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d66c-145">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5d66c-146">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d66c-146">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5d66c-147">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d66c-147">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5d66c-148">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5d66c-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="5d66c-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5d66c-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5d66c-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5d66c-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="5d66c-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5d66c-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5d66c-152">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5d66c-152">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5d66c-153">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5d66c-153">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="5d66c-154">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5d66c-154">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5d66c-155">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5d66c-155">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5d66c-156">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5d66c-156">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
