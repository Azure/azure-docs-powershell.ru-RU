---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: a9751806760a8e2265737e72d726fb491191fa5d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566962"
---
# <span data-ttu-id="2a1e5-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a1e5-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="2a1e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a1e5-102">SYNOPSIS</span></span>
<span data-ttu-id="2a1e5-103">Создание шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a1e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a1e5-104">SYNTAX</span></span>

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-FrontendIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]>]
 -FrontendPorts <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]>
 [-Probes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]>]
 -BackendAddressPools <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>
 -BackendHttpSettingsCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]>
 -HttpListeners <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]>
 [-UrlPathMaps <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]>]
 -RequestRoutingRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]>
 [-RedirectConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-EnableHttp2] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a1e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a1e5-105">DESCRIPTION</span></span>
<span data-ttu-id="2a1e5-106">Командлет **New-AzureRmApplicationGateway** создает шлюз приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="2a1e5-107">Для шлюза приложений требуются указанные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="2a1e5-108">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-108">A resource group.</span></span>
- <span data-ttu-id="2a1e5-109">Виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-109">A virtual network.</span></span>
- <span data-ttu-id="2a1e5-110">Пул серверного сервера, содержащий IP-адреса серверных серверов.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="2a1e5-111">Параметры пула серверов для заднего сервера.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-111">Back-end server pool settings.</span></span> <span data-ttu-id="2a1e5-112">У каждого пула есть такие параметры, как порт, протокол и сходство на основе файлов cookie, которые применяются ко всем серверам в пуле.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="2a1e5-113">IP-адреса переднего плана, которые являются IP-адресами, открытыми на шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="2a1e5-114">Интерфейсный IP-адрес может быть общедоступным IP-адресом или внутренним IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="2a1e5-115">Внешние порты, которые являются общедоступными портами, открытыми на шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="2a1e5-116">Трафик, который нажимает эти порты, перенаправляется на серверные серверы.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="2a1e5-117">Правило маршрутизации запросов, связывающее прослушиватель и пул серверного сервера.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="2a1e5-118">Правило определяет, на какой серверный пул должен перенаправляться трафик при каждом обращении к определенному прослушивателю.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="2a1e5-119">У прослушивателя есть интерфейсный порт, клиентский IP-адрес, протокол (HTTP или HTTPS) и имя сертификата SSL (при настройке разгрузки SSL).</span><span class="sxs-lookup"><span data-stu-id="2a1e5-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="2a1e5-120">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a1e5-120">EXAMPLES</span></span>

### <span data-ttu-id="2a1e5-121">Пример 1: Создание шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="2a1e5-121">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzureRmResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzureRmApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzureRmApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzureRmApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="2a1e5-122">В следующем примере создается шлюз приложений, в результате чего создаются группа ресурсов и виртуальная сеть, а также указанные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="2a1e5-123">Пул серверов в серверной части</span><span class="sxs-lookup"><span data-stu-id="2a1e5-123">A back-end server pool</span></span>
- <span data-ttu-id="2a1e5-124">Параметры пула серверов в серверной части</span><span class="sxs-lookup"><span data-stu-id="2a1e5-124">Back-end server pool settings</span></span>
- <span data-ttu-id="2a1e5-125">Интерфейсные порты</span><span class="sxs-lookup"><span data-stu-id="2a1e5-125">Front-end ports</span></span>
- <span data-ttu-id="2a1e5-126">IP-адреса интерфейса пользователя</span><span class="sxs-lookup"><span data-stu-id="2a1e5-126">Front-end IP addresses</span></span>
- <span data-ttu-id="2a1e5-127">Правило маршрутизации запросов</span><span class="sxs-lookup"><span data-stu-id="2a1e5-127">A request routing rule</span></span>

<span data-ttu-id="2a1e5-128">Эти четыре команды создают виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="2a1e5-129">Первая команда создает конфигурацию подсети.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="2a1e5-130">Вторая команда создает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="2a1e5-131">Третья команда проверяет конфигурацию подсети, а четвертая команда проверяет, успешно ли создана виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="2a1e5-132">Следующие команды создают шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="2a1e5-133">Первая команда создает IP-конфигурацию с именем GatewayIp01 для подсети, созданной ранее.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="2a1e5-134">Вторая команда создает пул серверных серверов с именем Pool01 со списком серверных IP-адресов и сохраняет пул в переменной $Pool.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="2a1e5-135">Третья команда создает параметры для пула ресурсов на внутреннем сервере и сохраняет параметры в переменной $PoolSetting.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="2a1e5-136">В этой команде создается порт переднего плана на порту 80 с именем FrontEndPort01 и хранится порт в переменной $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="2a1e5-137">Пятая команда создает общедоступный IP-адрес с помощью New-AzureRmPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-137">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="2a1e5-138">Шестая команда создает IP-конфигурацию переднего плана с помощью $PublicIp, называет ее FrontEndPortConfig01 и сохраняет в переменной $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="2a1e5-139">Команда седьмая создает прослушиватель с помощью ранее созданного $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="2a1e5-140">Восьмая команда создает правило для слушателя.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="2a1e5-141">Команда девятка задает SKU.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="2a1e5-142">Десятая команда создает шлюз, используя объекты, заданные предыдущими командами.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="2a1e5-143">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a1e5-143">PARAMETERS</span></span>

