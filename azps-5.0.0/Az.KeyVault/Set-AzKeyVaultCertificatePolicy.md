---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 963a7005e95941a644b35a57f80b558f02e2d6a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312350"
---
# <span data-ttu-id="ab321-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="ab321-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="ab321-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ab321-102">SYNOPSIS</span></span>
<span data-ttu-id="ab321-103">Создание или обновление политики сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="ab321-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="ab321-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ab321-104">SYNTAX</span></span>

### <span data-ttu-id="ab321-105">ExpandedRenewPercentage (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ab321-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab321-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="ab321-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab321-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="ab321-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab321-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab321-108">DESCRIPTION</span></span>
<span data-ttu-id="ab321-109">Командлет **Set-AzKeyVaultCertificatePolicy** создает или обновляет политику для сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="ab321-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="ab321-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ab321-110">EXAMPLES</span></span>

### <span data-ttu-id="ab321-111">Пример 1: Настройка политики сертификата</span><span class="sxs-lookup"><span data-stu-id="ab321-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="ab321-112">Эта команда задает политику сертификата TestCert01 в хранилище ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="ab321-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="ab321-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ab321-113">PARAMETERS</span></span>

### <span data-ttu-id="ab321-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="ab321-114">-CertificateTransparency</span></span>
<span data-ttu-id="ab321-115">Указывает, включена ли прозрачность сертификата для этого сертификата или поставщика; Если не указано, по умолчанию используется значение true.</span><span class="sxs-lookup"><span data-stu-id="ab321-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'.</span></span>
<span data-ttu-id="ab321-116">`-IssuerName` При задании этого свойства должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="ab321-116">`-IssuerName` needs to be specified when setting this property.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-117">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="ab321-117">-CertificateType</span></span>
<span data-ttu-id="ab321-118">Указывает тип сертификата для поставщика.</span><span class="sxs-lookup"><span data-stu-id="ab321-118">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-119">-Кривая</span><span class="sxs-lookup"><span data-stu-id="ab321-119">-Curve</span></span>
<span data-ttu-id="ab321-120">Указывает имя эллиптической кривой для ключа сертификата.</span><span class="sxs-lookup"><span data-stu-id="ab321-120">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="ab321-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ab321-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ab321-122">P-256</span><span class="sxs-lookup"><span data-stu-id="ab321-122">P-256</span></span>
- <span data-ttu-id="ab321-123">P-384</span><span class="sxs-lookup"><span data-stu-id="ab321-123">P-384</span></span>
- <span data-ttu-id="ab321-124">P-521</span><span class="sxs-lookup"><span data-stu-id="ab321-124">P-521</span></span>
- <span data-ttu-id="ab321-125">P – 256 KБ</span><span class="sxs-lookup"><span data-stu-id="ab321-125">P-256K</span></span>
- <span data-ttu-id="ab321-126">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="ab321-126">SECP256K1</span></span>

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

