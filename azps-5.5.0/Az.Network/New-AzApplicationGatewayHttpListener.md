---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: a6fc3eb16cc82f7a0964e8cd0c1697a083771016
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236876"
---
# <span data-ttu-id="7eea1-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7eea1-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7eea1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eea1-102">SYNOPSIS</span></span>
<span data-ttu-id="7eea1-103">Создает http-прослушивание для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="7eea1-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="7eea1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7eea1-104">SYNTAX</span></span>

### <span data-ttu-id="7eea1-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7eea1-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-SslProfileId <String>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7eea1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7eea1-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7eea1-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7eea1-107">DESCRIPTION</span></span>
<span data-ttu-id="7eea1-108">С **помощью cmdlet New-AzApplicationGatewayHttpListener** создается http-прослушивание для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="7eea1-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="7eea1-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7eea1-109">EXAMPLES</span></span>

### <span data-ttu-id="7eea1-110">Пример 1. Создание http-прослушивание</span><span class="sxs-lookup"><span data-stu-id="7eea1-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="7eea1-111">Эта команда создает http-прослушивание с именем Listener01 и сохраняет результат в переменной с $Listener.</span><span class="sxs-lookup"><span data-stu-id="7eea1-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="7eea1-112">Пример 2. Создание http-прослушивание с помощью SSL</span><span class="sxs-lookup"><span data-stu-id="7eea1-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="7eea1-113">Эта команда создает http-прослушивание, использующее внезагрузку SSL, и предоставляет SSL-сертификат в переменной $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="7eea1-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="7eea1-114">Команда сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="7eea1-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="7eea1-115">Пример 3. Создание прослушки HTTP с помощью политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="7eea1-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="7eea1-116">Эта команда создает HTTP-прослушивание с именем Listener01 firewallPolicy как $firewallPolicy и сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="7eea1-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="7eea1-117">Пример 4. Добавление программы HTTPS-прослушивания с именами SSL и HostNames</span><span class="sxs-lookup"><span data-stu-id="7eea1-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="7eea1-118">Эта команда создает http-прослушивание, использующее внезагрузку SSL, и предоставляет SSL-сертификат в переменной $SSLCert 01 вместе с двумя hostNames.</span><span class="sxs-lookup"><span data-stu-id="7eea1-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="7eea1-119">Команда сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="7eea1-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="7eea1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7eea1-120">PARAMETERS</span></span>

### <span data-ttu-id="7eea1-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="7eea1-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="7eea1-122">Ошибка клиента шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="7eea1-122">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eea1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eea1-123">-DefaultProfile</span></span>
<span data-ttu-id="7eea1-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7eea1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eea1-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7eea1-125">-FirewallPolicy</span></span>
<span data-ttu-id="7eea1-126">Указывает ссылку на объект в политике брандмауэра верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="7eea1-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="7eea1-127">Ссылку на объект можно создать с помощью New-AzApplicationGatewayWebApplicationFirewallPolicy-управления.</span><span class="sxs-lookup"><span data-stu-id="7eea1-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="7eea1-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" Политика брандмауэра, созданная с помощью командлета выше, может быть передана на уровне пути.</span><span class="sxs-lookup"><span data-stu-id="7eea1-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="7eea1-129">Над командой, над командой, он создает параметры политики по умолчанию и управляемые правила.</span><span class="sxs-lookup"><span data-stu-id="7eea1-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="7eea1-130">Вместо стандартных значений пользователи могут указывать PolicySettings и ManagedRules New-AzApplicationGatewayFirewallPolicySettings и New-AzApplicationGatewayFirewallPolicyManagedRules соответственно.</span><span class="sxs-lookup"><span data-stu-id="7eea1-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eea1-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="7eea1-131">-FirewallPolicyId</span></span>
<span data-ttu-id="7eea1-132">Определяет ИД существующего ресурса брандмауэра веб-приложения верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="7eea1-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="7eea1-133">Коды политики брандмауэра можно вернуть с помощью Get-AzApplicationGatewayWebApplicationFirewallPolicy управления.</span><span class="sxs-lookup"><span data-stu-id="7eea1-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="7eea1-134">После того как у нас есть ИД, вы можете использовать параметр *FirewallPolicyId* вместо *параметра FirewallPolicy.*</span><span class="sxs-lookup"><span data-stu-id="7eea1-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="7eea1-135">Например: -FirewallPolicyId /subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="7eea1-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

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

