---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: b096c87e588c48b609fe0a55be7344b39df98c87
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914045"
---
# <span data-ttu-id="8ee80-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ee80-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="8ee80-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ee80-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee80-103">Создание нового ресурса сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="8ee80-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ee80-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ee80-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ee80-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ee80-105">DESCRIPTION</span></span>
<span data-ttu-id="8ee80-106">Командлет New-AzureRmNetworkWatcher создает новый ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="8ee80-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="8ee80-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ee80-107">EXAMPLES</span></span>

### <span data-ttu-id="8ee80-108">Пример 1: Создание наблюдателя сети</span><span class="sxs-lookup"><span data-stu-id="8ee80-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="8ee80-109">В этом примере создается новый наблюдатель сети внутри созданной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ee80-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="8ee80-110">Обратите внимание, что для каждого региона на каждую подписку может быть создано только один наблюдатель сети.</span><span class="sxs-lookup"><span data-stu-id="8ee80-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="8ee80-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ee80-111">PARAMETERS</span></span>

### <span data-ttu-id="8ee80-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ee80-112">-DefaultProfile</span></span>
<span data-ttu-id="8ee80-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ee80-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ee80-114">-Location</span><span class="sxs-lookup"><span data-stu-id="8ee80-114">-Location</span></span>
<span data-ttu-id="8ee80-115">Поиска.</span><span class="sxs-lookup"><span data-stu-id="8ee80-115">Location.</span></span>

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

### <span data-ttu-id="8ee80-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8ee80-116">-Name</span></span>
<span data-ttu-id="8ee80-117">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="8ee80-117">The network watcher name.</span></span>

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

### <span data-ttu-id="8ee80-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee80-118">-ResourceGroupName</span></span>
<span data-ttu-id="8ee80-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ee80-119">The resource group name.</span></span>

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

### <span data-ttu-id="8ee80-120">-Тег</span><span class="sxs-lookup"><span data-stu-id="8ee80-120">-Tag</span></span>
<span data-ttu-id="8ee80-121">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="8ee80-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8ee80-122">Например:</span><span class="sxs-lookup"><span data-stu-id="8ee80-122">For example:</span></span>

<span data-ttu-id="8ee80-123">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="8ee80-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8ee80-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ee80-124">-Confirm</span></span>
<span data-ttu-id="8ee80-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8ee80-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ee80-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ee80-126">-WhatIf</span></span>
<span data-ttu-id="8ee80-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8ee80-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ee80-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8ee80-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ee80-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee80-129">CommonParameters</span></span>
<span data-ttu-id="8ee80-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ee80-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee80-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ee80-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee80-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ee80-132">INPUTS</span></span>

### <span data-ttu-id="8ee80-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8ee80-133">System.String</span></span>
<span data-ttu-id="8ee80-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8ee80-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8ee80-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ee80-135">OUTPUTS</span></span>

### <span data-ttu-id="8ee80-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ee80-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="8ee80-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ee80-137">NOTES</span></span>
<span data-ttu-id="8ee80-138">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети</span><span class="sxs-lookup"><span data-stu-id="8ee80-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="8ee80-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ee80-139">RELATED LINKS</span></span>

[<span data-ttu-id="8ee80-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ee80-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="8ee80-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ee80-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="8ee80-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ee80-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8ee80-143">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8ee80-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="8ee80-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ee80-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8ee80-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ee80-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8ee80-146">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ee80-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8ee80-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8ee80-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="8ee80-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8ee80-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="8ee80-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8ee80-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8ee80-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8ee80-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="8ee80-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8ee80-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