### <span data-ttu-id="ab321-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab321-127">-DefaultProfile</span></span>
<span data-ttu-id="ab321-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ab321-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab321-129">-Отключено</span><span class="sxs-lookup"><span data-stu-id="ab321-129">-Disabled</span></span>
<span data-ttu-id="ab321-130">Указывает, что политика сертификата отключена.</span><span class="sxs-lookup"><span data-stu-id="ab321-130">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-131">-DnsName</span><span class="sxs-lookup"><span data-stu-id="ab321-131">-DnsName</span></span>
<span data-ttu-id="ab321-132">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="ab321-132">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-133">-EKU</span><span class="sxs-lookup"><span data-stu-id="ab321-133">-Ekus</span></span>
<span data-ttu-id="ab321-134">Определяет использование расширенных клавиш (EKU) в сертификате.</span><span class="sxs-lookup"><span data-stu-id="ab321-134">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-135">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="ab321-135">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="ab321-136">Указывает число дней, по истечении которого служба автоматического продления подписки запускается.</span><span class="sxs-lookup"><span data-stu-id="ab321-136">Specifies the number of days before expiration when automatic renewal should start.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-137">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="ab321-137">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="ab321-138">Указывает процент времени жизни, после которого начинается автоматический процесс уведомления.</span><span class="sxs-lookup"><span data-stu-id="ab321-138">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab321-139">-InputObject</span></span>
<span data-ttu-id="ab321-140">Указывает политику сертификата.</span><span class="sxs-lookup"><span data-stu-id="ab321-140">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-141">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="ab321-141">-IssuerName</span></span>
<span data-ttu-id="ab321-142">Указывает имя поставщика для этого сертификата.</span><span class="sxs-lookup"><span data-stu-id="ab321-142">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-143">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="ab321-143">-KeyNotExportable</span></span>
<span data-ttu-id="ab321-144">Указывает на то, что ключ не может быть экспортирован.</span><span class="sxs-lookup"><span data-stu-id="ab321-144">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-145">-KeySize</span><span class="sxs-lookup"><span data-stu-id="ab321-145">-KeySize</span></span>
<span data-ttu-id="ab321-146">Задает размер ключа сертификата.</span><span class="sxs-lookup"><span data-stu-id="ab321-146">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="ab321-147">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ab321-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ab321-148">2048</span><span class="sxs-lookup"><span data-stu-id="ab321-148">2048</span></span>
- <span data-ttu-id="ab321-149">3072</span><span class="sxs-lookup"><span data-stu-id="ab321-149">3072</span></span>
- <span data-ttu-id="ab321-150">4096</span><span class="sxs-lookup"><span data-stu-id="ab321-150">4096</span></span>
- <span data-ttu-id="ab321-151">256</span><span class="sxs-lookup"><span data-stu-id="ab321-151">256</span></span>
- <span data-ttu-id="ab321-152">384</span><span class="sxs-lookup"><span data-stu-id="ab321-152">384</span></span>
- <span data-ttu-id="ab321-153">521</span><span class="sxs-lookup"><span data-stu-id="ab321-153">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: 2048
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-154">-KeyType</span><span class="sxs-lookup"><span data-stu-id="ab321-154">-KeyType</span></span>
<span data-ttu-id="ab321-155">Задает тип ключа для ключа, который служит для резервного копирования сертификата.</span><span class="sxs-lookup"><span data-stu-id="ab321-155">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="ab321-156">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ab321-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ab321-157">Корпорация</span><span class="sxs-lookup"><span data-stu-id="ab321-157">RSA</span></span>
- <span data-ttu-id="ab321-158">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="ab321-158">RSA-HSM</span></span>
- <span data-ttu-id="ab321-159">ЕС</span><span class="sxs-lookup"><span data-stu-id="ab321-159">EC</span></span>
- <span data-ttu-id="ab321-160">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="ab321-160">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-161">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="ab321-161">-KeyUsage</span></span>
<span data-ttu-id="ab321-162">Задает использование ключа в сертификате.</span><span class="sxs-lookup"><span data-stu-id="ab321-162">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-163">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ab321-163">-Name</span></span>
<span data-ttu-id="ab321-164">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="ab321-164">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-165">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab321-165">-PassThru</span></span>
<span data-ttu-id="ab321-166">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="ab321-166">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ab321-167">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ab321-167">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-168">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="ab321-168">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="ab321-169">Указывает количество дней до истечения срока действия, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="ab321-169">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-170">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="ab321-170">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="ab321-171">Указывает процент времени жизни, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="ab321-171">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-172">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="ab321-172">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="ab321-173">Указывает на то, что сертификат повторно использует ключ во время продления.</span><span class="sxs-lookup"><span data-stu-id="ab321-173">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-174">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="ab321-174">-SecretContentType</span></span>
<span data-ttu-id="ab321-175">Указывает тип контента нового секрета в новом хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="ab321-175">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="ab321-176">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ab321-176">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ab321-177">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="ab321-177">application/x-pkcs12</span></span>
- <span data-ttu-id="ab321-178">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="ab321-178">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-179">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="ab321-179">-SubjectName</span></span>
<span data-ttu-id="ab321-180">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="ab321-180">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="ab321-181">-ValidityInMonths</span></span>
<span data-ttu-id="ab321-182">Указывает число месяцев, на которое действителен сертификат.</span><span class="sxs-lookup"><span data-stu-id="ab321-182">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-183">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ab321-183">-VaultName</span></span>
<span data-ttu-id="ab321-184">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="ab321-184">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab321-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab321-185">-Confirm</span></span>
<span data-ttu-id="ab321-186">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ab321-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab321-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab321-187">-WhatIf</span></span>
<span data-ttu-id="ab321-188">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ab321-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab321-189">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ab321-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab321-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab321-190">CommonParameters</span></span>
<span data-ttu-id="ab321-191">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ab321-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab321-192">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab321-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab321-193">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ab321-193">INPUTS</span></span>

### <span data-ttu-id="ab321-194">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="ab321-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="ab321-195">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab321-195">OUTPUTS</span></span>

### <span data-ttu-id="ab321-196">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="ab321-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="ab321-197">Пуск</span><span class="sxs-lookup"><span data-stu-id="ab321-197">NOTES</span></span>

## <span data-ttu-id="ab321-198">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab321-198">RELATED LINKS</span></span>

[<span data-ttu-id="ab321-199">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="ab321-199">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="ab321-200">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="ab321-200">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

