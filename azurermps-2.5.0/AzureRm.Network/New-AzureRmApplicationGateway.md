---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 73b72c6585fb4c7487b43dc99b3494cdc99bf7a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913810"
---
# <span data-ttu-id="37ac4-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37ac4-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="37ac4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="37ac4-103">Создание шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37ac4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37ac4-104">SYNTAX</span></span>

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
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37ac4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37ac4-105">DESCRIPTION</span></span>
<span data-ttu-id="37ac4-106">Командлет **New-AzureRmApplicationGateway** создает шлюз приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="37ac4-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="37ac4-107">Для шлюза приложений требуются указанные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="37ac4-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="37ac4-108">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="37ac4-108">A resource group.</span></span>
- <span data-ttu-id="37ac4-109">Виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="37ac4-109">A virtual network.</span></span>
- <span data-ttu-id="37ac4-110">Пул серверного сервера, содержащий IP-адреса серверных серверов.</span><span class="sxs-lookup"><span data-stu-id="37ac4-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="37ac4-111">Параметры пула серверов для заднего сервера.</span><span class="sxs-lookup"><span data-stu-id="37ac4-111">Back-end server pool settings.</span></span> <span data-ttu-id="37ac4-112">У каждого пула есть такие параметры, как порт, протокол и сходство на основе файлов cookie, которые применяются ко всем серверам в пуле.</span><span class="sxs-lookup"><span data-stu-id="37ac4-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="37ac4-113">IP-адреса переднего плана, которые являются IP-адресами, открытыми на шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="37ac4-114">Интерфейсный IP-адрес может быть общедоступным IP-адресом или внутренним IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="37ac4-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="37ac4-115">Внешние порты, которые являются общедоступными портами, открытыми на шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="37ac4-116">Трафик, который нажимает эти порты, перенаправляется на серверные серверы.</span><span class="sxs-lookup"><span data-stu-id="37ac4-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="37ac4-117">Правило маршрутизации запросов, связывающее прослушиватель и пул серверного сервера.</span><span class="sxs-lookup"><span data-stu-id="37ac4-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="37ac4-118">Правило определяет, на какой серверный пул должен перенаправляться трафик при каждом обращении к определенному прослушивателю.</span><span class="sxs-lookup"><span data-stu-id="37ac4-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="37ac4-119">У прослушивателя есть интерфейсный порт, клиентский IP-адрес, протокол (HTTP или HTTPS) и имя сертификата SSL (при настройке разгрузки SSL).</span><span class="sxs-lookup"><span data-stu-id="37ac4-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="37ac4-120">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37ac4-120">EXAMPLES</span></span>

### <span data-ttu-id="37ac4-121">Пример 1: Создание шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="37ac4-121">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="37ac4-122">В следующем примере создается шлюз приложений, в результате чего создаются группа ресурсов и виртуальная сеть, а также указанные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="37ac4-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="37ac4-123">Пул серверов в серверной части</span><span class="sxs-lookup"><span data-stu-id="37ac4-123">A back-end server pool</span></span>
- <span data-ttu-id="37ac4-124">Параметры пула серверов в серверной части</span><span class="sxs-lookup"><span data-stu-id="37ac4-124">Back-end server pool settings</span></span>
- <span data-ttu-id="37ac4-125">Интерфейсные порты</span><span class="sxs-lookup"><span data-stu-id="37ac4-125">Front-end ports</span></span>
- <span data-ttu-id="37ac4-126">IP-адреса интерфейса пользователя</span><span class="sxs-lookup"><span data-stu-id="37ac4-126">Front-end IP addresses</span></span>
- <span data-ttu-id="37ac4-127">Правило маршрутизации запросов</span><span class="sxs-lookup"><span data-stu-id="37ac4-127">A request routing rule</span></span>

