---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d525a47dde9551e5d48c7c316cf6844323b75e81
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910298"
---
# <span data-ttu-id="a7b7a-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="a7b7a-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="a7b7a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7b7a-102">SYNOPSIS</span></span>
<span data-ttu-id="a7b7a-103">Возвращает политику для сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="a7b7a-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="a7b7a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7b7a-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7b7a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7b7a-105">DESCRIPTION</span></span>
<span data-ttu-id="a7b7a-106">Командлет **Get-AzKeyVaultCertificatePolicy** получает политику для сертификата в хранилище ключей Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a7b7a-106">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="a7b7a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7b7a-107">EXAMPLES</span></span>

### <span data-ttu-id="a7b7a-108">Пример 1: получение политики сертификата</span><span class="sxs-lookup"><span data-stu-id="a7b7a-108">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
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
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailOnly                       : False
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="a7b7a-109">Эта команда возвращает политику сертификата TestCert01 сертификата в хранилище ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="a7b7a-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="a7b7a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7b7a-110">PARAMETERS</span></span>

### <span data-ttu-id="a7b7a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7b7a-111">-DefaultProfile</span></span>
<span data-ttu-id="a7b7a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a7b7a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7b7a-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a7b7a-113">-Name</span></span>
<span data-ttu-id="a7b7a-114">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="a7b7a-114">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b7a-115">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a7b7a-115">-VaultName</span></span>
<span data-ttu-id="a7b7a-116">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="a7b7a-116">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b7a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7b7a-117">CommonParameters</span></span>
<span data-ttu-id="a7b7a-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7b7a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7b7a-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7b7a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7b7a-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7b7a-120">INPUTS</span></span>

### <span data-ttu-id="a7b7a-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="a7b7a-121">None</span></span>
<span data-ttu-id="a7b7a-122">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a7b7a-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a7b7a-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7b7a-123">OUTPUTS</span></span>

### <span data-ttu-id="a7b7a-124">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="a7b7a-124">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="a7b7a-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7b7a-125">NOTES</span></span>

## <span data-ttu-id="a7b7a-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7b7a-126">RELATED LINKS</span></span>

[<span data-ttu-id="a7b7a-127">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="a7b7a-127">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="a7b7a-128">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="a7b7a-128">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

