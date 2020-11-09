---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 370662b1d24f9b5b71653506be7a3add5a3801f8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312365"
---
# <span data-ttu-id="4aadf-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4aadf-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4aadf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4aadf-102">SYNOPSIS</span></span>
<span data-ttu-id="4aadf-103">Создает объект политики сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="4aadf-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="4aadf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4aadf-104">SYNTAX</span></span>

### <span data-ttu-id="4aadf-105">SubjectName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4aadf-105">SubjectName (Default)</span></span>
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

### <span data-ttu-id="4aadf-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="4aadf-106">DNSNames</span></span>
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

## <span data-ttu-id="4aadf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4aadf-107">DESCRIPTION</span></span>
<span data-ttu-id="4aadf-108">Командлет **New-AzKeyVaultCertificatePolicy** создает объект политики сертификата в памяти для хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="4aadf-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="4aadf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4aadf-109">EXAMPLES</span></span>

### <span data-ttu-id="4aadf-110">Пример 1: Создание политики сертификата</span><span class="sxs-lookup"><span data-stu-id="4aadf-110">Example 1: Create a certificate policy</span></span>
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

<span data-ttu-id="4aadf-111">Эта команда создает политику сертификата, действующую в течение шести месяцев, и повторно использует ключ для обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="4aadf-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

### <span data-ttu-id="4aadf-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4aadf-112">Example 2</span></span>

