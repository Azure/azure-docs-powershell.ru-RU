---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 370662b1d24f9b5b71653506be7a3add5a3801f8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425844"
---
# <span data-ttu-id="10f82-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="10f82-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="10f82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10f82-102">SYNOPSIS</span></span>
<span data-ttu-id="10f82-103">Создает объект политики сертификатов в памяти.</span><span class="sxs-lookup"><span data-stu-id="10f82-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="10f82-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="10f82-104">SYNTAX</span></span>

### <span data-ttu-id="10f82-105">SubjectName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="10f82-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10f82-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="10f82-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10f82-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10f82-107">DESCRIPTION</span></span>
<span data-ttu-id="10f82-108">Cmdlet **New-AzKeyVaultCertificatePolicy** создает объект политики сертификатов в памяти для хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="10f82-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="10f82-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="10f82-109">EXAMPLES</span></span>

### <span data-ttu-id="10f82-110">Пример 1. Создание политики сертификатов</span><span class="sxs-lookup"><span data-stu-id="10f82-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
Curve                           :
Exportable                      :
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        :
KeyUsage                        :
Ekus                            :
ValidityInMonths                : 6
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry :
RenewAtPercentageLifetime       :
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
CertificateTransparency         :
Enabled                         : True
Created                         :
Updated                         :
```

<span data-ttu-id="10f82-111">Эта команда создает политику сертификата, действительную в течение шести месяцев, и повторно использовать ключ для продления сертификата.</span><span class="sxs-lookup"><span data-stu-id="10f82-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

### <span data-ttu-id="10f82-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="10f82-112">Example 2</span></span>

<span data-ttu-id="10f82-113">Создает объект политики сертификатов в памяти.</span><span class="sxs-lookup"><span data-stu-id="10f82-113">Creates an in-memory certificate policy object.</span></span> <span data-ttu-id="10f82-114">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="10f82-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzKeyVaultCertificatePolicy -IssuerName 'Self' -KeyType RSA -RenewAtNumberOfDaysBeforeExpiry <Int32> -SecretContentType application/x-pkcs12 -SubjectName 'CN=contoso.com' -ValidityInMonths 6
```

### <span data-ttu-id="10f82-115">Пример 3. Создание сертификата "Альтернативное имя субъекта" (SAN)</span><span class="sxs-lookup"><span data-stu-id="10f82-115">Example 3: Create a Subject Alternate Name (or SAN) certificate</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -DnsName "contoso.com","support.contoso.com","docs.contoso.com" -IssuerName "Self"

SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Curve                           :
Exportable                      :
ReuseKeyOnRenewal               : False
SubjectName                     : CN=contoso.com
DnsNames                        : {contoso.com, support.contoso.com, docs.contoso.com}
KeyUsage                        :
Ekus                            :
ValidityInMonths                :
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry :
RenewAtPercentageLifetime       :
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
CertificateTransparency         :
Enabled                         : True
Created                         :
Updated                         :
```

<span data-ttu-id="10f82-116">В этом примере создается сертификат SAN с 3 именами DNS.</span><span class="sxs-lookup"><span data-stu-id="10f82-116">This example creates a SAN certificate with 3 DNS names.</span></span>

## <span data-ttu-id="10f82-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10f82-117">PARAMETERS</span></span>

### <span data-ttu-id="10f82-118">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="10f82-118">-CertificateTransparency</span></span>
<span data-ttu-id="10f82-119">Указывает, включена ли прозрачность сертификата для этого сертификата или выпуска; если не указано, по умолчанию задано значение true.</span><span class="sxs-lookup"><span data-stu-id="10f82-119">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-120">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="10f82-120">-CertificateType</span></span>
<span data-ttu-id="10f82-121">Тип сертификата, который нужно выдать.</span><span class="sxs-lookup"><span data-stu-id="10f82-121">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-122">-Кривая</span><span class="sxs-lookup"><span data-stu-id="10f82-122">-Curve</span></span>
<span data-ttu-id="10f82-123">Указывает название многоliptic curve ключа сертификата.</span><span class="sxs-lookup"><span data-stu-id="10f82-123">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="10f82-124">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="10f82-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="10f82-125">P-256</span><span class="sxs-lookup"><span data-stu-id="10f82-125">P-256</span></span>
- <span data-ttu-id="10f82-126">P-384</span><span class="sxs-lookup"><span data-stu-id="10f82-126">P-384</span></span>
- <span data-ttu-id="10f82-127">P-521</span><span class="sxs-lookup"><span data-stu-id="10f82-127">P-521</span></span>
- <span data-ttu-id="10f82-128">P-256K</span><span class="sxs-lookup"><span data-stu-id="10f82-128">P-256K</span></span>
- <span data-ttu-id="10f82-129">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="10f82-129">SECP256K1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: P-256, P-384, P-521, P-256K, SECP256K1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10f82-130">-DefaultProfile</span></span>
<span data-ttu-id="10f82-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="10f82-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10f82-132">-Disabled</span><span class="sxs-lookup"><span data-stu-id="10f82-132">-Disabled</span></span>
<span data-ttu-id="10f82-133">Указывает на то, что политика сертификата отключена.</span><span class="sxs-lookup"><span data-stu-id="10f82-133">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-134">-DnsName</span><span class="sxs-lookup"><span data-stu-id="10f82-134">-DnsName</span></span>
<span data-ttu-id="10f82-135">Указывает имена DNS в сертификате.</span><span class="sxs-lookup"><span data-stu-id="10f82-135">Specifies the DNS names in the certificate.</span></span> <span data-ttu-id="10f82-136">Альтернативные имена темы (SANs) можно у указывает как имена DNS.</span><span class="sxs-lookup"><span data-stu-id="10f82-136">Subject Alternative Names (SANs) can be specified as DNS names.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: DNSNames
Aliases: DnsNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-137">-Ekus</span><span class="sxs-lookup"><span data-stu-id="10f82-137">-Ekus</span></span>
<span data-ttu-id="10f82-138">Указывает расширенные возможности использования ключей (EKUs) в сертификате.</span><span class="sxs-lookup"><span data-stu-id="10f82-138">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-139">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="10f82-139">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="10f82-140">Определяет, за сколько дней до окончания срока действия начнется процесс автоматического уведомления.</span><span class="sxs-lookup"><span data-stu-id="10f82-140">Specifies how many days before expiry the automatic notification process begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-141">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="10f82-141">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="10f82-142">Указывает процент времени существования, после которого начнется автоматическая обработка уведомления.</span><span class="sxs-lookup"><span data-stu-id="10f82-142">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-143">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="10f82-143">-IssuerName</span></span>
<span data-ttu-id="10f82-144">Указывает имя выпускаемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="10f82-144">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-145">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="10f82-145">-KeyNotExportable</span></span>
<span data-ttu-id="10f82-146">Указывает на то, что ключ не экспортируется.</span><span class="sxs-lookup"><span data-stu-id="10f82-146">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-147">-KeySize</span><span class="sxs-lookup"><span data-stu-id="10f82-147">-KeySize</span></span>
<span data-ttu-id="10f82-148">Определяет размер ключа сертификата.</span><span class="sxs-lookup"><span data-stu-id="10f82-148">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="10f82-149">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="10f82-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="10f82-150">2048</span><span class="sxs-lookup"><span data-stu-id="10f82-150">2048</span></span>
- <span data-ttu-id="10f82-151">3072</span><span class="sxs-lookup"><span data-stu-id="10f82-151">3072</span></span>
- <span data-ttu-id="10f82-152">4096</span><span class="sxs-lookup"><span data-stu-id="10f82-152">4096</span></span>
- <span data-ttu-id="10f82-153">256</span><span class="sxs-lookup"><span data-stu-id="10f82-153">256</span></span>
- <span data-ttu-id="10f82-154">384</span><span class="sxs-lookup"><span data-stu-id="10f82-154">384</span></span>
- <span data-ttu-id="10f82-155">521</span><span class="sxs-lookup"><span data-stu-id="10f82-155">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-156">-KeyType</span><span class="sxs-lookup"><span data-stu-id="10f82-156">-KeyType</span></span>
<span data-ttu-id="10f82-157">Определяет тип ключа, который будет возвращать сертификат.</span><span class="sxs-lookup"><span data-stu-id="10f82-157">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="10f82-158">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="10f82-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="10f82-159">RSA</span><span class="sxs-lookup"><span data-stu-id="10f82-159">RSA</span></span>
- <span data-ttu-id="10f82-160">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="10f82-160">RSA-HSM</span></span>
- <span data-ttu-id="10f82-161">EC</span><span class="sxs-lookup"><span data-stu-id="10f82-161">EC</span></span>
- <span data-ttu-id="10f82-162">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="10f82-162">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-163">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="10f82-163">-KeyUsage</span></span>
<span data-ttu-id="10f82-164">Указывает использование ключа в сертификате.</span><span class="sxs-lookup"><span data-stu-id="10f82-164">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: (All)
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-165">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="10f82-165">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="10f82-166">Количество дней до окончания срока действия, после которого начнется автоматическая процедура продления сертификата.</span><span class="sxs-lookup"><span data-stu-id="10f82-166">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-167">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="10f82-167">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="10f82-168">Указывает процент времени существования, после которого начнется автоматическая процедура продления сертификата.</span><span class="sxs-lookup"><span data-stu-id="10f82-168">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-169">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="10f82-169">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="10f82-170">Указывает на повторное использование ключа сертификатом во время продления.</span><span class="sxs-lookup"><span data-stu-id="10f82-170">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-171">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="10f82-171">-SecretContentType</span></span>
<span data-ttu-id="10f82-172">Определяет тип контента нового секретного сейфа.</span><span class="sxs-lookup"><span data-stu-id="10f82-172">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="10f82-173">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="10f82-173">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="10f82-174">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="10f82-174">application/x-pkcs12</span></span>
- <span data-ttu-id="10f82-175">application/x-pem-file</span><span class="sxs-lookup"><span data-stu-id="10f82-175">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-176">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="10f82-176">-SubjectName</span></span>
<span data-ttu-id="10f82-177">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="10f82-177">Specifies the subject name of the certificate.</span></span> 

> [!NOTE]
> <span data-ttu-id="10f82-178">Если в свойстве параметра необходимо использовать запятую (,) или точка (.), необходимо заключить поле свойства `SubjectName` в кавычках.</span><span class="sxs-lookup"><span data-stu-id="10f82-178">If you must use a comma (,) or a period (.) within a property in the `SubjectName` parameter, you must enclose the property field in quotation marks.</span></span> <span data-ttu-id="10f82-179">Например, вы можете использовать O="Contoso, Ltd".</span><span class="sxs-lookup"><span data-stu-id="10f82-179">For example, you may use O="Contoso, Ltd."</span></span> <span data-ttu-id="10f82-180">в поле "Название организации".</span><span class="sxs-lookup"><span data-stu-id="10f82-180">in the Organization Name field.</span></span>

```yaml
Type: System.String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="10f82-181">-ValidityInMonths</span></span>
<span data-ttu-id="10f82-182">Указывает, на определенное количество месяцев действителен сертификат.</span><span class="sxs-lookup"><span data-stu-id="10f82-182">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10f82-183">-Confirm</span></span>
<span data-ttu-id="10f82-184">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10f82-184">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10f82-185">-WhatIf</span></span>
<span data-ttu-id="10f82-186">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10f82-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10f82-187">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="10f82-187">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10f82-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10f82-188">CommonParameters</span></span>
<span data-ttu-id="10f82-189">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10f82-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10f82-190">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10f82-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10f82-191">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10f82-191">INPUTS</span></span>

### <span data-ttu-id="10f82-192">System.String</span><span class="sxs-lookup"><span data-stu-id="10f82-192">System.String</span></span>

### <span data-ttu-id="10f82-193">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="10f82-193">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="10f82-194">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="10f82-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="10f82-195">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="10f82-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="10f82-196">System.Collections.Generic.List'1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="10f82-196">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="10f82-197">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="10f82-197">OUTPUTS</span></span>

### <span data-ttu-id="10f82-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="10f82-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="10f82-199">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="10f82-199">NOTES</span></span>

## <span data-ttu-id="10f82-200">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10f82-200">RELATED LINKS</span></span>

[<span data-ttu-id="10f82-201">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="10f82-201">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="10f82-202">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="10f82-202">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

