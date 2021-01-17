---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: dadb58348305434294a9a435a136733f0b6ef1e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422404"
---
# <span data-ttu-id="fff4d-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fff4d-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="fff4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fff4d-102">SYNOPSIS</span></span>
<span data-ttu-id="fff4d-103">Добавляет конфигурацию переднего IP-адреса к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="fff4d-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="fff4d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fff4d-104">SYNTAX</span></span>

### <span data-ttu-id="fff4d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fff4d-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fff4d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fff4d-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fff4d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fff4d-107">DESCRIPTION</span></span>
<span data-ttu-id="fff4d-108">Для шлюза приложения добавляется конфигурация переднего IP-адреса **Add-AzApplicationGatewayFrontendIPConfig.**</span><span class="sxs-lookup"><span data-stu-id="fff4d-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="fff4d-109">Шлюз приложения поддерживает два типа конфигураций переднего IP-адреса:</span><span class="sxs-lookup"><span data-stu-id="fff4d-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="fff4d-110">Общедоступные IP-адреса</span><span class="sxs-lookup"><span data-stu-id="fff4d-110">Public IP addresses</span></span>
- <span data-ttu-id="fff4d-111">Частные IP-адреса с использованием внутренней балансировки нагрузки (ILB) Шлюз приложения может иметь как минимум один общедоступный IP-адрес и один частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="fff4d-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="fff4d-112">Добавьте общедоступный и частный IP-адреса в качестве отдельных ip-адресов переднего ip-адреса.</span><span class="sxs-lookup"><span data-stu-id="fff4d-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="fff4d-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fff4d-113">EXAMPLES</span></span>

### <span data-ttu-id="fff4d-114">Пример 1. Добавление общего IP-адреса в качестве ip-адреса переднего</span><span class="sxs-lookup"><span data-stu-id="fff4d-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="fff4d-115">Первая команда создает общедоступный IP-адрес и сохраняет его в переменной $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="fff4d-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="fff4d-116">Вторая команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw Ресурса.</span><span class="sxs-lookup"><span data-stu-id="fff4d-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fff4d-117">Третья команда добавляет у шлюза в $AppGw ip-адрес переднего $AppGw, используя адрес, $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="fff4d-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="fff4d-118">Пример 2. Добавление статического закрытого IP-адреса в качестве ip-адреса переднего</span><span class="sxs-lookup"><span data-stu-id="fff4d-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="fff4d-119">Первая команда получает виртуальную сеть VNet01, которая принадлежит группе ресурсов ResourceGroup01, и сохраняет ее в переменной $VNet ресурса.</span><span class="sxs-lookup"><span data-stu-id="fff4d-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="fff4d-120">Вторая команда получает конфигурацию подсети "Подсеть" с $VNet из первой команды и сохраняет ее в $Subnet переменной.</span><span class="sxs-lookup"><span data-stu-id="fff4d-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="fff4d-121">Третья команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="fff4d-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fff4d-122">Четвертая команда добавляет конфигурацию переднего IP-адреса FrontendIP02 с использованием $Subnet из второй команды и личного IP-адреса 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="fff4d-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="fff4d-123">Пример 3. Добавление динамического закрытого IP-адреса в качестве IP-адреса переднего</span><span class="sxs-lookup"><span data-stu-id="fff4d-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="fff4d-124">Первая команда получает виртуальную сеть VNet01, которая принадлежит группе ресурсов ResourceGroup01, и сохраняет ее в переменной $VNet ресурса.</span><span class="sxs-lookup"><span data-stu-id="fff4d-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="fff4d-125">Вторая команда получает конфигурацию подсети "Подсеть" с $VNet из первой команды и сохраняет ее в $Subnet переменной.</span><span class="sxs-lookup"><span data-stu-id="fff4d-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="fff4d-126">Третья команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="fff4d-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fff4d-127">Четвертая команда добавляет переднюю конфигурацию IP-адреса FrontendIP02 с $Subnet из второй команды.</span><span class="sxs-lookup"><span data-stu-id="fff4d-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="fff4d-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fff4d-128">PARAMETERS</span></span>

