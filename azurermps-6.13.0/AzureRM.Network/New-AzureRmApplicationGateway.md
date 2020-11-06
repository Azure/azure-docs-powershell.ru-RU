---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: 67da94a783d932501413008523c744f6695f6024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562896"
---
# <span data-ttu-id="0507b-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0507b-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="0507b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0507b-102">SYNOPSIS</span></span>
<span data-ttu-id="0507b-103">Создание шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0507b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0507b-104">SYNTAX</span></span>

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-TrustedRootCertificate <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]>]
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
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0507b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0507b-105">DESCRIPTION</span></span>
<span data-ttu-id="0507b-106">Командлет **New-AzureRmApplicationGateway** создает шлюз приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="0507b-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="0507b-107">Для шлюза приложений требуются указанные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="0507b-107">An application gateway requires the following:</span></span>
- <span data-ttu-id="0507b-108">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0507b-108">A resource group.</span></span>
- <span data-ttu-id="0507b-109">Виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="0507b-109">A virtual network.</span></span>
- <span data-ttu-id="0507b-110">Пул серверного сервера, содержащий IP-адреса серверных серверов.</span><span class="sxs-lookup"><span data-stu-id="0507b-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="0507b-111">Параметры пула серверов для заднего сервера.</span><span class="sxs-lookup"><span data-stu-id="0507b-111">Back-end server pool settings.</span></span> <span data-ttu-id="0507b-112">У каждого пула есть такие параметры, как порт, протокол и сходство на основе файлов cookie, которые применяются ко всем серверам в пуле.</span><span class="sxs-lookup"><span data-stu-id="0507b-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="0507b-113">IP-адреса переднего плана, которые являются IP-адресами, открытыми на шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="0507b-114">Интерфейсный IP-адрес может быть общедоступным IP-адресом или внутренним IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="0507b-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="0507b-115">Внешние порты, которые являются общедоступными портами, открытыми на шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="0507b-116">Трафик, который нажимает эти порты, перенаправляется на серверные серверы.</span><span class="sxs-lookup"><span data-stu-id="0507b-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="0507b-117">Правило маршрутизации запросов, связывающее прослушиватель и пул серверного сервера.</span><span class="sxs-lookup"><span data-stu-id="0507b-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="0507b-118">Правило определяет, на какой серверный пул должен перенаправляться трафик при каждом обращении к определенному прослушивателю.</span><span class="sxs-lookup"><span data-stu-id="0507b-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="0507b-119">У прослушивателя есть интерфейсный порт, клиентский IP-адрес, протокол (HTTP или HTTPS) и имя сертификата SSL (при настройке разгрузки SSL).</span><span class="sxs-lookup"><span data-stu-id="0507b-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="0507b-120">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0507b-120">EXAMPLES</span></span>