<span data-ttu-id="4aadf-113">Создает объект политики сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="4aadf-113">Creates an in-memory certificate policy object.</span></span> <span data-ttu-id="4aadf-114">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="4aadf-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzKeyVaultCertificatePolicy -IssuerName 'Self' -KeyType RSA -RenewAtNumberOfDaysBeforeExpiry <Int32> -SecretContentType application/x-pkcs12 -SubjectName 'CN=contoso.com' -ValidityInMonths 6
```

### <span data-ttu-id="4aadf-115">Пример 3: создание сертификата для альтернативного имени субъекта (или SAN)</span><span class="sxs-lookup"><span data-stu-id="4aadf-115">Example 3: Create a Subject Alternate Name (or SAN) certificate</span></span>

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

<span data-ttu-id="4aadf-116">В этом примере создается сертификат SAN с тремя DNS-именами.</span><span class="sxs-lookup"><span data-stu-id="4aadf-116">This example creates a SAN certificate with 3 DNS names.</span></span>

## <span data-ttu-id="4aadf-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4aadf-117">PARAMETERS</span></span>

### <span data-ttu-id="4aadf-118">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="4aadf-118">-CertificateTransparency</span></span>
<span data-ttu-id="4aadf-119">Указывает, включена ли прозрачность сертификата для этого сертификата или поставщика; Если не указано, используется значение по умолчанию "true"</span><span class="sxs-lookup"><span data-stu-id="4aadf-119">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="4aadf-120">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="4aadf-120">-CertificateType</span></span>
<span data-ttu-id="4aadf-121">Указывает тип сертификата для поставщика.</span><span class="sxs-lookup"><span data-stu-id="4aadf-121">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="4aadf-122">-Кривая</span><span class="sxs-lookup"><span data-stu-id="4aadf-122">-Curve</span></span>
<span data-ttu-id="4aadf-123">Указывает имя эллиптической кривой для ключа сертификата.</span><span class="sxs-lookup"><span data-stu-id="4aadf-123">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="4aadf-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4aadf-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4aadf-125">P-256</span><span class="sxs-lookup"><span data-stu-id="4aadf-125">P-256</span></span>
- <span data-ttu-id="4aadf-126">P-384</span><span class="sxs-lookup"><span data-stu-id="4aadf-126">P-384</span></span>
- <span data-ttu-id="4aadf-127">P-521</span><span class="sxs-lookup"><span data-stu-id="4aadf-127">P-521</span></span>
- <span data-ttu-id="4aadf-128">P – 256 KБ</span><span class="sxs-lookup"><span data-stu-id="4aadf-128">P-256K</span></span>
- <span data-ttu-id="4aadf-129">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="4aadf-129">SECP256K1</span></span>

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

### <span data-ttu-id="4aadf-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aadf-130">-DefaultProfile</span></span>
<span data-ttu-id="4aadf-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4aadf-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4aadf-132">-Отключено</span><span class="sxs-lookup"><span data-stu-id="4aadf-132">-Disabled</span></span>
<span data-ttu-id="4aadf-133">Указывает, что политика сертификата отключена.</span><span class="sxs-lookup"><span data-stu-id="4aadf-133">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="4aadf-134">-DnsName</span><span class="sxs-lookup"><span data-stu-id="4aadf-134">-DnsName</span></span>
<span data-ttu-id="4aadf-135">Указывает DNS-имена в сертификате.</span><span class="sxs-lookup"><span data-stu-id="4aadf-135">Specifies the DNS names in the certificate.</span></span> <span data-ttu-id="4aadf-136">Дополнительные имена субъектов (SAN) можно указывать в DNS-именах.</span><span class="sxs-lookup"><span data-stu-id="4aadf-136">Subject Alternative Names (SANs) can be specified as DNS names.</span></span>

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

### <span data-ttu-id="4aadf-137">-EKU</span><span class="sxs-lookup"><span data-stu-id="4aadf-137">-Ekus</span></span>
<span data-ttu-id="4aadf-138">Определяет использование расширенных клавиш (EKU) в сертификате.</span><span class="sxs-lookup"><span data-stu-id="4aadf-138">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="4aadf-139">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="4aadf-139">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="4aadf-140">Задает количество дней, по истечении которого начинается процесс автоматического уведомления.</span><span class="sxs-lookup"><span data-stu-id="4aadf-140">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="4aadf-141">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="4aadf-141">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="4aadf-142">Указывает процент времени жизни, после которого начинается автоматический процесс уведомления.</span><span class="sxs-lookup"><span data-stu-id="4aadf-142">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="4aadf-143">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="4aadf-143">-IssuerName</span></span>
<span data-ttu-id="4aadf-144">Указывает имя поставщика сертификата.</span><span class="sxs-lookup"><span data-stu-id="4aadf-144">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="4aadf-145">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="4aadf-145">-KeyNotExportable</span></span>
<span data-ttu-id="4aadf-146">Указывает на то, что ключ не может быть экспортирован.</span><span class="sxs-lookup"><span data-stu-id="4aadf-146">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="4aadf-147">-KeySize</span><span class="sxs-lookup"><span data-stu-id="4aadf-147">-KeySize</span></span>
<span data-ttu-id="4aadf-148">Задает размер ключа сертификата.</span><span class="sxs-lookup"><span data-stu-id="4aadf-148">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="4aadf-149">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4aadf-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4aadf-150">2048</span><span class="sxs-lookup"><span data-stu-id="4aadf-150">2048</span></span>
- <span data-ttu-id="4aadf-151">3072</span><span class="sxs-lookup"><span data-stu-id="4aadf-151">3072</span></span>
- <span data-ttu-id="4aadf-152">4096</span><span class="sxs-lookup"><span data-stu-id="4aadf-152">4096</span></span>
- <span data-ttu-id="4aadf-153">256</span><span class="sxs-lookup"><span data-stu-id="4aadf-153">256</span></span>
- <span data-ttu-id="4aadf-154">384</span><span class="sxs-lookup"><span data-stu-id="4aadf-154">384</span></span>
- <span data-ttu-id="4aadf-155">521</span><span class="sxs-lookup"><span data-stu-id="4aadf-155">521</span></span>

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

### <span data-ttu-id="4aadf-156">-KeyType</span><span class="sxs-lookup"><span data-stu-id="4aadf-156">-KeyType</span></span>
<span data-ttu-id="4aadf-157">Задает тип ключа для ключа, который служит для резервного копирования сертификата.</span><span class="sxs-lookup"><span data-stu-id="4aadf-157">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="4aadf-158">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4aadf-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4aadf-159">Корпорация</span><span class="sxs-lookup"><span data-stu-id="4aadf-159">RSA</span></span>
- <span data-ttu-id="4aadf-160">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="4aadf-160">RSA-HSM</span></span>
- <span data-ttu-id="4aadf-161">ЕС</span><span class="sxs-lookup"><span data-stu-id="4aadf-161">EC</span></span>
- <span data-ttu-id="4aadf-162">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="4aadf-162">EC-HSM</span></span>

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

### <span data-ttu-id="4aadf-163">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="4aadf-163">-KeyUsage</span></span>
<span data-ttu-id="4aadf-164">Задает использование ключа в сертификате.</span><span class="sxs-lookup"><span data-stu-id="4aadf-164">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="4aadf-165">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="4aadf-165">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="4aadf-166">Указывает количество дней до истечения срока действия, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="4aadf-166">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="4aadf-167">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="4aadf-167">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="4aadf-168">Указывает процент времени жизни, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="4aadf-168">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="4aadf-169">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="4aadf-169">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="4aadf-170">Указывает на то, что сертификат повторно использует ключ во время продления.</span><span class="sxs-lookup"><span data-stu-id="4aadf-170">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="4aadf-171">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="4aadf-171">-SecretContentType</span></span>
<span data-ttu-id="4aadf-172">Указывает тип контента нового секрета в новом хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="4aadf-172">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="4aadf-173">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4aadf-173">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4aadf-174">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="4aadf-174">application/x-pkcs12</span></span>
- <span data-ttu-id="4aadf-175">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="4aadf-175">application/x-pem-file</span></span>

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

### <span data-ttu-id="4aadf-176">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="4aadf-176">-SubjectName</span></span>
<span data-ttu-id="4aadf-177">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="4aadf-177">Specifies the subject name of the certificate.</span></span> 

> [!NOTE]
> <span data-ttu-id="4aadf-178">Если необходимо использовать запятую (,) или точку (.) в свойстве в `SubjectName` параметре, необходимо заключить поле свойства в кавычки.</span><span class="sxs-lookup"><span data-stu-id="4aadf-178">If you must use a comma (,) or a period (.) within a property in the `SubjectName` parameter, you must enclose the property field in quotation marks.</span></span> <span data-ttu-id="4aadf-179">Например, вы можете использовать O = "Contoso, Ltd.".</span><span class="sxs-lookup"><span data-stu-id="4aadf-179">For example, you may use O="Contoso, Ltd."</span></span> <span data-ttu-id="4aadf-180">в поле Название организации.</span><span class="sxs-lookup"><span data-stu-id="4aadf-180">in the Organization Name field.</span></span>

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

### <span data-ttu-id="4aadf-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="4aadf-181">-ValidityInMonths</span></span>
<span data-ttu-id="4aadf-182">Указывает число месяцев, на которое действителен сертификат.</span><span class="sxs-lookup"><span data-stu-id="4aadf-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="4aadf-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4aadf-183">-Confirm</span></span>
<span data-ttu-id="4aadf-184">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4aadf-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aadf-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aadf-185">-WhatIf</span></span>
<span data-ttu-id="4aadf-186">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4aadf-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aadf-187">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4aadf-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aadf-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aadf-188">CommonParameters</span></span>
<span data-ttu-id="4aadf-189">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4aadf-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aadf-190">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4aadf-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aadf-191">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4aadf-191">INPUTS</span></span>

### <span data-ttu-id="4aadf-192">System. String</span><span class="sxs-lookup"><span data-stu-id="4aadf-192">System.String</span></span>

### <span data-ttu-id="4aadf-193">System. Collections. Generic. List "1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4aadf-193">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4aadf-194">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4aadf-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4aadf-195">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4aadf-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4aadf-196">System. Collections. Generic. List "1 [[System. Security. Cryptography. X509Certificates. X509KeyUsageFlags, System. Security. Cryptography. X509Certificates, Version = 4.2.1.0, культура = нейтральная, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="4aadf-196">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="4aadf-197">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4aadf-197">OUTPUTS</span></span>

### <span data-ttu-id="4aadf-198">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4aadf-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4aadf-199">Пуск</span><span class="sxs-lookup"><span data-stu-id="4aadf-199">NOTES</span></span>

## <span data-ttu-id="4aadf-200">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4aadf-200">RELATED LINKS</span></span>

[<span data-ttu-id="4aadf-201">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4aadf-201">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="4aadf-202">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4aadf-202">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

