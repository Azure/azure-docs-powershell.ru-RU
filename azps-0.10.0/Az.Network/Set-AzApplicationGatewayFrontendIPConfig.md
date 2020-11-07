---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: e85976f77ece9af89ecd532ff0a3236039abb9fd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911073"
---
# <span data-ttu-id="3730e-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3730e-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="3730e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3730e-102">SYNOPSIS</span></span>
<span data-ttu-id="3730e-103">Изменяет конфигурацию IP-адреса интерфейса пользователя.</span><span class="sxs-lookup"><span data-stu-id="3730e-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="3730e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3730e-104">SYNTAX</span></span>

### <span data-ttu-id="3730e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3730e-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3730e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3730e-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3730e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3730e-107">DESCRIPTION</span></span>
<span data-ttu-id="3730e-108">Командлет **Set-AzApplicationGatewayFrontendIPConfig** обновляет интерфейсную конфигурацию IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3730e-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>

<span data-ttu-id="3730e-109">Шлюз приложений поддерживает два типа интерфейсных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="3730e-109">An application gateway supports two types of front-end IP addresses:</span></span> 

- <span data-ttu-id="3730e-110">Общедоступные IP-адреса</span><span class="sxs-lookup"><span data-stu-id="3730e-110">Public IP addresses</span></span>
- <span data-ttu-id="3730e-111">Частные IP-адреса, для которых в конфигурации используется внутренняя балансировка нагрузки (ILB).</span><span class="sxs-lookup"><span data-stu-id="3730e-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB)</span></span>

<span data-ttu-id="3730e-112">У шлюза приложения может быть только один общедоступный IP-адрес и один частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="3730e-112">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="3730e-113">Общедоступный IP-адрес и частный IP-адрес следует добавлять отдельно в качестве интерфейсных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="3730e-113">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="3730e-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3730e-114">EXAMPLES</span></span>

### <span data-ttu-id="3730e-115">Пример 1: настройка общедоступного IP-адреса в качестве интерфейса IP для шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="3730e-115">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="3730e-116">Первая команда создает объект общедоступного IP-адреса и сохраняет его в переменной $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="3730e-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>

<span data-ttu-id="3730e-117">Вторая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3730e-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="3730e-118">Третья команда обновляет IP-конфигурацию переднего плана с именем FrontEndIp01 для шлюза в $AppGw, используя адрес, хранящийся в $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="3730e-118">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="3730e-119">Пример 2. Установка статического IP-адреса в качестве клиентского IP-адреса шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="3730e-119">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="3730e-120">Первая команда возвращает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $VNet.</span><span class="sxs-lookup"><span data-stu-id="3730e-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="3730e-121">Вторая команда получает конфигурацию подсети с именем Subnet01, используя $VNet из первой команды и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="3730e-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="3730e-122">Третья команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3730e-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="3730e-123">Четвертая команда добавляет IP-конфигурацию переднего плана с именем FrontendIP02, используя $Subnet из второй команды и частного IP-адреса 10.0.1.1.</span><span class="sxs-lookup"><span data-stu-id="3730e-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="3730e-124">Пример 3: Настройка динамического частного IP-адреса в качестве клиентского IP-адреса шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="3730e-124">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="3730e-125">Первая команда возвращает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $VNet.</span><span class="sxs-lookup"><span data-stu-id="3730e-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="3730e-126">Вторая команда получает конфигурацию подсети с именем Subnet01, используя $VNet из первой команды и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="3730e-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="3730e-127">Третья команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3730e-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="3730e-128">Четвертая команда добавляет IP-конфигурацию переднего плана с именем FrontendIP02, используя $Subnet из второй команды.</span><span class="sxs-lookup"><span data-stu-id="3730e-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="3730e-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3730e-129">PARAMETERS</span></span>

### <span data-ttu-id="3730e-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3730e-130">-ApplicationGateway</span></span>
<span data-ttu-id="3730e-131">Указывает объект шлюза приложения, в котором будет изменена IP-конфигурация интерфейса пользователя.</span><span class="sxs-lookup"><span data-stu-id="3730e-131">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="3730e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3730e-132">-DefaultProfile</span></span>
<span data-ttu-id="3730e-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3730e-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3730e-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3730e-134">-Name</span></span>
<span data-ttu-id="3730e-135">Указывает имя конфигурации переднего плана IP-адреса, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3730e-135">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3730e-136">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="3730e-136">-PrivateIPAddress</span></span>
<span data-ttu-id="3730e-137">Задает частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="3730e-137">Specifies the private IP address.</span></span>
<span data-ttu-id="3730e-138">Если указан, этот IP-адрес выделяется из подсети статически.</span><span class="sxs-lookup"><span data-stu-id="3730e-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="3730e-139">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="3730e-139">-PublicIPAddress</span></span>
<span data-ttu-id="3730e-140">Указывает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="3730e-140">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="3730e-141">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="3730e-141">-PublicIPAddressId</span></span>
<span data-ttu-id="3730e-142">Указывает идентификатор общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3730e-142">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="3730e-143">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="3730e-143">-Subnet</span></span>
<span data-ttu-id="3730e-144">Указывает подсеть, используемую шлюзом приложений.</span><span class="sxs-lookup"><span data-stu-id="3730e-144">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="3730e-145">Укажите этот параметр, если шлюз использует частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="3730e-145">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="3730e-146">Если указан адрес *PrivateIPAddress* , он должен входить в эту подсеть.</span><span class="sxs-lookup"><span data-stu-id="3730e-146">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="3730e-147">Если *PrivateIPAddress* не указан, то один из IP-адресов из этой подсети динамически выбирается как ИНТЕРФЕЙСНЫЙ IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="3730e-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="3730e-148">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3730e-148">-SubnetId</span></span>
<span data-ttu-id="3730e-149">Указывает идентификатор подсети.</span><span class="sxs-lookup"><span data-stu-id="3730e-149">Specifies the subnet ID.</span></span>
<span data-ttu-id="3730e-150">Укажите этот параметр, если шлюз использует частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="3730e-150">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="3730e-151">Если указан параметр *PrivateIPAddress* , он должен входить в эту подсеть.</span><span class="sxs-lookup"><span data-stu-id="3730e-151">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="3730e-152">Если *PrivateIPAddress* не указан, то один из IP-адресов из этой подсети динамически выбирается как ИНТЕРФЕЙСНЫЙ IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="3730e-152">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="3730e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3730e-153">CommonParameters</span></span>
<span data-ttu-id="3730e-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3730e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3730e-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3730e-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3730e-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3730e-156">INPUTS</span></span>

### <span data-ttu-id="3730e-157">System. String</span><span class="sxs-lookup"><span data-stu-id="3730e-157">System.String</span></span>

## <span data-ttu-id="3730e-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3730e-158">OUTPUTS</span></span>

### <span data-ttu-id="3730e-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3730e-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3730e-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="3730e-160">NOTES</span></span>

## <span data-ttu-id="3730e-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3730e-161">RELATED LINKS</span></span>

[<span data-ttu-id="3730e-162">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3730e-162">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3730e-163">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3730e-163">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3730e-164">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3730e-164">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3730e-165">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3730e-165">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3730e-166">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3730e-166">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


