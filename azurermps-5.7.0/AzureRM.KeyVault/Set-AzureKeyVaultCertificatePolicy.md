---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: e960aa211b53c79087e67e2bd86504e597a718d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569011"
---
# <span data-ttu-id="3d403-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3d403-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="3d403-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d403-102">SYNOPSIS</span></span>
<span data-ttu-id="3d403-103">Создание или обновление политики сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="3d403-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d403-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d403-104">SYNTAX</span></span>

### <span data-ttu-id="3d403-105">ExpandedRenewPercentage (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3d403-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d403-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="3d403-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d403-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="3d403-107">ExpandedRenewNumber</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 -RenewAtNumberOfDaysBeforeExpiry <Int32> [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>]
 [-Disabled] [-SubjectName <String>] [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d403-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d403-108">DESCRIPTION</span></span>
<span data-ttu-id="3d403-109">Командлет **Set-AzureKeyVaultCertificatePolicy** создает или обновляет политику для сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="3d403-109">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="3d403-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d403-110">EXAMPLES</span></span>

### <span data-ttu-id="3d403-111">Пример 1: Настройка политики сертификата</span><span class="sxs-lookup"><span data-stu-id="3d403-111">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="3d403-112">Эта команда задает политику сертификата TestCert01 в хранилище ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="3d403-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="3d403-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d403-113">PARAMETERS</span></span>

### <span data-ttu-id="3d403-114">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="3d403-114">-CertificateType</span></span>
<span data-ttu-id="3d403-115">Указывает тип сертификата для поставщика.</span><span class="sxs-lookup"><span data-stu-id="3d403-115">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d403-116">-DefaultProfile</span></span>
<span data-ttu-id="3d403-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3d403-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-118">-Отключено</span><span class="sxs-lookup"><span data-stu-id="3d403-118">-Disabled</span></span>
<span data-ttu-id="3d403-119">Указывает, что политика сертификата отключена.</span><span class="sxs-lookup"><span data-stu-id="3d403-119">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-120">-DnsName</span><span class="sxs-lookup"><span data-stu-id="3d403-120">-DnsName</span></span>
<span data-ttu-id="3d403-121">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="3d403-121">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-122">-EKU</span><span class="sxs-lookup"><span data-stu-id="3d403-122">-Ekus</span></span>
<span data-ttu-id="3d403-123">Определяет использование расширенных клавиш (EKU) в сертификате.</span><span class="sxs-lookup"><span data-stu-id="3d403-123">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-124">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="3d403-124">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="3d403-125">Указывает число дней, по истечении которого служба автоматического продления подписки запускается.</span><span class="sxs-lookup"><span data-stu-id="3d403-125">Specifies the number of days before expiration when automatic renewal should start.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-126">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="3d403-126">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="3d403-127">Указывает процент времени жизни, после которого начинается автоматический процесс уведомления.</span><span class="sxs-lookup"><span data-stu-id="3d403-127">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d403-128">-InputObject</span></span>
<span data-ttu-id="3d403-129">Указывает политику сертификата.</span><span class="sxs-lookup"><span data-stu-id="3d403-129">Specifies the certificate policy.</span></span>

```yaml
Type: PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-130">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="3d403-130">-IssuerName</span></span>
<span data-ttu-id="3d403-131">Указывает имя поставщика для этого сертификата.</span><span class="sxs-lookup"><span data-stu-id="3d403-131">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-132">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="3d403-132">-KeyNotExportable</span></span>
<span data-ttu-id="3d403-133">Указывает на то, что ключ не может быть экспортирован.</span><span class="sxs-lookup"><span data-stu-id="3d403-133">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-134">-KeyType</span><span class="sxs-lookup"><span data-stu-id="3d403-134">-KeyType</span></span>
<span data-ttu-id="3d403-135">Задает тип ключа для ключа, который служит для резервного копирования сертификата.</span><span class="sxs-lookup"><span data-stu-id="3d403-135">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="3d403-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3d403-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d403-137">Корпорация</span><span class="sxs-lookup"><span data-stu-id="3d403-137">RSA</span></span>
- <span data-ttu-id="3d403-138">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="3d403-138">RSA-HSM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-139">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="3d403-139">-KeyUsage</span></span>
<span data-ttu-id="3d403-140">Задает использование ключа в сертификате.</span><span class="sxs-lookup"><span data-stu-id="3d403-140">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d403-141">-Name</span></span>
<span data-ttu-id="3d403-142">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="3d403-142">Specifies the name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d403-143">-PassThru</span></span>
<span data-ttu-id="3d403-144">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="3d403-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3d403-145">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3d403-145">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-146">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="3d403-146">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="3d403-147">Указывает количество дней до истечения срока действия, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="3d403-147">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-148">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="3d403-148">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="3d403-149">Указывает процент времени жизни, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="3d403-149">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-150">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="3d403-150">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="3d403-151">Указывает на то, что сертификат повторно использует ключ во время продления.</span><span class="sxs-lookup"><span data-stu-id="3d403-151">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-152">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="3d403-152">-SecretContentType</span></span>
<span data-ttu-id="3d403-153">Указывает тип контента нового секрета в новом хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="3d403-153">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="3d403-154">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3d403-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d403-155">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="3d403-155">application/x-pkcs12</span></span>
- <span data-ttu-id="3d403-156">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="3d403-156">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-157">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="3d403-157">-SubjectName</span></span>
<span data-ttu-id="3d403-158">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="3d403-158">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-159">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="3d403-159">-ValidityInMonths</span></span>
<span data-ttu-id="3d403-160">Указывает число месяцев, на которое действителен сертификат.</span><span class="sxs-lookup"><span data-stu-id="3d403-160">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-161">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3d403-161">-VaultName</span></span>
<span data-ttu-id="3d403-162">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3d403-162">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d403-163">-Confirm</span></span>
<span data-ttu-id="3d403-164">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3d403-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d403-165">-WhatIf</span></span>
<span data-ttu-id="3d403-166">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3d403-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d403-167">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3d403-167">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d403-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d403-168">CommonParameters</span></span>
<span data-ttu-id="3d403-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d403-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d403-170">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d403-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d403-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d403-171">INPUTS</span></span>

### <span data-ttu-id="3d403-172">Ничего</span><span class="sxs-lookup"><span data-stu-id="3d403-172">None</span></span>
<span data-ttu-id="3d403-173">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3d403-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d403-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d403-174">OUTPUTS</span></span>

### <span data-ttu-id="3d403-175">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3d403-175">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="3d403-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d403-176">NOTES</span></span>

## <span data-ttu-id="3d403-177">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d403-177">RELATED LINKS</span></span>

[<span data-ttu-id="3d403-178">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3d403-178">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="3d403-179">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3d403-179">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

