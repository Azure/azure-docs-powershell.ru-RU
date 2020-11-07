---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
ms.openlocfilehash: e1e0714c070c47d4be2cff0893a4428bdf0949c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734436"
---
# <span data-ttu-id="41f94-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41f94-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="41f94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41f94-102">SYNOPSIS</span></span>
<span data-ttu-id="41f94-103">Создание нового ресурса сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="41f94-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41f94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41f94-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41f94-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41f94-105">DESCRIPTION</span></span>
<span data-ttu-id="41f94-106">Командлет New-AzureRmNetworkWatcher создает новый ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="41f94-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="41f94-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41f94-107">EXAMPLES</span></span>

### <span data-ttu-id="41f94-108">Пример 1: Создание наблюдателя сети</span><span class="sxs-lookup"><span data-stu-id="41f94-108">Example 1: Create a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="41f94-109">В этом примере создается новый наблюдатель сети внутри созданной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41f94-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="41f94-110">Обратите внимание, что для каждого региона на каждую подписку может быть создано только один наблюдатель сети.</span><span class="sxs-lookup"><span data-stu-id="41f94-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="41f94-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41f94-111">PARAMETERS</span></span>

### <span data-ttu-id="41f94-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41f94-112">-DefaultProfile</span></span>
<span data-ttu-id="41f94-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41f94-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41f94-114">-Location</span><span class="sxs-lookup"><span data-stu-id="41f94-114">-Location</span></span>
<span data-ttu-id="41f94-115">Поиска.</span><span class="sxs-lookup"><span data-stu-id="41f94-115">Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41f94-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="41f94-116">-Name</span></span>
<span data-ttu-id="41f94-117">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="41f94-117">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41f94-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41f94-118">-ResourceGroupName</span></span>
<span data-ttu-id="41f94-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41f94-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41f94-120">-Тег</span><span class="sxs-lookup"><span data-stu-id="41f94-120">-Tag</span></span>
<span data-ttu-id="41f94-121">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="41f94-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="41f94-122">Например:</span><span class="sxs-lookup"><span data-stu-id="41f94-122">For example:</span></span>

<span data-ttu-id="41f94-123">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="41f94-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41f94-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41f94-124">-Confirm</span></span>
<span data-ttu-id="41f94-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="41f94-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f94-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41f94-126">-WhatIf</span></span>
<span data-ttu-id="41f94-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="41f94-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41f94-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="41f94-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f94-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f94-129">CommonParameters</span></span>
<span data-ttu-id="41f94-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41f94-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41f94-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41f94-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f94-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41f94-132">INPUTS</span></span>

### <span data-ttu-id="41f94-133">System. String</span><span class="sxs-lookup"><span data-stu-id="41f94-133">System.String</span></span>
<span data-ttu-id="41f94-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="41f94-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="41f94-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41f94-135">OUTPUTS</span></span>

### <span data-ttu-id="41f94-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41f94-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="41f94-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="41f94-137">NOTES</span></span>
<span data-ttu-id="41f94-138">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети</span><span class="sxs-lookup"><span data-stu-id="41f94-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="41f94-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41f94-139">RELATED LINKS</span></span>

[<span data-ttu-id="41f94-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41f94-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="41f94-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41f94-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="41f94-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41f94-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41f94-143">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="41f94-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="41f94-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41f94-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41f94-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41f94-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41f94-146">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41f94-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41f94-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="41f94-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="41f94-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="41f94-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="41f94-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="41f94-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="41f94-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="41f94-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="41f94-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="41f94-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
