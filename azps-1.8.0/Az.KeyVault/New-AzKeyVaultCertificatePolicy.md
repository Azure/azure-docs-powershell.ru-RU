---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: e5b03660c37dff6333479c19d7de039d368fd4ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900174"
---
# <span data-ttu-id="4ccb4-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4ccb4-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4ccb4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ccb4-102">SYNOPSIS</span></span>
<span data-ttu-id="4ccb4-103">Создает объект политики сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="4ccb4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ccb4-104">SYNTAX</span></span>

### <span data-ttu-id="4ccb4-105">SubjectName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ccb4-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ccb4-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="4ccb4-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ccb4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ccb4-107">DESCRIPTION</span></span>
<span data-ttu-id="4ccb4-108">Командлет **New-AzKeyVaultCertificatePolicy** создает объект политики сертификата в памяти для хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="4ccb4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ccb4-109">EXAMPLES</span></span>

### <span data-ttu-id="4ccb4-110">Пример 1: Создание политики сертификата</span><span class="sxs-lookup"><span data-stu-id="4ccb4-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
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

<span data-ttu-id="4ccb4-111">Эта команда создает политику сертификата, действующую в течение шести месяцев, и повторно использует ключ для обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="4ccb4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ccb4-112">PARAMETERS</span></span>

### <span data-ttu-id="4ccb4-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="4ccb4-113">-CertificateType</span></span>
<span data-ttu-id="4ccb4-114">Указывает тип сертификата для поставщика.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-114">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="4ccb4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ccb4-115">-DefaultProfile</span></span>
<span data-ttu-id="4ccb4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4ccb4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ccb4-117">-Отключено</span><span class="sxs-lookup"><span data-stu-id="4ccb4-117">-Disabled</span></span>
<span data-ttu-id="4ccb4-118">Указывает, что политика сертификата отключена.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-118">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="4ccb4-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="4ccb4-119">-DnsName</span></span>
<span data-ttu-id="4ccb4-120">Указывает DNS-имена в сертификате.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-120">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="4ccb4-121">-EKU</span><span class="sxs-lookup"><span data-stu-id="4ccb4-121">-Ekus</span></span>
<span data-ttu-id="4ccb4-122">Определяет использование расширенных клавиш (EKU) в сертификате.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="4ccb4-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="4ccb4-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="4ccb4-124">Задает количество дней, по истечении которого начинается процесс автоматического уведомления.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="4ccb4-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="4ccb4-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="4ccb4-126">Указывает процент времени жизни, после которого начинается автоматический процесс уведомления.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="4ccb4-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="4ccb4-127">-IssuerName</span></span>
<span data-ttu-id="4ccb4-128">Указывает имя поставщика сертификата.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-128">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="4ccb4-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="4ccb4-129">-KeyNotExportable</span></span>
<span data-ttu-id="4ccb4-130">Указывает на то, что ключ не может быть экспортирован.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-130">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="4ccb4-131">-KeyType</span><span class="sxs-lookup"><span data-stu-id="4ccb4-131">-KeyType</span></span>
<span data-ttu-id="4ccb4-132">Задает тип ключа для ключа, который служит для резервного копирования сертификата.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="4ccb4-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4ccb4-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ccb4-134">Корпорация</span><span class="sxs-lookup"><span data-stu-id="4ccb4-134">RSA</span></span>
- <span data-ttu-id="4ccb4-135">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="4ccb4-135">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ccb4-136">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="4ccb4-136">-KeyUsage</span></span>
<span data-ttu-id="4ccb4-137">Задает использование ключа в сертификате.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-137">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="4ccb4-138">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="4ccb4-138">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="4ccb4-139">Указывает количество дней до истечения срока действия, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-139">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="4ccb4-140">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="4ccb4-140">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="4ccb4-141">Указывает процент времени жизни, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-141">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="4ccb4-142">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="4ccb4-142">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="4ccb4-143">Указывает на то, что сертификат повторно использует ключ во время продления.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-143">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="4ccb4-144">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="4ccb4-144">-SecretContentType</span></span>
<span data-ttu-id="4ccb4-145">Указывает тип контента нового секрета в новом хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-145">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="4ccb4-146">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4ccb4-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ccb4-147">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="4ccb4-147">application/x-pkcs12</span></span>
- <span data-ttu-id="4ccb4-148">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="4ccb4-148">application/x-pem-file</span></span>

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

### <span data-ttu-id="4ccb4-149">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="4ccb4-149">-SubjectName</span></span>
<span data-ttu-id="4ccb4-150">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-150">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="4ccb4-151">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="4ccb4-151">-ValidityInMonths</span></span>
<span data-ttu-id="4ccb4-152">Указывает число месяцев, на которое действителен сертификат.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-152">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="4ccb4-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ccb4-153">-Confirm</span></span>
<span data-ttu-id="4ccb4-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ccb4-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ccb4-155">-WhatIf</span></span>
<span data-ttu-id="4ccb4-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ccb4-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ccb4-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ccb4-158">CommonParameters</span></span>
<span data-ttu-id="4ccb4-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ccb4-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ccb4-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ccb4-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ccb4-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ccb4-161">INPUTS</span></span>

### <span data-ttu-id="4ccb4-162">System. String</span><span class="sxs-lookup"><span data-stu-id="4ccb4-162">System.String</span></span>

### <span data-ttu-id="4ccb4-163">System. Collections. Generic. List "1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4ccb4-163">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4ccb4-164">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4ccb4-164">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4ccb4-165">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4ccb4-165">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4ccb4-166">System. Collections. Generic. List "1 [[System. Security. Cryptography. X509Certificates. X509KeyUsageFlags, System. Security. Cryptography. X509Certificates, Version = 4.2.1.0, культура = нейтральная, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="4ccb4-166">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="4ccb4-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ccb4-167">OUTPUTS</span></span>

### <span data-ttu-id="4ccb4-168">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4ccb4-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4ccb4-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ccb4-169">NOTES</span></span>

## <span data-ttu-id="4ccb4-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ccb4-170">RELATED LINKS</span></span>

[<span data-ttu-id="4ccb4-171">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4ccb4-171">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="4ccb4-172">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4ccb4-172">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

