---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 8930041959712b7533651262a39409e884ffb177
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412460"
---
# <span data-ttu-id="1295d-101">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1295d-101">Add-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="1295d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1295d-102">SYNOPSIS</span></span>
<span data-ttu-id="1295d-103">Добавляет профиль SSL в шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="1295d-103">Adds SSL profile to an application gateway.</span></span>

## <span data-ttu-id="1295d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1295d-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1295d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1295d-105">DESCRIPTION</span></span>
<span data-ttu-id="1295d-106">**Cmdlet Add-AzApplicationGatewaySslProfile** добавляет профиль SSL к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="1295d-106">The **Add-AzApplicationGatewaySslProfile** cmdlet adds a SSL profile to an application gateway.</span></span> <span data-ttu-id="1295d-107">Профиль SSL применяется к протоколу HTTPS Вуаля.</span><span class="sxs-lookup"><span data-stu-id="1295d-107">The SSL profile is applied to HTTPS Listeners.</span></span>

## <span data-ttu-id="1295d-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1295d-108">EXAMPLES</span></span>

### <span data-ttu-id="1295d-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1295d-109">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $trustedClient02 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert02" -CertificateFile "C:\clientCAChain2.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfile01Name -ApplicationGateway $AppGw -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01,$trustedClient02
```

<span data-ttu-id="1295d-110">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1295d-110">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1295d-111">Вторая команда создает новую политику SSL и сохраняет ее в переменной $sslPolicy.</span><span class="sxs-lookup"><span data-stu-id="1295d-111">The second command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="1295d-112">Третья и четвертая команды создают две новые цепочки сертификатов доверенных клиентских ЦС и сохраняет их в переменных $ClientCert 01 и $ClientCert 02.</span><span class="sxs-lookup"><span data-stu-id="1295d-112">The third and fourth command creates two new trusted client CA certificate chains and stores them in the $ClientCert01 and $ClientCert02 variables.</span></span>
<span data-ttu-id="1295d-113">Пятая команда добавляет профиль SSL с SSL-политикой и цепочками сертификатов доверенных клиентских ЦС в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1295d-113">The fifth command adds the SSL profile with the the ssl policy and trusted client CA certificate chains to the application gateway $AppGw.</span></span>

## <span data-ttu-id="1295d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1295d-114">PARAMETERS</span></span>

### <span data-ttu-id="1295d-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1295d-115">-ApplicationGateway</span></span>
<span data-ttu-id="1295d-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1295d-116">The applicationGateway</span></span>

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

### <span data-ttu-id="1295d-117">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1295d-117">-ClientAuthConfiguration</span></span>
<span data-ttu-id="1295d-118">Параметры конфигурации проверки подлинности клиента</span><span class="sxs-lookup"><span data-stu-id="1295d-118">Client authentication configuration settings</span></span>

```yaml
Type: PSApplicationGatewayClientAuthConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1295d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1295d-119">-DefaultProfile</span></span>
<span data-ttu-id="1295d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1295d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1295d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1295d-121">-Name</span></span>
<span data-ttu-id="1295d-122">Имя профиля SSL</span><span class="sxs-lookup"><span data-stu-id="1295d-122">The name of the SSL profile</span></span>

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

### <span data-ttu-id="1295d-123">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="1295d-123">-SslPolicy</span></span>
<span data-ttu-id="1295d-124">Политика SSL</span><span class="sxs-lookup"><span data-stu-id="1295d-124">SSL policy</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1295d-125">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="1295d-125">-TrustedClientCertificates</span></span>
<span data-ttu-id="1295d-126">Цепочки сертификатов доверенных клиентов ЦС</span><span class="sxs-lookup"><span data-stu-id="1295d-126">The trusted client CA certificate chains</span></span>

```yaml
Type: PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1295d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1295d-127">CommonParameters</span></span>
<span data-ttu-id="1295d-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1295d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1295d-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1295d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1295d-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1295d-130">INPUTS</span></span>

### <span data-ttu-id="1295d-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1295d-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1295d-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1295d-132">OUTPUTS</span></span>

### <span data-ttu-id="1295d-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1295d-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1295d-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1295d-134">NOTES</span></span>

## <span data-ttu-id="1295d-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1295d-135">RELATED LINKS</span></span>

[<span data-ttu-id="1295d-136">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1295d-136">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="1295d-137">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1295d-137">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="1295d-138">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1295d-138">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="1295d-139">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1295d-139">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)