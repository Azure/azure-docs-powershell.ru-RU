---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: b72b072307ee4d8ae304888e2d1b3db4a36be3aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328554"
---
# <span data-ttu-id="90ade-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="90ade-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="90ade-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90ade-102">SYNOPSIS</span></span>
<span data-ttu-id="90ade-103">Изменяет конфигурацию переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="90ade-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="90ade-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="90ade-104">SYNTAX</span></span>

### <span data-ttu-id="90ade-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="90ade-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90ade-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="90ade-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90ade-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90ade-107">DESCRIPTION</span></span>
<span data-ttu-id="90ade-108">Для обновления ip-конфигурации переднего ip-адреса обновляется проектлет **Set-AzApplicationGatewayFrontendIPConfig.**</span><span class="sxs-lookup"><span data-stu-id="90ade-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="90ade-109">Шлюз приложения поддерживает два типа IP-адресов переднего типа:</span><span class="sxs-lookup"><span data-stu-id="90ade-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="90ade-110">Общедоступные IP-адреса</span><span class="sxs-lookup"><span data-stu-id="90ade-110">Public IP addresses</span></span>
- <span data-ttu-id="90ade-111">Частные IP-адреса, для которых в конфигурации используется внутренняя балансировка нагрузки (ILB), шлюз приложения может иметь как минимум один общедоступный IP-адрес и один частный.</span><span class="sxs-lookup"><span data-stu-id="90ade-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="90ade-112">Общедоступный и частный IP-адреса следует добавлять отдельно в качестве IP-адресов переднего.</span><span class="sxs-lookup"><span data-stu-id="90ade-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="90ade-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="90ade-113">EXAMPLES</span></span>

### <span data-ttu-id="90ade-114">Пример 1. Настройка общего IP-адреса в качестве переднего IP-адреса шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="90ade-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="90ade-115">Первая команда создает общедоступный IP-адрес и сохраняет его в переменной $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="90ade-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="90ade-116">Вторая команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw Ресурса.</span><span class="sxs-lookup"><span data-stu-id="90ade-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="90ade-117">Третья команда обновляет ip-конфигурацию переднего IP-адреса FrontEndIp01 для шлюза в $AppGw, используя адрес, $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="90ade-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="90ade-118">Пример 2. Настройка статического закрытого IP-адреса в качестве переднего IP-адреса шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="90ade-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="90ade-119">Первая команда получает виртуальную сеть VNet01, которая принадлежит группе ресурсов ResourceGroup01, и сохраняет ее в переменной $VNet ресурса.</span><span class="sxs-lookup"><span data-stu-id="90ade-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="90ade-120">Вторая команда получает конфигурацию подсети "Подсеть" с $VNet из первой команды и сохраняет ее в $Subnet переменной.</span><span class="sxs-lookup"><span data-stu-id="90ade-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="90ade-121">Третья команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="90ade-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="90ade-122">Четвертая команда добавляет конфигурацию переднего IP-адреса FrontendIP02 с использованием $Subnet из второй команды и личного IP-адреса 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="90ade-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="90ade-123">Пример 3. Настройка динамического закрытого IP-адреса в качестве переднего IP-адреса шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="90ade-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="90ade-124">Первая команда получает виртуальную сеть VNet01, которая принадлежит группе ресурсов ResourceGroup01, и сохраняет ее в переменной $VNet ресурса.</span><span class="sxs-lookup"><span data-stu-id="90ade-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="90ade-125">Вторая команда получает конфигурацию подсети "Подсеть" с $VNet из первой команды и сохраняет ее в $Subnet переменной.</span><span class="sxs-lookup"><span data-stu-id="90ade-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="90ade-126">Третья команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="90ade-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="90ade-127">Четвертая команда добавляет переднюю конфигурацию IP-адреса FrontendIP02 с $Subnet из второй команды.</span><span class="sxs-lookup"><span data-stu-id="90ade-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="90ade-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90ade-128">PARAMETERS</span></span>

### <span data-ttu-id="90ade-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90ade-129">-ApplicationGateway</span></span>
<span data-ttu-id="90ade-130">Указывает объект шлюза приложения, в котором нужно изменить конфигурацию переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="90ade-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="90ade-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ade-131">-DefaultProfile</span></span>
<span data-ttu-id="90ade-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90ade-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90ade-133">-Name</span><span class="sxs-lookup"><span data-stu-id="90ade-133">-Name</span></span>
<span data-ttu-id="90ade-134">Указывает имя ip-конфигурации переднего ip-адреса, которая изменяется этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90ade-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="90ade-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="90ade-135">-PrivateIPAddress</span></span>
<span data-ttu-id="90ade-136">Указывает частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="90ade-136">Specifies the private IP address.</span></span>
<span data-ttu-id="90ade-137">Если задан этот IP-адрес, он статически выделяется из подсети.</span><span class="sxs-lookup"><span data-stu-id="90ade-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="90ade-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="90ade-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="90ade-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="90ade-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="90ade-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="90ade-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="90ade-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="90ade-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="90ade-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="90ade-142">-PublicIPAddress</span></span>
<span data-ttu-id="90ade-143">Указывает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="90ade-143">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="90ade-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="90ade-144">-PublicIPAddressId</span></span>
<span data-ttu-id="90ade-145">Определяет ИД общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="90ade-145">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="90ade-146">-Subnet</span><span class="sxs-lookup"><span data-stu-id="90ade-146">-Subnet</span></span>
<span data-ttu-id="90ade-147">Подсеть, которая используется шлюзом приложения.</span><span class="sxs-lookup"><span data-stu-id="90ade-147">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="90ade-148">Укажите этот параметр, если шлюз использует частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="90ade-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="90ade-149">Если указан *адрес PrivateIPAddress,* он должен принадлежать данной подсети.</span><span class="sxs-lookup"><span data-stu-id="90ade-149">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="90ade-150">Если *адрес PrivateIPAddress* не указан, один из IP-адресов этой подсети динамически выбирается в качестве ip-адреса переднего IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="90ade-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="90ade-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="90ade-151">-SubnetId</span></span>
<span data-ttu-id="90ade-152">Определяет ИД подсети.</span><span class="sxs-lookup"><span data-stu-id="90ade-152">Specifies the subnet ID.</span></span>
<span data-ttu-id="90ade-153">Укажите этот параметр, если шлюз использует частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="90ade-153">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="90ade-154">Если указан *параметр PrivateIPAddress,* он должен принадлежать этой подсети.</span><span class="sxs-lookup"><span data-stu-id="90ade-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="90ade-155">Если *адрес PrivateIPAddress* не указан, один из IP-адресов этой подсети динамически выбирается в качестве переднего IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="90ade-155">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="90ade-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ade-156">CommonParameters</span></span>
<span data-ttu-id="90ade-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90ade-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ade-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90ade-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ade-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90ade-159">INPUTS</span></span>

### <span data-ttu-id="90ade-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90ade-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="90ade-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="90ade-161">OUTPUTS</span></span>

### <span data-ttu-id="90ade-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90ade-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="90ade-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="90ade-163">NOTES</span></span>

## <span data-ttu-id="90ade-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90ade-164">RELATED LINKS</span></span>

[<span data-ttu-id="90ade-165">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="90ade-165">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="90ade-166">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="90ade-166">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="90ade-167">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="90ade-167">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="90ade-168">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="90ade-168">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="90ade-169">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="90ade-169">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


