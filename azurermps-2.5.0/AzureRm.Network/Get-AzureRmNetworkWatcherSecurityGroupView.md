---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
ms.openlocfilehash: fad852ff589b2929df83775a2fa955e72663cfa2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913452"
---
# <span data-ttu-id="6fae4-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6fae4-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="6fae4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6fae4-102">SYNOPSIS</span></span>
<span data-ttu-id="6fae4-103">Просмотр настроенных и эффективных правил сетевой группы безопасности, примененных к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6fae4-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fae4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6fae4-104">SYNTAX</span></span>

### <span data-ttu-id="6fae4-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6fae4-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fae4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6fae4-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fae4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fae4-107">DESCRIPTION</span></span>
<span data-ttu-id="6fae4-108">Get-AzureRmNetworkWatcherSecurityGroupView позволяет просматривать настроенные и эффективные правила групп безопасности сети, примененные к ВМ.</span><span class="sxs-lookup"><span data-stu-id="6fae4-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="6fae4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6fae4-109">EXAMPLES</span></span>

### <span data-ttu-id="6fae4-110">---Пример 1: вызов представления группы безопасности на виртуальной машине---</span><span class="sxs-lookup"><span data-stu-id="6fae4-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="6fae4-111">В приведенном выше примере сначала нужно получить доступ к региональному наблюдатель сети, а затем виртуальной машине в регионе.</span><span class="sxs-lookup"><span data-stu-id="6fae4-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="6fae4-112">Затем мы создаем на выбранной виртуальной машине вызов представления группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="6fae4-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="6fae4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6fae4-113">PARAMETERS</span></span>

### <span data-ttu-id="6fae4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fae4-114">-AsJob</span></span>
<span data-ttu-id="6fae4-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6fae4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6fae4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fae4-116">-DefaultProfile</span></span>
<span data-ttu-id="6fae4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6fae4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fae4-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6fae4-118">-NetworkWatcher</span></span>
<span data-ttu-id="6fae4-119">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="6fae4-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="6fae4-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6fae4-120">-NetworkWatcherName</span></span>
<span data-ttu-id="6fae4-121">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="6fae4-121">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fae4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fae4-122">-ResourceGroupName</span></span>
<span data-ttu-id="6fae4-123">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="6fae4-123">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fae4-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="6fae4-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="6fae4-125">Идентификатор целевой виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="6fae4-125">The target VM Id</span></span>

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

### <span data-ttu-id="6fae4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fae4-126">CommonParameters</span></span>
<span data-ttu-id="6fae4-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6fae4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fae4-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fae4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fae4-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6fae4-129">INPUTS</span></span>

### <span data-ttu-id="6fae4-130">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6fae4-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6fae4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6fae4-131">System.String</span></span>

## <span data-ttu-id="6fae4-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fae4-132">OUTPUTS</span></span>

### <span data-ttu-id="6fae4-133">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="6fae4-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="6fae4-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="6fae4-134">NOTES</span></span>
<span data-ttu-id="6fae4-135">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, поток, IP</span><span class="sxs-lookup"><span data-stu-id="6fae4-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="6fae4-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6fae4-136">RELATED LINKS</span></span>

[<span data-ttu-id="6fae4-137">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6fae4-137">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6fae4-138">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6fae4-138">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6fae4-139">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6fae4-139">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6fae4-140">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6fae4-140">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="6fae4-141">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6fae4-141">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="6fae4-142">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6fae4-142">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="6fae4-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6fae4-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6fae4-144">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6fae4-144">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6fae4-145">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6fae4-145">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="6fae4-146">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6fae4-146">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6fae4-147">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6fae4-147">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6fae4-148">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6fae4-148">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

