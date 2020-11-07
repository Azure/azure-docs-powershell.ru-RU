---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: a6635afc19f95f32d7c50ff7a92ba5868a5945e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900210"
---
# <span data-ttu-id="c1f15-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c1f15-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c1f15-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1f15-102">SYNOPSIS</span></span>
<span data-ttu-id="c1f15-103">Возвращает политику для сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="c1f15-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="c1f15-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1f15-104">SYNTAX</span></span>

### <span data-ttu-id="c1f15-105">VaultAndCertName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c1f15-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1f15-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c1f15-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1f15-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1f15-107">DESCRIPTION</span></span>
<span data-ttu-id="c1f15-108">Командлет **Get-AzKeyVaultCertificatePolicy** получает политику для сертификата в хранилище ключей Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="c1f15-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="c1f15-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1f15-109">EXAMPLES</span></span>

### <span data-ttu-id="c1f15-110">Пример 1: получение политики сертификата</span><span class="sxs-lookup"><span data-stu-id="c1f15-110">Example 1: Get a certificate policy</span></span>
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

<span data-ttu-id="c1f15-111">Эта команда возвращает политику сертификата TestCert01 сертификата в хранилище ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="c1f15-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="c1f15-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1f15-112">PARAMETERS</span></span>

### <span data-ttu-id="c1f15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1f15-113">-DefaultProfile</span></span>
<span data-ttu-id="c1f15-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c1f15-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1f15-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1f15-115">-InputObject</span></span>
<span data-ttu-id="c1f15-116">Объект сертификата.</span><span class="sxs-lookup"><span data-stu-id="c1f15-116">Certificate Object.</span></span>

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

### <span data-ttu-id="c1f15-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c1f15-117">-Name</span></span>
<span data-ttu-id="c1f15-118">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="c1f15-118">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="c1f15-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c1f15-119">-VaultName</span></span>
<span data-ttu-id="c1f15-120">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="c1f15-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="c1f15-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1f15-121">CommonParameters</span></span>
<span data-ttu-id="c1f15-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1f15-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1f15-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1f15-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1f15-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1f15-124">INPUTS</span></span>

### <span data-ttu-id="c1f15-125">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c1f15-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="c1f15-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1f15-126">OUTPUTS</span></span>

### <span data-ttu-id="c1f15-127">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c1f15-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c1f15-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1f15-128">NOTES</span></span>

## <span data-ttu-id="c1f15-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1f15-129">RELATED LINKS</span></span>

[<span data-ttu-id="c1f15-130">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c1f15-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="c1f15-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c1f15-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