<span data-ttu-id="37ac4-128">Эти четыре команды создают виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="37ac4-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="37ac4-129">Первая команда создает конфигурацию подсети.</span><span class="sxs-lookup"><span data-stu-id="37ac4-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="37ac4-130">Вторая команда создает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="37ac4-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="37ac4-131">Третья команда проверяет конфигурацию подсети, а четвертая команда проверяет, успешно ли создана виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="37ac4-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="37ac4-132">Следующие команды создают шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="37ac4-133">Первая команда создает IP-конфигурацию с именем GatewayIp01 для подсети, созданной ранее.</span><span class="sxs-lookup"><span data-stu-id="37ac4-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="37ac4-134">Вторая команда создает пул серверных серверов с именем Pool01 со списком серверных IP-адресов и сохраняет пул в переменной $Pool.</span><span class="sxs-lookup"><span data-stu-id="37ac4-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="37ac4-135">Третья команда создает параметры для пула ресурсов на внутреннем сервере и сохраняет параметры в переменной $PoolSetting.</span><span class="sxs-lookup"><span data-stu-id="37ac4-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="37ac4-136">В этой команде создается порт переднего плана на порту 80 с именем FrontEndPort01 и хранится порт в переменной $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="37ac4-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="37ac4-137">Пятая команда создает общедоступный IP-адрес с помощью New-AzureRmPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="37ac4-137">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="37ac4-138">Шестая команда создает IP-конфигурацию переднего плана с помощью $PublicIp, называет ее FrontEndPortConfig01 и сохраняет в переменной $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="37ac4-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="37ac4-139">Команда седьмая создает прослушиватель с помощью ранее созданного $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="37ac4-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="37ac4-140">Восьмая команда создает правило для слушателя.</span><span class="sxs-lookup"><span data-stu-id="37ac4-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="37ac4-141">Команда девятка задает SKU.</span><span class="sxs-lookup"><span data-stu-id="37ac4-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="37ac4-142">Десятая команда создает шлюз, используя объекты, заданные предыдущими командами.</span><span class="sxs-lookup"><span data-stu-id="37ac4-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="37ac4-143">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37ac4-143">PARAMETERS</span></span>

### <span data-ttu-id="37ac4-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37ac4-144">-AsJob</span></span>
<span data-ttu-id="37ac4-145">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="37ac4-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37ac4-146">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="37ac4-146">-AuthenticationCertificates</span></span>
<span data-ttu-id="37ac4-147">Определяет сертификаты проверки подлинности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-147">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="37ac4-148">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="37ac4-148">-BackendAddressPools</span></span>
<span data-ttu-id="37ac4-149">Указывает список пулов серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-149">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="37ac4-150">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="37ac4-150">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="37ac4-151">Указывает список параметров HTTP для серверного шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-151">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="37ac4-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ac4-152">-DefaultProfile</span></span>
<span data-ttu-id="37ac4-153">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37ac4-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37ac4-154">-Force</span><span class="sxs-lookup"><span data-stu-id="37ac4-154">-Force</span></span>
<span data-ttu-id="37ac4-155">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="37ac4-155">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="37ac4-156">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="37ac4-156">-FrontendIPConfigurations</span></span>
<span data-ttu-id="37ac4-157">Задает список IP-конфигураций интерфейсов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-157">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="37ac4-158">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="37ac4-158">-FrontendPorts</span></span>
<span data-ttu-id="37ac4-159">Задает список интерфейсных портов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-159">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="37ac4-160">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="37ac4-160">-GatewayIPConfigurations</span></span>
<span data-ttu-id="37ac4-161">Задает список IP-конфигураций для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-161">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="37ac4-162">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="37ac4-162">-HttpListeners</span></span>
<span data-ttu-id="37ac4-163">Задает список прослушивателей HTTP для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-163">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="37ac4-164">-Location</span><span class="sxs-lookup"><span data-stu-id="37ac4-164">-Location</span></span>
<span data-ttu-id="37ac4-165">Указывает область, в которой нужно создать шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="37ac4-165">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="37ac4-166">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="37ac4-166">-Name</span></span>
<span data-ttu-id="37ac4-167">Указывает имя шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-167">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="37ac4-168">-Зонды</span><span class="sxs-lookup"><span data-stu-id="37ac4-168">-Probes</span></span>
<span data-ttu-id="37ac4-169">Указывает зонды для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-169">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="37ac4-170">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="37ac4-170">-RedirectConfigurations</span></span>
<span data-ttu-id="37ac4-171">Список конфигурации перенаправления</span><span class="sxs-lookup"><span data-stu-id="37ac4-171">The list of redirect configuration</span></span>

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

