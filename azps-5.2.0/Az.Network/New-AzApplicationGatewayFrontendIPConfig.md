---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: c1c2f9fc3cbe528687f0a276c1b5feed3bbdb4b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410319"
---
# <span data-ttu-id="167d5-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="167d5-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="167d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="167d5-102">SYNOPSIS</span></span>
<span data-ttu-id="167d5-103">Создает конфигурацию ip-адреса переднего ip-адреса для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="167d5-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="167d5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="167d5-104">SYNTAX</span></span>

### <span data-ttu-id="167d5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="167d5-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="167d5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="167d5-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="167d5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="167d5-107">DESCRIPTION</span></span>
<span data-ttu-id="167d5-108">Для шлюза приложения Azure создается клиентский IP-адрес конфигурации **New-AzApplicationGatewayFrontendIPConfig.**</span><span class="sxs-lookup"><span data-stu-id="167d5-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuration for an Azure application gateway.</span></span>
<span data-ttu-id="167d5-109">Шлюз приложения поддерживает два типа конфигурации переднего IP-адреса:</span><span class="sxs-lookup"><span data-stu-id="167d5-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="167d5-110">Общедоступные IP-адреса : частные IP-адреса с использованием внутренней балансировки нагрузки (ILB).</span><span class="sxs-lookup"><span data-stu-id="167d5-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="167d5-111">Шлюз приложения может иметь как минимум один общедоступный и один частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="167d5-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="167d5-112">Общедоступный и частный IP-адреса следует добавлять отдельно в качестве IP-адресов переднего.</span><span class="sxs-lookup"><span data-stu-id="167d5-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="167d5-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="167d5-113">EXAMPLES</span></span>

### <span data-ttu-id="167d5-114">Пример 1. Создание передней конфигурации IP-адреса с использованием объекта общедоступных IP-ресурсов</span><span class="sxs-lookup"><span data-stu-id="167d5-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="167d5-115">Первая команда создает объект общедоступных IP-ресурсов и сохраняет его в переменной $PublicIP.</span><span class="sxs-lookup"><span data-stu-id="167d5-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="167d5-116">Вторая команда использует $PublicIP, чтобы создать новую конфигурацию переднего IP-адреса с именем FrontEndIP01 и $FrontEnd переменной.</span><span class="sxs-lookup"><span data-stu-id="167d5-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="167d5-117">Пример 2. Создание статического закрытого IP-адреса в качестве переднего IP-адреса</span><span class="sxs-lookup"><span data-stu-id="167d5-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="167d5-118">Первая команда получает виртуальную сеть VNet01, которая принадлежит к группе ресурсов ResourceGroup01, и сохраняет ее в переменной $VNet ресурса.</span><span class="sxs-lookup"><span data-stu-id="167d5-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="167d5-119">Вторая команда получает конфигурацию подсети "Подсеть" с $VNet из первой команды и сохраняет ее в $Subnet переменной.</span><span class="sxs-lookup"><span data-stu-id="167d5-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="167d5-120">Третья команда создает конфигурацию переднего IP-адреса с именем FrontEndIP02, используя $Subnet из второй команды и личный IP-адрес 10.0.1.1, а затем сохраняет его в переменной $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="167d5-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="167d5-121">Пример 3. Создание динамического закрытого IP-адреса в качестве переднего IP-адреса</span><span class="sxs-lookup"><span data-stu-id="167d5-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="167d5-122">Первая команда получает виртуальную сеть VNet01, которая принадлежит к группе ресурсов ResourceGroup01, и сохраняет ее в переменной $VNet ресурса.</span><span class="sxs-lookup"><span data-stu-id="167d5-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="167d5-123">Вторая команда получает конфигурацию подсети "Подсеть" с $VNet из первой команды и сохраняет ее в $Subnet переменной.</span><span class="sxs-lookup"><span data-stu-id="167d5-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="167d5-124">Третья команда создает конфигурацию переднего IP-адреса с именем FrontEndIP03 $Subnet из второй команды и сохраняет ее в переменной $FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="167d5-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="167d5-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="167d5-125">PARAMETERS</span></span>

