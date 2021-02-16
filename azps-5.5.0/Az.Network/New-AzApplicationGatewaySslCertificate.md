---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 31d9c5d5c627f4d3451c47584b09760655e77342
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227761"
---
# <span data-ttu-id="b89f2-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b89f2-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b89f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b89f2-102">SYNOPSIS</span></span>
<span data-ttu-id="b89f2-103">Создает SSL-сертификат для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="b89f2-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b89f2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b89f2-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b89f2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b89f2-105">DESCRIPTION</span></span>
<span data-ttu-id="b89f2-106">**Новый-AzApplicationGatewaySslCertificate** создает SSL-сертификат для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="b89f2-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b89f2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b89f2-107">EXAMPLES</span></span>

### <span data-ttu-id="b89f2-108">Пример 1. Создание SSL-сертификата для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="b89f2-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="b89f2-109">Эта команда создает SSL-сертификат с именем Cert01 для шлюза приложения по умолчанию и сохраняет результат в переменной с $Cert.</span><span class="sxs-lookup"><span data-stu-id="b89f2-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="b89f2-110">Пример 2. Создайте SSL-сертификат с помощью keyVault Secret (без секретного ключа версии) и добавьте его в шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="b89f2-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="b89f2-111">Получите секрет и создайте SSL-сертификат с `New-AzApplicationGatewaySslCertificate` помощью.</span><span class="sxs-lookup"><span data-stu-id="b89f2-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="b89f2-112">Примечание. Поскольку в этом окне есть секретная версия, шлюз приложения регулярно синхронизирует сертификат с keyVault.</span><span class="sxs-lookup"><span data-stu-id="b89f2-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="b89f2-113">Пример 3. Создайте SSL-сертификат с помощью keyVault Secret и добавьте его в шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="b89f2-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="b89f2-114">Получите секрет и создайте SSL-сертификат с `New-AzApplicationGatewaySslCertificate` помощью.</span><span class="sxs-lookup"><span data-stu-id="b89f2-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="b89f2-115">Примечание. Если необходимо, чтобы шлюз приложения синхронизировал сертификат с KeyVault, предосообщите менее секретныйid версии.</span><span class="sxs-lookup"><span data-stu-id="b89f2-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="b89f2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b89f2-116">PARAMETERS</span></span>

### <span data-ttu-id="b89f2-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b89f2-117">-CertificateFile</span></span>
<span data-ttu-id="b89f2-118">Путь к PFX-файлу SSL-сертификата, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b89f2-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b89f2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b89f2-119">-DefaultProfile</span></span>
<span data-ttu-id="b89f2-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b89f2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b89f2-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="b89f2-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="b89f2-122">SecretId (uri) секретного ключа KeyVault.</span><span class="sxs-lookup"><span data-stu-id="b89f2-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="b89f2-123">Используйте этот параметр, если нужно использовать определенную версию секретного документа.</span><span class="sxs-lookup"><span data-stu-id="b89f2-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="b89f2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b89f2-124">-Name</span></span>
<span data-ttu-id="b89f2-125">Указывает имя SSL-сертификата, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b89f2-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b89f2-126">-Password</span><span class="sxs-lookup"><span data-stu-id="b89f2-126">-Password</span></span>
<span data-ttu-id="b89f2-127">Определяет пароль SSL-адреса, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b89f2-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b89f2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b89f2-128">CommonParameters</span></span>
<span data-ttu-id="b89f2-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b89f2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b89f2-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b89f2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b89f2-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b89f2-131">INPUTS</span></span>

### <span data-ttu-id="b89f2-132">Нет</span><span class="sxs-lookup"><span data-stu-id="b89f2-132">None</span></span>

## <span data-ttu-id="b89f2-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b89f2-133">OUTPUTS</span></span>

### <span data-ttu-id="b89f2-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b89f2-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b89f2-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b89f2-135">NOTES</span></span>

## <span data-ttu-id="b89f2-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b89f2-136">RELATED LINKS</span></span>

[<span data-ttu-id="b89f2-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b89f2-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b89f2-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b89f2-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b89f2-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b89f2-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b89f2-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b89f2-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


