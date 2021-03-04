---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 17ef06c6f91f650da95ddcbfb87b09a60c1948d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956787"
---
# <span data-ttu-id="785ba-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="785ba-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="785ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="785ba-102">SYNOPSIS</span></span>
<span data-ttu-id="785ba-103">Изменяет конфигурацию IP-адреса переднего ip-адреса.</span><span class="sxs-lookup"><span data-stu-id="785ba-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="785ba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="785ba-104">SYNTAX</span></span>

### <span data-ttu-id="785ba-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="785ba-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="785ba-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="785ba-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="785ba-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="785ba-107">DESCRIPTION</span></span>
<span data-ttu-id="785ba-108">Для обновления ip-конфигурации переднего ip-адреса обновляется проектлет **Set-AzApplicationGatewayFrontendIPConfig.**</span><span class="sxs-lookup"><span data-stu-id="785ba-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="785ba-109">Шлюз приложения поддерживает два типа IP-адресов переднего типа:</span><span class="sxs-lookup"><span data-stu-id="785ba-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="785ba-110">Общедоступные IP-адреса</span><span class="sxs-lookup"><span data-stu-id="785ba-110">Public IP addresses</span></span>
- <span data-ttu-id="785ba-111">Частные IP-адреса, для которых в конфигурации используется внутренняя балансировка нагрузки (ILB), шлюз приложения может иметь как минимум один общедоступный IP-адрес и один частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="785ba-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="785ba-112">Общедоступный и частный IP-адреса следует добавлять отдельно в качестве IP-адресов переднего.</span><span class="sxs-lookup"><span data-stu-id="785ba-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="785ba-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="785ba-113">EXAMPLES</span></span>

### <span data-ttu-id="785ba-114">Пример 1. Настройка общего IP-адреса в качестве переднего IP-адреса шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="785ba-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="785ba-115">Первая команда создает общедоступный IP-адрес и сохраняет его в переменной $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="785ba-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="785ba-116">Вторая команда получает шлюз приложения ApplicationGateway01, который принадлежит группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw Ресурса.</span><span class="sxs-lookup"><span data-stu-id="785ba-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="785ba-117">Третья команда обновляет ip-конфигурацию переднего IP-адреса FrontEndIp01 для шлюза в $AppGw, используя адрес, $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="785ba-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="785ba-118">Пример 2. Настройка статического закрытого IP-адреса в качестве переднего IP-адреса шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="785ba-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="785ba-119">Первая команда получает виртуальную сеть VNet01, которая принадлежит к группе ресурсов ResourceGroup01, и сохраняет ее в переменной $VNet ресурса.</span><span class="sxs-lookup"><span data-stu-id="785ba-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="785ba-120">Вторая команда получает конфигурацию подсети "Подсеть" с $VNet из первой команды и сохраняет ее в $Subnet переменной.</span><span class="sxs-lookup"><span data-stu-id="785ba-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="785ba-121">Третья команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="785ba-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="785ba-122">Четвертая команда добавляет конфигурацию переднего IP-адреса FrontendIP02 с использованием $Subnet из второй команды и личного IP-адреса 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="785ba-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="785ba-123">Пример 3. Настройка динамического закрытого IP-адреса в качестве переднего IP-адреса шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="785ba-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="785ba-124">Первая команда получает виртуальную сеть VNet01, которая принадлежит к группе ресурсов ResourceGroup01, и сохраняет ее в переменной $VNet ресурса.</span><span class="sxs-lookup"><span data-stu-id="785ba-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="785ba-125">Вторая команда получает конфигурацию подсети "Подсеть" с $VNet из первой команды и сохраняет ее в $Subnet переменной.</span><span class="sxs-lookup"><span data-stu-id="785ba-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="785ba-126">Третья команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="785ba-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="785ba-127">Четвертая команда добавляет переднюю конфигурацию IP-адреса FrontendIP02 с $Subnet из второй команды.</span><span class="sxs-lookup"><span data-stu-id="785ba-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="785ba-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="785ba-128">PARAMETERS</span></span>

### <span data-ttu-id="785ba-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="785ba-129">-ApplicationGateway</span></span>
<span data-ttu-id="785ba-130">Указывает объект шлюза приложения, в котором нужно изменить конфигурацию переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="785ba-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="785ba-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="785ba-131">-DefaultProfile</span></span>
<span data-ttu-id="785ba-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="785ba-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="785ba-133">-Name</span><span class="sxs-lookup"><span data-stu-id="785ba-133">-Name</span></span>
<span data-ttu-id="785ba-134">Указывает имя ip-конфигурации переднего ip-адреса, которая изменяется этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="785ba-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="785ba-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="785ba-135">-PrivateIPAddress</span></span>
<span data-ttu-id="785ba-136">Указывает частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="785ba-136">Specifies the private IP address.</span></span>
<span data-ttu-id="785ba-137">При этом этот IP-адрес статически выделяется из подсети.</span><span class="sxs-lookup"><span data-stu-id="785ba-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="785ba-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="785ba-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="785ba-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="785ba-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="785ba-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="785ba-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="785ba-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="785ba-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="785ba-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="785ba-142">-PublicIPAddress</span></span>
<span data-ttu-id="785ba-143">Указывает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="785ba-143">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="785ba-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="785ba-144">-PublicIPAddressId</span></span>
<span data-ttu-id="785ba-145">Определяет ИД общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="785ba-145">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="785ba-146">-Subnet</span><span class="sxs-lookup"><span data-stu-id="785ba-146">-Subnet</span></span>
<span data-ttu-id="785ba-147">Подсеть, которая используется шлюзом приложения.</span><span class="sxs-lookup"><span data-stu-id="785ba-147">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="785ba-148">Укажите этот параметр, если шлюз использует частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="785ba-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="785ba-149">Если указан *адрес PrivateIPAddress,* он должен принадлежать данной подсети.</span><span class="sxs-lookup"><span data-stu-id="785ba-149">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="785ba-150">Если *адрес PrivateIPAddress* не указан, один из IP-адресов этой подсети динамически выбирается в качестве ip-адреса переднего IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="785ba-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="785ba-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="785ba-151">-SubnetId</span></span>
<span data-ttu-id="785ba-152">Определяет ИД подсети.</span><span class="sxs-lookup"><span data-stu-id="785ba-152">Specifies the subnet ID.</span></span>
<span data-ttu-id="785ba-153">Укажите этот параметр, если шлюз использует частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="785ba-153">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="785ba-154">Если указан *параметр PrivateIPAddress,* он должен принадлежать этой подсети.</span><span class="sxs-lookup"><span data-stu-id="785ba-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="785ba-155">Если *адрес PrivateIPAddress* не указан, один из IP-адресов этой подсети динамически выбирается в качестве ip-адреса переднего IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="785ba-155">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="785ba-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="785ba-156">CommonParameters</span></span>
<span data-ttu-id="785ba-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="785ba-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="785ba-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="785ba-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="785ba-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="785ba-159">INPUTS</span></span>

### <span data-ttu-id="785ba-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="785ba-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="785ba-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="785ba-161">OUTPUTS</span></span>

### <span data-ttu-id="785ba-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="785ba-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="785ba-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="785ba-163">NOTES</span></span>

## <span data-ttu-id="785ba-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="785ba-164">RELATED LINKS</span></span>

[<span data-ttu-id="785ba-165">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="785ba-165">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="785ba-166">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="785ba-166">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="785ba-167">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="785ba-167">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="785ba-168">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="785ba-168">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="785ba-169">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="785ba-169">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


