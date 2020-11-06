---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 381ce302a8404c0bb643db0fc82e392fe53d956a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559760"
---
# <span data-ttu-id="5cff5-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5cff5-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="5cff5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5cff5-102">SYNOPSIS</span></span>
<span data-ttu-id="5cff5-103">Создает объект политики сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="5cff5-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cff5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5cff5-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cff5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cff5-105">DESCRIPTION</span></span>
<span data-ttu-id="5cff5-106">Командлет **New-AzureKeyVaultCertificatePolicy** создает объект политики сертификата в памяти для хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="5cff5-106">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="5cff5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5cff5-107">EXAMPLES</span></span>

### <span data-ttu-id="5cff5-108">Пример 1: Создание политики сертификата</span><span class="sxs-lookup"><span data-stu-id="5cff5-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="5cff5-109">Эта команда создает политику сертификата, действующую в течение шести месяцев, и повторно использует ключ для обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="5cff5-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="5cff5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5cff5-110">PARAMETERS</span></span>

### <span data-ttu-id="5cff5-111">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="5cff5-111">-CertificateType</span></span>
<span data-ttu-id="5cff5-112">Указывает тип сертификата для поставщика.</span><span class="sxs-lookup"><span data-stu-id="5cff5-112">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="5cff5-113">-Отключено</span><span class="sxs-lookup"><span data-stu-id="5cff5-113">-Disabled</span></span>
<span data-ttu-id="5cff5-114">Указывает, что политика сертификата отключена.</span><span class="sxs-lookup"><span data-stu-id="5cff5-114">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="5cff5-115">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="5cff5-115">-DnsNames</span></span>
<span data-ttu-id="5cff5-116">Указывает DNS-имена в сертификате.</span><span class="sxs-lookup"><span data-stu-id="5cff5-116">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="5cff5-117">-EKU</span><span class="sxs-lookup"><span data-stu-id="5cff5-117">-Ekus</span></span>
<span data-ttu-id="5cff5-118">Определяет использование расширенных клавиш (EKU) в сертификате.</span><span class="sxs-lookup"><span data-stu-id="5cff5-118">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="5cff5-119">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="5cff5-119">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="5cff5-120">Задает количество дней, по истечении которого начинается процесс автоматического уведомления.</span><span class="sxs-lookup"><span data-stu-id="5cff5-120">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="5cff5-121">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="5cff5-121">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="5cff5-122">Указывает процент времени жизни, после которого начинается автоматический процесс уведомления.</span><span class="sxs-lookup"><span data-stu-id="5cff5-122">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="5cff5-123">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="5cff5-123">-IssuerName</span></span>
<span data-ttu-id="5cff5-124">Указывает имя поставщика сертификата.</span><span class="sxs-lookup"><span data-stu-id="5cff5-124">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cff5-125">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="5cff5-125">-KeyNotExportable</span></span>
<span data-ttu-id="5cff5-126">Указывает на то, что ключ не может быть экспортирован.</span><span class="sxs-lookup"><span data-stu-id="5cff5-126">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="5cff5-127">-KeyType</span><span class="sxs-lookup"><span data-stu-id="5cff5-127">-KeyType</span></span>
<span data-ttu-id="5cff5-128">Задает тип ключа для ключа, который служит для резервного копирования сертификата.</span><span class="sxs-lookup"><span data-stu-id="5cff5-128">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="5cff5-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5cff5-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5cff5-130">Корпорация</span><span class="sxs-lookup"><span data-stu-id="5cff5-130">RSA</span></span>
- <span data-ttu-id="5cff5-131">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="5cff5-131">RSA-HSM</span></span>

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

### <span data-ttu-id="5cff5-132">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="5cff5-132">-KeyUsage</span></span>
<span data-ttu-id="5cff5-133">Задает использование ключа в сертификате.</span><span class="sxs-lookup"><span data-stu-id="5cff5-133">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="5cff5-134">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="5cff5-134">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="5cff5-135">Указывает количество дней до истечения срока действия, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="5cff5-135">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="5cff5-136">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="5cff5-136">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="5cff5-137">Указывает процент времени жизни, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="5cff5-137">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="5cff5-138">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="5cff5-138">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="5cff5-139">Указывает на то, что сертификат повторно использует ключ во время продления.</span><span class="sxs-lookup"><span data-stu-id="5cff5-139">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="5cff5-140">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="5cff5-140">-SecretContentType</span></span>
<span data-ttu-id="5cff5-141">Указывает тип контента нового секрета в новом хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="5cff5-141">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="5cff5-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5cff5-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5cff5-143">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="5cff5-143">application/x-pkcs12</span></span>
- <span data-ttu-id="5cff5-144">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="5cff5-144">application/x-pem-file</span></span>

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

### <span data-ttu-id="5cff5-145">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="5cff5-145">-SubjectName</span></span>
<span data-ttu-id="5cff5-146">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="5cff5-146">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="5cff5-147">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="5cff5-147">-ValidityInMonths</span></span>
<span data-ttu-id="5cff5-148">Указывает число месяцев, на которое действителен сертификат.</span><span class="sxs-lookup"><span data-stu-id="5cff5-148">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="5cff5-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cff5-149">-Confirm</span></span>
<span data-ttu-id="5cff5-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5cff5-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cff5-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cff5-151">-WhatIf</span></span>
<span data-ttu-id="5cff5-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5cff5-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cff5-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5cff5-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cff5-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cff5-154">-DefaultProfile</span></span>
<span data-ttu-id="5cff5-155">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5cff5-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cff5-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cff5-156">CommonParameters</span></span>
<span data-ttu-id="5cff5-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5cff5-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cff5-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cff5-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cff5-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5cff5-159">INPUTS</span></span>

## <span data-ttu-id="5cff5-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cff5-160">OUTPUTS</span></span>

### <span data-ttu-id="5cff5-161">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5cff5-161">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="5cff5-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="5cff5-162">NOTES</span></span>

## <span data-ttu-id="5cff5-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5cff5-163">RELATED LINKS</span></span>

[<span data-ttu-id="5cff5-164">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5cff5-164">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="5cff5-165">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5cff5-165">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

