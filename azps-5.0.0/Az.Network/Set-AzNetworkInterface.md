---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249196"
---
# <span data-ttu-id="cd2cf-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd2cf-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="cd2cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd2cf-102">SYNOPSIS</span></span>
<span data-ttu-id="cd2cf-103">Обновляет сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-103">Updates a network interface.</span></span>

## <span data-ttu-id="cd2cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd2cf-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd2cf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd2cf-105">DESCRIPTION</span></span>
<span data-ttu-id="cd2cf-106">Параметр **Set-AzNetworkInterface** обновляет сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="cd2cf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd2cf-107">EXAMPLES</span></span>

### <span data-ttu-id="cd2cf-108">Пример 1: Настройка сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="cd2cf-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="cd2cf-109">В этом примере осуществляется настройка сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-109">This example configures a network interface.</span></span>
<span data-ttu-id="cd2cf-110">Первая команда получает сетевой интерфейс с именем NetworkInterface1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="cd2cf-111">Вторая команда задает частный IP-адрес конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="cd2cf-112">Третья команда задает статический метод выделения для частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="cd2cf-113">Четвертая команда задает тег в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="cd2cf-114">Пятая команда использует данные, хранящиеся в переменной $Nic, для задания сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="cd2cf-115">Пример 2: изменение параметров DNS для сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="cd2cf-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="cd2cf-116">Первая команда получает сетевой интерфейс с именем NetworkInterface1, который существует в рамках группы ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="cd2cf-117">Вторая команда добавляет DNS-сервер 192.168.1.100 в этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="cd2cf-118">Третья команда применяет эти изменения к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="cd2cf-119">Чтобы удалить DNS-сервер, следуйте приведенным выше командам, но замените ". Добавить "с". Remove (удалить) во второй команде.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="cd2cf-120">Пример 3: включение IP-переадресации на сетевом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="cd2cf-120">Example 3: Enable IP forwarding on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="cd2cf-121">Первая команда возвращает существующий сетевой интерфейс с именем NetworkInterface1 и сохраняет его в переменной $nic.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="cd2cf-122">Вторая команда изменяет значение "перенаправление IP" на "истина".</span><span class="sxs-lookup"><span data-stu-id="cd2cf-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="cd2cf-123">Наконец, третья команда применяет изменения к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="cd2cf-124">Чтобы отключить переадресацию IP на сетевом интерфейсе, следуйте примеру примера, но не забудьте изменить вторую команду на "$nic. EnableIPForwarding = 0 ".</span><span class="sxs-lookup"><span data-stu-id="cd2cf-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="cd2cf-125">Пример 4: изменение подсети сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="cd2cf-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="cd2cf-126">Первая команда получает сетевой интерфейс NetworkInterface1 и сохраняет его в переменной $nic.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="cd2cf-127">Вторая команда возвращает виртуальную сеть, связанную с подсетью, с которой будет связан сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="cd2cf-128">Вторая команда получает подсеть и сохраняет ее в переменной $subnet 2.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="cd2cf-129">Третья команда, связанная с основным частным IP-адресом сетевого интерфейса с новой подсетью.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="cd2cf-130">Наконец, последняя команда применит эти изменения к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="cd2cf-131">Перед изменением подсети должны быть динамические IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="cd2cf-132">Если у вас есть статические IP-конфигурации, измените ее на Dynamic, прежде чем продолжить.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="cd2cf-133">Если у сетевого интерфейса есть несколько конфигураций IP-адресов, перед выполнением последней команды Set-AzNetworkInterface необходимо выполнить команду "вперед" для всех этих конфигураций IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="cd2cf-134">Это можно сделать с помощью команды "вперед", но заменить "0" на нужный номер.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="cd2cf-135">Если сетевой интерфейс имеет N конфигураций IP, должны существовать N-1 этих команд.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="cd2cf-136">Пример 5: связывание и отмена связи группы безопасности сети с сетевым интерфейсом</span><span class="sxs-lookup"><span data-stu-id="cd2cf-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="cd2cf-137">Первая команда возвращает существующий сетевой интерфейс с именем NetworkInterface1 и сохраняет его в переменной $nic.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="cd2cf-138">Вторая команда получает существующую сетевую группу безопасности с именем MyNSG и сохраняет ее в переменной $nsg.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="cd2cf-139">Третья команда назначает $nsg $nicу.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="cd2cf-140">Наконец, команда "вперед" применяет изменения сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="cd2cf-141">Чтобы отменить связь сетевых групп безопасности с сетевым интерфейсом, просто замените $nsg в третьей команде $null.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="cd2cf-142">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd2cf-142">PARAMETERS</span></span>

### <span data-ttu-id="cd2cf-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd2cf-143">-AsJob</span></span>
<span data-ttu-id="cd2cf-144">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cd2cf-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd2cf-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd2cf-145">-DefaultProfile</span></span>
<span data-ttu-id="cd2cf-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd2cf-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd2cf-147">-NetworkInterface</span></span>
<span data-ttu-id="cd2cf-148">Указывает объект сетевого интерфейса, представляющий состояние, для которого должен быть установлен сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

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

### <span data-ttu-id="cd2cf-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd2cf-149">CommonParameters</span></span>
<span data-ttu-id="cd2cf-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd2cf-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd2cf-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd2cf-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd2cf-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd2cf-152">INPUTS</span></span>

### <span data-ttu-id="cd2cf-153">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd2cf-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="cd2cf-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd2cf-154">OUTPUTS</span></span>

### <span data-ttu-id="cd2cf-155">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd2cf-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="cd2cf-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd2cf-156">NOTES</span></span>

## <span data-ttu-id="cd2cf-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd2cf-157">RELATED LINKS</span></span>

[<span data-ttu-id="cd2cf-158">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd2cf-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="cd2cf-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd2cf-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="cd2cf-160">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd2cf-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="cd2cf-161">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd2cf-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
