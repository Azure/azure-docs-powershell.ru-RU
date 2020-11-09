---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: a5a1533038f8e11a30dd3fdeedd590b8186597b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318011"
---
# <span data-ttu-id="8f72f-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8f72f-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="8f72f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f72f-102">SYNOPSIS</span></span>
<span data-ttu-id="8f72f-103">Создание SSL-сертификата для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="8f72f-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="8f72f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f72f-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f72f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f72f-105">DESCRIPTION</span></span>
<span data-ttu-id="8f72f-106">Командлет **New-AzApplicationGatewaySslCertificate** создает SSL-сертификат для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="8f72f-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="8f72f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f72f-107">EXAMPLES</span></span>

### <span data-ttu-id="8f72f-108">Пример 1: создание SSL-сертификата для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="8f72f-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="8f72f-109">Эта команда создает SSL-сертификат с именем Cert01 для шлюза приложений по умолчанию и сохраняет результат в переменной с именем $Cert.</span><span class="sxs-lookup"><span data-stu-id="8f72f-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="8f72f-110">Пример 2: создание SSL-сертификата с использованием секрета KeyVault (не менее secretId) и добавление к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="8f72f-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="8f72f-111">Получите секрет и создайте сертификат SSL с помощью `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="8f72f-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="8f72f-112">Примечание. в этом случае ниже приведена версия secretId, которая будет синхронизировать сертификаты через KeyVault.</span><span class="sxs-lookup"><span data-stu-id="8f72f-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="8f72f-113">Пример 3: создание SSL-сертификата с использованием секрета KeyVault и добавление его в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="8f72f-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="8f72f-114">Получите секрет и создайте сертификат SSL с помощью `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="8f72f-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="8f72f-115">Примечание. Если необходимо, чтобы шлюз приложений синхронизирует сертификат с KeyVault, укажите версию, не менее secretId.</span><span class="sxs-lookup"><span data-stu-id="8f72f-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="8f72f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f72f-116">PARAMETERS</span></span>

### <span data-ttu-id="8f72f-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8f72f-117">-CertificateFile</span></span>
<span data-ttu-id="8f72f-118">Указывает путь PFX-файла SSL-сертификата, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8f72f-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8f72f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f72f-119">-DefaultProfile</span></span>
<span data-ttu-id="8f72f-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f72f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f72f-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="8f72f-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="8f72f-122">SecretId (URI) секрета KeyVault.</span><span class="sxs-lookup"><span data-stu-id="8f72f-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="8f72f-123">Используйте этот параметр, если необходимо использовать определенную версию секрета.</span><span class="sxs-lookup"><span data-stu-id="8f72f-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="8f72f-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f72f-124">-Name</span></span>
<span data-ttu-id="8f72f-125">Указывает имя SSL-сертификата, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8f72f-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8f72f-126">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="8f72f-126">-Password</span></span>
<span data-ttu-id="8f72f-127">Указывает пароль SSL, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8f72f-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8f72f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f72f-128">CommonParameters</span></span>
<span data-ttu-id="8f72f-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f72f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f72f-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f72f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f72f-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f72f-131">INPUTS</span></span>

### <span data-ttu-id="8f72f-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="8f72f-132">None</span></span>

## <span data-ttu-id="8f72f-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f72f-133">OUTPUTS</span></span>

### <span data-ttu-id="8f72f-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8f72f-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="8f72f-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f72f-135">NOTES</span></span>

## <span data-ttu-id="8f72f-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f72f-136">RELATED LINKS</span></span>

[<span data-ttu-id="8f72f-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8f72f-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8f72f-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8f72f-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8f72f-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8f72f-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8f72f-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8f72f-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


