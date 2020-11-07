---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: cace33dd9831dcfcc01f2a57eefb5f28367966d9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909645"
---
# <span data-ttu-id="84574-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84574-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="84574-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84574-102">SYNOPSIS</span></span>
<span data-ttu-id="84574-103">Создание нового ресурса сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="84574-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="84574-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84574-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84574-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84574-105">DESCRIPTION</span></span>
<span data-ttu-id="84574-106">Командлет New-AzNetworkWatcher создает новый ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="84574-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="84574-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84574-107">EXAMPLES</span></span>

### <span data-ttu-id="84574-108">Пример 1: Создание наблюдателя сети</span><span class="sxs-lookup"><span data-stu-id="84574-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="84574-109">В этом примере создается новый наблюдатель сети внутри созданной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84574-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="84574-110">Обратите внимание, что для каждого региона на каждую подписку может быть создано только один наблюдатель сети.</span><span class="sxs-lookup"><span data-stu-id="84574-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="84574-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84574-111">PARAMETERS</span></span>

### <span data-ttu-id="84574-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84574-112">-DefaultProfile</span></span>
<span data-ttu-id="84574-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84574-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84574-114">-Location</span><span class="sxs-lookup"><span data-stu-id="84574-114">-Location</span></span>
<span data-ttu-id="84574-115">Поиска.</span><span class="sxs-lookup"><span data-stu-id="84574-115">Location.</span></span>

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

### <span data-ttu-id="84574-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="84574-116">-Name</span></span>
<span data-ttu-id="84574-117">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="84574-117">The network watcher name.</span></span>

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

### <span data-ttu-id="84574-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84574-118">-ResourceGroupName</span></span>
<span data-ttu-id="84574-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84574-119">The resource group name.</span></span>

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

### <span data-ttu-id="84574-120">-Тег</span><span class="sxs-lookup"><span data-stu-id="84574-120">-Tag</span></span>
<span data-ttu-id="84574-121">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="84574-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="84574-122">Например:</span><span class="sxs-lookup"><span data-stu-id="84574-122">For example:</span></span>

<span data-ttu-id="84574-123">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="84574-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="84574-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84574-124">-Confirm</span></span>
<span data-ttu-id="84574-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="84574-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84574-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84574-126">-WhatIf</span></span>
<span data-ttu-id="84574-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="84574-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84574-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="84574-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84574-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84574-129">CommonParameters</span></span>
<span data-ttu-id="84574-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84574-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84574-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84574-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84574-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84574-132">INPUTS</span></span>

### <span data-ttu-id="84574-133">System. String</span><span class="sxs-lookup"><span data-stu-id="84574-133">System.String</span></span>
<span data-ttu-id="84574-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="84574-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="84574-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84574-135">OUTPUTS</span></span>

### <span data-ttu-id="84574-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84574-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="84574-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="84574-137">NOTES</span></span>
<span data-ttu-id="84574-138">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети</span><span class="sxs-lookup"><span data-stu-id="84574-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="84574-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84574-139">RELATED LINKS</span></span>

[<span data-ttu-id="84574-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84574-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="84574-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84574-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="84574-142">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84574-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84574-143">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="84574-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="84574-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84574-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84574-145">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84574-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84574-146">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84574-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84574-147">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="84574-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="84574-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="84574-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="84574-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="84574-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="84574-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="84574-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="84574-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="84574-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
