---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 1dd4285b75f8c1c067f15be34a334d4d48fb4f7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225713"
---
# <span data-ttu-id="1b2a9-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1b2a9-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="1b2a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b2a9-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2a9-103">Обновляет SSL-сертификат для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1b2a9-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="1b2a9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1b2a9-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b2a9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b2a9-105">DESCRIPTION</span></span>
<span data-ttu-id="1b2a9-106">**Cmdlet Set-AzApplicationGatewaySslCertificate** обновляет SSL-сертификат для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1b2a9-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="1b2a9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1b2a9-107">EXAMPLES</span></span>

### <span data-ttu-id="1b2a9-108">Пример 1. Обновление существующего SSL-сертификата в шлюзе приложения</span><span class="sxs-lookup"><span data-stu-id="1b2a9-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="1b2a9-109">Обновление SSL-сертификата для шлюза приложения ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="1b2a9-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="1b2a9-110">Пример 2. Обновление существующего SSL-сертификата с помощью keyVault Secret (без секретного ключа версии) на шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="1b2a9-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="1b2a9-111">Получите секрет и обновите существующий SSL-сертификат с `Set-AzApplicationGatewaySslCertificate` помощью.</span><span class="sxs-lookup"><span data-stu-id="1b2a9-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="1b2a9-112">Пример 3. Обновление существующего SSL-сертификата с помощью keyVault Secret в шлюзе приложения</span><span class="sxs-lookup"><span data-stu-id="1b2a9-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="1b2a9-113">Получите секрет и обновите существующий SSL-сертификат с `Set-AzApplicationGatewaySslCertificate` помощью.</span><span class="sxs-lookup"><span data-stu-id="1b2a9-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="1b2a9-114">Примечание. Если необходимо, чтобы шлюз приложения синхронизировал сертификат с KeyVault, предосообщите менее секретныйid версии.</span><span class="sxs-lookup"><span data-stu-id="1b2a9-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="1b2a9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b2a9-115">PARAMETERS</span></span>

### <span data-ttu-id="1b2a9-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b2a9-116">-ApplicationGateway</span></span>
<span data-ttu-id="1b2a9-117">Указывает шлюз приложения, с которым связан SSL-сертификат.</span><span class="sxs-lookup"><span data-stu-id="1b2a9-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="1b2a9-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="1b2a9-118">-CertificateFile</span></span>
<span data-ttu-id="1b2a9-119">Путь к SSL-сертификату.</span><span class="sxs-lookup"><span data-stu-id="1b2a9-119">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="1b2a9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2a9-120">-DefaultProfile</span></span>
<span data-ttu-id="1b2a9-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b2a9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b2a9-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="1b2a9-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="1b2a9-123">Секрет KeyVault Secret в SecretId (uri).</span><span class="sxs-lookup"><span data-stu-id="1b2a9-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="1b2a9-124">Используйте этот параметр, если нужно использовать определенную версию секретного документа.</span><span class="sxs-lookup"><span data-stu-id="1b2a9-124">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="1b2a9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1b2a9-125">-Name</span></span>
<span data-ttu-id="1b2a9-126">Указывает имя SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="1b2a9-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="1b2a9-127">-Password</span><span class="sxs-lookup"><span data-stu-id="1b2a9-127">-Password</span></span>
<span data-ttu-id="1b2a9-128">Указывает пароль SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="1b2a9-128">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="1b2a9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2a9-129">CommonParameters</span></span>
<span data-ttu-id="1b2a9-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b2a9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2a9-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b2a9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2a9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b2a9-132">INPUTS</span></span>

### <span data-ttu-id="1b2a9-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b2a9-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1b2a9-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1b2a9-134">OUTPUTS</span></span>

### <span data-ttu-id="1b2a9-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b2a9-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1b2a9-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1b2a9-136">NOTES</span></span>

## <span data-ttu-id="1b2a9-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b2a9-137">RELATED LINKS</span></span>

[<span data-ttu-id="1b2a9-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1b2a9-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1b2a9-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1b2a9-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1b2a9-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1b2a9-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1b2a9-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1b2a9-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


