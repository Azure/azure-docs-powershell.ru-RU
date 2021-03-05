---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 09e58a029d3011c2abcee035ee23640f801825b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970696"
---
# <span data-ttu-id="da8a7-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="da8a7-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="da8a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da8a7-102">SYNOPSIS</span></span>
<span data-ttu-id="da8a7-103">Создает или обновляет политику для сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="da8a7-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="da8a7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="da8a7-104">SYNTAX</span></span>

### <span data-ttu-id="da8a7-105">ExpandedRenewPercentage (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da8a7-105">ExpandedRenewPercentage (Default)</span></span>
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

### <span data-ttu-id="da8a7-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="da8a7-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da8a7-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="da8a7-107">ExpandedRenewNumber</span></span>
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

## <span data-ttu-id="da8a7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da8a7-108">DESCRIPTION</span></span>
<span data-ttu-id="da8a7-109">Для сертификата в хранилище ключей создается или обновляется политика **Set-AzKeyVaultCertificatePolicy.**</span><span class="sxs-lookup"><span data-stu-id="da8a7-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="da8a7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="da8a7-110">EXAMPLES</span></span>

### <span data-ttu-id="da8a7-111">Пример 1. Настройка политики сертификатов</span><span class="sxs-lookup"><span data-stu-id="da8a7-111">Example 1: Set a certificate policy</span></span>
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

<span data-ttu-id="da8a7-112">Эта команда задает политику для сертификата TestCert01 в хранилище ключа ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="da8a7-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="da8a7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da8a7-113">PARAMETERS</span></span>

### <span data-ttu-id="da8a7-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="da8a7-114">-CertificateTransparency</span></span>
<span data-ttu-id="da8a7-115">Указывает, включена ли прозрачность сертификата для этого сертификата или выпуска; если не указано, по умолчанию задано значение true.</span><span class="sxs-lookup"><span data-stu-id="da8a7-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'.</span></span>
<span data-ttu-id="da8a7-116">`-IssuerName` при настройке этого свойства.</span><span class="sxs-lookup"><span data-stu-id="da8a7-116">`-IssuerName` needs to be specified when setting this property.</span></span>

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

### <span data-ttu-id="da8a7-117">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="da8a7-117">-CertificateType</span></span>
<span data-ttu-id="da8a7-118">Тип сертификата для выпуска.</span><span class="sxs-lookup"><span data-stu-id="da8a7-118">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="da8a7-119">-Кривая</span><span class="sxs-lookup"><span data-stu-id="da8a7-119">-Curve</span></span>
<span data-ttu-id="da8a7-120">Указывает название многоliptic curve ключа сертификата.</span><span class="sxs-lookup"><span data-stu-id="da8a7-120">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="da8a7-121">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="da8a7-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da8a7-122">P-256</span><span class="sxs-lookup"><span data-stu-id="da8a7-122">P-256</span></span>
- <span data-ttu-id="da8a7-123">P-384</span><span class="sxs-lookup"><span data-stu-id="da8a7-123">P-384</span></span>
- <span data-ttu-id="da8a7-124">P-521</span><span class="sxs-lookup"><span data-stu-id="da8a7-124">P-521</span></span>
- <span data-ttu-id="da8a7-125">P-256K</span><span class="sxs-lookup"><span data-stu-id="da8a7-125">P-256K</span></span>
- <span data-ttu-id="da8a7-126">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="da8a7-126">SECP256K1</span></span>

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

### <span data-ttu-id="da8a7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da8a7-127">-DefaultProfile</span></span>
<span data-ttu-id="da8a7-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="da8a7-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da8a7-129">-Disabled</span><span class="sxs-lookup"><span data-stu-id="da8a7-129">-Disabled</span></span>
<span data-ttu-id="da8a7-130">Указывает на то, что политика сертификата отключена.</span><span class="sxs-lookup"><span data-stu-id="da8a7-130">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="da8a7-131">-DnsName</span><span class="sxs-lookup"><span data-stu-id="da8a7-131">-DnsName</span></span>
<span data-ttu-id="da8a7-132">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="da8a7-132">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="da8a7-133">-Ekus</span><span class="sxs-lookup"><span data-stu-id="da8a7-133">-Ekus</span></span>
<span data-ttu-id="da8a7-134">Указывает расширенные возможности использования ключей (EKUs) в сертификате.</span><span class="sxs-lookup"><span data-stu-id="da8a7-134">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="da8a7-135">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="da8a7-135">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="da8a7-136">Количество дней до окончания срока действия, в течение чего должно начаться автоматическое продление.</span><span class="sxs-lookup"><span data-stu-id="da8a7-136">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="da8a7-137">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="da8a7-137">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="da8a7-138">Указывает процент времени существования, после которого начнется автоматическая обработка уведомления.</span><span class="sxs-lookup"><span data-stu-id="da8a7-138">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="da8a7-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da8a7-139">-InputObject</span></span>
<span data-ttu-id="da8a7-140">Политика сертификатов.</span><span class="sxs-lookup"><span data-stu-id="da8a7-140">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="da8a7-141">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="da8a7-141">-IssuerName</span></span>
<span data-ttu-id="da8a7-142">Указывает имя выпуска для этого сертификата.</span><span class="sxs-lookup"><span data-stu-id="da8a7-142">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="da8a7-143">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="da8a7-143">-KeyNotExportable</span></span>
<span data-ttu-id="da8a7-144">Указывает на то, что ключ не экспортируется.</span><span class="sxs-lookup"><span data-stu-id="da8a7-144">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="da8a7-145">-KeySize</span><span class="sxs-lookup"><span data-stu-id="da8a7-145">-KeySize</span></span>
<span data-ttu-id="da8a7-146">Определяет размер ключа сертификата.</span><span class="sxs-lookup"><span data-stu-id="da8a7-146">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="da8a7-147">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="da8a7-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da8a7-148">2048</span><span class="sxs-lookup"><span data-stu-id="da8a7-148">2048</span></span>
- <span data-ttu-id="da8a7-149">3072</span><span class="sxs-lookup"><span data-stu-id="da8a7-149">3072</span></span>
- <span data-ttu-id="da8a7-150">4096</span><span class="sxs-lookup"><span data-stu-id="da8a7-150">4096</span></span>
- <span data-ttu-id="da8a7-151">256</span><span class="sxs-lookup"><span data-stu-id="da8a7-151">256</span></span>
- <span data-ttu-id="da8a7-152">384</span><span class="sxs-lookup"><span data-stu-id="da8a7-152">384</span></span>
- <span data-ttu-id="da8a7-153">521</span><span class="sxs-lookup"><span data-stu-id="da8a7-153">521</span></span>

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

