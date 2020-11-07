---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: fe315ac4b6c29b8ffd1c82c8045ba9b7a7aab4a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909906"
---
# <span data-ttu-id="2c0d8-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2c0d8-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="2c0d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c0d8-102">SYNOPSIS</span></span>
<span data-ttu-id="2c0d8-103">Просмотр настроенных и эффективных правил сетевой группы безопасности, примененных к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2c0d8-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="2c0d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c0d8-104">SYNTAX</span></span>

### <span data-ttu-id="2c0d8-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2c0d8-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c0d8-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2c0d8-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c0d8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c0d8-107">DESCRIPTION</span></span>
<span data-ttu-id="2c0d8-108">Get-AzNetworkWatcherSecurityGroupView позволяет просматривать настроенные и эффективные правила групп безопасности сети, примененные к ВМ.</span><span class="sxs-lookup"><span data-stu-id="2c0d8-108">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="2c0d8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c0d8-109">EXAMPLES</span></span>

### <span data-ttu-id="2c0d8-110">---Пример 1: вызов представления группы безопасности на виртуальной машине---</span><span class="sxs-lookup"><span data-stu-id="2c0d8-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="2c0d8-111">В приведенном выше примере сначала нужно получить доступ к региональному наблюдатель сети, а затем виртуальной машине в регионе.</span><span class="sxs-lookup"><span data-stu-id="2c0d8-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="2c0d8-112">Затем мы создаем на выбранной виртуальной машине вызов представления группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="2c0d8-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="2c0d8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c0d8-113">PARAMETERS</span></span>

### <span data-ttu-id="2c0d8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c0d8-114">-AsJob</span></span>
<span data-ttu-id="2c0d8-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2c0d8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c0d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c0d8-116">-DefaultProfile</span></span>
<span data-ttu-id="2c0d8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c0d8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c0d8-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c0d8-118">-NetworkWatcher</span></span>
<span data-ttu-id="2c0d8-119">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="2c0d8-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="2c0d8-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2c0d8-120">-NetworkWatcherName</span></span>
<span data-ttu-id="2c0d8-121">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="2c0d8-121">The name of network watcher.</span></span>

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

### <span data-ttu-id="2c0d8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c0d8-122">-ResourceGroupName</span></span>
<span data-ttu-id="2c0d8-123">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="2c0d8-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2c0d8-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="2c0d8-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="2c0d8-125">Идентификатор целевой виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="2c0d8-125">The target VM Id</span></span>

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

### <span data-ttu-id="2c0d8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c0d8-126">CommonParameters</span></span>
<span data-ttu-id="2c0d8-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c0d8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c0d8-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c0d8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c0d8-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c0d8-129">INPUTS</span></span>

### <span data-ttu-id="2c0d8-130">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c0d8-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2c0d8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2c0d8-131">System.String</span></span>

## <span data-ttu-id="2c0d8-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c0d8-132">OUTPUTS</span></span>

### <span data-ttu-id="2c0d8-133">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="2c0d8-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="2c0d8-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c0d8-134">NOTES</span></span>
<span data-ttu-id="2c0d8-135">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, поток, IP</span><span class="sxs-lookup"><span data-stu-id="2c0d8-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="2c0d8-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c0d8-136">RELATED LINKS</span></span>

[<span data-ttu-id="2c0d8-137">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c0d8-137">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2c0d8-138">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c0d8-138">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2c0d8-139">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c0d8-139">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2c0d8-140">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2c0d8-140">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2c0d8-141">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2c0d8-141">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2c0d8-142">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2c0d8-142">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2c0d8-143">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2c0d8-143">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2c0d8-144">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c0d8-144">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2c0d8-145">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2c0d8-145">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2c0d8-146">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c0d8-146">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2c0d8-147">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c0d8-147">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2c0d8-148">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c0d8-148">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

