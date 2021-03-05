---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 4dde5ab085dede4520b26a4fbeb3255cc62c0fe8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982488"
---
# <span data-ttu-id="aff7e-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="aff7e-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="aff7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aff7e-102">SYNOPSIS</span></span>
<span data-ttu-id="aff7e-103">Добавляет SSL-сертификат к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="aff7e-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="aff7e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aff7e-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aff7e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aff7e-105">DESCRIPTION</span></span>
<span data-ttu-id="aff7e-106">**Cmdlet Add-AzApplicationGatewaySslCertificate** добавляет SSL-сертификат к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="aff7e-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="aff7e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aff7e-107">EXAMPLES</span></span>

### <span data-ttu-id="aff7e-108">Пример 1. Добавление SSL-сертификата с помощью pfx в шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="aff7e-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="aff7e-109">Эта команда получает шлюз приложения ApplicationGateway01 и добавляет в него SSL-сертификат с именем Cert01.</span><span class="sxs-lookup"><span data-stu-id="aff7e-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="aff7e-110">Пример 2. Добавление SSL-сертификата с помощью keyVault Secret (без секретного ключа версии) на шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="aff7e-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.SecretId.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="aff7e-111">Получите секрет и со ссылкой на него, чтобы добавить его к `Add-AzApplicationGatewaySslCertificate` шлюзу приложения с именем. `Cert01`</span><span class="sxs-lookup"><span data-stu-id="aff7e-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="aff7e-112">Примечание. Поскольку в этом окне есть секретная версия, шлюз приложения регулярно синхронизирует сертификат с keyVault.</span><span class="sxs-lookup"><span data-stu-id="aff7e-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="aff7e-113">Пример 3. Добавление SSL-сертификата с помощью keyVault Secret (versioned secretId) на шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="aff7e-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="aff7e-114">Получите секрет и со ссылкой на него, чтобы добавить его к `Add-AzApplicationGatewaySslCertificate` шлюзу приложения с именем. `Cert01`</span><span class="sxs-lookup"><span data-stu-id="aff7e-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="aff7e-115">Примечание. Если необходимо, чтобы шлюз приложения синхронизировал сертификат с KeyVault, предосообщите менее секретныйid версии.</span><span class="sxs-lookup"><span data-stu-id="aff7e-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="aff7e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aff7e-116">PARAMETERS</span></span>

### <span data-ttu-id="aff7e-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aff7e-117">-ApplicationGateway</span></span>
<span data-ttu-id="aff7e-118">Указывает имя шлюза приложения, к которому этот cmdlet добавляет SSL-сертификат.</span><span class="sxs-lookup"><span data-stu-id="aff7e-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="aff7e-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="aff7e-119">-CertificateFile</span></span>
<span data-ttu-id="aff7e-120">Указывает PFX-файл SSL-сертификата, который добавляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aff7e-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="aff7e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff7e-121">-DefaultProfile</span></span>
<span data-ttu-id="aff7e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aff7e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aff7e-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="aff7e-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="aff7e-124">SecretId (uri) секретного ключа KeyVault.</span><span class="sxs-lookup"><span data-stu-id="aff7e-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="aff7e-125">Используйте этот параметр, если нужно использовать определенную версию секретного документа.</span><span class="sxs-lookup"><span data-stu-id="aff7e-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="aff7e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="aff7e-126">-Name</span></span>
<span data-ttu-id="aff7e-127">Указывает имя SSL-сертификата, который добавляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aff7e-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="aff7e-128">-Password</span><span class="sxs-lookup"><span data-stu-id="aff7e-128">-Password</span></span>
<span data-ttu-id="aff7e-129">Пароль SSL-сертификата, который добавляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aff7e-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="aff7e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff7e-130">CommonParameters</span></span>
<span data-ttu-id="aff7e-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aff7e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff7e-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aff7e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff7e-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aff7e-133">INPUTS</span></span>

### <span data-ttu-id="aff7e-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aff7e-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="aff7e-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aff7e-135">OUTPUTS</span></span>

### <span data-ttu-id="aff7e-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aff7e-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="aff7e-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aff7e-137">NOTES</span></span>

## <span data-ttu-id="aff7e-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aff7e-138">RELATED LINKS</span></span>

[<span data-ttu-id="aff7e-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="aff7e-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="aff7e-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="aff7e-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="aff7e-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="aff7e-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="aff7e-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="aff7e-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