### <span data-ttu-id="0507b-121">Пример 1: Создание шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="0507b-121">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="0507b-122">В следующем примере создается шлюз приложений, в результате чего создаются группа ресурсов и виртуальная сеть, а также указанные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="0507b-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="0507b-123">Пул серверов в серверной части</span><span class="sxs-lookup"><span data-stu-id="0507b-123">A back-end server pool</span></span>
- <span data-ttu-id="0507b-124">Параметры пула серверов в серверной части</span><span class="sxs-lookup"><span data-stu-id="0507b-124">Back-end server pool settings</span></span>
- <span data-ttu-id="0507b-125">Интерфейсные порты</span><span class="sxs-lookup"><span data-stu-id="0507b-125">Front-end ports</span></span>
- <span data-ttu-id="0507b-126">IP-адреса интерфейса пользователя</span><span class="sxs-lookup"><span data-stu-id="0507b-126">Front-end IP addresses</span></span>
- <span data-ttu-id="0507b-127">Правило маршрутизации запросов эти четыре команды создают виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="0507b-127">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="0507b-128">Первая команда создает конфигурацию подсети.</span><span class="sxs-lookup"><span data-stu-id="0507b-128">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="0507b-129">Вторая команда создает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="0507b-129">The second command creates a virtual network.</span></span>
<span data-ttu-id="0507b-130">Третья команда проверяет конфигурацию подсети, а четвертая команда проверяет, успешно ли создана виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="0507b-130">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="0507b-131">Следующие команды создают шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-131">The following commands create the application gateway.</span></span>
<span data-ttu-id="0507b-132">Первая команда создает IP-конфигурацию с именем GatewayIp01 для подсети, созданной ранее.</span><span class="sxs-lookup"><span data-stu-id="0507b-132">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="0507b-133">Вторая команда создает пул серверных серверов с именем Pool01 со списком серверных IP-адресов и сохраняет пул в переменной $Pool.</span><span class="sxs-lookup"><span data-stu-id="0507b-133">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="0507b-134">Третья команда создает параметры для пула ресурсов на внутреннем сервере и сохраняет параметры в переменной $PoolSetting.</span><span class="sxs-lookup"><span data-stu-id="0507b-134">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="0507b-135">В этой команде создается порт переднего плана на порту 80 с именем FrontEndPort01 и хранится порт в переменной $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="0507b-135">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="0507b-136">Пятая команда создает общедоступный IP-адрес с помощью New-AzureRmPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="0507b-136">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="0507b-137">Шестая команда создает IP-конфигурацию переднего плана с помощью $PublicIp, называет ее FrontEndPortConfig01 и сохраняет в переменной $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="0507b-137">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="0507b-138">Команда седьмая создает прослушиватель с помощью ранее созданного $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="0507b-138">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="0507b-139">Восьмая команда создает правило для слушателя.</span><span class="sxs-lookup"><span data-stu-id="0507b-139">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="0507b-140">Команда девятка задает SKU.</span><span class="sxs-lookup"><span data-stu-id="0507b-140">The ninth command sets the SKU.</span></span>
<span data-ttu-id="0507b-141">Десятая команда создает шлюз, используя объекты, заданные предыдущими командами.</span><span class="sxs-lookup"><span data-stu-id="0507b-141">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="0507b-142">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0507b-142">PARAMETERS</span></span>

### <span data-ttu-id="0507b-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0507b-143">-AsJob</span></span>
<span data-ttu-id="0507b-144">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0507b-144">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0507b-145">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="0507b-145">-AuthenticationCertificates</span></span>
<span data-ttu-id="0507b-146">Определяет сертификаты проверки подлинности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-146">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="0507b-147">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0507b-147">-AutoscaleConfiguration</span></span>
<span data-ttu-id="0507b-148">Настройка автомасштабирования</span><span class="sxs-lookup"><span data-stu-id="0507b-148">Autoscale Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0507b-149">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="0507b-149">-BackendAddressPools</span></span>
<span data-ttu-id="0507b-150">Указывает список пулов серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-150">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="0507b-151">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="0507b-151">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="0507b-152">Указывает список параметров HTTP для серверного шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-152">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="0507b-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0507b-153">-DefaultProfile</span></span>
<span data-ttu-id="0507b-154">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0507b-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0507b-155">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="0507b-155">-EnableFIPS</span></span>
<span data-ttu-id="0507b-156">Включен ли FIPS.</span><span class="sxs-lookup"><span data-stu-id="0507b-156">Whether FIPS is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0507b-157">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="0507b-157">-EnableHttp2</span></span>
<span data-ttu-id="0507b-158">Включена ли HTTP2.</span><span class="sxs-lookup"><span data-stu-id="0507b-158">Whether HTTP2 is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0507b-159">-Force</span><span class="sxs-lookup"><span data-stu-id="0507b-159">-Force</span></span>
<span data-ttu-id="0507b-160">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="0507b-160">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0507b-161">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="0507b-161">-FrontendIPConfigurations</span></span>
<span data-ttu-id="0507b-162">Задает список IP-конфигураций интерфейсов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-162">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="0507b-163">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="0507b-163">-FrontendPorts</span></span>
<span data-ttu-id="0507b-164">Задает список интерфейсных портов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-164">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="0507b-165">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="0507b-165">-GatewayIPConfigurations</span></span>
<span data-ttu-id="0507b-166">Задает список IP-конфигураций для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-166">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="0507b-167">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="0507b-167">-HttpListeners</span></span>
<span data-ttu-id="0507b-168">Задает список прослушивателей HTTP для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-168">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="0507b-169">-Location</span><span class="sxs-lookup"><span data-stu-id="0507b-169">-Location</span></span>
<span data-ttu-id="0507b-170">Указывает область, в которой нужно создать шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="0507b-170">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0507b-171">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0507b-171">-Name</span></span>
<span data-ttu-id="0507b-172">Указывает имя шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-172">Specifies the name of application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0507b-173">-Зонды</span><span class="sxs-lookup"><span data-stu-id="0507b-173">-Probes</span></span>
<span data-ttu-id="0507b-174">Указывает зонды для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-174">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="0507b-175">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="0507b-175">-RedirectConfigurations</span></span>
<span data-ttu-id="0507b-176">Список конфигурации перенаправления</span><span class="sxs-lookup"><span data-stu-id="0507b-176">The list of redirect configuration</span></span>

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

