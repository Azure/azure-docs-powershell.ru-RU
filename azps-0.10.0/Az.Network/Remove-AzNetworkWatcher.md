---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: 276cd57a51b6b457f2f4d205932cdbfabd7613b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911126"
---
# <span data-ttu-id="d1041-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d1041-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="d1041-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1041-102">SYNOPSIS</span></span>
<span data-ttu-id="d1041-103">Удаление наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="d1041-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="d1041-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1041-104">SYNTAX</span></span>

```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1041-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1041-105">DESCRIPTION</span></span>
<span data-ttu-id="d1041-106">Командлет Remove-AzNetworkWatcher удаляет ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="d1041-106">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="d1041-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1041-107">EXAMPLES</span></span>

### <span data-ttu-id="d1041-108">--------------------------Пример 1: создание и удаление наблюдателя сети--------------------------</span><span class="sxs-lookup"><span data-stu-id="d1041-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="d1041-109">В этом примере в группе ресурсов создается наблюдатель сети, а затем немедленно удаляется.</span><span class="sxs-lookup"><span data-stu-id="d1041-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="d1041-110">Обратите внимание, что для каждого региона на каждую подписку может быть создано только один наблюдатель сети.</span><span class="sxs-lookup"><span data-stu-id="d1041-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="d1041-111">Чтобы отключить вывод запроса при удалении виртуальной сети, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="d1041-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="d1041-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1041-112">PARAMETERS</span></span>

### <span data-ttu-id="d1041-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1041-113">-AsJob</span></span>
<span data-ttu-id="d1041-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d1041-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1041-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1041-115">-DefaultProfile</span></span>
<span data-ttu-id="d1041-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1041-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1041-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d1041-117">-Name</span></span>
<span data-ttu-id="d1041-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d1041-118">The resource name.</span></span>

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

### <span data-ttu-id="d1041-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1041-119">-PassThru</span></span>
<span data-ttu-id="d1041-120">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="d1041-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1041-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1041-121">-ResourceGroupName</span></span>
<span data-ttu-id="d1041-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1041-122">The resource group name.</span></span>

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

### <span data-ttu-id="d1041-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1041-123">-Confirm</span></span>
<span data-ttu-id="d1041-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d1041-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1041-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1041-125">-WhatIf</span></span>
<span data-ttu-id="d1041-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d1041-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1041-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d1041-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1041-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1041-128">CommonParameters</span></span>
<span data-ttu-id="d1041-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1041-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1041-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1041-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1041-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1041-131">INPUTS</span></span>

### <span data-ttu-id="d1041-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d1041-132">System.String</span></span>

## <span data-ttu-id="d1041-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1041-133">OUTPUTS</span></span>

### <span data-ttu-id="d1041-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="d1041-134">System.Object</span></span>

## <span data-ttu-id="d1041-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1041-135">NOTES</span></span>
<span data-ttu-id="d1041-136">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети</span><span class="sxs-lookup"><span data-stu-id="d1041-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="d1041-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1041-137">RELATED LINKS</span></span>

[<span data-ttu-id="d1041-138">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d1041-138">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d1041-139">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d1041-139">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d1041-140">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d1041-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d1041-141">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d1041-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d1041-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d1041-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d1041-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d1041-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d1041-144">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d1041-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d1041-145">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d1041-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d1041-146">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d1041-146">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d1041-147">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d1041-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d1041-148">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d1041-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d1041-149">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d1041-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
