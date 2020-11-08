---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 9505194ef562c7faf292d5bbf2fe3de20ac7995f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236063"
---
# <span data-ttu-id="ceaa8-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ceaa8-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ceaa8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ceaa8-102">SYNOPSIS</span></span>
<span data-ttu-id="ceaa8-103">Создает прослушиватель HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="ceaa8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ceaa8-104">SYNTAX</span></span>

### <span data-ttu-id="ceaa8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ceaa8-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-HostName <String>]
 [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ceaa8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ceaa8-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ceaa8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ceaa8-107">DESCRIPTION</span></span>
<span data-ttu-id="ceaa8-108">Командлет **New-AzApplicationGatewayHttpListener** создает прослушиватель HTTP для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="ceaa8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ceaa8-109">EXAMPLES</span></span>

### <span data-ttu-id="ceaa8-110">Пример 1: создание прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="ceaa8-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="ceaa8-111">Эта команда создает прослушиватель HTTP с именем Listener01 и сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="ceaa8-112">Пример 2: создание прослушивателя HTTP с помощью SSL</span><span class="sxs-lookup"><span data-stu-id="ceaa8-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="ceaa8-113">Эта команда создает прослушиватель HTTP, использующий разгрузку SSL, и предоставляет сертификат SSL в переменной $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="ceaa8-114">Команда сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="ceaa8-115">Пример 3: создание прослушивателя HTTP с использованием политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="ceaa8-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="ceaa8-116">Эта команда создает прослушиватель HTTP с именем Listener01, FirewallPolicy как $firewallPolicy и сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="ceaa8-117">Пример 4: Добавление прослушивателя HTTPS с SSL и HostName</span><span class="sxs-lookup"><span data-stu-id="ceaa8-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="ceaa8-118">Эта команда создает прослушиватель HTTP, использующий разгрузку SSL, и предоставляет сертификат SSL в переменной $SSLCert 01 вместе с двумя именем узла.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="ceaa8-119">Команда сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="ceaa8-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ceaa8-120">PARAMETERS</span></span>

### <span data-ttu-id="ceaa8-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="ceaa8-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="ceaa8-122">Ошибка клиента в шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="ceaa8-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="ceaa8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceaa8-123">-DefaultProfile</span></span>
<span data-ttu-id="ceaa8-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceaa8-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ceaa8-125">-FirewallPolicy</span></span>
<span data-ttu-id="ceaa8-126">Указывает ссылку на объект для политики брандмауэра верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="ceaa8-127">Ссылку на объект можно создать с помощью New-AzApplicationGatewayWebApplicationFirewallPolicy командлета.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="ceaa8-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-Name "wafPolicy1"-ResourceGroup "rgName" Политика брандмауэра, созданная с помощью приведенного выше unifiedgroup, может быть указана на уровне пути и правила.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="ceaa8-129">Команда "он больше" создаст параметры политики по умолчанию и управляемые правила.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="ceaa8-130">Вместо значений по умолчанию пользователи могут задать PolicySettings, ManagedRules с помощью New-AzApplicationGatewayFirewallPolicySettings и New-AzApplicationGatewayFirewallPolicyManagedRules соответственно.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

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

### <span data-ttu-id="ceaa8-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="ceaa8-131">-FirewallPolicyId</span></span>
<span data-ttu-id="ceaa8-132">Указывает идентификатор существующего ресурса межсетевого экрана веб-приложения верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="ceaa8-133">Идентификаторы политик брандмауэра можно вернуть с помощью командлета Get-AzApplicationGatewayWebApplicationFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="ceaa8-134">После того как у нас есть идентификатор, вы можете использовать параметр *FirewallPolicyId* вместо параметра *firewallpolicy* .</span><span class="sxs-lookup"><span data-stu-id="ceaa8-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="ceaa8-135">Например:-FirewallPolicyId/Subscriptions/<Subscription-ID>/resourceGroups/<ресурсов-ID>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="ceaa8-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

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

### <span data-ttu-id="ceaa8-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ceaa8-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="ceaa8-137">Задает интерфейсный объект конфигурации IP для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="ceaa8-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ceaa8-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="ceaa8-139">Указывает идентификатор IP-конфигурации переднего плана для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="ceaa8-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="ceaa8-140">-FrontendPort</span></span>
<span data-ttu-id="ceaa8-141">Задает интерфейсный порт для HTTP-прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-141">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="ceaa8-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="ceaa8-142">-FrontendPortId</span></span>
<span data-ttu-id="ceaa8-143">Указывает идентификатор объекта переднего порта для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="ceaa8-144">-HostName</span><span class="sxs-lookup"><span data-stu-id="ceaa8-144">-HostName</span></span>
<span data-ttu-id="ceaa8-145">Указывает имя узла для прослушивателя HTTP шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-145">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="ceaa8-146">-HostName</span><span class="sxs-lookup"><span data-stu-id="ceaa8-146">-HostNames</span></span>
<span data-ttu-id="ceaa8-147">Имена узлов</span><span class="sxs-lookup"><span data-stu-id="ceaa8-147">Host names</span></span>

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

### <span data-ttu-id="ceaa8-148">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ceaa8-148">-Name</span></span>
<span data-ttu-id="ceaa8-149">Указывает имя прослушивателя HTTP, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ceaa8-150">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="ceaa8-150">-Protocol</span></span>
<span data-ttu-id="ceaa8-151">Указывает протокол, который использует прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-151">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="ceaa8-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="ceaa8-152">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="ceaa8-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="ceaa8-153">-SslCertificate</span></span>
<span data-ttu-id="ceaa8-154">Указывает объект сертификата SSL для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="ceaa8-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="ceaa8-155">-SslCertificateId</span></span>
<span data-ttu-id="ceaa8-156">Задает ИД SSL-сертификата для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="ceaa8-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceaa8-157">CommonParameters</span></span>
<span data-ttu-id="ceaa8-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ceaa8-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceaa8-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceaa8-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceaa8-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ceaa8-160">INPUTS</span></span>

### <span data-ttu-id="ceaa8-161">Ничего</span><span class="sxs-lookup"><span data-stu-id="ceaa8-161">None</span></span>

## <span data-ttu-id="ceaa8-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ceaa8-162">OUTPUTS</span></span>

### <span data-ttu-id="ceaa8-163">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ceaa8-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ceaa8-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="ceaa8-164">NOTES</span></span>

## <span data-ttu-id="ceaa8-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ceaa8-165">RELATED LINKS</span></span>

[<span data-ttu-id="ceaa8-166">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ceaa8-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ceaa8-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ceaa8-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ceaa8-168">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ceaa8-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ceaa8-169">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ceaa8-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


