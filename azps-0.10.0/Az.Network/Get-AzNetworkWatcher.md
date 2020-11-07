---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: d312eaa9f75fc13ecba0b00aa0fea64b5d3ea2e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909941"
---
# <span data-ttu-id="f8b36-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8b36-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="f8b36-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8b36-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b36-103">Возвращает свойства наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="f8b36-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="f8b36-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8b36-104">SYNTAX</span></span>

### <span data-ttu-id="f8b36-105">Получить</span><span class="sxs-lookup"><span data-stu-id="f8b36-105">Get</span></span>
```
Get-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8b36-106">Список</span><span class="sxs-lookup"><span data-stu-id="f8b36-106">List</span></span>
```
Get-AzNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8b36-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8b36-107">DESCRIPTION</span></span>
<span data-ttu-id="f8b36-108">Командлет Get-AzNetworkWatcher получает один или несколько ресурсов сетевого наблюдателя Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b36-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="f8b36-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8b36-109">EXAMPLES</span></span>

### <span data-ttu-id="f8b36-110">--------------------------Пример 1: получение сетевого наблюдателя--------------------------</span><span class="sxs-lookup"><span data-stu-id="f8b36-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="f8b36-111">Возвращает наблюдатель сети с именем NetworkWatcher_westcentralus в группе NetworkWatcherRG ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f8b36-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="f8b36-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8b36-112">PARAMETERS</span></span>

### <span data-ttu-id="f8b36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b36-113">-DefaultProfile</span></span>
<span data-ttu-id="f8b36-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b36-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8b36-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f8b36-115">-Name</span></span>
<span data-ttu-id="f8b36-116">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="f8b36-116">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b36-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8b36-117">-ResourceGroupName</span></span>
<span data-ttu-id="f8b36-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f8b36-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b36-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b36-119">CommonParameters</span></span>
<span data-ttu-id="f8b36-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8b36-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b36-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8b36-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b36-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8b36-122">INPUTS</span></span>

### <span data-ttu-id="f8b36-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="f8b36-123">None</span></span>

## <span data-ttu-id="f8b36-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8b36-124">OUTPUTS</span></span>

### <span data-ttu-id="f8b36-125">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8b36-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="f8b36-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8b36-126">NOTES</span></span>
<span data-ttu-id="f8b36-127">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети</span><span class="sxs-lookup"><span data-stu-id="f8b36-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="f8b36-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8b36-128">RELATED LINKS</span></span>

[<span data-ttu-id="f8b36-129">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8b36-129">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f8b36-130">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8b36-130">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f8b36-131">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f8b36-131">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f8b36-132">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f8b36-132">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f8b36-133">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f8b36-133">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f8b36-134">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f8b36-134">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f8b36-135">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f8b36-135">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f8b36-136">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f8b36-136">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f8b36-137">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f8b36-137">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f8b36-138">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f8b36-138">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f8b36-139">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f8b36-139">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f8b36-140">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f8b36-140">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
