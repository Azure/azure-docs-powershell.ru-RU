---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 84465161d726108749e09d4a928e22aea8050c92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015059"
---
# <span data-ttu-id="e36f7-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e36f7-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e36f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e36f7-102">SYNOPSIS</span></span>
<span data-ttu-id="e36f7-103">Создает SSL-сертификат для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="e36f7-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="e36f7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e36f7-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e36f7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e36f7-105">DESCRIPTION</span></span>
<span data-ttu-id="e36f7-106">**Новый-AzApplicationGatewaySslCertificate** создает SSL-сертификат для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="e36f7-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="e36f7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e36f7-107">EXAMPLES</span></span>

### <span data-ttu-id="e36f7-108">Пример 1. Создание SSL-сертификата для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="e36f7-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="e36f7-109">Эта команда создает SSL-сертификат с именем Cert01 для шлюза приложения по умолчанию и сохраняет результат в переменной с $Cert.</span><span class="sxs-lookup"><span data-stu-id="e36f7-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="e36f7-110">Пример 2. Создайте SSL-сертификат с помощью keyVault Secret (без секретного ключа версии) и добавьте его в шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="e36f7-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="e36f7-111">Получите секрет и создайте SSL-сертификат с `New-AzApplicationGatewaySslCertificate` помощью.</span><span class="sxs-lookup"><span data-stu-id="e36f7-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="e36f7-112">Примечание. Поскольку в этом окне есть секретная версия, шлюз приложения регулярно синхронизирует сертификат с keyVault.</span><span class="sxs-lookup"><span data-stu-id="e36f7-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="e36f7-113">Пример 3. Создайте SSL-сертификат с помощью keyVault Secret и добавьте его в шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="e36f7-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="e36f7-114">Получите секрет и создайте SSL-сертификат с `New-AzApplicationGatewaySslCertificate` помощью.</span><span class="sxs-lookup"><span data-stu-id="e36f7-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="e36f7-115">Примечание. Если необходимо, чтобы шлюз приложения синхронизировал сертификат с KeyVault, предоплаченный для версии.</span><span class="sxs-lookup"><span data-stu-id="e36f7-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="e36f7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e36f7-116">PARAMETERS</span></span>

### <span data-ttu-id="e36f7-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e36f7-117">-CertificateFile</span></span>
<span data-ttu-id="e36f7-118">Путь к PFX-файлу SSL-сертификата, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e36f7-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e36f7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e36f7-119">-DefaultProfile</span></span>
<span data-ttu-id="e36f7-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e36f7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e36f7-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="e36f7-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="e36f7-122">SecretId (uri) секретного ключа KeyVault.</span><span class="sxs-lookup"><span data-stu-id="e36f7-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="e36f7-123">Используйте этот параметр, если нужно использовать определенную версию секретного документа.</span><span class="sxs-lookup"><span data-stu-id="e36f7-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="e36f7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e36f7-124">-Name</span></span>
<span data-ttu-id="e36f7-125">Указывает имя SSL-сертификата, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e36f7-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e36f7-126">-Password</span><span class="sxs-lookup"><span data-stu-id="e36f7-126">-Password</span></span>
<span data-ttu-id="e36f7-127">Определяет пароль SSL-адреса, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e36f7-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e36f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36f7-128">CommonParameters</span></span>
<span data-ttu-id="e36f7-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e36f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36f7-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e36f7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36f7-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e36f7-131">INPUTS</span></span>

### <span data-ttu-id="e36f7-132">Нет</span><span class="sxs-lookup"><span data-stu-id="e36f7-132">None</span></span>

## <span data-ttu-id="e36f7-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e36f7-133">OUTPUTS</span></span>

### <span data-ttu-id="e36f7-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e36f7-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e36f7-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e36f7-135">NOTES</span></span>

## <span data-ttu-id="e36f7-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e36f7-136">RELATED LINKS</span></span>

[<span data-ttu-id="e36f7-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e36f7-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e36f7-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e36f7-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e36f7-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e36f7-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e36f7-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e36f7-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


