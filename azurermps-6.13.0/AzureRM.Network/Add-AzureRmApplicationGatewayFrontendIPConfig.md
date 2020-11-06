---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: d19f5489adff642ad9b02a7f3bb364338bd1e566
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568890"
---
# <span data-ttu-id="da374-101">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="da374-101">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="da374-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da374-102">SYNOPSIS</span></span>
<span data-ttu-id="da374-103">Добавление интерфейсной конфигурации IP к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="da374-103">Adds a front-end IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da374-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da374-104">SYNTAX</span></span>

### <span data-ttu-id="da374-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="da374-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da374-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="da374-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da374-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da374-107">DESCRIPTION</span></span>
<span data-ttu-id="da374-108">Командлет **Add-AzureRmApplicationGatewayFrontendIPConfig** добавляет IP-конфигурацию переднего плана в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="da374-108">The **Add-AzureRmApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="da374-109">Шлюз приложений поддерживает два типа клиентских конфигураций IP.</span><span class="sxs-lookup"><span data-stu-id="da374-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="da374-110">Общедоступные IP-адреса</span><span class="sxs-lookup"><span data-stu-id="da374-110">Public IP addresses</span></span>
- <span data-ttu-id="da374-111">Частные IP-адреса с помощью внутренней балансировки нагрузки (ILB). шлюз приложений может иметь не более одного общедоступного IP-адреса и один частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="da374-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="da374-112">Добавьте общедоступный IP-адрес и частный IP-адрес в качестве отдельных интерфейсных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="da374-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="da374-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da374-113">EXAMPLES</span></span>

### <span data-ttu-id="da374-114">Пример 1: Добавление общедоступного IP-адреса в качестве интерфейса пользователя</span><span class="sxs-lookup"><span data-stu-id="da374-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="da374-115">Первая команда создает объект общедоступного IP-адреса и сохраняет его в переменной $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="da374-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="da374-116">Вторая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="da374-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="da374-117">Третья команда добавляет IP-конфигурацию переднего плана с именем FrontEndIp01 для шлюза в $AppGw, используя адрес, хранящийся в $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="da374-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="da374-118">Пример 2: Добавление статического IP-адреса в качестве интерфейса</span><span class="sxs-lookup"><span data-stu-id="da374-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="da374-119">Первая команда возвращает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $VNet.</span><span class="sxs-lookup"><span data-stu-id="da374-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="da374-120">Вторая команда получает конфигурацию подсети с именем Subnet01, используя $VNet из первой команды и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="da374-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="da374-121">Третья команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="da374-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="da374-122">Четвертая команда добавляет IP-конфигурацию переднего плана с именем FrontendIP02, используя $Subnet из второй команды и частного IP-адреса 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="da374-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="da374-123">Пример 3. Добавление динамического закрытого IP-адреса в качестве интерфейса для переднего плана</span><span class="sxs-lookup"><span data-stu-id="da374-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="da374-124">Первая команда возвращает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $VNet.</span><span class="sxs-lookup"><span data-stu-id="da374-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="da374-125">Вторая команда получает конфигурацию подсети с именем Subnet01, используя $VNet из первой команды и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="da374-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="da374-126">Третья команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="da374-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="da374-127">Четвертая команда добавляет IP-конфигурацию переднего плана с именем FrontendIP02, используя $Subnet из второй команды.</span><span class="sxs-lookup"><span data-stu-id="da374-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="da374-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da374-128">PARAMETERS</span></span>

### <span data-ttu-id="da374-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="da374-129">-ApplicationGateway</span></span>
<span data-ttu-id="da374-130">Указывает шлюз приложений, к которому этот командлет добавляет интерфейс IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="da374-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="da374-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da374-131">-DefaultProfile</span></span>
<span data-ttu-id="da374-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da374-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da374-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="da374-133">-Name</span></span>
<span data-ttu-id="da374-134">Указывает имя добавляемой интерфейсной конфигурации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="da374-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="da374-135">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="da374-135">-PrivateIPAddress</span></span>
<span data-ttu-id="da374-136">Задает частный IP-адрес, который добавляется в качестве интерфейса IP для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="da374-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="da374-137">Если указан, этот IP-адрес выделяется из подсети статически.</span><span class="sxs-lookup"><span data-stu-id="da374-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="da374-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="da374-138">-PublicIPAddress</span></span>
<span data-ttu-id="da374-139">Указывает общедоступный IP-адрес, который добавляется этим командлетом в качестве клиентского IP-адреса для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="da374-139">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="da374-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="da374-140">-PublicIPAddressId</span></span>
<span data-ttu-id="da374-141">Указывает идентификатор общедоступного IP-адреса, который добавляется этим командлетом в качестве клиентского IP-адреса для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="da374-141">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="da374-142">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="da374-142">-Subnet</span></span>
<span data-ttu-id="da374-143">Указывает подсеть, которая добавляется этим командлетом в качестве интерфейсной конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="da374-143">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="da374-144">Если указать этот параметр, это означает, что шлюз приложения поддерживает личную конфигурацию на основе IP.</span><span class="sxs-lookup"><span data-stu-id="da374-144">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="da374-145">Если указан параметр *PrivateIPAddress* , он должен входить в эту подсеть.</span><span class="sxs-lookup"><span data-stu-id="da374-145">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="da374-146">Если *PrivateIPAddress* не указан, то один из IP-адресов из этой подсети динамически выбирается как ИНТЕРФЕЙСНЫЙ IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="da374-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="da374-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="da374-147">-SubnetId</span></span>
<span data-ttu-id="da374-148">Указывает идентификатор подсети, который добавляется этим командлетом в качестве интерфейсной конфигурации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="da374-148">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="da374-149">Передача подсети подразумевает использование частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="da374-149">Passing subnet implies private IP.</span></span>
<span data-ttu-id="da374-150">Если указан параметр *PrivateIPAddresss* , он должен входить в эту подсеть.</span><span class="sxs-lookup"><span data-stu-id="da374-150">If the *PrivateIPAddresss* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="da374-151">В противном случае один из IP-адресов из этой подсети динамически выбирается как интерфейсный IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="da374-151">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="da374-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da374-152">CommonParameters</span></span>
<span data-ttu-id="da374-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da374-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da374-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da374-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da374-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da374-155">INPUTS</span></span>

### <span data-ttu-id="da374-156">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="da374-156">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="da374-157">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="da374-157">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="da374-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da374-158">OUTPUTS</span></span>

### <span data-ttu-id="da374-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="da374-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="da374-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="da374-160">NOTES</span></span>

## <span data-ttu-id="da374-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da374-161">RELATED LINKS</span></span>

[<span data-ttu-id="da374-162">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="da374-162">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="da374-163">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="da374-163">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="da374-164">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="da374-164">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="da374-165">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="da374-165">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