### <span data-ttu-id="167d5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="167d5-126">-DefaultProfile</span></span>
<span data-ttu-id="167d5-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="167d5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="167d5-128">-Name</span><span class="sxs-lookup"><span data-stu-id="167d5-128">-Name</span></span>
<span data-ttu-id="167d5-129">Указывает имя ip-конфигурации переднего ip-адреса, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="167d5-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="167d5-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="167d5-130">-PrivateIPAddress</span></span>
<span data-ttu-id="167d5-131">Указывает частный IP-адрес, который этот cmdlet связывает с IP-адресом переднего ip-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="167d5-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="167d5-132">Это можно сделать только в том случае, если указана подсеть.</span><span class="sxs-lookup"><span data-stu-id="167d5-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="167d5-133">Этот IP-адрес статически выделен из подсети.</span><span class="sxs-lookup"><span data-stu-id="167d5-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="167d5-134">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="167d5-134">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="167d5-135">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="167d5-135">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="167d5-136">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="167d5-136">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="167d5-137">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="167d5-137">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="167d5-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="167d5-138">-PublicIPAddress</span></span>
<span data-ttu-id="167d5-139">Указывает общедоступный IP-адрес, который этот cmdlet связывает с IP-адресом переднего ip-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="167d5-139">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="167d5-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="167d5-140">-PublicIPAddressId</span></span>
<span data-ttu-id="167d5-141">Указывает общедоступный IP-адрес, который этот cmdlet связывает с ip-адресом переднего ip-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="167d5-141">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="167d5-142">-Subnet</span><span class="sxs-lookup"><span data-stu-id="167d5-142">-Subnet</span></span>
<span data-ttu-id="167d5-143">Определяет объект подсети, который этот cmdlet связывает с IP-адресом переднего ip-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="167d5-143">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="167d5-144">Если этот параметр указан, предполагается, что шлюз использует частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="167d5-144">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="167d5-145">Если *задан параметр PrivateIPAddress,* он должен принадлежать к подсети, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="167d5-145">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="167d5-146">Если *адрес PrivateIPAddress* не указан, один из IP-адресов этой подсети динамически выбирается в качестве ip-адреса переднего IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="167d5-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="167d5-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="167d5-147">-SubnetId</span></span>
<span data-ttu-id="167d5-148">Определяет код подсети, который этот cmdlet связывает с ip-конфигурацией шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="167d5-148">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="167d5-149">Если указать параметр *"Подсеть",* это означает, что шлюз использует частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="167d5-149">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="167d5-150">Если *задан параметр PrivateIPAddress,* он должен принадлежать к подсети, указанной *подсетей.*</span><span class="sxs-lookup"><span data-stu-id="167d5-150">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="167d5-151">Если *адрес PrivateIPAddress* не указан, один из IP-адресов этой подсети динамически выбирается в качестве ip-адреса переднего IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="167d5-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="167d5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="167d5-152">CommonParameters</span></span>
<span data-ttu-id="167d5-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="167d5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="167d5-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="167d5-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="167d5-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="167d5-155">INPUTS</span></span>

### <span data-ttu-id="167d5-156">Нет</span><span class="sxs-lookup"><span data-stu-id="167d5-156">None</span></span>

## <span data-ttu-id="167d5-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="167d5-157">OUTPUTS</span></span>

### <span data-ttu-id="167d5-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="167d5-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="167d5-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="167d5-159">NOTES</span></span>

## <span data-ttu-id="167d5-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="167d5-160">RELATED LINKS</span></span>

[<span data-ttu-id="167d5-161">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="167d5-161">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="167d5-162">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="167d5-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="167d5-163">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="167d5-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="167d5-164">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="167d5-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


