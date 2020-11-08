---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 5a6b88ce85b8b9296d9666955a93d1240b631634
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072542"
---
# <span data-ttu-id="c661a-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c661a-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c661a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c661a-102">SYNOPSIS</span></span>
<span data-ttu-id="c661a-103">Создание или обновление политики сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="c661a-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="c661a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c661a-104">SYNTAX</span></span>

### <span data-ttu-id="c661a-105">ExpandedRenewPercentage (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c661a-105">ExpandedRenewPercentage (Default)</span></span>
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

### <span data-ttu-id="c661a-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="c661a-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c661a-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="c661a-107">ExpandedRenewNumber</span></span>
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

## <span data-ttu-id="c661a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c661a-108">DESCRIPTION</span></span>
<span data-ttu-id="c661a-109">Командлет **Set-AzKeyVaultCertificatePolicy** создает или обновляет политику для сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="c661a-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="c661a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c661a-110">EXAMPLES</span></span>

### <span data-ttu-id="c661a-111">Пример 1: Настройка политики сертификата</span><span class="sxs-lookup"><span data-stu-id="c661a-111">Example 1: Set a certificate policy</span></span>
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

<span data-ttu-id="c661a-112">Эта команда задает политику сертификата TestCert01 в хранилище ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="c661a-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="c661a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c661a-113">PARAMETERS</span></span>

### <span data-ttu-id="c661a-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="c661a-114">-CertificateTransparency</span></span>
<span data-ttu-id="c661a-115">Указывает, включена ли прозрачность сертификата для этого сертификата или поставщика; Если не указано, используется значение по умолчанию "true"</span><span class="sxs-lookup"><span data-stu-id="c661a-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="c661a-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="c661a-116">-CertificateType</span></span>
<span data-ttu-id="c661a-117">Указывает тип сертификата для поставщика.</span><span class="sxs-lookup"><span data-stu-id="c661a-117">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="c661a-118">-Кривая</span><span class="sxs-lookup"><span data-stu-id="c661a-118">-Curve</span></span>
<span data-ttu-id="c661a-119">Указывает имя эллиптической кривой для ключа сертификата.</span><span class="sxs-lookup"><span data-stu-id="c661a-119">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="c661a-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c661a-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c661a-121">P-256</span><span class="sxs-lookup"><span data-stu-id="c661a-121">P-256</span></span>
- <span data-ttu-id="c661a-122">P-384</span><span class="sxs-lookup"><span data-stu-id="c661a-122">P-384</span></span>
- <span data-ttu-id="c661a-123">P-521</span><span class="sxs-lookup"><span data-stu-id="c661a-123">P-521</span></span>
- <span data-ttu-id="c661a-124">P – 256 KБ</span><span class="sxs-lookup"><span data-stu-id="c661a-124">P-256K</span></span>
- <span data-ttu-id="c661a-125">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="c661a-125">SECP256K1</span></span>

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

### <span data-ttu-id="c661a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c661a-126">-DefaultProfile</span></span>
<span data-ttu-id="c661a-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c661a-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c661a-128">-Отключено</span><span class="sxs-lookup"><span data-stu-id="c661a-128">-Disabled</span></span>
<span data-ttu-id="c661a-129">Указывает, что политика сертификата отключена.</span><span class="sxs-lookup"><span data-stu-id="c661a-129">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="c661a-130">-DnsName</span><span class="sxs-lookup"><span data-stu-id="c661a-130">-DnsName</span></span>
<span data-ttu-id="c661a-131">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="c661a-131">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="c661a-132">-EKU</span><span class="sxs-lookup"><span data-stu-id="c661a-132">-Ekus</span></span>
<span data-ttu-id="c661a-133">Определяет использование расширенных клавиш (EKU) в сертификате.</span><span class="sxs-lookup"><span data-stu-id="c661a-133">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="c661a-134">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="c661a-134">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="c661a-135">Указывает число дней, по истечении которого служба автоматического продления подписки запускается.</span><span class="sxs-lookup"><span data-stu-id="c661a-135">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="c661a-136">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="c661a-136">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="c661a-137">Указывает процент времени жизни, после которого начинается автоматический процесс уведомления.</span><span class="sxs-lookup"><span data-stu-id="c661a-137">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="c661a-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c661a-138">-InputObject</span></span>
<span data-ttu-id="c661a-139">Указывает политику сертификата.</span><span class="sxs-lookup"><span data-stu-id="c661a-139">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="c661a-140">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="c661a-140">-IssuerName</span></span>
<span data-ttu-id="c661a-141">Указывает имя поставщика для этого сертификата.</span><span class="sxs-lookup"><span data-stu-id="c661a-141">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="c661a-142">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="c661a-142">-KeyNotExportable</span></span>
<span data-ttu-id="c661a-143">Указывает на то, что ключ не может быть экспортирован.</span><span class="sxs-lookup"><span data-stu-id="c661a-143">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="c661a-144">-KeySize</span><span class="sxs-lookup"><span data-stu-id="c661a-144">-KeySize</span></span>
<span data-ttu-id="c661a-145">Задает размер ключа сертификата.</span><span class="sxs-lookup"><span data-stu-id="c661a-145">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="c661a-146">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c661a-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c661a-147">2048</span><span class="sxs-lookup"><span data-stu-id="c661a-147">2048</span></span>
- <span data-ttu-id="c661a-148">3072</span><span class="sxs-lookup"><span data-stu-id="c661a-148">3072</span></span>
- <span data-ttu-id="c661a-149">4096</span><span class="sxs-lookup"><span data-stu-id="c661a-149">4096</span></span>
- <span data-ttu-id="c661a-150">256</span><span class="sxs-lookup"><span data-stu-id="c661a-150">256</span></span>
- <span data-ttu-id="c661a-151">384</span><span class="sxs-lookup"><span data-stu-id="c661a-151">384</span></span>
- <span data-ttu-id="c661a-152">521</span><span class="sxs-lookup"><span data-stu-id="c661a-152">521</span></span>

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

