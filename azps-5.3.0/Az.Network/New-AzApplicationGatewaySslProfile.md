---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: a9b0d41ad700d0591e38fa339c38efb85cb00859
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421791"
---
# <span data-ttu-id="f3ad7-101">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f3ad7-101">New-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="f3ad7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ad7-103">Создает SSL-профиль шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="f3ad7-103">Creates SSL profile for an application gateway.</span></span>

## <span data-ttu-id="f3ad7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f3ad7-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslProfile -Name <String> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3ad7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3ad7-105">DESCRIPTION</span></span>
<span data-ttu-id="f3ad7-106">Для шлюза приложения создается **SSL-профиль New-AzApplicationGatewaySslProfile.**</span><span class="sxs-lookup"><span data-stu-id="f3ad7-106">The **New-AzApplicationGatewaySslProfile** cmdlet creates SSL profile for an application gateway.</span></span> <span data-ttu-id="f3ad7-107">Профиль SSL настраивается в httpS-протоколе.</span><span class="sxs-lookup"><span data-stu-id="f3ad7-107">The ssl profile is configured on the HTTPS listeners.</span></span>

## <span data-ttu-id="f3ad7-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f3ad7-108">EXAMPLES</span></span>

### <span data-ttu-id="f3ad7-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f3ad7-109">Example 1</span></span>
```powershell
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $profile = New-AzApplicationGatewaySslProfile -Name $sslProfile01Name -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01
```
<span data-ttu-id="f3ad7-110">Первая команда создает новую политику SSL и сохраняет ее в переменной $sslPolicy.</span><span class="sxs-lookup"><span data-stu-id="f3ad7-110">The first command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="f3ad7-111">Вторая команда создает цепочки сертификатов доверенных клиентских ЦС и сохраняет их в переменной $ClientCert 01.</span><span class="sxs-lookup"><span data-stu-id="f3ad7-111">The second command creates a trusted client CA certificate chains and stores them in the $ClientCert01 variable.</span></span>
<span data-ttu-id="f3ad7-112">Третья команда создает новый профиль SSL с помощью политики ssl и цепочки сертификатов доверенных клиентских ЦС.</span><span class="sxs-lookup"><span data-stu-id="f3ad7-112">The third command create a new SSL profile with the the ssl policy and trusted client CA certificate chain.</span></span>

## <span data-ttu-id="f3ad7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3ad7-113">PARAMETERS</span></span>

### <span data-ttu-id="f3ad7-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3ad7-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="f3ad7-115">Параметры конфигурации проверки подлинности клиента</span><span class="sxs-lookup"><span data-stu-id="f3ad7-115">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="f3ad7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ad7-116">-DefaultProfile</span></span>
<span data-ttu-id="f3ad7-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3ad7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3ad7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f3ad7-118">-Name</span></span>
<span data-ttu-id="f3ad7-119">Имя профиля SSL</span><span class="sxs-lookup"><span data-stu-id="f3ad7-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="f3ad7-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="f3ad7-120">-SslPolicy</span></span>
<span data-ttu-id="f3ad7-121">Политика SSL</span><span class="sxs-lookup"><span data-stu-id="f3ad7-121">SSL policy</span></span>

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

### <span data-ttu-id="f3ad7-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="f3ad7-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="f3ad7-123">Цепочки сертификатов доверенных клиентов ЦС</span><span class="sxs-lookup"><span data-stu-id="f3ad7-123">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="f3ad7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ad7-124">CommonParameters</span></span>
<span data-ttu-id="f3ad7-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ad7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ad7-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3ad7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ad7-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3ad7-127">INPUTS</span></span>

### <span data-ttu-id="f3ad7-128">Нет</span><span class="sxs-lookup"><span data-stu-id="f3ad7-128">None</span></span>

## <span data-ttu-id="f3ad7-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f3ad7-129">OUTPUTS</span></span>

### <span data-ttu-id="f3ad7-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f3ad7-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="f3ad7-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f3ad7-131">NOTES</span></span>

## <span data-ttu-id="f3ad7-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3ad7-132">RELATED LINKS</span></span>

[<span data-ttu-id="f3ad7-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f3ad7-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="f3ad7-134">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f3ad7-134">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="f3ad7-135">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f3ad7-135">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="f3ad7-136">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f3ad7-136">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)