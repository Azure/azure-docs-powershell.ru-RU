---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: caa0961c1b7aebd5fd2f9883831d733a0fa69f1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567988"
---
# <span data-ttu-id="c0912-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c0912-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c0912-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0912-102">SYNOPSIS</span></span>
<span data-ttu-id="c0912-103">Создает объект политики сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="c0912-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0912-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0912-104">SYNTAX</span></span>

### <span data-ttu-id="c0912-105">SubjectName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0912-105">SubjectName (Default)</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled] [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0912-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="c0912-106">DNSNames</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0912-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0912-107">DESCRIPTION</span></span>
<span data-ttu-id="c0912-108">Командлет **New-AzureKeyVaultCertificatePolicy** создает объект политики сертификата в памяти для хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="c0912-108">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="c0912-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0912-109">EXAMPLES</span></span>

### <span data-ttu-id="c0912-110">Пример 1: Создание политики сертификата</span><span class="sxs-lookup"><span data-stu-id="c0912-110">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="c0912-111">Эта команда создает политику сертификата, действующую в течение шести месяцев, и повторно использует ключ для обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="c0912-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="c0912-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0912-112">PARAMETERS</span></span>

### <span data-ttu-id="c0912-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="c0912-113">-CertificateType</span></span>
<span data-ttu-id="c0912-114">Указывает тип сертификата для поставщика.</span><span class="sxs-lookup"><span data-stu-id="c0912-114">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0912-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0912-115">-DefaultProfile</span></span>
<span data-ttu-id="c0912-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c0912-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0912-117">-Отключено</span><span class="sxs-lookup"><span data-stu-id="c0912-117">-Disabled</span></span>
<span data-ttu-id="c0912-118">Указывает, что политика сертификата отключена.</span><span class="sxs-lookup"><span data-stu-id="c0912-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0912-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="c0912-119">-DnsName</span></span>
<span data-ttu-id="c0912-120">Указывает DNS-имена в сертификате.</span><span class="sxs-lookup"><span data-stu-id="c0912-120">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="c0912-121">-EKU</span><span class="sxs-lookup"><span data-stu-id="c0912-121">-Ekus</span></span>
<span data-ttu-id="c0912-122">Определяет использование расширенных клавиш (EKU) в сертификате.</span><span class="sxs-lookup"><span data-stu-id="c0912-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="c0912-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="c0912-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="c0912-124">Задает количество дней, по истечении которого начинается процесс автоматического уведомления.</span><span class="sxs-lookup"><span data-stu-id="c0912-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="c0912-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="c0912-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="c0912-126">Указывает процент времени жизни, после которого начинается автоматический процесс уведомления.</span><span class="sxs-lookup"><span data-stu-id="c0912-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="c0912-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="c0912-127">-IssuerName</span></span>
<span data-ttu-id="c0912-128">Указывает имя поставщика сертификата.</span><span class="sxs-lookup"><span data-stu-id="c0912-128">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="c0912-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="c0912-129">-KeyNotExportable</span></span>
<span data-ttu-id="c0912-130">Указывает на то, что ключ не может быть экспортирован.</span><span class="sxs-lookup"><span data-stu-id="c0912-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0912-131">-KeyType</span><span class="sxs-lookup"><span data-stu-id="c0912-131">-KeyType</span></span>
<span data-ttu-id="c0912-132">Задает тип ключа для ключа, который служит для резервного копирования сертификата.</span><span class="sxs-lookup"><span data-stu-id="c0912-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="c0912-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c0912-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c0912-134">Корпорация</span><span class="sxs-lookup"><span data-stu-id="c0912-134">RSA</span></span>
- <span data-ttu-id="c0912-135">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="c0912-135">RSA-HSM</span></span>

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

### <span data-ttu-id="c0912-136">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="c0912-136">-KeyUsage</span></span>
<span data-ttu-id="c0912-137">Задает использование ключа в сертификате.</span><span class="sxs-lookup"><span data-stu-id="c0912-137">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="c0912-138">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="c0912-138">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="c0912-139">Указывает количество дней до истечения срока действия, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="c0912-139">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="c0912-140">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="c0912-140">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="c0912-141">Указывает процент времени жизни, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="c0912-141">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="c0912-142">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="c0912-142">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="c0912-143">Указывает на то, что сертификат повторно использует ключ во время продления.</span><span class="sxs-lookup"><span data-stu-id="c0912-143">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0912-144">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="c0912-144">-SecretContentType</span></span>
<span data-ttu-id="c0912-145">Указывает тип контента нового секрета в новом хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="c0912-145">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="c0912-146">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c0912-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c0912-147">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="c0912-147">application/x-pkcs12</span></span>
- <span data-ttu-id="c0912-148">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="c0912-148">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0912-149">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="c0912-149">-SubjectName</span></span>
<span data-ttu-id="c0912-150">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="c0912-150">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0912-151">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="c0912-151">-ValidityInMonths</span></span>
<span data-ttu-id="c0912-152">Указывает число месяцев, на которое действителен сертификат.</span><span class="sxs-lookup"><span data-stu-id="c0912-152">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="c0912-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0912-153">-Confirm</span></span>
<span data-ttu-id="c0912-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c0912-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0912-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0912-155">-WhatIf</span></span>
<span data-ttu-id="c0912-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c0912-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0912-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c0912-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0912-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0912-158">CommonParameters</span></span>
<span data-ttu-id="c0912-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0912-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0912-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0912-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0912-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0912-161">INPUTS</span></span>

### <span data-ttu-id="c0912-162">Ничего</span><span class="sxs-lookup"><span data-stu-id="c0912-162">None</span></span>
<span data-ttu-id="c0912-163">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c0912-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c0912-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0912-164">OUTPUTS</span></span>

### <span data-ttu-id="c0912-165">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c0912-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c0912-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0912-166">NOTES</span></span>

## <span data-ttu-id="c0912-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0912-167">RELATED LINKS</span></span>

[<span data-ttu-id="c0912-168">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c0912-168">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="c0912-169">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c0912-169">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

