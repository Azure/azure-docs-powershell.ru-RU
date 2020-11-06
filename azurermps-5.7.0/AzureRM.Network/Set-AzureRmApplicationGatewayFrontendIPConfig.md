---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 38a74e6f11516b3a873709dfec118ffd2a1ad6ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568558"
---
# <span data-ttu-id="617eb-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="617eb-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="617eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="617eb-102">SYNOPSIS</span></span>
<span data-ttu-id="617eb-103">Изменяет конфигурацию IP-адреса интерфейса пользователя.</span><span class="sxs-lookup"><span data-stu-id="617eb-103">Modifies a front-end IP address configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="617eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="617eb-104">SYNTAX</span></span>

### <span data-ttu-id="617eb-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="617eb-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="617eb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="617eb-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="617eb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="617eb-107">DESCRIPTION</span></span>
<span data-ttu-id="617eb-108">Командлет **Set-AzureRmApplicationGatewayFrontendIPConfig** обновляет интерфейсную конфигурацию IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="617eb-108">The **Set-AzureRmApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>

<span data-ttu-id="617eb-109">Шлюз приложений поддерживает два типа интерфейсных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="617eb-109">An application gateway supports two types of front-end IP addresses:</span></span> 

- <span data-ttu-id="617eb-110">Общедоступные IP-адреса</span><span class="sxs-lookup"><span data-stu-id="617eb-110">Public IP addresses</span></span>
- <span data-ttu-id="617eb-111">Частные IP-адреса, для которых в конфигурации используется внутренняя балансировка нагрузки (ILB).</span><span class="sxs-lookup"><span data-stu-id="617eb-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB)</span></span>

<span data-ttu-id="617eb-112">У шлюза приложения может быть только один общедоступный IP-адрес и один частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="617eb-112">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="617eb-113">Общедоступный IP-адрес и частный IP-адрес следует добавлять отдельно в качестве интерфейсных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="617eb-113">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="617eb-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="617eb-114">EXAMPLES</span></span>

### <span data-ttu-id="617eb-115">Пример 1: настройка общедоступного IP-адреса в качестве интерфейса IP для шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="617eb-115">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="617eb-116">Первая команда создает объект общедоступного IP-адреса и сохраняет его в переменной $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="617eb-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>

<span data-ttu-id="617eb-117">Вторая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="617eb-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="617eb-118">Третья команда обновляет IP-конфигурацию переднего плана с именем FrontEndIp01 для шлюза в $AppGw, используя адрес, хранящийся в $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="617eb-118">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="617eb-119">Пример 2. Установка статического IP-адреса в качестве клиентского IP-адреса шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="617eb-119">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="617eb-120">Первая команда возвращает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $VNet.</span><span class="sxs-lookup"><span data-stu-id="617eb-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="617eb-121">Вторая команда получает конфигурацию подсети с именем Subnet01, используя $VNet из первой команды и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="617eb-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="617eb-122">Третья команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="617eb-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="617eb-123">Четвертая команда добавляет IP-конфигурацию переднего плана с именем FrontendIP02, используя $Subnet из второй команды и частного IP-адреса 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="617eb-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="617eb-124">Пример 3: Настройка динамического частного IP-адреса в качестве клиентского IP-адреса шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="617eb-124">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="617eb-125">Первая команда возвращает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $VNet.</span><span class="sxs-lookup"><span data-stu-id="617eb-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="617eb-126">Вторая команда получает конфигурацию подсети с именем Subnet01, используя $VNet из первой команды и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="617eb-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="617eb-127">Третья команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="617eb-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="617eb-128">Четвертая команда добавляет IP-конфигурацию переднего плана с именем FrontendIP02, используя $Subnet из второй команды.</span><span class="sxs-lookup"><span data-stu-id="617eb-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="617eb-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="617eb-129">PARAMETERS</span></span>

### <span data-ttu-id="617eb-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="617eb-130">-ApplicationGateway</span></span>
<span data-ttu-id="617eb-131">Указывает объект шлюза приложения, в котором будет изменена IP-конфигурация интерфейса пользователя.</span><span class="sxs-lookup"><span data-stu-id="617eb-131">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="617eb-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="617eb-132">-DefaultProfile</span></span>
<span data-ttu-id="617eb-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="617eb-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="617eb-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="617eb-134">-Name</span></span>
<span data-ttu-id="617eb-135">Указывает имя конфигурации переднего плана IP-адреса, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="617eb-135">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="617eb-136">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="617eb-136">-PrivateIPAddress</span></span>
<span data-ttu-id="617eb-137">Задает частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="617eb-137">Specifies the private IP address.</span></span>
<span data-ttu-id="617eb-138">Если указан, этот IP-адрес выделяется из подсети статически.</span><span class="sxs-lookup"><span data-stu-id="617eb-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="617eb-139">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="617eb-139">-PublicIPAddress</span></span>
<span data-ttu-id="617eb-140">Указывает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="617eb-140">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="617eb-141">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="617eb-141">-PublicIPAddressId</span></span>
<span data-ttu-id="617eb-142">Указывает идентификатор общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="617eb-142">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="617eb-143">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="617eb-143">-Subnet</span></span>
<span data-ttu-id="617eb-144">Указывает подсеть, используемую шлюзом приложений.</span><span class="sxs-lookup"><span data-stu-id="617eb-144">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="617eb-145">Укажите этот параметр, если шлюз использует частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="617eb-145">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="617eb-146">Если указан адрес *PrivateIPAddress* , он должен входить в эту подсеть.</span><span class="sxs-lookup"><span data-stu-id="617eb-146">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="617eb-147">Если *PrivateIPAddress* не указан, то один из IP-адресов из этой подсети динамически выбирается как ИНТЕРФЕЙСНЫЙ IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="617eb-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="617eb-148">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="617eb-148">-SubnetId</span></span>
<span data-ttu-id="617eb-149">Указывает идентификатор подсети.</span><span class="sxs-lookup"><span data-stu-id="617eb-149">Specifies the subnet ID.</span></span>
<span data-ttu-id="617eb-150">Укажите этот параметр, если шлюз использует частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="617eb-150">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="617eb-151">Если указан параметр *PrivateIPAddress* , он должен входить в эту подсеть.</span><span class="sxs-lookup"><span data-stu-id="617eb-151">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="617eb-152">Если *PrivateIPAddress* не указан, то один из IP-адресов из этой подсети динамически выбирается как ИНТЕРФЕЙСНЫЙ IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="617eb-152">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="617eb-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="617eb-153">CommonParameters</span></span>
<span data-ttu-id="617eb-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="617eb-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="617eb-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="617eb-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="617eb-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="617eb-156">INPUTS</span></span>

### <span data-ttu-id="617eb-157">System. String</span><span class="sxs-lookup"><span data-stu-id="617eb-157">System.String</span></span>

## <span data-ttu-id="617eb-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="617eb-158">OUTPUTS</span></span>

### <span data-ttu-id="617eb-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="617eb-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="617eb-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="617eb-160">NOTES</span></span>

## <span data-ttu-id="617eb-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="617eb-161">RELATED LINKS</span></span>

[<span data-ttu-id="617eb-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="617eb-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="617eb-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="617eb-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="617eb-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="617eb-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="617eb-165">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="617eb-165">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="617eb-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="617eb-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)