### <span data-ttu-id="c661a-153">-KeyType</span><span class="sxs-lookup"><span data-stu-id="c661a-153">-KeyType</span></span>
<span data-ttu-id="c661a-154">Задает тип ключа для ключа, который служит для резервного копирования сертификата.</span><span class="sxs-lookup"><span data-stu-id="c661a-154">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="c661a-155">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c661a-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c661a-156">Корпорация</span><span class="sxs-lookup"><span data-stu-id="c661a-156">RSA</span></span>
- <span data-ttu-id="c661a-157">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="c661a-157">RSA-HSM</span></span>
- <span data-ttu-id="c661a-158">ЕС</span><span class="sxs-lookup"><span data-stu-id="c661a-158">EC</span></span>
- <span data-ttu-id="c661a-159">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="c661a-159">EC-HSM</span></span>

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

### <span data-ttu-id="c661a-160">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="c661a-160">-KeyUsage</span></span>
<span data-ttu-id="c661a-161">Задает использование ключа в сертификате.</span><span class="sxs-lookup"><span data-stu-id="c661a-161">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="c661a-162">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c661a-162">-Name</span></span>
<span data-ttu-id="c661a-163">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="c661a-163">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="c661a-164">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c661a-164">-PassThru</span></span>
<span data-ttu-id="c661a-165">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="c661a-165">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c661a-166">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c661a-166">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c661a-167">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="c661a-167">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="c661a-168">Указывает количество дней до истечения срока действия, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="c661a-168">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="c661a-169">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="c661a-169">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="c661a-170">Указывает процент времени жизни, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="c661a-170">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="c661a-171">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="c661a-171">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="c661a-172">Указывает на то, что сертификат повторно использует ключ во время продления.</span><span class="sxs-lookup"><span data-stu-id="c661a-172">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="c661a-173">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="c661a-173">-SecretContentType</span></span>
<span data-ttu-id="c661a-174">Указывает тип контента нового секрета в новом хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="c661a-174">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="c661a-175">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c661a-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c661a-176">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="c661a-176">application/x-pkcs12</span></span>
- <span data-ttu-id="c661a-177">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="c661a-177">application/x-pem-file</span></span>

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

### <span data-ttu-id="c661a-178">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="c661a-178">-SubjectName</span></span>
<span data-ttu-id="c661a-179">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="c661a-179">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="c661a-180">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="c661a-180">-ValidityInMonths</span></span>
<span data-ttu-id="c661a-181">Указывает число месяцев, на которое действителен сертификат.</span><span class="sxs-lookup"><span data-stu-id="c661a-181">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="c661a-182">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c661a-182">-VaultName</span></span>
<span data-ttu-id="c661a-183">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="c661a-183">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="c661a-184">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c661a-184">-Confirm</span></span>
<span data-ttu-id="c661a-185">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c661a-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c661a-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c661a-186">-WhatIf</span></span>
<span data-ttu-id="c661a-187">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c661a-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c661a-188">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c661a-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c661a-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c661a-189">CommonParameters</span></span>
<span data-ttu-id="c661a-190">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c661a-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c661a-191">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c661a-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c661a-192">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c661a-192">INPUTS</span></span>

### <span data-ttu-id="c661a-193">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c661a-193">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c661a-194">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c661a-194">OUTPUTS</span></span>

### <span data-ttu-id="c661a-195">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c661a-195">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c661a-196">Пуск</span><span class="sxs-lookup"><span data-stu-id="c661a-196">NOTES</span></span>

## <span data-ttu-id="c661a-197">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c661a-197">RELATED LINKS</span></span>

[<span data-ttu-id="c661a-198">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c661a-198">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="c661a-199">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c661a-199">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

