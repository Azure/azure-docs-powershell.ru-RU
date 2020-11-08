---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: b0d690358fb5598b1a88ecb7fe169c8ef3d2718f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074881"
---
# <span data-ttu-id="e5072-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="e5072-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="e5072-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5072-102">SYNOPSIS</span></span>
<span data-ttu-id="e5072-103">Создает объект политики сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="e5072-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="e5072-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5072-104">SYNTAX</span></span>

### <span data-ttu-id="e5072-105">SubjectName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5072-105">SubjectName (Default)</span></span>
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

### <span data-ttu-id="e5072-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="e5072-106">DNSNames</span></span>
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

## <span data-ttu-id="e5072-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5072-107">DESCRIPTION</span></span>
<span data-ttu-id="e5072-108">Командлет **New-AzKeyVaultCertificatePolicy** создает объект политики сертификата в памяти для хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="e5072-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="e5072-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5072-109">EXAMPLES</span></span>

### <span data-ttu-id="e5072-110">Пример 1: Создание политики сертификата</span><span class="sxs-lookup"><span data-stu-id="e5072-110">Example 1: Create a certificate policy</span></span>
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

<span data-ttu-id="e5072-111">Эта команда создает политику сертификата, действующую в течение шести месяцев, и повторно использует ключ для обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="e5072-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="e5072-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5072-112">PARAMETERS</span></span>

### <span data-ttu-id="e5072-113">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="e5072-113">-CertificateTransparency</span></span>
<span data-ttu-id="e5072-114">Указывает, включена ли прозрачность сертификата для этого сертификата или поставщика; Если не указано, используется значение по умолчанию "true"</span><span class="sxs-lookup"><span data-stu-id="e5072-114">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="e5072-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="e5072-115">-CertificateType</span></span>
<span data-ttu-id="e5072-116">Указывает тип сертификата для поставщика.</span><span class="sxs-lookup"><span data-stu-id="e5072-116">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="e5072-117">-Кривая</span><span class="sxs-lookup"><span data-stu-id="e5072-117">-Curve</span></span>
<span data-ttu-id="e5072-118">Указывает имя эллиптической кривой для ключа сертификата.</span><span class="sxs-lookup"><span data-stu-id="e5072-118">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="e5072-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e5072-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e5072-120">P-256</span><span class="sxs-lookup"><span data-stu-id="e5072-120">P-256</span></span>
- <span data-ttu-id="e5072-121">P-384</span><span class="sxs-lookup"><span data-stu-id="e5072-121">P-384</span></span>
- <span data-ttu-id="e5072-122">P-521</span><span class="sxs-lookup"><span data-stu-id="e5072-122">P-521</span></span>
- <span data-ttu-id="e5072-123">P – 256 KБ</span><span class="sxs-lookup"><span data-stu-id="e5072-123">P-256K</span></span>
- <span data-ttu-id="e5072-124">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="e5072-124">SECP256K1</span></span>

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

### <span data-ttu-id="e5072-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5072-125">-DefaultProfile</span></span>
<span data-ttu-id="e5072-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e5072-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5072-127">-Отключено</span><span class="sxs-lookup"><span data-stu-id="e5072-127">-Disabled</span></span>
<span data-ttu-id="e5072-128">Указывает, что политика сертификата отключена.</span><span class="sxs-lookup"><span data-stu-id="e5072-128">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="e5072-129">-DnsName</span><span class="sxs-lookup"><span data-stu-id="e5072-129">-DnsName</span></span>
<span data-ttu-id="e5072-130">Указывает DNS-имена в сертификате.</span><span class="sxs-lookup"><span data-stu-id="e5072-130">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="e5072-131">-EKU</span><span class="sxs-lookup"><span data-stu-id="e5072-131">-Ekus</span></span>
<span data-ttu-id="e5072-132">Определяет использование расширенных клавиш (EKU) в сертификате.</span><span class="sxs-lookup"><span data-stu-id="e5072-132">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="e5072-133">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="e5072-133">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="e5072-134">Задает количество дней, по истечении которого начинается процесс автоматического уведомления.</span><span class="sxs-lookup"><span data-stu-id="e5072-134">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="e5072-135">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="e5072-135">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="e5072-136">Указывает процент времени жизни, после которого начинается автоматический процесс уведомления.</span><span class="sxs-lookup"><span data-stu-id="e5072-136">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="e5072-137">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="e5072-137">-IssuerName</span></span>
<span data-ttu-id="e5072-138">Указывает имя поставщика сертификата.</span><span class="sxs-lookup"><span data-stu-id="e5072-138">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="e5072-139">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="e5072-139">-KeyNotExportable</span></span>
<span data-ttu-id="e5072-140">Указывает на то, что ключ не может быть экспортирован.</span><span class="sxs-lookup"><span data-stu-id="e5072-140">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="e5072-141">-KeySize</span><span class="sxs-lookup"><span data-stu-id="e5072-141">-KeySize</span></span>
<span data-ttu-id="e5072-142">Задает размер ключа сертификата.</span><span class="sxs-lookup"><span data-stu-id="e5072-142">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="e5072-143">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e5072-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e5072-144">2048</span><span class="sxs-lookup"><span data-stu-id="e5072-144">2048</span></span>
- <span data-ttu-id="e5072-145">3072</span><span class="sxs-lookup"><span data-stu-id="e5072-145">3072</span></span>
- <span data-ttu-id="e5072-146">4096</span><span class="sxs-lookup"><span data-stu-id="e5072-146">4096</span></span>
- <span data-ttu-id="e5072-147">256</span><span class="sxs-lookup"><span data-stu-id="e5072-147">256</span></span>
- <span data-ttu-id="e5072-148">384</span><span class="sxs-lookup"><span data-stu-id="e5072-148">384</span></span>
- <span data-ttu-id="e5072-149">521</span><span class="sxs-lookup"><span data-stu-id="e5072-149">521</span></span>

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

