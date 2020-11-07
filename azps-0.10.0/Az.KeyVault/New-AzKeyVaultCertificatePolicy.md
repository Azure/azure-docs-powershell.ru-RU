---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 83eea8c8a030c5d22368bc0ede42c71e92df14a2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910291"
---
# <span data-ttu-id="c31ed-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c31ed-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c31ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c31ed-102">SYNOPSIS</span></span>
<span data-ttu-id="c31ed-103">Создает объект политики сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="c31ed-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="c31ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c31ed-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c31ed-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c31ed-105">DESCRIPTION</span></span>
<span data-ttu-id="c31ed-106">Командлет **New-AzKeyVaultCertificatePolicy** создает объект политики сертификата в памяти для хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="c31ed-106">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="c31ed-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c31ed-107">EXAMPLES</span></span>

### <span data-ttu-id="c31ed-108">Пример 1: Создание политики сертификата</span><span class="sxs-lookup"><span data-stu-id="c31ed-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="c31ed-109">Эта команда создает политику сертификата, действующую в течение шести месяцев, и повторно использует ключ для обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="c31ed-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="c31ed-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c31ed-110">PARAMETERS</span></span>

### <span data-ttu-id="c31ed-111">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="c31ed-111">-CertificateType</span></span>
<span data-ttu-id="c31ed-112">Указывает тип сертификата для поставщика.</span><span class="sxs-lookup"><span data-stu-id="c31ed-112">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="c31ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c31ed-113">-DefaultProfile</span></span>
<span data-ttu-id="c31ed-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c31ed-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c31ed-115">-Отключено</span><span class="sxs-lookup"><span data-stu-id="c31ed-115">-Disabled</span></span>
<span data-ttu-id="c31ed-116">Указывает, что политика сертификата отключена.</span><span class="sxs-lookup"><span data-stu-id="c31ed-116">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="c31ed-117">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="c31ed-117">-DnsNames</span></span>
<span data-ttu-id="c31ed-118">Указывает DNS-имена в сертификате.</span><span class="sxs-lookup"><span data-stu-id="c31ed-118">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="c31ed-119">-EKU</span><span class="sxs-lookup"><span data-stu-id="c31ed-119">-Ekus</span></span>
<span data-ttu-id="c31ed-120">Определяет использование расширенных клавиш (EKU) в сертификате.</span><span class="sxs-lookup"><span data-stu-id="c31ed-120">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="c31ed-121">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="c31ed-121">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="c31ed-122">Задает количество дней, по истечении которого начинается процесс автоматического уведомления.</span><span class="sxs-lookup"><span data-stu-id="c31ed-122">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="c31ed-123">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="c31ed-123">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="c31ed-124">Указывает процент времени жизни, после которого начинается автоматический процесс уведомления.</span><span class="sxs-lookup"><span data-stu-id="c31ed-124">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="c31ed-125">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="c31ed-125">-IssuerName</span></span>
<span data-ttu-id="c31ed-126">Указывает имя поставщика сертификата.</span><span class="sxs-lookup"><span data-stu-id="c31ed-126">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c31ed-127">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="c31ed-127">-KeyNotExportable</span></span>
<span data-ttu-id="c31ed-128">Указывает на то, что ключ не может быть экспортирован.</span><span class="sxs-lookup"><span data-stu-id="c31ed-128">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="c31ed-129">-KeyType</span><span class="sxs-lookup"><span data-stu-id="c31ed-129">-KeyType</span></span>
<span data-ttu-id="c31ed-130">Задает тип ключа для ключа, который служит для резервного копирования сертификата.</span><span class="sxs-lookup"><span data-stu-id="c31ed-130">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="c31ed-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c31ed-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c31ed-132">Корпорация</span><span class="sxs-lookup"><span data-stu-id="c31ed-132">RSA</span></span>
- <span data-ttu-id="c31ed-133">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="c31ed-133">RSA-HSM</span></span>

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

### <span data-ttu-id="c31ed-134">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="c31ed-134">-KeyUsage</span></span>
<span data-ttu-id="c31ed-135">Задает использование ключа в сертификате.</span><span class="sxs-lookup"><span data-stu-id="c31ed-135">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="c31ed-136">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="c31ed-136">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="c31ed-137">Указывает количество дней до истечения срока действия, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="c31ed-137">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="c31ed-138">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="c31ed-138">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="c31ed-139">Указывает процент времени жизни, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="c31ed-139">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="c31ed-140">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="c31ed-140">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="c31ed-141">Указывает на то, что сертификат повторно использует ключ во время продления.</span><span class="sxs-lookup"><span data-stu-id="c31ed-141">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="c31ed-142">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="c31ed-142">-SecretContentType</span></span>
<span data-ttu-id="c31ed-143">Указывает тип контента нового секрета в новом хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="c31ed-143">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="c31ed-144">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c31ed-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c31ed-145">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="c31ed-145">application/x-pkcs12</span></span>
- <span data-ttu-id="c31ed-146">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="c31ed-146">application/x-pem-file</span></span>

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

### <span data-ttu-id="c31ed-147">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="c31ed-147">-SubjectName</span></span>
<span data-ttu-id="c31ed-148">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="c31ed-148">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="c31ed-149">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="c31ed-149">-ValidityInMonths</span></span>
<span data-ttu-id="c31ed-150">Указывает число месяцев, на которое действителен сертификат.</span><span class="sxs-lookup"><span data-stu-id="c31ed-150">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="c31ed-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c31ed-151">-Confirm</span></span>
<span data-ttu-id="c31ed-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c31ed-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c31ed-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c31ed-153">-WhatIf</span></span>
<span data-ttu-id="c31ed-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c31ed-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c31ed-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c31ed-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c31ed-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c31ed-156">CommonParameters</span></span>
<span data-ttu-id="c31ed-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c31ed-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c31ed-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c31ed-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c31ed-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c31ed-159">INPUTS</span></span>

### <span data-ttu-id="c31ed-160">Ничего</span><span class="sxs-lookup"><span data-stu-id="c31ed-160">None</span></span>
<span data-ttu-id="c31ed-161">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c31ed-161">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c31ed-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c31ed-162">OUTPUTS</span></span>

### <span data-ttu-id="c31ed-163">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c31ed-163">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c31ed-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="c31ed-164">NOTES</span></span>

## <span data-ttu-id="c31ed-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c31ed-165">RELATED LINKS</span></span>

[<span data-ttu-id="c31ed-166">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c31ed-166">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="c31ed-167">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c31ed-167">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

