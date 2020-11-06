---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
ms.openlocfilehash: 9df0d0855ca22e9ea7141a99c69c8b44f16f489d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569924"
---
# <span data-ttu-id="aaf3c-101">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aaf3c-101">Get-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="aaf3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aaf3c-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf3c-103">Возвращает свойства наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-103">Gets the properties of a Network Watcher</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaf3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aaf3c-104">SYNTAX</span></span>

### <span data-ttu-id="aaf3c-105">Получить</span><span class="sxs-lookup"><span data-stu-id="aaf3c-105">Get</span></span>
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aaf3c-106">Список</span><span class="sxs-lookup"><span data-stu-id="aaf3c-106">List</span></span>
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aaf3c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaf3c-107">DESCRIPTION</span></span>
<span data-ttu-id="aaf3c-108">Командлет Get-AzureRmNetworkWatcher получает один или несколько ресурсов сетевого наблюдателя Azure.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-108">The Get-AzureRmNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="aaf3c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aaf3c-109">EXAMPLES</span></span>

### <span data-ttu-id="aaf3c-110">--------------------------Пример 1: получение сетевого наблюдателя--------------------------</span><span class="sxs-lookup"><span data-stu-id="aaf3c-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="aaf3c-111">Возвращает наблюдатель сети с именем NetworkWatcher_westcentralus в группе NetworkWatcherRG ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="aaf3c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aaf3c-112">PARAMETERS</span></span>

### <span data-ttu-id="aaf3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf3c-113">-DefaultProfile</span></span>
<span data-ttu-id="aaf3c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaf3c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aaf3c-115">-Name</span></span>
<span data-ttu-id="aaf3c-116">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-116">The network watcher name.</span></span>

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

### <span data-ttu-id="aaf3c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaf3c-117">-ResourceGroupName</span></span>
<span data-ttu-id="aaf3c-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-118">The resource group name.</span></span>

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

### <span data-ttu-id="aaf3c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf3c-119">CommonParameters</span></span>
<span data-ttu-id="aaf3c-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf3c-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaf3c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf3c-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aaf3c-122">INPUTS</span></span>

### <span data-ttu-id="aaf3c-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="aaf3c-123">None</span></span>

## <span data-ttu-id="aaf3c-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaf3c-124">OUTPUTS</span></span>

### <span data-ttu-id="aaf3c-125">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aaf3c-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="aaf3c-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="aaf3c-126">NOTES</span></span>
<span data-ttu-id="aaf3c-127">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети</span><span class="sxs-lookup"><span data-stu-id="aaf3c-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="aaf3c-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aaf3c-128">RELATED LINKS</span></span>

[<span data-ttu-id="aaf3c-129">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aaf3c-129">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="aaf3c-130">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aaf3c-130">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="aaf3c-131">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aaf3c-131">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="aaf3c-132">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="aaf3c-132">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="aaf3c-133">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aaf3c-133">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="aaf3c-134">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aaf3c-134">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="aaf3c-135">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aaf3c-135">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="aaf3c-136">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="aaf3c-136">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="aaf3c-137">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="aaf3c-137">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="aaf3c-138">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="aaf3c-138">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="aaf3c-139">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="aaf3c-139">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="aaf3c-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="aaf3c-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