### <span data-ttu-id="e5072-150">-KeyType</span><span class="sxs-lookup"><span data-stu-id="e5072-150">-KeyType</span></span>
<span data-ttu-id="e5072-151">Задает тип ключа для ключа, который служит для резервного копирования сертификата.</span><span class="sxs-lookup"><span data-stu-id="e5072-151">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="e5072-152">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e5072-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e5072-153">Корпорация</span><span class="sxs-lookup"><span data-stu-id="e5072-153">RSA</span></span>
- <span data-ttu-id="e5072-154">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="e5072-154">RSA-HSM</span></span>
- <span data-ttu-id="e5072-155">ЕС</span><span class="sxs-lookup"><span data-stu-id="e5072-155">EC</span></span>
- <span data-ttu-id="e5072-156">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="e5072-156">EC-HSM</span></span>

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

### <span data-ttu-id="e5072-157">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="e5072-157">-KeyUsage</span></span>
<span data-ttu-id="e5072-158">Задает использование ключа в сертификате.</span><span class="sxs-lookup"><span data-stu-id="e5072-158">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="e5072-159">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="e5072-159">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="e5072-160">Указывает количество дней до истечения срока действия, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="e5072-160">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="e5072-161">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="e5072-161">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="e5072-162">Указывает процент времени жизни, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="e5072-162">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="e5072-163">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="e5072-163">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="e5072-164">Указывает на то, что сертификат повторно использует ключ во время продления.</span><span class="sxs-lookup"><span data-stu-id="e5072-164">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="e5072-165">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="e5072-165">-SecretContentType</span></span>
<span data-ttu-id="e5072-166">Указывает тип контента нового секрета в новом хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="e5072-166">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="e5072-167">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e5072-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e5072-168">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="e5072-168">application/x-pkcs12</span></span>
- <span data-ttu-id="e5072-169">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="e5072-169">application/x-pem-file</span></span>

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

### <span data-ttu-id="e5072-170">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="e5072-170">-SubjectName</span></span>
<span data-ttu-id="e5072-171">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="e5072-171">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="e5072-172">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="e5072-172">-ValidityInMonths</span></span>
<span data-ttu-id="e5072-173">Указывает число месяцев, на которое действителен сертификат.</span><span class="sxs-lookup"><span data-stu-id="e5072-173">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="e5072-174">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5072-174">-Confirm</span></span>
<span data-ttu-id="e5072-175">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e5072-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5072-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5072-176">-WhatIf</span></span>
<span data-ttu-id="e5072-177">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e5072-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5072-178">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e5072-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5072-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5072-179">CommonParameters</span></span>
<span data-ttu-id="e5072-180">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5072-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5072-181">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5072-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5072-182">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5072-182">INPUTS</span></span>

### <span data-ttu-id="e5072-183">System. String</span><span class="sxs-lookup"><span data-stu-id="e5072-183">System.String</span></span>

### <span data-ttu-id="e5072-184">System. Collections. Generic. List "1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e5072-184">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e5072-185">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e5072-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e5072-186">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e5072-186">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e5072-187">System. Collections. Generic. List "1 [[System. Security. Cryptography. X509Certificates. X509KeyUsageFlags, System. Security. Cryptography. X509Certificates, Version = 4.2.1.0, культура = нейтральная, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="e5072-187">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="e5072-188">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5072-188">OUTPUTS</span></span>

### <span data-ttu-id="e5072-189">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="e5072-189">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="e5072-190">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5072-190">NOTES</span></span>

## <span data-ttu-id="e5072-191">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5072-191">RELATED LINKS</span></span>

[<span data-ttu-id="e5072-192">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="e5072-192">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="e5072-193">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="e5072-193">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

