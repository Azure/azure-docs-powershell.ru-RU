---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: dadb58348305434294a9a435a136733f0b6ef1e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247278"
---
# <span data-ttu-id="0553d-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0553d-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="0553d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0553d-102">SYNOPSIS</span></span>
<span data-ttu-id="0553d-103">Добавление интерфейсной конфигурации IP к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="0553d-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="0553d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0553d-104">SYNTAX</span></span>

### <span data-ttu-id="0553d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0553d-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0553d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0553d-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0553d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0553d-107">DESCRIPTION</span></span>
<span data-ttu-id="0553d-108">Командлет **Add-AzApplicationGatewayFrontendIPConfig** добавляет IP-конфигурацию переднего плана в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="0553d-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="0553d-109">Шлюз приложений поддерживает два типа клиентских конфигураций IP.</span><span class="sxs-lookup"><span data-stu-id="0553d-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="0553d-110">Общедоступные IP-адреса</span><span class="sxs-lookup"><span data-stu-id="0553d-110">Public IP addresses</span></span>
- <span data-ttu-id="0553d-111">Частные IP-адреса с помощью внутренней балансировки нагрузки (ILB). шлюз приложений может иметь не более одного общедоступного IP-адреса и один частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="0553d-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="0553d-112">Добавьте общедоступный IP-адрес и частный IP-адрес в качестве отдельных интерфейсных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="0553d-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="0553d-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0553d-113">EXAMPLES</span></span>

### <span data-ttu-id="0553d-114">Пример 1: Добавление общедоступного IP-адреса в качестве интерфейса пользователя</span><span class="sxs-lookup"><span data-stu-id="0553d-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="0553d-115">Первая команда создает объект общедоступного IP-адреса и сохраняет его в переменной $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="0553d-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="0553d-116">Вторая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0553d-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0553d-117">Третья команда добавляет IP-конфигурацию переднего плана с именем FrontEndIp01 для шлюза в $AppGw, используя адрес, хранящийся в $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="0553d-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="0553d-118">Пример 2: Добавление статического IP-адреса в качестве интерфейса</span><span class="sxs-lookup"><span data-stu-id="0553d-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="0553d-119">Первая команда возвращает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $VNet.</span><span class="sxs-lookup"><span data-stu-id="0553d-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="0553d-120">Вторая команда получает конфигурацию подсети с именем Subnet01, используя $VNet из первой команды и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="0553d-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="0553d-121">Третья команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0553d-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0553d-122">Четвертая команда добавляет IP-конфигурацию переднего плана с именем FrontendIP02, используя $Subnet из второй команды и частного IP-адреса 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="0553d-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="0553d-123">Пример 3. Добавление динамического закрытого IP-адреса в качестве интерфейса для переднего плана</span><span class="sxs-lookup"><span data-stu-id="0553d-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="0553d-124">Первая команда возвращает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $VNet.</span><span class="sxs-lookup"><span data-stu-id="0553d-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="0553d-125">Вторая команда получает конфигурацию подсети с именем Subnet01, используя $VNet из первой команды и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="0553d-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="0553d-126">Третья команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0553d-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0553d-127">Четвертая команда добавляет IP-конфигурацию переднего плана с именем FrontendIP02, используя $Subnet из второй команды.</span><span class="sxs-lookup"><span data-stu-id="0553d-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="0553d-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0553d-128">PARAMETERS</span></span>

### <span data-ttu-id="0553d-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0553d-129">-ApplicationGateway</span></span>
<span data-ttu-id="0553d-130">Указывает шлюз приложений, к которому этот командлет добавляет интерфейс IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0553d-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0553d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0553d-131">-DefaultProfile</span></span>
<span data-ttu-id="0553d-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0553d-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0553d-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0553d-133">-Name</span></span>
<span data-ttu-id="0553d-134">Указывает имя добавляемой интерфейсной конфигурации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="0553d-134">Specifies the name of the front-end IP configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0553d-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="0553d-135">-PrivateIPAddress</span></span>
<span data-ttu-id="0553d-136">Задает частный IP-адрес, который добавляется в качестве интерфейса IP для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0553d-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="0553d-137">Если указан, этот IP-адрес выделяется из подсети статически.</span><span class="sxs-lookup"><span data-stu-id="0553d-137">If specified, this IP is statically allocated from the subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0553d-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0553d-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="0553d-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0553d-139">PrivateLinkConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0553d-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0553d-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="0553d-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0553d-141">PrivateLinkConfigurationId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0553d-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="0553d-142">-PublicIPAddress</span></span>
<span data-ttu-id="0553d-143">Указывает общедоступный IP-адрес, который добавляется этим командлетом в качестве клиентского IP-адреса для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0553d-143">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0553d-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="0553d-144">-PublicIPAddressId</span></span>
<span data-ttu-id="0553d-145">Указывает идентификатор общедоступного IP-адреса, который добавляется этим командлетом в качестве клиентского IP-адреса для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0553d-145">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0553d-146">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="0553d-146">-Subnet</span></span>
<span data-ttu-id="0553d-147">Указывает подсеть, которая добавляется этим командлетом в качестве интерфейсной конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="0553d-147">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="0553d-148">Если указать этот параметр, это означает, что шлюз приложения поддерживает личную конфигурацию на основе IP.</span><span class="sxs-lookup"><span data-stu-id="0553d-148">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="0553d-149">Если указан параметр *PrivateIPAddress* , он должен входить в эту подсеть.</span><span class="sxs-lookup"><span data-stu-id="0553d-149">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="0553d-150">Если *PrivateIPAddress* не указан, то один из IP-адресов из этой подсети динамически выбирается как ИНТЕРФЕЙСНЫЙ IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0553d-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0553d-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0553d-151">-SubnetId</span></span>
<span data-ttu-id="0553d-152">Указывает идентификатор подсети, который добавляется этим командлетом в качестве интерфейсной конфигурации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="0553d-152">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="0553d-153">Передача подсети подразумевает использование частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="0553d-153">Passing subnet implies private IP.</span></span>
<span data-ttu-id="0553d-154">Если указан параметр *PrivateIPAddress* , он должен входить в эту подсеть.</span><span class="sxs-lookup"><span data-stu-id="0553d-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="0553d-155">В противном случае один из IP-адресов из этой подсети динамически выбирается как интерфейсный IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0553d-155">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0553d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0553d-156">CommonParameters</span></span>
<span data-ttu-id="0553d-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0553d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0553d-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0553d-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0553d-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0553d-159">INPUTS</span></span>

### <span data-ttu-id="0553d-160">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0553d-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0553d-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0553d-161">OUTPUTS</span></span>

### <span data-ttu-id="0553d-162">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0553d-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0553d-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="0553d-163">NOTES</span></span>

## <span data-ttu-id="0553d-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0553d-164">RELATED LINKS</span></span>

[<span data-ttu-id="0553d-165">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0553d-165">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0553d-166">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0553d-166">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0553d-167">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0553d-167">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0553d-168">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0553d-168">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