### <span data-ttu-id="7eea1-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7eea1-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="7eea1-137">Определяет объект конфигурации переднего IP-адреса для http-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="7eea1-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eea1-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7eea1-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="7eea1-139">Определяет ID-адрес передней конфигурации IP-адреса для прослушки HTTP-адреса.</span><span class="sxs-lookup"><span data-stu-id="7eea1-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="7eea1-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="7eea1-140">-FrontendPort</span></span>
<span data-ttu-id="7eea1-141">Указывает стойкий порт для прослушки HTTP.</span><span class="sxs-lookup"><span data-stu-id="7eea1-141">Specifies the front-end port for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eea1-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="7eea1-142">-FrontendPortId</span></span>
<span data-ttu-id="7eea1-143">Определяет ИД объекта переднего порта для прослушки HTTP.</span><span class="sxs-lookup"><span data-stu-id="7eea1-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="7eea1-144">-HostName</span><span class="sxs-lookup"><span data-stu-id="7eea1-144">-HostName</span></span>
<span data-ttu-id="7eea1-145">Указывает имя сайта http-прослушивание шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="7eea1-145">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="7eea1-146">-HostNames</span><span class="sxs-lookup"><span data-stu-id="7eea1-146">-HostNames</span></span>
<span data-ttu-id="7eea1-147">Host names (Имена хостов)</span><span class="sxs-lookup"><span data-stu-id="7eea1-147">Host names</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eea1-148">-Name</span><span class="sxs-lookup"><span data-stu-id="7eea1-148">-Name</span></span>
<span data-ttu-id="7eea1-149">Указывает имя http-прослушивание, которое создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7eea1-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7eea1-150">-Protocol</span><span class="sxs-lookup"><span data-stu-id="7eea1-150">-Protocol</span></span>
<span data-ttu-id="7eea1-151">Протокол, который использует http-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="7eea1-151">Specifies the protocol that the HTTP listener uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eea1-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="7eea1-152">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eea1-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="7eea1-153">-SslCertificate</span></span>
<span data-ttu-id="7eea1-154">Указывает объект SSL-сертификата для http-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="7eea1-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eea1-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="7eea1-155">-SslCertificateId</span></span>
<span data-ttu-id="7eea1-156">Определяет ИД SSL-сертификата для прослушки HTTP- или SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="7eea1-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="7eea1-157">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="7eea1-157">-SslProfile</span></span>
<span data-ttu-id="7eea1-158">SslProfile</span><span class="sxs-lookup"><span data-stu-id="7eea1-158">SslProfile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eea1-159">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="7eea1-159">-SslProfileId</span></span>
<span data-ttu-id="7eea1-160">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="7eea1-160">SslProfileId</span></span>

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

### <span data-ttu-id="7eea1-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eea1-161">CommonParameters</span></span>
<span data-ttu-id="7eea1-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eea1-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eea1-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7eea1-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eea1-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7eea1-164">INPUTS</span></span>

### <span data-ttu-id="7eea1-165">Нет</span><span class="sxs-lookup"><span data-stu-id="7eea1-165">None</span></span>

## <span data-ttu-id="7eea1-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7eea1-166">OUTPUTS</span></span>

### <span data-ttu-id="7eea1-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7eea1-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7eea1-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7eea1-168">NOTES</span></span>

## <span data-ttu-id="7eea1-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7eea1-169">RELATED LINKS</span></span>

[<span data-ttu-id="7eea1-170">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7eea1-170">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="7eea1-171">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7eea1-171">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="7eea1-172">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7eea1-172">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="7eea1-173">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7eea1-173">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


