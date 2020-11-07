---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 8d03d93a374f2184a995d9cbcdb83050aa98a8ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733848"
---
# <span data-ttu-id="23d90-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="23d90-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="23d90-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23d90-102">SYNOPSIS</span></span>
<span data-ttu-id="23d90-103">Возвращает политику для сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="23d90-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23d90-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23d90-104">SYNTAX</span></span>

### <span data-ttu-id="23d90-105">VaultAndCertName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23d90-105">VaultAndCertName (Default)</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23d90-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="23d90-106">InputObject</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23d90-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23d90-107">DESCRIPTION</span></span>
<span data-ttu-id="23d90-108">Командлет **Get-AzureKeyVaultCertificatePolicy** получает политику для сертификата в хранилище ключей Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="23d90-108">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="23d90-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23d90-109">EXAMPLES</span></span>

### <span data-ttu-id="23d90-110">Пример 1: получение политики сертификата</span><span class="sxs-lookup"><span data-stu-id="23d90-110">Example 1: Get a certificate policy</span></span>
```powershell
PS C:\ >Get-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"

SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Exportable                      : True
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        : 
Ekus                            : {1.3.6.1.5.5.7.3.1, 1.3.6.1.5.5.7.3.2}
ValidityInMonths                : 6
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="23d90-111">Эта команда возвращает политику сертификата TestCert01 сертификата в хранилище ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="23d90-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="23d90-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23d90-112">PARAMETERS</span></span>

### <span data-ttu-id="23d90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d90-113">-DefaultProfile</span></span>
<span data-ttu-id="23d90-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="23d90-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d90-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23d90-115">-InputObject</span></span>
<span data-ttu-id="23d90-116">Объект сертификата.</span><span class="sxs-lookup"><span data-stu-id="23d90-116">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23d90-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="23d90-117">-Name</span></span>
<span data-ttu-id="23d90-118">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="23d90-118">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d90-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="23d90-119">-VaultName</span></span>
<span data-ttu-id="23d90-120">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="23d90-120">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d90-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d90-121">CommonParameters</span></span>
<span data-ttu-id="23d90-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23d90-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d90-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23d90-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d90-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23d90-124">INPUTS</span></span>

### <span data-ttu-id="23d90-125">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="23d90-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="23d90-126">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="23d90-126">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="23d90-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23d90-127">OUTPUTS</span></span>

### <span data-ttu-id="23d90-128">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="23d90-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="23d90-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="23d90-129">NOTES</span></span>

## <span data-ttu-id="23d90-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23d90-130">RELATED LINKS</span></span>

[<span data-ttu-id="23d90-131">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="23d90-131">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="23d90-132">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="23d90-132">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

