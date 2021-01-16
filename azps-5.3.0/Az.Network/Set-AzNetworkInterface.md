---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519894"
---
# <span data-ttu-id="67e8c-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="67e8c-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="67e8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="67e8c-103">Обновляет сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="67e8c-103">Updates a network interface.</span></span>

## <span data-ttu-id="67e8c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67e8c-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67e8c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67e8c-105">DESCRIPTION</span></span>
<span data-ttu-id="67e8c-106">Шрифт **Set-AzNetworkInterface** обновляет сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="67e8c-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="67e8c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67e8c-107">EXAMPLES</span></span>

### <span data-ttu-id="67e8c-108">Пример 1. Настройка сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="67e8c-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="67e8c-109">В этом примере настроен сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="67e8c-109">This example configures a network interface.</span></span>
<span data-ttu-id="67e8c-110">Первая команда получает сетевой интерфейс NetworkInterface1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="67e8c-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="67e8c-111">Вторая команда задает частный IP-адрес конфигурации IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="67e8c-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="67e8c-112">Третья команда задает способ выделения частных IP-адресов статический.</span><span class="sxs-lookup"><span data-stu-id="67e8c-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="67e8c-113">Четвертая команда задает тег в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="67e8c-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="67e8c-114">Пятая команда использует данные из переменной $Nic для изменения сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="67e8c-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="67e8c-115">Пример 2. Изменение параметров DNS в интерфейсе сети</span><span class="sxs-lookup"><span data-stu-id="67e8c-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="67e8c-116">Первая команда получает сетевой интерфейс NetworkInterface1, который существует в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="67e8c-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="67e8c-117">Вторая команда добавляет в интерфейс DNS-сервер 192.168.1.100.</span><span class="sxs-lookup"><span data-stu-id="67e8c-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="67e8c-118">Третья команда применяет эти изменения к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="67e8c-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="67e8c-119">Чтобы удалить DNS-сервер, выполните указанные выше команды, но замените ". "Добавить" с помощью ". Удалить" во второй команде.</span><span class="sxs-lookup"><span data-stu-id="67e8c-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="67e8c-120">Пример 3. Включить переадваровку IP-адресов в сетевом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="67e8c-120">Example 3: Enable IP forwarding on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="67e8c-121">Первая команда получает существующий сетевой интерфейс NetworkInterface1 и сохраняет его в переменной $nic.</span><span class="sxs-lookup"><span data-stu-id="67e8c-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="67e8c-122">Вторая команда изменяет значение переадваровки IP-адресов на истина.</span><span class="sxs-lookup"><span data-stu-id="67e8c-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="67e8c-123">Наконец, изменения в сетевом интерфейсе применяются третьей командой.</span><span class="sxs-lookup"><span data-stu-id="67e8c-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="67e8c-124">Чтобы отключить переадваровку IP-адресов в сетевом интерфейсе, выполните пример, но обязательно измените вторую команду на "$nic. EnableIPForwarding = 0".</span><span class="sxs-lookup"><span data-stu-id="67e8c-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="67e8c-125">Пример 4. Изменение подсети сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="67e8c-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="67e8c-126">Первая команда получает сетевой интерфейс NetworkInterface1 и сохраняет его в переменной $nic.</span><span class="sxs-lookup"><span data-stu-id="67e8c-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="67e8c-127">Вторая команда возвращает виртуальную сеть, связанную с подсетью, с которую будет связан сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="67e8c-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="67e8c-128">Вторая команда получает подсеть и сохраняет ее в переменной $subnet 2.</span><span class="sxs-lookup"><span data-stu-id="67e8c-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="67e8c-129">Третья команда, связанная с основным частным IP-адресом сетевого интерфейса, с новой подсетей.</span><span class="sxs-lookup"><span data-stu-id="67e8c-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="67e8c-130">Наконец, эти изменения применены последней командой в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="67e8c-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="67e8c-131">Для изменения подсети конфигурации IP-адресов должны быть динамическими.</span><span class="sxs-lookup"><span data-stu-id="67e8c-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="67e8c-132">Если у вас есть статические конфигурации IP-адресов, перед началом процедуры измените его на динамический.</span><span class="sxs-lookup"><span data-stu-id="67e8c-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="67e8c-133">Если в сетевом интерфейсе несколько конфигураций IP-адресов, для всех этих конфигураций необходимо выполнять конечную команду Set-AzNetworkInterface IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="67e8c-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="67e8c-134">Это можно сделать с помощью команды, которая была заменена на "0" соответствующим номером.</span><span class="sxs-lookup"><span data-stu-id="67e8c-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="67e8c-135">Если сетевой интерфейс имеет конфигурацию N IP, то N-1 из этих команд должны существовать.</span><span class="sxs-lookup"><span data-stu-id="67e8c-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="67e8c-136">Пример 5. Связывать и диссоциировать группу безопасности сети с сетевым интерфейсом</span><span class="sxs-lookup"><span data-stu-id="67e8c-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="67e8c-137">Первая команда получает существующий сетевой интерфейс NetworkInterface1 и сохраняет его в переменной $nic.</span><span class="sxs-lookup"><span data-stu-id="67e8c-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="67e8c-138">Вторая команда получает существующую группу безопасности сети MyNSG и сохраняет ее в переменной $nsg сети.</span><span class="sxs-lookup"><span data-stu-id="67e8c-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="67e8c-139">Третья команда назначает $nsg $nic.</span><span class="sxs-lookup"><span data-stu-id="67e8c-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="67e8c-140">Наконец, с помощью этой команды изменения применяются к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="67e8c-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="67e8c-141">Чтобы отменить группировку безопасности в сетевом интерфейсе, просто замените $nsg третьей командой на $null.</span><span class="sxs-lookup"><span data-stu-id="67e8c-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="67e8c-142">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67e8c-142">PARAMETERS</span></span>

### <span data-ttu-id="67e8c-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67e8c-143">-AsJob</span></span>
<span data-ttu-id="67e8c-144">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="67e8c-144">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67e8c-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e8c-145">-DefaultProfile</span></span>
<span data-ttu-id="67e8c-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67e8c-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67e8c-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="67e8c-147">-NetworkInterface</span></span>
<span data-ttu-id="67e8c-148">Определяет объект сетевого интерфейса, представляющий состояние, в котором должен быть установлен сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="67e8c-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67e8c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e8c-149">CommonParameters</span></span>
<span data-ttu-id="67e8c-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67e8c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e8c-151">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67e8c-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e8c-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67e8c-152">INPUTS</span></span>

### <span data-ttu-id="67e8c-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="67e8c-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="67e8c-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67e8c-154">OUTPUTS</span></span>

### <span data-ttu-id="67e8c-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="67e8c-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="67e8c-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67e8c-156">NOTES</span></span>

## <span data-ttu-id="67e8c-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67e8c-157">RELATED LINKS</span></span>

[<span data-ttu-id="67e8c-158">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="67e8c-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="67e8c-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="67e8c-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="67e8c-160">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="67e8c-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="67e8c-161">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="67e8c-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
