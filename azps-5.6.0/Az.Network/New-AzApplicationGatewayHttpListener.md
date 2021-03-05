---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 1399dba141cb885e0ad184a588707e7c4f4efe7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997240"
---
# <span data-ttu-id="53f92-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="53f92-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="53f92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53f92-102">SYNOPSIS</span></span>
<span data-ttu-id="53f92-103">Создает http-прослушивание для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="53f92-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="53f92-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="53f92-104">SYNTAX</span></span>

### <span data-ttu-id="53f92-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="53f92-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-SslProfileId <String>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53f92-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="53f92-106">SetByResource</span></span>
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

## <span data-ttu-id="53f92-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53f92-107">DESCRIPTION</span></span>
<span data-ttu-id="53f92-108">С **помощью cmdlet New-AzApplicationGatewayHttpListener** создается http-прослушивание для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="53f92-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="53f92-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="53f92-109">EXAMPLES</span></span>

### <span data-ttu-id="53f92-110">Пример 1. Создание http-прослушивание</span><span class="sxs-lookup"><span data-stu-id="53f92-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="53f92-111">Эта команда создает HTTP-прослушивание с именем Listener01 и сохраняет результат в переменной с $Listener.</span><span class="sxs-lookup"><span data-stu-id="53f92-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="53f92-112">Пример 2. Создание http-прослушивание с помощью SSL</span><span class="sxs-lookup"><span data-stu-id="53f92-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="53f92-113">Эта команда создает http-прослушивание, использующее внезагрузку SSL, и предоставляет SSL-сертификат в переменной $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="53f92-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="53f92-114">Команда сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="53f92-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="53f92-115">Пример 3. Создание http-прослушивание с помощью политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="53f92-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="53f92-116">Эта команда создает HTTP-прослушивание с именем Listener01 firewallPolicy как $firewallPolicy и сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="53f92-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="53f92-117">Пример 4. Добавление программы HTTPS-прослушивания с именами SSL и HostNames</span><span class="sxs-lookup"><span data-stu-id="53f92-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="53f92-118">Эта команда создает http-прослушивание, использующее внезагрузку SSL, и предоставляет SSL-сертификат в переменной $SSLCert 01 вместе с двумя hostNames.</span><span class="sxs-lookup"><span data-stu-id="53f92-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="53f92-119">Команда сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="53f92-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="53f92-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53f92-120">PARAMETERS</span></span>

### <span data-ttu-id="53f92-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f92-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="53f92-122">Ошибка клиента шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="53f92-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="53f92-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f92-123">-DefaultProfile</span></span>
<span data-ttu-id="53f92-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53f92-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53f92-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="53f92-125">-FirewallPolicy</span></span>
<span data-ttu-id="53f92-126">Указывает ссылку на объект в политике брандмауэра верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="53f92-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="53f92-127">Ссылку на объект можно создать с помощью New-AzApplicationGatewayWebApplicationFirewallPolicy-управления.</span><span class="sxs-lookup"><span data-stu-id="53f92-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="53f92-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be refer at a path-rule level.</span><span class="sxs-lookup"><span data-stu-id="53f92-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="53f92-129">Над этой командой он создал бы параметры политики по умолчанию и управляемые правила.</span><span class="sxs-lookup"><span data-stu-id="53f92-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="53f92-130">Вместо стандартных значений пользователи могут указать PolicySettings и ManagedRules New-AzApplicationGatewayFirewallPolicySettings и New-AzApplicationGatewayFirewallPolicyManagedRules соответственно.</span><span class="sxs-lookup"><span data-stu-id="53f92-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

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

