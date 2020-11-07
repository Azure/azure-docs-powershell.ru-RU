---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 805c8d31b075a39fa8ccc407024aa5a32a91fdb6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909913"
---
# <span data-ttu-id="f075c-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f075c-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="f075c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f075c-102">SYNOPSIS</span></span>
<span data-ttu-id="f075c-103">Список всех поставщиков услуг Интернета для определенного региона Azure.</span><span class="sxs-lookup"><span data-stu-id="f075c-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="f075c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f075c-104">SYNTAX</span></span>

### <span data-ttu-id="f075c-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f075c-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f075c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f075c-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f075c-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f075c-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f075c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f075c-108">DESCRIPTION</span></span>
<span data-ttu-id="f075c-109">В Get-AzNetworkWatcherReachabilityProvidersList перечислены все поставщики услуг Интернета, доступные в указанном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="f075c-109">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="f075c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f075c-110">EXAMPLES</span></span>

### <span data-ttu-id="f075c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f075c-111">Example 1</span></span>
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

<span data-ttu-id="f075c-112">Список всех доступных поставщиков в Сиэтле, WA для центра обработки данных Azure на Запад США.</span><span class="sxs-lookup"><span data-stu-id="f075c-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="f075c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f075c-113">PARAMETERS</span></span>

### <span data-ttu-id="f075c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f075c-114">-AsJob</span></span>
<span data-ttu-id="f075c-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f075c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f075c-116">-Город</span><span class="sxs-lookup"><span data-stu-id="f075c-116">-City</span></span>
<span data-ttu-id="f075c-117">Название города.</span><span class="sxs-lookup"><span data-stu-id="f075c-117">The name of the city.</span></span>

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

### <span data-ttu-id="f075c-118">-Country</span><span class="sxs-lookup"><span data-stu-id="f075c-118">-Country</span></span>
<span data-ttu-id="f075c-119">Название страны.</span><span class="sxs-lookup"><span data-stu-id="f075c-119">The name of the country.</span></span>

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

### <span data-ttu-id="f075c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f075c-120">-DefaultProfile</span></span>
<span data-ttu-id="f075c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f075c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f075c-122">-Location</span><span class="sxs-lookup"><span data-stu-id="f075c-122">-Location</span></span>
<span data-ttu-id="f075c-123">Необязательные регионы Azure для определения области запроса.</span><span class="sxs-lookup"><span data-stu-id="f075c-123">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="f075c-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f075c-124">-NetworkWatcher</span></span>
<span data-ttu-id="f075c-125">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="f075c-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="f075c-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f075c-126">-NetworkWatcherName</span></span>
<span data-ttu-id="f075c-127">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="f075c-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="f075c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f075c-128">-ResourceGroupName</span></span>
<span data-ttu-id="f075c-129">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="f075c-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f075c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f075c-130">-ResourceId</span></span>
<span data-ttu-id="f075c-131">Идентификатор ресурса наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="f075c-131">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="f075c-132">-State</span><span class="sxs-lookup"><span data-stu-id="f075c-132">-State</span></span>
<span data-ttu-id="f075c-133">Имя состояния.</span><span class="sxs-lookup"><span data-stu-id="f075c-133">The name of the state.</span></span>

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

### <span data-ttu-id="f075c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f075c-134">CommonParameters</span></span>
<span data-ttu-id="f075c-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f075c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f075c-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f075c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f075c-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f075c-137">INPUTS</span></span>

### <span data-ttu-id="f075c-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f075c-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f075c-139">System. String System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f075c-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f075c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f075c-140">OUTPUTS</span></span>

### <span data-ttu-id="f075c-141">Microsoft. Azure. Commands. Network. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="f075c-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="f075c-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f075c-142">NOTES</span></span>
<span data-ttu-id="f075c-143">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, далее, прыжок</span><span class="sxs-lookup"><span data-stu-id="f075c-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="f075c-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f075c-144">RELATED LINKS</span></span>

[<span data-ttu-id="f075c-145">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f075c-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f075c-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f075c-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f075c-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f075c-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f075c-148">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f075c-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f075c-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f075c-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f075c-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f075c-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f075c-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f075c-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f075c-152">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f075c-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f075c-153">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f075c-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f075c-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f075c-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f075c-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f075c-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f075c-156">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f075c-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