### <span data-ttu-id="da8a7-154">-KeyType</span><span class="sxs-lookup"><span data-stu-id="da8a7-154">-KeyType</span></span>
<span data-ttu-id="da8a7-155">Определяет тип ключа, который будет возвращать сертификат.</span><span class="sxs-lookup"><span data-stu-id="da8a7-155">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="da8a7-156">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="da8a7-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da8a7-157">RSA</span><span class="sxs-lookup"><span data-stu-id="da8a7-157">RSA</span></span>
- <span data-ttu-id="da8a7-158">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="da8a7-158">RSA-HSM</span></span>
- <span data-ttu-id="da8a7-159">EC</span><span class="sxs-lookup"><span data-stu-id="da8a7-159">EC</span></span>
- <span data-ttu-id="da8a7-160">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="da8a7-160">EC-HSM</span></span>

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

### <span data-ttu-id="da8a7-161">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="da8a7-161">-KeyUsage</span></span>
<span data-ttu-id="da8a7-162">Указывает использование ключа в сертификате.</span><span class="sxs-lookup"><span data-stu-id="da8a7-162">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="da8a7-163">-Name</span><span class="sxs-lookup"><span data-stu-id="da8a7-163">-Name</span></span>
<span data-ttu-id="da8a7-164">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="da8a7-164">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="da8a7-165">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da8a7-165">-PassThru</span></span>
<span data-ttu-id="da8a7-166">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="da8a7-166">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="da8a7-167">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="da8a7-167">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="da8a7-168">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="da8a7-168">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="da8a7-169">Количество дней до окончания срока действия, после которого начнется автоматическая процедура продления сертификата.</span><span class="sxs-lookup"><span data-stu-id="da8a7-169">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="da8a7-170">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="da8a7-170">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="da8a7-171">Указывает процент времени существования, после которого начнется автоматическая процедура продления сертификата.</span><span class="sxs-lookup"><span data-stu-id="da8a7-171">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="da8a7-172">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="da8a7-172">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="da8a7-173">Указывает на повторное использование ключа сертификатом во время продления.</span><span class="sxs-lookup"><span data-stu-id="da8a7-173">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="da8a7-174">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="da8a7-174">-SecretContentType</span></span>
<span data-ttu-id="da8a7-175">Определяет тип контента нового секретного сейфа.</span><span class="sxs-lookup"><span data-stu-id="da8a7-175">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="da8a7-176">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="da8a7-176">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da8a7-177">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="da8a7-177">application/x-pkcs12</span></span>
- <span data-ttu-id="da8a7-178">application/x-pem-file</span><span class="sxs-lookup"><span data-stu-id="da8a7-178">application/x-pem-file</span></span>

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

### <span data-ttu-id="da8a7-179">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="da8a7-179">-SubjectName</span></span>
<span data-ttu-id="da8a7-180">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="da8a7-180">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="da8a7-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="da8a7-181">-ValidityInMonths</span></span>
<span data-ttu-id="da8a7-182">Указывает, на определенное количество месяцев действителен сертификат.</span><span class="sxs-lookup"><span data-stu-id="da8a7-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="da8a7-183">-VaultName</span><span class="sxs-lookup"><span data-stu-id="da8a7-183">-VaultName</span></span>
<span data-ttu-id="da8a7-184">Указывает имя сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="da8a7-184">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="da8a7-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da8a7-185">-Confirm</span></span>
<span data-ttu-id="da8a7-186">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da8a7-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da8a7-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da8a7-187">-WhatIf</span></span>
<span data-ttu-id="da8a7-188">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da8a7-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da8a7-189">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="da8a7-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da8a7-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da8a7-190">CommonParameters</span></span>
<span data-ttu-id="da8a7-191">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da8a7-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da8a7-192">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da8a7-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da8a7-193">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da8a7-193">INPUTS</span></span>

### <span data-ttu-id="da8a7-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="da8a7-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="da8a7-195">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="da8a7-195">OUTPUTS</span></span>

### <span data-ttu-id="da8a7-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="da8a7-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="da8a7-197">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="da8a7-197">NOTES</span></span>

## <span data-ttu-id="da8a7-198">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da8a7-198">RELATED LINKS</span></span>

[<span data-ttu-id="da8a7-199">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="da8a7-199">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="da8a7-200">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="da8a7-200">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

