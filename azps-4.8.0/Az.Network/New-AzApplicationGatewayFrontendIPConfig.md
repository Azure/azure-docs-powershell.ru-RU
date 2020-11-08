---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: c1c2f9fc3cbe528687f0a276c1b5feed3bbdb4b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236061"
---
# <span data-ttu-id="2a9c2-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2a9c2-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="2a9c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a9c2-102">SYNOPSIS</span></span>
<span data-ttu-id="2a9c2-103">Создает интерфейсную конфигурацию IP-конфигурации для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="2a9c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a9c2-104">SYNTAX</span></span>

### <span data-ttu-id="2a9c2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a9c2-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a9c2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2a9c2-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a9c2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a9c2-107">DESCRIPTION</span></span>
<span data-ttu-id="2a9c2-108">Командлет **New-AzApplicationGatewayFrontendIPConfig** создает интерфейсную конфигурацию IP-конфигурации для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuration for an Azure application gateway.</span></span>
<span data-ttu-id="2a9c2-109">Шлюз приложений поддерживает два типа интерфейсных IP-конфигураций.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="2a9c2-110">Общедоступные IP-адреса — частные IP-адреса с помощью внутренней балансировки нагрузки (ILB).</span><span class="sxs-lookup"><span data-stu-id="2a9c2-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="2a9c2-111">У шлюза приложения может быть только один общедоступный IP-адрес и один частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="2a9c2-112">Общедоступный IP-адрес и частный IP-адрес следует добавлять отдельно в качестве интерфейсных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="2a9c2-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a9c2-113">EXAMPLES</span></span>

### <span data-ttu-id="2a9c2-114">Пример 1: создание интерфейса IP-конфигурации с помощью общедоступного объекта ресурсов IP</span><span class="sxs-lookup"><span data-stu-id="2a9c2-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="2a9c2-115">Первая команда создает объект общедоступного ресурса IP и сохраняет его в переменной $PublicIP.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="2a9c2-116">Вторая команда использует $PublicIP для создания новой интерфейсной IP-конфигурации с именем FrontEndIP01 и сохраняет ее в переменной $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="2a9c2-117">Пример 2: Создание статического IP-адреса в качестве интерфейса с интерфейсом пользователя</span><span class="sxs-lookup"><span data-stu-id="2a9c2-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="2a9c2-118">Первая команда возвращает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $VNet.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="2a9c2-119">Вторая команда получает конфигурацию подсети с именем Subnet01, используя $VNet из первой команды и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="2a9c2-120">Третья команда создает IP-конфигурацию переднего плана с именем FrontEndIP02, используя $Subnet из второй команды и частного IP-адреса 10.0.1.1, а затем сохраняет его в переменной $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="2a9c2-121">Пример 3: Создание динамического закрытого IP-адреса в качестве интерфейса для переднего плана</span><span class="sxs-lookup"><span data-stu-id="2a9c2-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="2a9c2-122">Первая команда возвращает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $VNet.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="2a9c2-123">Вторая команда получает конфигурацию подсети с именем Subnet01, используя $VNet из первой команды и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="2a9c2-124">Третья команда создает интерфейсную IP-конфигурацию с именем FrontEndIP03, используя $Subnet из второй команды и сохраняет ее в переменной $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="2a9c2-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a9c2-125">PARAMETERS</span></span>

### <span data-ttu-id="2a9c2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a9c2-126">-DefaultProfile</span></span>
<span data-ttu-id="2a9c2-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a9c2-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2a9c2-128">-Name</span></span>
<span data-ttu-id="2a9c2-129">Задает имя интерфейса IP-конфигурации, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2a9c2-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="2a9c2-130">-PrivateIPAddress</span></span>
<span data-ttu-id="2a9c2-131">Задает частный IP-адрес, с которым этот командлет связывается с интерфейсным IP-адресом шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="2a9c2-132">Это может быть указано только в том случае, если указана подсеть.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="2a9c2-133">Этот IP-адрес является статическим, так как он выделяется из подсети.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="2a9c2-134">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a9c2-134">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="2a9c2-135">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a9c2-135">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="2a9c2-136">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2a9c2-136">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="2a9c2-137">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2a9c2-137">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="2a9c2-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="2a9c2-138">-PublicIPAddress</span></span>
<span data-ttu-id="2a9c2-139">Указывает общедоступный объект IP-адреса, который этот командлет связывает с интерфейсным IP-адресом шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-139">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="2a9c2-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="2a9c2-140">-PublicIPAddressId</span></span>
<span data-ttu-id="2a9c2-141">Указывает идентификатор общедоступного IP-адреса, который этот командлет связывает с интерфейсным IP-адресом шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-141">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="2a9c2-142">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="2a9c2-142">-Subnet</span></span>
<span data-ttu-id="2a9c2-143">Указывает объект подсети, с которым этот командлет связывается с интерфейсным IP-адресом шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-143">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="2a9c2-144">Если указать этот параметр, это означает, что шлюз использует частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-144">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="2a9c2-145">Если указан параметр *PrivateIPAddress* , он должен принадлежать к подсети, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-145">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="2a9c2-146">Если *PrivateIPAddress* не указан, то один из IP-адресов из этой подсети динамически выбирается как ИНТЕРФЕЙСНЫЙ IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="2a9c2-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2a9c2-147">-SubnetId</span></span>
<span data-ttu-id="2a9c2-148">Указывает идентификатор подсети, который этот командлет свяжет с интерфейсной конфигурацией IP на шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-148">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="2a9c2-149">Если указан параметр *Subnet* , это означает, что шлюз использует частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-149">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="2a9c2-150">Если указан параметр *PrivateIPAddress* , он должен входить в подсеть, указанную в *подсети*.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-150">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="2a9c2-151">Если *PrivateIPAddress* не указан, то один из IP-адресов из этой подсети динамически выбирается как ИНТЕРФЕЙСНЫЙ IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="2a9c2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a9c2-152">CommonParameters</span></span>
<span data-ttu-id="2a9c2-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a9c2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a9c2-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a9c2-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a9c2-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a9c2-155">INPUTS</span></span>

### <span data-ttu-id="2a9c2-156">Ничего</span><span class="sxs-lookup"><span data-stu-id="2a9c2-156">None</span></span>

## <span data-ttu-id="2a9c2-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a9c2-157">OUTPUTS</span></span>

### <span data-ttu-id="2a9c2-158">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a9c2-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="2a9c2-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a9c2-159">NOTES</span></span>

## <span data-ttu-id="2a9c2-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a9c2-160">RELATED LINKS</span></span>

[<span data-ttu-id="2a9c2-161">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2a9c2-161">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2a9c2-162">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2a9c2-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2a9c2-163">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2a9c2-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2a9c2-164">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2a9c2-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


