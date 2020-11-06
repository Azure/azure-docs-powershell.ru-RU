---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
ms.openlocfilehash: ee92fd78d3a69b38620b2af543e01db7569d3b70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557712"
---
# <span data-ttu-id="cd399-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd399-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="cd399-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd399-102">SYNOPSIS</span></span>
<span data-ttu-id="cd399-103">Удаление наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="cd399-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd399-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd399-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd399-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd399-105">DESCRIPTION</span></span>
<span data-ttu-id="cd399-106">Командлет Remove-AzureRmNetworkWatcher удаляет ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="cd399-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="cd399-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd399-107">EXAMPLES</span></span>

### <span data-ttu-id="cd399-108">--------------------------Пример 1: создание и удаление наблюдателя сети--------------------------</span><span class="sxs-lookup"><span data-stu-id="cd399-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="cd399-109">В этом примере в группе ресурсов создается наблюдатель сети, а затем немедленно удаляется.</span><span class="sxs-lookup"><span data-stu-id="cd399-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="cd399-110">Обратите внимание, что для каждого региона на каждую подписку может быть создано только один наблюдатель сети.</span><span class="sxs-lookup"><span data-stu-id="cd399-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="cd399-111">Чтобы отключить вывод запроса при удалении виртуальной сети, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="cd399-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="cd399-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd399-112">PARAMETERS</span></span>

### <span data-ttu-id="cd399-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cd399-113">-Name</span></span>
<span data-ttu-id="cd399-114">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="cd399-114">The resource name.</span></span>

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

### <span data-ttu-id="cd399-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd399-115">-PassThru</span></span>
<span data-ttu-id="cd399-116">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="cd399-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd399-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd399-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd399-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cd399-118">The resource group name.</span></span>

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

### <span data-ttu-id="cd399-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd399-119">-Confirm</span></span>
<span data-ttu-id="cd399-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cd399-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd399-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd399-121">-WhatIf</span></span>
<span data-ttu-id="cd399-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cd399-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd399-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd399-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd399-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd399-124">-DefaultProfile</span></span>
<span data-ttu-id="cd399-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd399-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd399-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd399-126">CommonParameters</span></span>
<span data-ttu-id="cd399-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd399-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd399-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd399-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd399-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd399-129">INPUTS</span></span>

### <span data-ttu-id="cd399-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cd399-130">System.String</span></span>

## <span data-ttu-id="cd399-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd399-131">OUTPUTS</span></span>

### <span data-ttu-id="cd399-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="cd399-132">System.Object</span></span>

## <span data-ttu-id="cd399-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd399-133">NOTES</span></span>
<span data-ttu-id="cd399-134">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети</span><span class="sxs-lookup"><span data-stu-id="cd399-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="cd399-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd399-135">RELATED LINKS</span></span>

[<span data-ttu-id="cd399-136">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd399-136">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="cd399-137">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd399-137">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="cd399-138">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd399-138">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd399-139">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cd399-139">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="cd399-140">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd399-140">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd399-141">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd399-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd399-142">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd399-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd399-143">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="cd399-143">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="cd399-144">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cd399-144">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="cd399-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cd399-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="cd399-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cd399-146">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="cd399-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cd399-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