### <span data-ttu-id="2a1e5-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a1e5-144">-AsJob</span></span>
<span data-ttu-id="2a1e5-145">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2a1e5-145">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-146">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="2a1e5-146">-AuthenticationCertificates</span></span>
<span data-ttu-id="2a1e5-147">Определяет сертификаты проверки подлинности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-147">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-148">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="2a1e5-148">-BackendAddressPools</span></span>
<span data-ttu-id="2a1e5-149">Указывает список пулов серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-149">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-150">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="2a1e5-150">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="2a1e5-151">Указывает список параметров HTTP для серверного шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-151">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a1e5-152">-DefaultProfile</span></span>
<span data-ttu-id="2a1e5-153">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a1e5-154">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="2a1e5-154">-EnableHttp2</span></span>
<span data-ttu-id="2a1e5-155">Включена ли HTTP2.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-155">Whether HTTP2 is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-156">-Force</span><span class="sxs-lookup"><span data-stu-id="2a1e5-156">-Force</span></span>
<span data-ttu-id="2a1e5-157">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-157">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-158">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="2a1e5-158">-FrontendIPConfigurations</span></span>
<span data-ttu-id="2a1e5-159">Задает список IP-конфигураций интерфейсов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-159">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-160">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="2a1e5-160">-FrontendPorts</span></span>
<span data-ttu-id="2a1e5-161">Задает список интерфейсных портов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-161">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-162">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="2a1e5-162">-GatewayIPConfigurations</span></span>
<span data-ttu-id="2a1e5-163">Задает список IP-конфигураций для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-163">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-164">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="2a1e5-164">-HttpListeners</span></span>
<span data-ttu-id="2a1e5-165">Задает список прослушивателей HTTP для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-165">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-166">-Location</span><span class="sxs-lookup"><span data-stu-id="2a1e5-166">-Location</span></span>
<span data-ttu-id="2a1e5-167">Указывает область, в которой нужно создать шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-167">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-168">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2a1e5-168">-Name</span></span>
<span data-ttu-id="2a1e5-169">Указывает имя шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-169">Specifies the name of application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-170">-Зонды</span><span class="sxs-lookup"><span data-stu-id="2a1e5-170">-Probes</span></span>
<span data-ttu-id="2a1e5-171">Указывает зонды для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-171">Specifies probes for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-172">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="2a1e5-172">-RedirectConfigurations</span></span>
<span data-ttu-id="2a1e5-173">Список конфигурации перенаправления</span><span class="sxs-lookup"><span data-stu-id="2a1e5-173">The list of redirect configuration</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-174">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="2a1e5-174">-RequestRoutingRules</span></span>
<span data-ttu-id="2a1e5-175">Указывает список правил маршрутизации запросов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-175">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-176">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a1e5-176">-ResourceGroupName</span></span>
<span data-ttu-id="2a1e5-177">Указывает имя группы ресурсов, в которой нужно создать шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-177">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-178">-SKU</span><span class="sxs-lookup"><span data-stu-id="2a1e5-178">-Sku</span></span>
<span data-ttu-id="2a1e5-179">Задает единицу хранения (SKU) шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-179">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySku
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-180">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="2a1e5-180">-SslCertificates</span></span>
<span data-ttu-id="2a1e5-181">Указывает список SSL-сертификатов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-181">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-182">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="2a1e5-182">-SslPolicy</span></span>
<span data-ttu-id="2a1e5-183">Указывает политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-183">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-184">-Тег</span><span class="sxs-lookup"><span data-stu-id="2a1e5-184">-Tag</span></span>
<span data-ttu-id="2a1e5-185">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-185">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2a1e5-186">Например:</span><span class="sxs-lookup"><span data-stu-id="2a1e5-186">For example:</span></span>

<span data-ttu-id="2a1e5-187">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="2a1e5-187">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-188">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="2a1e5-188">-UrlPathMaps</span></span>
<span data-ttu-id="2a1e5-189">Указывает карты URL-пути для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-189">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-190">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a1e5-190">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="2a1e5-191">Определяет конфигурацию брандмауэра веб-приложения (WAF).</span><span class="sxs-lookup"><span data-stu-id="2a1e5-191">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="2a1e5-192">Вы можете использовать командлет Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration, чтобы получить WAF.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-192">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-193">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a1e5-193">-Confirm</span></span>
<span data-ttu-id="2a1e5-194">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-194">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a1e5-195">-WhatIf</span></span>
<span data-ttu-id="2a1e5-196">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a1e5-197">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-197">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a1e5-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a1e5-198">CommonParameters</span></span>
<span data-ttu-id="2a1e5-199">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a1e5-200">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a1e5-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a1e5-201">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a1e5-201">INPUTS</span></span>

### <span data-ttu-id="2a1e5-202">Ничего</span><span class="sxs-lookup"><span data-stu-id="2a1e5-202">None</span></span>
<span data-ttu-id="2a1e5-203">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2a1e5-203">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2a1e5-204">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a1e5-204">OUTPUTS</span></span>

### <span data-ttu-id="2a1e5-205">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a1e5-205">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2a1e5-206">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a1e5-206">NOTES</span></span>

## <span data-ttu-id="2a1e5-207">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a1e5-207">RELATED LINKS</span></span>

[<span data-ttu-id="2a1e5-208">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2a1e5-208">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="2a1e5-209">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2a1e5-209">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="2a1e5-210">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2a1e5-210">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2a1e5-211">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2a1e5-211">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="2a1e5-212">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="2a1e5-212">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="2a1e5-213">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a1e5-213">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2a1e5-214">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2a1e5-214">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2a1e5-215">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="2a1e5-215">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="2a1e5-216">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2a1e5-216">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="2a1e5-217">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2a1e5-217">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
