---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 0fa72c48693335dd3df6ab3c1cf8040c5343cc84
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078843"
---
# <span data-ttu-id="dd117-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dd117-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="dd117-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd117-102">SYNOPSIS</span></span>
<span data-ttu-id="dd117-103">Обновляет SSL-сертификат для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="dd117-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="dd117-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd117-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd117-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd117-105">DESCRIPTION</span></span>
<span data-ttu-id="dd117-106">Командлет **Set-AzApplicationGatewaySslCertificate** обновляет SSL-сертификат для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="dd117-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="dd117-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd117-107">EXAMPLES</span></span>

### <span data-ttu-id="dd117-108">Пример 1: обновление существующего SSL-сертификата на шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="dd117-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="dd117-109">Обновите существующий SSL-сертификат для шлюза приложений с именем ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="dd117-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="dd117-110">Пример 2: обновление существующего SSL-сертификата с помощью KeyVault Secret (не менее secretId) на шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="dd117-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="dd117-111">Получите секрет и обновите существующий SSL-сертификат с помощью `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="dd117-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="dd117-112">Пример 3: обновление существующего SSL-сертификата с помощью KeyVault Secret на шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="dd117-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="dd117-113">Получите секрет и обновите существующий SSL-сертификат с помощью `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="dd117-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="dd117-114">Примечание. Если необходимо, чтобы шлюз приложений синхронизирует сертификат с KeyVault, укажите версию, не менее secretId.</span><span class="sxs-lookup"><span data-stu-id="dd117-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="dd117-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd117-115">PARAMETERS</span></span>

### <span data-ttu-id="dd117-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dd117-116">-ApplicationGateway</span></span>
<span data-ttu-id="dd117-117">Указывает шлюз приложений, с которым связан SSL-сертификат.</span><span class="sxs-lookup"><span data-stu-id="dd117-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd117-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="dd117-118">-CertificateFile</span></span>
<span data-ttu-id="dd117-119">Указывает путь SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="dd117-119">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="dd117-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd117-120">-DefaultProfile</span></span>
<span data-ttu-id="dd117-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd117-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd117-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="dd117-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="dd117-123">SecretId (URI) секрета KeyVault.</span><span class="sxs-lookup"><span data-stu-id="dd117-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="dd117-124">Используйте этот параметр, если необходимо использовать определенную версию секрета.</span><span class="sxs-lookup"><span data-stu-id="dd117-124">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="dd117-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dd117-125">-Name</span></span>
<span data-ttu-id="dd117-126">Задает имя SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="dd117-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="dd117-127">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="dd117-127">-Password</span></span>
<span data-ttu-id="dd117-128">Указывает пароль SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="dd117-128">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd117-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd117-129">CommonParameters</span></span>
<span data-ttu-id="dd117-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd117-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd117-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd117-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd117-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd117-132">INPUTS</span></span>

### <span data-ttu-id="dd117-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dd117-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dd117-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd117-134">OUTPUTS</span></span>

### <span data-ttu-id="dd117-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dd117-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dd117-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd117-136">NOTES</span></span>

## <span data-ttu-id="dd117-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd117-137">RELATED LINKS</span></span>

[<span data-ttu-id="dd117-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dd117-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="dd117-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dd117-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="dd117-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dd117-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="dd117-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dd117-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

