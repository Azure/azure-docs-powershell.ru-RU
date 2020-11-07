---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 84b92468f4945cbe25404b81f4c6403254a23ad3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914026"
---
# <span data-ttu-id="059be-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="059be-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="059be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="059be-102">SYNOPSIS</span></span>
<span data-ttu-id="059be-103">Удаление наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="059be-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="059be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="059be-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="059be-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="059be-105">DESCRIPTION</span></span>
<span data-ttu-id="059be-106">Командлет Remove-AzureRmNetworkWatcher удаляет ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="059be-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="059be-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="059be-107">EXAMPLES</span></span>

### <span data-ttu-id="059be-108">--------------------------Пример 1: создание и удаление наблюдателя сети--------------------------</span><span class="sxs-lookup"><span data-stu-id="059be-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="059be-109">В этом примере в группе ресурсов создается наблюдатель сети, а затем немедленно удаляется.</span><span class="sxs-lookup"><span data-stu-id="059be-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="059be-110">Обратите внимание, что для каждого региона на каждую подписку может быть создано только один наблюдатель сети.</span><span class="sxs-lookup"><span data-stu-id="059be-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="059be-111">Чтобы отключить вывод запроса при удалении виртуальной сети, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="059be-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="059be-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="059be-112">PARAMETERS</span></span>

### <span data-ttu-id="059be-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="059be-113">-AsJob</span></span>
<span data-ttu-id="059be-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="059be-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="059be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059be-115">-DefaultProfile</span></span>
<span data-ttu-id="059be-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="059be-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="059be-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="059be-117">-Name</span></span>
<span data-ttu-id="059be-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="059be-118">The resource name.</span></span>

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

### <span data-ttu-id="059be-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="059be-119">-PassThru</span></span>
<span data-ttu-id="059be-120">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="059be-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="059be-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="059be-121">-ResourceGroupName</span></span>
<span data-ttu-id="059be-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="059be-122">The resource group name.</span></span>

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

### <span data-ttu-id="059be-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="059be-123">-Confirm</span></span>
<span data-ttu-id="059be-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="059be-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="059be-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="059be-125">-WhatIf</span></span>
<span data-ttu-id="059be-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="059be-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="059be-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="059be-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="059be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059be-128">CommonParameters</span></span>
<span data-ttu-id="059be-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="059be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059be-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="059be-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059be-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="059be-131">INPUTS</span></span>

### <span data-ttu-id="059be-132">System. String</span><span class="sxs-lookup"><span data-stu-id="059be-132">System.String</span></span>

## <span data-ttu-id="059be-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="059be-133">OUTPUTS</span></span>

### <span data-ttu-id="059be-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="059be-134">System.Object</span></span>

## <span data-ttu-id="059be-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="059be-135">NOTES</span></span>
<span data-ttu-id="059be-136">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети</span><span class="sxs-lookup"><span data-stu-id="059be-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="059be-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="059be-137">RELATED LINKS</span></span>

[<span data-ttu-id="059be-138">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="059be-138">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="059be-139">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="059be-139">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="059be-140">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="059be-140">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="059be-141">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="059be-141">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="059be-142">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="059be-142">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="059be-143">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="059be-143">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="059be-144">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="059be-144">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="059be-145">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="059be-145">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="059be-146">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="059be-146">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="059be-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="059be-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="059be-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="059be-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="059be-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="059be-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
