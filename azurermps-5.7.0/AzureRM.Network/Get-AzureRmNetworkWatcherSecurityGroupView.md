---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 5b48cbabfe91b16924a1296a73354db659ec8f3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734984"
---
# <span data-ttu-id="dd305-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="dd305-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="dd305-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd305-102">SYNOPSIS</span></span>
<span data-ttu-id="dd305-103">Просмотр настроенных и эффективных правил сетевой группы безопасности, примененных к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="dd305-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd305-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd305-104">SYNTAX</span></span>

### <span data-ttu-id="dd305-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd305-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd305-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="dd305-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd305-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd305-107">DESCRIPTION</span></span>
<span data-ttu-id="dd305-108">Get-AzureRmNetworkWatcherSecurityGroupView позволяет просматривать настроенные и эффективные правила групп безопасности сети, примененные к ВМ.</span><span class="sxs-lookup"><span data-stu-id="dd305-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="dd305-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd305-109">EXAMPLES</span></span>

### <span data-ttu-id="dd305-110">---Пример 1: вызов представления группы безопасности на виртуальной машине---</span><span class="sxs-lookup"><span data-stu-id="dd305-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="dd305-111">В приведенном выше примере сначала нужно получить доступ к региональному наблюдатель сети, а затем виртуальной машине в регионе.</span><span class="sxs-lookup"><span data-stu-id="dd305-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="dd305-112">Затем мы создаем на выбранной виртуальной машине вызов представления группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="dd305-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="dd305-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd305-113">PARAMETERS</span></span>

### <span data-ttu-id="dd305-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd305-114">-AsJob</span></span>
<span data-ttu-id="dd305-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="dd305-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd305-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd305-116">-DefaultProfile</span></span>
<span data-ttu-id="dd305-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd305-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd305-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dd305-118">-NetworkWatcher</span></span>
<span data-ttu-id="dd305-119">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="dd305-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="dd305-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="dd305-120">-NetworkWatcherName</span></span>
<span data-ttu-id="dd305-121">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="dd305-121">The name of network watcher.</span></span>

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

### <span data-ttu-id="dd305-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd305-122">-ResourceGroupName</span></span>
<span data-ttu-id="dd305-123">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="dd305-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="dd305-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="dd305-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="dd305-125">Идентификатор целевой виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="dd305-125">The target VM Id</span></span>

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

### <span data-ttu-id="dd305-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd305-126">CommonParameters</span></span>
<span data-ttu-id="dd305-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd305-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd305-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd305-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd305-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd305-129">INPUTS</span></span>

### <span data-ttu-id="dd305-130">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dd305-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="dd305-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dd305-131">System.String</span></span>

## <span data-ttu-id="dd305-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd305-132">OUTPUTS</span></span>

### <span data-ttu-id="dd305-133">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="dd305-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="dd305-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd305-134">NOTES</span></span>
<span data-ttu-id="dd305-135">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, поток, IP</span><span class="sxs-lookup"><span data-stu-id="dd305-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="dd305-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd305-136">RELATED LINKS</span></span>

[<span data-ttu-id="dd305-137">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dd305-137">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dd305-138">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dd305-138">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dd305-139">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dd305-139">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dd305-140">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="dd305-140">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="dd305-141">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="dd305-141">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="dd305-142">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="dd305-142">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="dd305-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="dd305-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="dd305-144">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dd305-144">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dd305-145">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="dd305-145">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="dd305-146">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dd305-146">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dd305-147">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dd305-147">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dd305-148">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dd305-148">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

