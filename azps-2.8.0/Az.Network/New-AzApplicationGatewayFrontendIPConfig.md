---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 2ffd1d0a0ab3542636a2deec134d5bd233fd8ffa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902229"
---
# <span data-ttu-id="10d1c-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="10d1c-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="10d1c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10d1c-102">SYNOPSIS</span></span>
<span data-ttu-id="10d1c-103">Создает интерфейсную конфигурацию IP-конфигурации для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="10d1c-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="10d1c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10d1c-104">SYNTAX</span></span>

### <span data-ttu-id="10d1c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="10d1c-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10d1c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="10d1c-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10d1c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10d1c-107">DESCRIPTION</span></span>
<span data-ttu-id="10d1c-108">Командлет **New-AzApplicationGatewayFrontendIPConfig** создает интерфейсную конфигурацию IP-конфигурации для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="10d1c-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuration for an Azure application gateway.</span></span>
<span data-ttu-id="10d1c-109">Шлюз приложений поддерживает два типа интерфейсных IP-конфигураций.</span><span class="sxs-lookup"><span data-stu-id="10d1c-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="10d1c-110">Общедоступные IP-адреса — частные IP-адреса с помощью внутренней балансировки нагрузки (ILB).</span><span class="sxs-lookup"><span data-stu-id="10d1c-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="10d1c-111">У шлюза приложения может быть только один общедоступный IP-адрес и один частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="10d1c-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="10d1c-112">Общедоступный IP-адрес и частный IP-адрес следует добавлять отдельно в качестве интерфейсных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="10d1c-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="10d1c-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10d1c-113">EXAMPLES</span></span>

### <span data-ttu-id="10d1c-114">Пример 1: создание интерфейса IP-конфигурации с помощью общедоступного объекта ресурсов IP</span><span class="sxs-lookup"><span data-stu-id="10d1c-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="10d1c-115">Первая команда создает объект общедоступного ресурса IP и сохраняет его в переменной $PublicIP.</span><span class="sxs-lookup"><span data-stu-id="10d1c-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="10d1c-116">Вторая команда использует $PublicIP для создания новой интерфейсной IP-конфигурации с именем FrontEndIP01 и сохраняет ее в переменной $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="10d1c-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="10d1c-117">Пример 2: Создание статического IP-адреса в качестве интерфейса с интерфейсом пользователя</span><span class="sxs-lookup"><span data-stu-id="10d1c-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="10d1c-118">Первая команда возвращает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $VNet.</span><span class="sxs-lookup"><span data-stu-id="10d1c-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="10d1c-119">Вторая команда получает конфигурацию подсети с именем Subnet01, используя $VNet из первой команды и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="10d1c-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="10d1c-120">Третья команда создает IP-конфигурацию переднего плана с именем FrontEndIP02, используя $Subnet из второй команды и частного IP-адреса 10.0.1.1, а затем сохраняет его в переменной $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="10d1c-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="10d1c-121">Пример 3: Создание динамического закрытого IP-адреса в качестве интерфейса для переднего плана</span><span class="sxs-lookup"><span data-stu-id="10d1c-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="10d1c-122">Первая команда возвращает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $VNet.</span><span class="sxs-lookup"><span data-stu-id="10d1c-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="10d1c-123">Вторая команда получает конфигурацию подсети с именем Subnet01, используя $VNet из первой команды и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="10d1c-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="10d1c-124">Третья команда создает интерфейсную IP-конфигурацию с именем FrontEndIP03, используя $Subnet из второй команды и сохраняет ее в переменной $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="10d1c-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="10d1c-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10d1c-125">PARAMETERS</span></span>

### <span data-ttu-id="10d1c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d1c-126">-DefaultProfile</span></span>
<span data-ttu-id="10d1c-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10d1c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10d1c-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="10d1c-128">-Name</span></span>
<span data-ttu-id="10d1c-129">Задает имя интерфейса IP-конфигурации, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="10d1c-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d1c-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="10d1c-130">-PrivateIPAddress</span></span>
<span data-ttu-id="10d1c-131">Задает частный IP-адрес, с которым этот командлет связывается с интерфейсным IP-адресом шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="10d1c-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="10d1c-132">Это может быть указано только в том случае, если указана подсеть.</span><span class="sxs-lookup"><span data-stu-id="10d1c-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="10d1c-133">Этот IP-адрес является статическим, так как он выделяется из подсети.</span><span class="sxs-lookup"><span data-stu-id="10d1c-133">This IP is statically allocated from the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d1c-134">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="10d1c-134">-PublicIPAddress</span></span>
<span data-ttu-id="10d1c-135">Указывает общедоступный объект IP-адреса, который этот командлет связывает с интерфейсным IP-адресом шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="10d1c-135">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d1c-136">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="10d1c-136">-PublicIPAddressId</span></span>
<span data-ttu-id="10d1c-137">Указывает идентификатор общедоступного IP-адреса, который этот командлет связывает с интерфейсным IP-адресом шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="10d1c-137">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d1c-138">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="10d1c-138">-Subnet</span></span>
<span data-ttu-id="10d1c-139">Указывает объект подсети, с которым этот командлет связывается с интерфейсным IP-адресом шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="10d1c-139">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="10d1c-140">Если указать этот параметр, это означает, что шлюз использует частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="10d1c-140">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="10d1c-141">Если указан параметр *PrivateIPAddress* , он должен принадлежать к подсети, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="10d1c-141">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="10d1c-142">Если *PrivateIPAddress* не указан, то один из IP-адресов из этой подсети динамически выбирается как ИНТЕРФЕЙСНЫЙ IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="10d1c-142">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d1c-143">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="10d1c-143">-SubnetId</span></span>
<span data-ttu-id="10d1c-144">Указывает идентификатор подсети, который этот командлет свяжет с интерфейсной конфигурацией IP на шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="10d1c-144">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="10d1c-145">Если указан параметр *Subnet* , это означает, что шлюз использует частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="10d1c-145">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="10d1c-146">Если указан параметр *PrivateIPAddress* , он должен входить в подсеть, указанную в *подсети*.</span><span class="sxs-lookup"><span data-stu-id="10d1c-146">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="10d1c-147">Если *PrivateIPAddress* не указан, то один из IP-адресов из этой подсети динамически выбирается как ИНТЕРФЕЙСНЫЙ IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="10d1c-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d1c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d1c-148">CommonParameters</span></span>
<span data-ttu-id="10d1c-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10d1c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d1c-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10d1c-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d1c-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10d1c-151">INPUTS</span></span>

### <span data-ttu-id="10d1c-152">Ничего</span><span class="sxs-lookup"><span data-stu-id="10d1c-152">None</span></span>

## <span data-ttu-id="10d1c-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10d1c-153">OUTPUTS</span></span>

### <span data-ttu-id="10d1c-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="10d1c-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="10d1c-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="10d1c-155">NOTES</span></span>

## <span data-ttu-id="10d1c-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10d1c-156">RELATED LINKS</span></span>

[<span data-ttu-id="10d1c-157">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="10d1c-157">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="10d1c-158">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="10d1c-158">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="10d1c-159">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="10d1c-159">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="10d1c-160">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="10d1c-160">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


