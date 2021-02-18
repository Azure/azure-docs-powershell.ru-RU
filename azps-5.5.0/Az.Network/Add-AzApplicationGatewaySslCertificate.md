---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 6939f26dc06e0aa5ed56d3e905d30960094e8961
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241117"
---
# <span data-ttu-id="c978f-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c978f-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="c978f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c978f-102">SYNOPSIS</span></span>
<span data-ttu-id="c978f-103">Добавляет SSL-сертификат к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="c978f-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="c978f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c978f-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c978f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c978f-105">DESCRIPTION</span></span>
<span data-ttu-id="c978f-106">**Cmdlet Add-AzApplicationGatewaySslCertificate** добавляет SSL-сертификат к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="c978f-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="c978f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c978f-107">EXAMPLES</span></span>

### <span data-ttu-id="c978f-108">Пример 1. Добавление SSL-сертификата с помощью pfx в шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="c978f-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="c978f-109">Эта команда получает шлюз приложения ApplicationGateway01 и добавляет в него SSL-сертификат с именем Cert01.</span><span class="sxs-lookup"><span data-stu-id="c978f-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="c978f-110">Пример 2. Добавление SSL-сертификата с помощью keyVault Secret (без секретного ключа версии) на шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="c978f-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.SecretId.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="c978f-111">Получите секрет и со ссылкой на него, чтобы добавить его к `Add-AzApplicationGatewaySslCertificate` шлюзу приложения с именем. `Cert01`</span><span class="sxs-lookup"><span data-stu-id="c978f-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="c978f-112">Примечание. Поскольку в этом окне есть секретная версия, шлюз приложения регулярно синхронизирует сертификат с keyVault.</span><span class="sxs-lookup"><span data-stu-id="c978f-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="c978f-113">Пример 3. Добавление SSL-сертификата с помощью keyVault Secret (versioned secretId) на шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="c978f-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="c978f-114">Получите секрет и со ссылкой на него, чтобы добавить его к `Add-AzApplicationGatewaySslCertificate` шлюзу приложения с именем. `Cert01`</span><span class="sxs-lookup"><span data-stu-id="c978f-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="c978f-115">Примечание. Если необходимо, чтобы шлюз приложения синхронизировал сертификат с KeyVault, предосообщите менее секретныйid версии.</span><span class="sxs-lookup"><span data-stu-id="c978f-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="c978f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c978f-116">PARAMETERS</span></span>

### <span data-ttu-id="c978f-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c978f-117">-ApplicationGateway</span></span>
<span data-ttu-id="c978f-118">Указывает имя шлюза приложения, к которому этот cmdlet добавляет SSL-сертификат.</span><span class="sxs-lookup"><span data-stu-id="c978f-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="c978f-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c978f-119">-CertificateFile</span></span>
<span data-ttu-id="c978f-120">Указывает PFX-файл SSL-сертификата, который добавляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c978f-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="c978f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c978f-121">-DefaultProfile</span></span>
<span data-ttu-id="c978f-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c978f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c978f-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="c978f-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="c978f-124">Секрет KeyVault Secret в SecretId (uri).</span><span class="sxs-lookup"><span data-stu-id="c978f-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="c978f-125">Используйте этот параметр, если нужно использовать определенную версию секретного документа.</span><span class="sxs-lookup"><span data-stu-id="c978f-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="c978f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c978f-126">-Name</span></span>
<span data-ttu-id="c978f-127">Указывает имя SSL-сертификата, который добавляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c978f-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="c978f-128">-Password</span><span class="sxs-lookup"><span data-stu-id="c978f-128">-Password</span></span>
<span data-ttu-id="c978f-129">Пароль SSL-сертификата, который добавляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c978f-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="c978f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c978f-130">CommonParameters</span></span>
<span data-ttu-id="c978f-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c978f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c978f-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c978f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c978f-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c978f-133">INPUTS</span></span>

### <span data-ttu-id="c978f-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c978f-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c978f-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c978f-135">OUTPUTS</span></span>

### <span data-ttu-id="c978f-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c978f-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c978f-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c978f-137">NOTES</span></span>

## <span data-ttu-id="c978f-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c978f-138">RELATED LINKS</span></span>

[<span data-ttu-id="c978f-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c978f-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c978f-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c978f-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c978f-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c978f-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c978f-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c978f-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


