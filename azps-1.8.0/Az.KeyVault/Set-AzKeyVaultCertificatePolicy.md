---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: eec95cd9c7873d26f88390c5a623a6af40991dfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900118"
---
# <span data-ttu-id="6e166-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6e166-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="6e166-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e166-102">SYNOPSIS</span></span>
<span data-ttu-id="6e166-103">Создание или обновление политики сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="6e166-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="6e166-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e166-104">SYNTAX</span></span>

### <span data-ttu-id="6e166-105">ExpandedRenewPercentage (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6e166-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e166-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="6e166-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e166-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="6e166-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e166-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e166-108">DESCRIPTION</span></span>
<span data-ttu-id="6e166-109">Командлет **Set-AzKeyVaultCertificatePolicy** создает или обновляет политику для сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="6e166-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="6e166-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e166-110">EXAMPLES</span></span>

### <span data-ttu-id="6e166-111">Пример 1: Настройка политики сертификата</span><span class="sxs-lookup"><span data-stu-id="6e166-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="6e166-112">Эта команда задает политику сертификата TestCert01 в хранилище ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="6e166-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="6e166-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e166-113">PARAMETERS</span></span>

### <span data-ttu-id="6e166-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="6e166-114">-CertificateTransparency</span></span>
<span data-ttu-id="6e166-115">Указывает, включена ли прозрачность сертификата для этого сертификата или поставщика; Если не указано, используется значение по умолчанию "true"</span><span class="sxs-lookup"><span data-stu-id="6e166-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="6e166-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="6e166-116">-CertificateType</span></span>
<span data-ttu-id="6e166-117">Указывает тип сертификата для поставщика.</span><span class="sxs-lookup"><span data-stu-id="6e166-117">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="6e166-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e166-118">-DefaultProfile</span></span>
<span data-ttu-id="6e166-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6e166-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e166-120">-Отключено</span><span class="sxs-lookup"><span data-stu-id="6e166-120">-Disabled</span></span>
<span data-ttu-id="6e166-121">Указывает, что политика сертификата отключена.</span><span class="sxs-lookup"><span data-stu-id="6e166-121">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="6e166-122">-DnsName</span><span class="sxs-lookup"><span data-stu-id="6e166-122">-DnsName</span></span>
<span data-ttu-id="6e166-123">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="6e166-123">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="6e166-124">-EKU</span><span class="sxs-lookup"><span data-stu-id="6e166-124">-Ekus</span></span>
<span data-ttu-id="6e166-125">Определяет использование расширенных клавиш (EKU) в сертификате.</span><span class="sxs-lookup"><span data-stu-id="6e166-125">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="6e166-126">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="6e166-126">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="6e166-127">Указывает число дней, по истечении которого служба автоматического продления подписки запускается.</span><span class="sxs-lookup"><span data-stu-id="6e166-127">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="6e166-128">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="6e166-128">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="6e166-129">Указывает процент времени жизни, после которого начинается автоматический процесс уведомления.</span><span class="sxs-lookup"><span data-stu-id="6e166-129">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="6e166-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e166-130">-InputObject</span></span>
<span data-ttu-id="6e166-131">Указывает политику сертификата.</span><span class="sxs-lookup"><span data-stu-id="6e166-131">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="6e166-132">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="6e166-132">-IssuerName</span></span>
<span data-ttu-id="6e166-133">Указывает имя поставщика для этого сертификата.</span><span class="sxs-lookup"><span data-stu-id="6e166-133">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="6e166-134">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="6e166-134">-KeyNotExportable</span></span>
<span data-ttu-id="6e166-135">Указывает на то, что ключ не может быть экспортирован.</span><span class="sxs-lookup"><span data-stu-id="6e166-135">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="6e166-136">-KeyType</span><span class="sxs-lookup"><span data-stu-id="6e166-136">-KeyType</span></span>
<span data-ttu-id="6e166-137">Задает тип ключа для ключа, который служит для резервного копирования сертификата.</span><span class="sxs-lookup"><span data-stu-id="6e166-137">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="6e166-138">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6e166-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6e166-139">Корпорация</span><span class="sxs-lookup"><span data-stu-id="6e166-139">RSA</span></span>
- <span data-ttu-id="6e166-140">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="6e166-140">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e166-141">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="6e166-141">-KeyUsage</span></span>
<span data-ttu-id="6e166-142">Задает использование ключа в сертификате.</span><span class="sxs-lookup"><span data-stu-id="6e166-142">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="6e166-143">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6e166-143">-Name</span></span>
<span data-ttu-id="6e166-144">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="6e166-144">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="6e166-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e166-145">-PassThru</span></span>
<span data-ttu-id="6e166-146">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="6e166-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6e166-147">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6e166-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6e166-148">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="6e166-148">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="6e166-149">Указывает количество дней до истечения срока действия, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="6e166-149">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="6e166-150">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="6e166-150">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="6e166-151">Указывает процент времени жизни, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="6e166-151">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="6e166-152">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="6e166-152">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="6e166-153">Указывает на то, что сертификат повторно использует ключ во время продления.</span><span class="sxs-lookup"><span data-stu-id="6e166-153">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="6e166-154">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="6e166-154">-SecretContentType</span></span>
<span data-ttu-id="6e166-155">Указывает тип контента нового секрета в новом хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="6e166-155">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="6e166-156">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6e166-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6e166-157">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="6e166-157">application/x-pkcs12</span></span>
- <span data-ttu-id="6e166-158">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="6e166-158">application/x-pem-file</span></span>

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

### <span data-ttu-id="6e166-159">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="6e166-159">-SubjectName</span></span>
<span data-ttu-id="6e166-160">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="6e166-160">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="6e166-161">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="6e166-161">-ValidityInMonths</span></span>
<span data-ttu-id="6e166-162">Указывает число месяцев, на которое действителен сертификат.</span><span class="sxs-lookup"><span data-stu-id="6e166-162">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="6e166-163">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6e166-163">-VaultName</span></span>
<span data-ttu-id="6e166-164">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="6e166-164">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="6e166-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e166-165">-Confirm</span></span>
<span data-ttu-id="6e166-166">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6e166-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e166-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e166-167">-WhatIf</span></span>
<span data-ttu-id="6e166-168">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6e166-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e166-169">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6e166-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e166-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e166-170">CommonParameters</span></span>
<span data-ttu-id="6e166-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e166-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e166-172">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e166-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e166-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e166-173">INPUTS</span></span>

### <span data-ttu-id="6e166-174">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6e166-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="6e166-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e166-175">OUTPUTS</span></span>

### <span data-ttu-id="6e166-176">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6e166-176">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="6e166-177">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e166-177">NOTES</span></span>

## <span data-ttu-id="6e166-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e166-178">RELATED LINKS</span></span>

[<span data-ttu-id="6e166-179">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6e166-179">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="6e166-180">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6e166-180">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