### <span data-ttu-id="53f92-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="53f92-131">-FirewallPolicyId</span></span>
<span data-ttu-id="53f92-132">Определяет ИД существующего ресурса брандмауэра веб-приложения верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="53f92-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="53f92-133">Коды политики брандмауэра можно вернуть с помощью Get-AzApplicationGatewayWebApplicationFirewallPolicy управления.</span><span class="sxs-lookup"><span data-stu-id="53f92-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="53f92-134">После того как у нас есть ИД, вы можете использовать параметр *FirewallPolicyId* вместо *параметра FirewallPolicy.*</span><span class="sxs-lookup"><span data-stu-id="53f92-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="53f92-135">Например: -FirewallPolicyId /subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="53f92-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

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

### <span data-ttu-id="53f92-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f92-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="53f92-137">Определяет объект конфигурации переднего IP-адреса для http-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="53f92-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="53f92-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="53f92-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="53f92-139">Определяет ID-адрес передней конфигурации IP-адреса для прослушки HTTP.</span><span class="sxs-lookup"><span data-stu-id="53f92-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="53f92-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="53f92-140">-FrontendPort</span></span>
<span data-ttu-id="53f92-141">Указывает стойкий порт для прослушки HTTP.</span><span class="sxs-lookup"><span data-stu-id="53f92-141">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="53f92-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="53f92-142">-FrontendPortId</span></span>
<span data-ttu-id="53f92-143">Определяет ИД объекта переднего порта для прослушки HTTP.</span><span class="sxs-lookup"><span data-stu-id="53f92-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="53f92-144">-HostName</span><span class="sxs-lookup"><span data-stu-id="53f92-144">-HostName</span></span>
<span data-ttu-id="53f92-145">Указывает имя сайта http-прослушивание шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="53f92-145">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="53f92-146">-HostNames</span><span class="sxs-lookup"><span data-stu-id="53f92-146">-HostNames</span></span>
<span data-ttu-id="53f92-147">Host names (Имена хостов)</span><span class="sxs-lookup"><span data-stu-id="53f92-147">Host names</span></span>

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

### <span data-ttu-id="53f92-148">-Name</span><span class="sxs-lookup"><span data-stu-id="53f92-148">-Name</span></span>
<span data-ttu-id="53f92-149">Указывает имя http-прослушивание, которое создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53f92-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="53f92-150">-Protocol</span><span class="sxs-lookup"><span data-stu-id="53f92-150">-Protocol</span></span>
<span data-ttu-id="53f92-151">Протокол, который использует http-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="53f92-151">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="53f92-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="53f92-152">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="53f92-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="53f92-153">-SslCertificate</span></span>
<span data-ttu-id="53f92-154">Указывает объект SSL-сертификата для http-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="53f92-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="53f92-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="53f92-155">-SslCertificateId</span></span>
<span data-ttu-id="53f92-156">Определяет ИД SSL-сертификата для прослушки HTTP- или SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="53f92-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="53f92-157">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="53f92-157">-SslProfile</span></span>
<span data-ttu-id="53f92-158">SslProfile</span><span class="sxs-lookup"><span data-stu-id="53f92-158">SslProfile</span></span>

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

### <span data-ttu-id="53f92-159">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="53f92-159">-SslProfileId</span></span>
<span data-ttu-id="53f92-160">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="53f92-160">SslProfileId</span></span>

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

### <span data-ttu-id="53f92-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f92-161">CommonParameters</span></span>
<span data-ttu-id="53f92-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53f92-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f92-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53f92-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f92-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53f92-164">INPUTS</span></span>

### <span data-ttu-id="53f92-165">Нет</span><span class="sxs-lookup"><span data-stu-id="53f92-165">None</span></span>

## <span data-ttu-id="53f92-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="53f92-166">OUTPUTS</span></span>

### <span data-ttu-id="53f92-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="53f92-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="53f92-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="53f92-168">NOTES</span></span>

## <span data-ttu-id="53f92-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53f92-169">RELATED LINKS</span></span>

[<span data-ttu-id="53f92-170">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="53f92-170">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="53f92-171">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="53f92-171">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="53f92-172">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="53f92-172">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="53f92-173">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="53f92-173">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


