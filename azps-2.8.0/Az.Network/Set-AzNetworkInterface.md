---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9273c4cf6d23825b931dda696e1a2ef8513aa68d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901781"
---
# <span data-ttu-id="181da-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="181da-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="181da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="181da-102">SYNOPSIS</span></span>
<span data-ttu-id="181da-103">Обновляет сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="181da-103">Updates a network interface.</span></span>

## <span data-ttu-id="181da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="181da-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="181da-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="181da-105">DESCRIPTION</span></span>
<span data-ttu-id="181da-106">Параметр **Set-AzNetworkInterface** обновляет сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="181da-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="181da-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="181da-107">EXAMPLES</span></span>

### <span data-ttu-id="181da-108">Пример 1: Настройка сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="181da-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="181da-109">В этом примере осуществляется настройка сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="181da-109">This example configures a network interface.</span></span>
<span data-ttu-id="181da-110">Первая команда получает сетевой интерфейс с именем NetworkInterface1 в группе ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="181da-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="181da-111">Вторая команда задает частный IP-адрес конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="181da-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="181da-112">Третья команда задает статический метод выделения для частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="181da-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="181da-113">Четвертая команда задает тег в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="181da-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="181da-114">Пятая команда использует данные, хранящиеся в переменной $Nic, для задания сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="181da-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="181da-115">Пример 2: изменение параметров DNS для сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="181da-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="181da-116">Первая команда получает сетевой интерфейс с именем NetworkInterface1, который существует в рамках группы ресурсов ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="181da-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="181da-117">Вторая команда добавляет DNS-сервер 192.168.1.100 в этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="181da-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="181da-118">Третья команда применяет эти изменения к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="181da-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="181da-119">Чтобы удалить DNS-сервер, следуйте приведенным выше командам, но замените ". Добавить "с". Remove (удалить) во второй команде.</span><span class="sxs-lookup"><span data-stu-id="181da-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="181da-120">Пример 3: включение IP-переадресации на сетевом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="181da-120">Example 3: Enable IP forwarding on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="181da-121">Первая команда возвращает существующий сетевой интерфейс с именем NetworkInterface1 и сохраняет его в переменной $nic.</span><span class="sxs-lookup"><span data-stu-id="181da-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="181da-122">Вторая команда изменяет значение "перенаправление IP" на "истина".</span><span class="sxs-lookup"><span data-stu-id="181da-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="181da-123">Наконец, третья команда применяет изменения к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="181da-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="181da-124">Чтобы отключить переадресацию IP на сетевом интерфейсе, следуйте примеру примера, но не забудьте изменить вторую команду на "$nic. EnableIPForwarding = 0 ".</span><span class="sxs-lookup"><span data-stu-id="181da-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="181da-125">Пример 4: изменение подсети сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="181da-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="181da-126">Первая команда получает сетевой интерфейс NetworkInterface1 и сохраняет его в переменной $nic.</span><span class="sxs-lookup"><span data-stu-id="181da-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="181da-127">Вторая команда возвращает виртуальную сеть, связанную с подсетью, с которой будет связан сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="181da-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="181da-128">Вторая команда получает подсеть и сохраняет ее в переменной $subnet 2.</span><span class="sxs-lookup"><span data-stu-id="181da-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="181da-129">Третья команда, связанная с основным частным IP-адресом сетевого интерфейса с новой подсетью.</span><span class="sxs-lookup"><span data-stu-id="181da-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="181da-130">Наконец, последняя команда применит эти изменения к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="181da-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="181da-131">Перед изменением подсети должны быть динамические IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="181da-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="181da-132">Если у вас есть статические IP-конфигурации, измените ее на Dynamic, прежде чем продолжить.</span><span class="sxs-lookup"><span data-stu-id="181da-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="181da-133">Если у сетевого интерфейса есть несколько конфигураций IP-адресов, перед выполнением последней команды Set-AzNetworkInterface необходимо выполнить команду "вперед" для всех этих конфигураций IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="181da-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="181da-134">Это можно сделать с помощью команды "вперед", но заменить "0" на нужный номер.</span><span class="sxs-lookup"><span data-stu-id="181da-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="181da-135">Если сетевой интерфейс имеет N конфигураций IP, должны существовать N-1 этих команд.</span><span class="sxs-lookup"><span data-stu-id="181da-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="181da-136">Пример 5: связывание и отмена связи группы безопасности сети с сетевым интерфейсом</span><span class="sxs-lookup"><span data-stu-id="181da-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="181da-137">Первая команда возвращает существующий сетевой интерфейс с именем NetworkInterface1 и сохраняет его в переменной $nic.</span><span class="sxs-lookup"><span data-stu-id="181da-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="181da-138">Вторая команда получает существующую сетевую группу безопасности с именем MyNSG и сохраняет ее в переменной $nsg.</span><span class="sxs-lookup"><span data-stu-id="181da-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="181da-139">Третья команда назначает $nsg $nicу.</span><span class="sxs-lookup"><span data-stu-id="181da-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="181da-140">Наконец, команда "вперед" применяет изменения сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="181da-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="181da-141">Чтобы отменить связь сетевых групп безопасности с сетевым интерфейсом, просто замените $nsg в третьей команде $null.</span><span class="sxs-lookup"><span data-stu-id="181da-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="181da-142">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="181da-142">PARAMETERS</span></span>

### <span data-ttu-id="181da-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="181da-143">-AsJob</span></span>
<span data-ttu-id="181da-144">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="181da-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="181da-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181da-145">-DefaultProfile</span></span>
<span data-ttu-id="181da-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="181da-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="181da-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="181da-147">-NetworkInterface</span></span>
<span data-ttu-id="181da-148">Указывает объект сетевого интерфейса, представляющий состояние, для которого должен быть установлен сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="181da-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

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

### <span data-ttu-id="181da-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181da-149">CommonParameters</span></span>
<span data-ttu-id="181da-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="181da-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181da-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="181da-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181da-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="181da-152">INPUTS</span></span>

### <span data-ttu-id="181da-153">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="181da-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="181da-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="181da-154">OUTPUTS</span></span>

### <span data-ttu-id="181da-155">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="181da-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="181da-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="181da-156">NOTES</span></span>

## <span data-ttu-id="181da-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="181da-157">RELATED LINKS</span></span>

[<span data-ttu-id="181da-158">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="181da-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="181da-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="181da-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="181da-160">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="181da-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="181da-161">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="181da-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
