---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 1317b35e957b46e6f39bfb0866e0429c01d35533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561752"
---
# <span data-ttu-id="0a648-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0a648-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0a648-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a648-102">SYNOPSIS</span></span>
<span data-ttu-id="0a648-103">Возвращает политику для сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="0a648-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a648-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a648-104">SYNTAX</span></span>

### <span data-ttu-id="0a648-105">VaultAndCertName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a648-105">VaultAndCertName (Default)</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a648-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0a648-106">InputObject</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a648-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a648-107">DESCRIPTION</span></span>
<span data-ttu-id="0a648-108">Командлет **Get-AzureKeyVaultCertificatePolicy** получает политику для сертификата в хранилище ключей Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="0a648-108">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="0a648-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a648-109">EXAMPLES</span></span>

### <span data-ttu-id="0a648-110">Пример 1: получение политики сертификата</span><span class="sxs-lookup"><span data-stu-id="0a648-110">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="0a648-111">Эта команда возвращает политику сертификата TestCert01 сертификата в хранилище ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="0a648-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="0a648-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a648-112">PARAMETERS</span></span>

### <span data-ttu-id="0a648-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a648-113">-DefaultProfile</span></span>
<span data-ttu-id="0a648-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0a648-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a648-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a648-115">-InputObject</span></span>
<span data-ttu-id="0a648-116">Объект сертификата.</span><span class="sxs-lookup"><span data-stu-id="0a648-116">Certificate Object.</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a648-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0a648-117">-Name</span></span>
<span data-ttu-id="0a648-118">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="0a648-118">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a648-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0a648-119">-VaultName</span></span>
<span data-ttu-id="0a648-120">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="0a648-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a648-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a648-121">CommonParameters</span></span>
<span data-ttu-id="0a648-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a648-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a648-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a648-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a648-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a648-124">INPUTS</span></span>

### <span data-ttu-id="0a648-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="0a648-125">None</span></span>
<span data-ttu-id="0a648-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0a648-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0a648-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a648-127">OUTPUTS</span></span>

### <span data-ttu-id="0a648-128">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0a648-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0a648-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a648-129">NOTES</span></span>

## <span data-ttu-id="0a648-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a648-130">RELATED LINKS</span></span>

[<span data-ttu-id="0a648-131">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0a648-131">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="0a648-132">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0a648-132">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

