---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 1d4014803f32fdb5e63fe375f2ea175d6f8e5460
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073783"
---
# <span data-ttu-id="da02e-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="da02e-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="da02e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da02e-102">SYNOPSIS</span></span>
<span data-ttu-id="da02e-103">Добавление SSL-сертификата в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="da02e-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="da02e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da02e-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da02e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da02e-105">DESCRIPTION</span></span>
<span data-ttu-id="da02e-106">Командлет **Add-AzApplicationGatewaySslCertificate** добавляет сертификат SSL в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="da02e-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="da02e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da02e-107">EXAMPLES</span></span>

### <span data-ttu-id="da02e-108">Пример 1: Добавление SSL-сертификата с помощью PFX для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="da02e-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="da02e-109">Эта команда получает шлюз приложения с именем ApplicationGateway01 и добавляет в него сертификат SSL с именем Cert01.</span><span class="sxs-lookup"><span data-stu-id="da02e-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="da02e-110">Пример 2: Добавление SSL-сертификата с использованием секрета KeyVault (secretId) для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="da02e-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="da02e-111">Получите секрет и сослаться на него, `Add-AzApplicationGatewaySslCertificate` чтобы добавить его в шлюз приложений с именем `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="da02e-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="da02e-112">Примечание. в этом случае ниже приведена версия secretId, которая будет синхронизировать сертификаты через KeyVault.</span><span class="sxs-lookup"><span data-stu-id="da02e-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="da02e-113">Пример 3: Добавление SSL-сертификата с помощью KeyVault Secret (Versioning secretId) к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="da02e-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="da02e-114">Получите секрет и сослаться на него, `Add-AzApplicationGatewaySslCertificate` чтобы добавить его в шлюз приложений с именем `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="da02e-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="da02e-115">Примечание. Если необходимо, чтобы шлюз приложений синхронизирует сертификат с KeyVault, укажите версию, не менее secretId.</span><span class="sxs-lookup"><span data-stu-id="da02e-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="da02e-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da02e-116">PARAMETERS</span></span>

### <span data-ttu-id="da02e-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="da02e-117">-ApplicationGateway</span></span>
<span data-ttu-id="da02e-118">Указывает имя шлюза приложений, с которым этот командлет добавляет сертификат SSL.</span><span class="sxs-lookup"><span data-stu-id="da02e-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="da02e-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="da02e-119">-CertificateFile</span></span>
<span data-ttu-id="da02e-120">Задает PFX-файл SSL-сертификата, который добавляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="da02e-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="da02e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da02e-121">-DefaultProfile</span></span>
<span data-ttu-id="da02e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da02e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da02e-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="da02e-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="da02e-124">SecretId (URI) секрета KeyVault.</span><span class="sxs-lookup"><span data-stu-id="da02e-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="da02e-125">Используйте этот параметр, если необходимо использовать определенную версию секрета.</span><span class="sxs-lookup"><span data-stu-id="da02e-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="da02e-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="da02e-126">-Name</span></span>
<span data-ttu-id="da02e-127">Указывает имя SSL-сертификата, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="da02e-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="da02e-128">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="da02e-128">-Password</span></span>
<span data-ttu-id="da02e-129">Указывает пароль SSL-сертификата, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="da02e-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="da02e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da02e-130">CommonParameters</span></span>
<span data-ttu-id="da02e-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da02e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da02e-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da02e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da02e-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da02e-133">INPUTS</span></span>

### <span data-ttu-id="da02e-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="da02e-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="da02e-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da02e-135">OUTPUTS</span></span>

### <span data-ttu-id="da02e-136">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="da02e-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="da02e-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="da02e-137">NOTES</span></span>

## <span data-ttu-id="da02e-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da02e-138">RELATED LINKS</span></span>

[<span data-ttu-id="da02e-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="da02e-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="da02e-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="da02e-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="da02e-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="da02e-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="da02e-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="da02e-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