### <span data-ttu-id="fff4d-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fff4d-129">-ApplicationGateway</span></span>
<span data-ttu-id="fff4d-130">Указывает шлюз приложения, к которому этот cmdlet добавляет конфигурацию переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="fff4d-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="fff4d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fff4d-131">-DefaultProfile</span></span>
<span data-ttu-id="fff4d-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fff4d-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fff4d-133">-Name</span><span class="sxs-lookup"><span data-stu-id="fff4d-133">-Name</span></span>
<span data-ttu-id="fff4d-134">Имя ip-конфигурации переднего ip-адреса, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="fff4d-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="fff4d-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="fff4d-135">-PrivateIPAddress</span></span>
<span data-ttu-id="fff4d-136">Указывает частный IP-адрес, который нужно добавить в качестве переднего IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="fff4d-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="fff4d-137">Если задан этот IP-адрес, он статически выделяется из подсети.</span><span class="sxs-lookup"><span data-stu-id="fff4d-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="fff4d-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="fff4d-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="fff4d-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="fff4d-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="fff4d-140">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fff4d-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="fff4d-141">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fff4d-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="fff4d-142">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="fff4d-142">-PublicIPAddress</span></span>
<span data-ttu-id="fff4d-143">Указывает общедоступный IP-адрес, который этот cmdlet добавляет в качестве переднего IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="fff4d-143">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="fff4d-144">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="fff4d-144">-PublicIPAddressId</span></span>
<span data-ttu-id="fff4d-145">Определяет код общего IP-адреса, который этот cmdlet добавляет в качестве переднего IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="fff4d-145">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="fff4d-146">-Subnet</span><span class="sxs-lookup"><span data-stu-id="fff4d-146">-Subnet</span></span>
<span data-ttu-id="fff4d-147">Указывает подсеть, которую этот cmdlet добавляет в качестве конфигурации переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="fff4d-147">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="fff4d-148">Если этот параметр указан, предполагается, что шлюз приложения поддерживает конфигурацию на основе частных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="fff4d-148">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="fff4d-149">Если указан *параметр PrivateIPAddress,* он должен принадлежать этой подсети.</span><span class="sxs-lookup"><span data-stu-id="fff4d-149">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="fff4d-150">Если *адрес PrivateIPAddress* не указан, один из IP-адресов этой подсети динамически выбирается в качестве переднего IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="fff4d-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="fff4d-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="fff4d-151">-SubnetId</span></span>
<span data-ttu-id="fff4d-152">Определяет код подсети, который этот cmdlet добавляет в качестве конфигурации переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="fff4d-152">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="fff4d-153">Передача подсети подразумевает частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="fff4d-153">Passing subnet implies private IP.</span></span>
<span data-ttu-id="fff4d-154">Если указан *параметр PrivateIPAddress,* он должен принадлежать этой подсети.</span><span class="sxs-lookup"><span data-stu-id="fff4d-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="fff4d-155">В противном случае один из IP-адресов из этой подсети динамически выбирается в качестве переднего IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="fff4d-155">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="fff4d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fff4d-156">CommonParameters</span></span>
<span data-ttu-id="fff4d-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fff4d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fff4d-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fff4d-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fff4d-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fff4d-159">INPUTS</span></span>

### <span data-ttu-id="fff4d-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fff4d-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fff4d-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fff4d-161">OUTPUTS</span></span>

### <span data-ttu-id="fff4d-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fff4d-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fff4d-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fff4d-163">NOTES</span></span>

## <span data-ttu-id="fff4d-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fff4d-164">RELATED LINKS</span></span>

[<span data-ttu-id="fff4d-165">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fff4d-165">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fff4d-166">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fff4d-166">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fff4d-167">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fff4d-167">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fff4d-168">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fff4d-168">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