### <span data-ttu-id="37ac4-172">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="37ac4-172">-RequestRoutingRules</span></span>
<span data-ttu-id="37ac4-173">Указывает список правил маршрутизации запросов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-173">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="37ac4-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37ac4-174">-ResourceGroupName</span></span>
<span data-ttu-id="37ac4-175">Указывает имя группы ресурсов, в которой нужно создать шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="37ac4-175">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="37ac4-176">-SKU</span><span class="sxs-lookup"><span data-stu-id="37ac4-176">-Sku</span></span>
<span data-ttu-id="37ac4-177">Задает единицу хранения (SKU) шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-177">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="37ac4-178">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="37ac4-178">-SslCertificates</span></span>
<span data-ttu-id="37ac4-179">Указывает список SSL-сертификатов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-179">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="37ac4-180">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="37ac4-180">-SslPolicy</span></span>
<span data-ttu-id="37ac4-181">Указывает политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-181">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="37ac4-182">-Тег</span><span class="sxs-lookup"><span data-stu-id="37ac4-182">-Tag</span></span>
<span data-ttu-id="37ac4-183">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="37ac4-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="37ac4-184">Например:</span><span class="sxs-lookup"><span data-stu-id="37ac4-184">For example:</span></span>

<span data-ttu-id="37ac4-185">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="37ac4-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="37ac4-186">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="37ac4-186">-UrlPathMaps</span></span>
<span data-ttu-id="37ac4-187">Указывает карты URL-пути для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="37ac4-187">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="37ac4-188">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="37ac4-188">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="37ac4-189">Определяет конфигурацию брандмауэра веб-приложения (WAF).</span><span class="sxs-lookup"><span data-stu-id="37ac4-189">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="37ac4-190">Вы можете использовать командлет Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration, чтобы получить WAF.</span><span class="sxs-lookup"><span data-stu-id="37ac4-190">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="37ac4-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37ac4-191">-Confirm</span></span>
<span data-ttu-id="37ac4-192">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="37ac4-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37ac4-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37ac4-193">-WhatIf</span></span>
<span data-ttu-id="37ac4-194">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="37ac4-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37ac4-195">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="37ac4-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37ac4-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ac4-196">CommonParameters</span></span>
<span data-ttu-id="37ac4-197">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37ac4-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ac4-198">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37ac4-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ac4-199">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37ac4-199">INPUTS</span></span>

## <span data-ttu-id="37ac4-200">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37ac4-200">OUTPUTS</span></span>

### <span data-ttu-id="37ac4-201">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37ac4-201">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="37ac4-202">Пуск</span><span class="sxs-lookup"><span data-stu-id="37ac4-202">NOTES</span></span>

## <span data-ttu-id="37ac4-203">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37ac4-203">RELATED LINKS</span></span>

[<span data-ttu-id="37ac4-204">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="37ac4-204">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="37ac4-205">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="37ac4-205">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="37ac4-206">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="37ac4-206">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="37ac4-207">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="37ac4-207">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="37ac4-208">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="37ac4-208">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="37ac4-209">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="37ac4-209">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="37ac4-210">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="37ac4-210">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="37ac4-211">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="37ac4-211">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="37ac4-212">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="37ac4-212">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="37ac4-213">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="37ac4-213">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
