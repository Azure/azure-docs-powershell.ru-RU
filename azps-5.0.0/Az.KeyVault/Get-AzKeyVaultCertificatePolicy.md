---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d6e2225cc7441d4c370d990aa45c9b2c2bb40457
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245317"
---
# <span data-ttu-id="8591c-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8591c-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="8591c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8591c-102">SYNOPSIS</span></span>
<span data-ttu-id="8591c-103">Возвращает политику для сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="8591c-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="8591c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8591c-104">SYNTAX</span></span>

### <span data-ttu-id="8591c-105">VaultAndCertName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8591c-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8591c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8591c-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8591c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8591c-107">DESCRIPTION</span></span>
<span data-ttu-id="8591c-108">Командлет **Get-AzKeyVaultCertificatePolicy** получает политику для сертификата в хранилище ключей Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="8591c-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="8591c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8591c-109">EXAMPLES</span></span>

### <span data-ttu-id="8591c-110">Пример 1: получение политики сертификата</span><span class="sxs-lookup"><span data-stu-id="8591c-110">Example 1: Get a certificate policy</span></span>
```powershell
PS C:\ >Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"

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

<span data-ttu-id="8591c-111">Эта команда возвращает политику сертификата TestCert01 сертификата в хранилище ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="8591c-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="8591c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8591c-112">PARAMETERS</span></span>

### <span data-ttu-id="8591c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8591c-113">-DefaultProfile</span></span>
<span data-ttu-id="8591c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8591c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8591c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8591c-115">-InputObject</span></span>
<span data-ttu-id="8591c-116">Объект сертификата.</span><span class="sxs-lookup"><span data-stu-id="8591c-116">Certificate Object.</span></span>

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

### <span data-ttu-id="8591c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8591c-117">-Name</span></span>
<span data-ttu-id="8591c-118">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="8591c-118">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="8591c-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8591c-119">-VaultName</span></span>
<span data-ttu-id="8591c-120">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8591c-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="8591c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8591c-121">CommonParameters</span></span>
<span data-ttu-id="8591c-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8591c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8591c-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8591c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8591c-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8591c-124">INPUTS</span></span>

### <span data-ttu-id="8591c-125">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8591c-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="8591c-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8591c-126">OUTPUTS</span></span>

### <span data-ttu-id="8591c-127">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8591c-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="8591c-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="8591c-128">NOTES</span></span>

## <span data-ttu-id="8591c-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8591c-129">RELATED LINKS</span></span>

[<span data-ttu-id="8591c-130">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8591c-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="8591c-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8591c-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)