### <span data-ttu-id="0507b-177">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="0507b-177">-RequestRoutingRules</span></span>
<span data-ttu-id="0507b-178">Указывает список правил маршрутизации запросов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-178">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="0507b-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0507b-179">-ResourceGroupName</span></span>
<span data-ttu-id="0507b-180">Указывает имя группы ресурсов, в которой нужно создать шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="0507b-180">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0507b-181">-SKU</span><span class="sxs-lookup"><span data-stu-id="0507b-181">-Sku</span></span>
<span data-ttu-id="0507b-182">Задает единицу хранения (SKU) шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-182">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0507b-183">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="0507b-183">-SslCertificates</span></span>
<span data-ttu-id="0507b-184">Указывает список SSL-сертификатов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-184">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="0507b-185">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="0507b-185">-SslPolicy</span></span>
<span data-ttu-id="0507b-186">Указывает политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-186">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0507b-187">-Тег</span><span class="sxs-lookup"><span data-stu-id="0507b-187">-Tag</span></span>
<span data-ttu-id="0507b-188">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="0507b-188">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0507b-189">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="0507b-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0507b-190">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0507b-190">-TrustedRootCertificate</span></span>
<span data-ttu-id="0507b-191">Список доверенных корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="0507b-191">The list of trusted root certificates</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0507b-192">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="0507b-192">-UrlPathMaps</span></span>
<span data-ttu-id="0507b-193">Указывает карты URL-пути для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-193">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="0507b-194">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="0507b-194">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="0507b-195">Определяет конфигурацию брандмауэра веб-приложения (WAF).</span><span class="sxs-lookup"><span data-stu-id="0507b-195">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="0507b-196">Вы можете использовать командлет Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration, чтобы получить WAF.</span><span class="sxs-lookup"><span data-stu-id="0507b-196">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0507b-197">-Zone</span><span class="sxs-lookup"><span data-stu-id="0507b-197">-Zone</span></span>
<span data-ttu-id="0507b-198">Список зон доступности, обозначающих, откуда должен быть получен шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="0507b-198">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0507b-199">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0507b-199">-Confirm</span></span>
<span data-ttu-id="0507b-200">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0507b-200">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0507b-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0507b-201">-WhatIf</span></span>
<span data-ttu-id="0507b-202">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0507b-202">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0507b-203">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0507b-203">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0507b-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0507b-204">CommonParameters</span></span>
<span data-ttu-id="0507b-205">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0507b-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0507b-206">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0507b-206">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0507b-207">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0507b-207">INPUTS</span></span>

### <span data-ttu-id="0507b-208">System. String</span><span class="sxs-lookup"><span data-stu-id="0507b-208">System.String</span></span>

### <span data-ttu-id="0507b-209">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="0507b-209">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="0507b-210">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="0507b-210">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="0507b-211">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0507b-211">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0507b-212">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0507b-212">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0507b-213">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0507b-213">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0507b-214">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0507b-214">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0507b-215">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0507b-215">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0507b-216">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0507b-216">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0507b-217">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0507b-217">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0507b-218">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0507b-218">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0507b-219">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0507b-219">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0507b-220">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0507b-220">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0507b-221">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0507b-221">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0507b-222">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0507b-222">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0507b-223">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="0507b-223">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="0507b-224">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0507b-224">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0507b-225">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0507b-225">OUTPUTS</span></span>

### <span data-ttu-id="0507b-226">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0507b-226">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0507b-227">Пуск</span><span class="sxs-lookup"><span data-stu-id="0507b-227">NOTES</span></span>

## <span data-ttu-id="0507b-228">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0507b-228">RELATED LINKS</span></span>

[<span data-ttu-id="0507b-229">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0507b-229">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0507b-230">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0507b-230">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="0507b-231">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0507b-231">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0507b-232">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="0507b-232">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="0507b-233">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0507b-233">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="0507b-234">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0507b-234">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="0507b-235">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0507b-235">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0507b-236">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="0507b-236">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="0507b-237">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0507b-237">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="0507b-238">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0507b-238">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
