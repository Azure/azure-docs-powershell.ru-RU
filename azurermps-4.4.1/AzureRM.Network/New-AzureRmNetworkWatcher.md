---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
ms.openlocfilehash: 10cc869bf6e0ac194ce5e2e77c69885a8e0a0d25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562476"
---
# <span data-ttu-id="8d589-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8d589-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="8d589-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d589-102">SYNOPSIS</span></span>
<span data-ttu-id="8d589-103">Создание нового ресурса сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="8d589-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d589-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d589-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d589-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d589-105">DESCRIPTION</span></span>
<span data-ttu-id="8d589-106">Командлет New-AzureRmNetworkWatcher создает новый ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="8d589-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="8d589-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d589-107">EXAMPLES</span></span>

### <span data-ttu-id="8d589-108">Пример 1: Создание наблюдателя сети</span><span class="sxs-lookup"><span data-stu-id="8d589-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="8d589-109">В этом примере создается новый наблюдатель сети внутри созданной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8d589-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="8d589-110">Обратите внимание, что для каждого региона на каждую подписку может быть создано только один наблюдатель сети.</span><span class="sxs-lookup"><span data-stu-id="8d589-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="8d589-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d589-111">PARAMETERS</span></span>

### <span data-ttu-id="8d589-112">-Location</span><span class="sxs-lookup"><span data-stu-id="8d589-112">-Location</span></span>
<span data-ttu-id="8d589-113">Поиска.</span><span class="sxs-lookup"><span data-stu-id="8d589-113">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d589-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8d589-114">-Name</span></span>
<span data-ttu-id="8d589-115">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="8d589-115">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d589-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d589-116">-ResourceGroupName</span></span>
<span data-ttu-id="8d589-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8d589-117">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d589-118">-Тег</span><span class="sxs-lookup"><span data-stu-id="8d589-118">-Tag</span></span>
<span data-ttu-id="8d589-119">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="8d589-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8d589-120">Например:</span><span class="sxs-lookup"><span data-stu-id="8d589-120">For example:</span></span>

<span data-ttu-id="8d589-121">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="8d589-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d589-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d589-122">-Confirm</span></span>
<span data-ttu-id="8d589-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8d589-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d589-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d589-124">-WhatIf</span></span>
<span data-ttu-id="8d589-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8d589-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d589-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8d589-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d589-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d589-127">-DefaultProfile</span></span>
<span data-ttu-id="8d589-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d589-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d589-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d589-129">CommonParameters</span></span>
<span data-ttu-id="8d589-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d589-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d589-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d589-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d589-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d589-132">INPUTS</span></span>

### <span data-ttu-id="8d589-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8d589-133">System.String</span></span>
<span data-ttu-id="8d589-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8d589-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8d589-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d589-135">OUTPUTS</span></span>

### <span data-ttu-id="8d589-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8d589-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="8d589-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d589-137">NOTES</span></span>
<span data-ttu-id="8d589-138">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети</span><span class="sxs-lookup"><span data-stu-id="8d589-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="8d589-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d589-139">RELATED LINKS</span></span>

[<span data-ttu-id="8d589-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8d589-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="8d589-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8d589-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="8d589-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8d589-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8d589-143">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8d589-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="8d589-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8d589-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8d589-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8d589-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8d589-146">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8d589-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8d589-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8d589-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="8d589-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8d589-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="8d589-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8d589-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8d589-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8d589-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="8d589-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8d589-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
