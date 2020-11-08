---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 30238f9466e87ab732b1b2b6d30bba26bcd4c83a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074325"
---
# <span data-ttu-id="2d9d2-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2d9d2-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="2d9d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d9d2-102">SYNOPSIS</span></span>
<span data-ttu-id="2d9d2-103">Добавление интерфейсной конфигурации IP к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="2d9d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d9d2-104">SYNTAX</span></span>

### <span data-ttu-id="2d9d2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2d9d2-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d9d2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2d9d2-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d9d2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d9d2-107">DESCRIPTION</span></span>
<span data-ttu-id="2d9d2-108">Командлет **Add-AzApplicationGatewayFrontendIPConfig** добавляет IP-конфигурацию переднего плана в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="2d9d2-109">Шлюз приложений поддерживает два типа клиентских конфигураций IP.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="2d9d2-110">Общедоступные IP-адреса</span><span class="sxs-lookup"><span data-stu-id="2d9d2-110">Public IP addresses</span></span>
- <span data-ttu-id="2d9d2-111">Частные IP-адреса с помощью внутренней балансировки нагрузки (ILB). шлюз приложений может иметь не более одного общедоступного IP-адреса и один частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="2d9d2-112">Добавьте общедоступный IP-адрес и частный IP-адрес в качестве отдельных интерфейсных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="2d9d2-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d9d2-113">EXAMPLES</span></span>

### <span data-ttu-id="2d9d2-114">Пример 1: Добавление общедоступного IP-адреса в качестве интерфейса пользователя</span><span class="sxs-lookup"><span data-stu-id="2d9d2-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="2d9d2-115">Первая команда создает объект общедоступного IP-адреса и сохраняет его в переменной $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="2d9d2-116">Вторая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2d9d2-117">Третья команда добавляет IP-конфигурацию переднего плана с именем FrontEndIp01 для шлюза в $AppGw, используя адрес, хранящийся в $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="2d9d2-118">Пример 2: Добавление статического IP-адреса в качестве интерфейса</span><span class="sxs-lookup"><span data-stu-id="2d9d2-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="2d9d2-119">Первая команда возвращает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $VNet.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="2d9d2-120">Вторая команда получает конфигурацию подсети с именем Subnet01, используя $VNet из первой команды и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="2d9d2-121">Третья команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2d9d2-122">Четвертая команда добавляет IP-конфигурацию переднего плана с именем FrontendIP02, используя $Subnet из второй команды и частного IP-адреса 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="2d9d2-123">Пример 3. Добавление динамического закрытого IP-адреса в качестве интерфейса для переднего плана</span><span class="sxs-lookup"><span data-stu-id="2d9d2-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="2d9d2-124">Первая команда возвращает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $VNet.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="2d9d2-125">Вторая команда получает конфигурацию подсети с именем Subnet01, используя $VNet из первой команды и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="2d9d2-126">Третья команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2d9d2-127">Четвертая команда добавляет IP-конфигурацию переднего плана с именем FrontendIP02, используя $Subnet из второй команды.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="2d9d2-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d9d2-128">PARAMETERS</span></span>

### <span data-ttu-id="2d9d2-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d9d2-129">-ApplicationGateway</span></span>
<span data-ttu-id="2d9d2-130">Указывает шлюз приложений, к которому этот командлет добавляет интерфейс IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d9d2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d9d2-131">-DefaultProfile</span></span>
<span data-ttu-id="2d9d2-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d9d2-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2d9d2-133">-Name</span></span>
<span data-ttu-id="2d9d2-134">Указывает имя добавляемой интерфейсной конфигурации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="2d9d2-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="2d9d2-135">-PrivateIPAddress</span></span>
<span data-ttu-id="2d9d2-136">Задает частный IP-адрес, который добавляется в качестве интерфейса IP для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="2d9d2-137">Если указан, этот IP-адрес выделяется из подсети статически.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="2d9d2-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="2d9d2-138">-PublicIPAddress</span></span>
<span data-ttu-id="2d9d2-139">Указывает общедоступный IP-адрес, который добавляется этим командлетом в качестве клиентского IP-адреса для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-139">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="2d9d2-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="2d9d2-140">-PublicIPAddressId</span></span>
<span data-ttu-id="2d9d2-141">Указывает идентификатор общедоступного IP-адреса, который добавляется этим командлетом в качестве клиентского IP-адреса для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-141">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="2d9d2-142">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="2d9d2-142">-Subnet</span></span>
<span data-ttu-id="2d9d2-143">Указывает подсеть, которая добавляется этим командлетом в качестве интерфейсной конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-143">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="2d9d2-144">Если указать этот параметр, это означает, что шлюз приложения поддерживает личную конфигурацию на основе IP.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-144">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="2d9d2-145">Если указан параметр *PrivateIPAddress* , он должен входить в эту подсеть.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-145">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="2d9d2-146">Если *PrivateIPAddress* не указан, то один из IP-адресов из этой подсети динамически выбирается как ИНТЕРФЕЙСНЫЙ IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="2d9d2-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2d9d2-147">-SubnetId</span></span>
<span data-ttu-id="2d9d2-148">Указывает идентификатор подсети, который добавляется этим командлетом в качестве интерфейсной конфигурации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-148">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="2d9d2-149">Передача подсети подразумевает использование частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-149">Passing subnet implies private IP.</span></span>
<span data-ttu-id="2d9d2-150">Если указан параметр *PrivateIPAddress* , он должен входить в эту подсеть.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-150">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="2d9d2-151">В противном случае один из IP-адресов из этой подсети динамически выбирается как интерфейсный IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-151">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="2d9d2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d9d2-152">CommonParameters</span></span>
<span data-ttu-id="2d9d2-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d9d2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d9d2-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d9d2-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d9d2-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d9d2-155">INPUTS</span></span>

### <span data-ttu-id="2d9d2-156">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d9d2-156">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2d9d2-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d9d2-157">OUTPUTS</span></span>

### <span data-ttu-id="2d9d2-158">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d9d2-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2d9d2-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d9d2-159">NOTES</span></span>

## <span data-ttu-id="2d9d2-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d9d2-160">RELATED LINKS</span></span>

[<span data-ttu-id="2d9d2-161">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2d9d2-161">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2d9d2-162">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2d9d2-162">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2d9d2-163">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2d9d2-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2d9d2-164">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2d9d2-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


