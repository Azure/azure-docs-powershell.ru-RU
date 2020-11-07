---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 160c98b141dbde36786404b58c694772dc86d323
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911157"
---
# <span data-ttu-id="4ce3a-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4ce3a-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4ce3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ce3a-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce3a-103">Создание или обновление политики сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="4ce3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ce3a-104">SYNTAX</span></span>

### <span data-ttu-id="4ce3a-105">Развернуто (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ce3a-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-SecretContentType <String>]
 [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ce3a-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="4ce3a-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ce3a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ce3a-107">DESCRIPTION</span></span>
<span data-ttu-id="4ce3a-108">Командлет **Set-AzKeyVaultCertificatePolicy** создает или обновляет политику для сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-108">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="4ce3a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ce3a-109">EXAMPLES</span></span>

### <span data-ttu-id="4ce3a-110">Пример 1: Настройка политики сертификата</span><span class="sxs-lookup"><span data-stu-id="4ce3a-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="4ce3a-111">Эта команда задает политику сертификата TestCert01 в хранилище ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="4ce3a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ce3a-112">PARAMETERS</span></span>

### <span data-ttu-id="4ce3a-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4ce3a-113">-CertificatePolicy</span></span>
<span data-ttu-id="4ce3a-114">Указывает политику сертификата.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-114">Specifies the certificate policy.</span></span>

```yaml
Type: KeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce3a-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="4ce3a-115">-CertificateType</span></span>
<span data-ttu-id="4ce3a-116">Указывает тип сертификата для поставщика.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce3a-117">-DefaultProfile</span></span>
<span data-ttu-id="4ce3a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4ce3a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ce3a-119">-Отключено</span><span class="sxs-lookup"><span data-stu-id="4ce3a-119">-Disabled</span></span>
<span data-ttu-id="4ce3a-120">Указывает, что политика сертификата отключена.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-120">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce3a-121">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="4ce3a-121">-DnsNames</span></span>
<span data-ttu-id="4ce3a-122">Указывает DNS-имена в сертификате.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-122">Specifies the DNS names in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce3a-123">-EKU</span><span class="sxs-lookup"><span data-stu-id="4ce3a-123">-Ekus</span></span>
<span data-ttu-id="4ce3a-124">Определяет использование расширенных клавиш (EKU) в сертификате.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-124">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce3a-125">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="4ce3a-125">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="4ce3a-126">Задает количество дней, по истечении которого начинается процесс автоматического уведомления.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-126">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="4ce3a-127">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="4ce3a-127">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="4ce3a-128">Указывает процент времени жизни, после которого начинается автоматический процесс уведомления.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-128">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="4ce3a-129">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="4ce3a-129">-IssuerName</span></span>
<span data-ttu-id="4ce3a-130">Указывает имя поставщика для этого сертификата.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-130">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce3a-131">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="4ce3a-131">-KeyNotExportable</span></span>
<span data-ttu-id="4ce3a-132">Указывает на то, что ключ не может быть экспортирован.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-132">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce3a-133">-KeyType</span><span class="sxs-lookup"><span data-stu-id="4ce3a-133">-KeyType</span></span>
<span data-ttu-id="4ce3a-134">Задает тип ключа для ключа, который служит для резервного копирования сертификата.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-134">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="4ce3a-135">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4ce3a-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4ce3a-136">Корпорация</span><span class="sxs-lookup"><span data-stu-id="4ce3a-136">RSA</span></span>
- <span data-ttu-id="4ce3a-137">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="4ce3a-137">RSA-HSM</span></span>

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

### <span data-ttu-id="4ce3a-138">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="4ce3a-138">-KeyUsage</span></span>
<span data-ttu-id="4ce3a-139">Задает использование ключа в сертификате.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-139">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce3a-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4ce3a-140">-Name</span></span>
<span data-ttu-id="4ce3a-141">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-141">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="4ce3a-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ce3a-142">-PassThru</span></span>
<span data-ttu-id="4ce3a-143">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4ce3a-144">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4ce3a-145">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="4ce3a-145">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="4ce3a-146">Указывает количество дней до истечения срока действия, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-146">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce3a-147">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="4ce3a-147">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="4ce3a-148">Указывает процент времени жизни, после которого начинается автоматический процесс обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-148">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce3a-149">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="4ce3a-149">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="4ce3a-150">Указывает на то, что сертификат повторно использует ключ во время продления.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-150">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce3a-151">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="4ce3a-151">-SecretContentType</span></span>
<span data-ttu-id="4ce3a-152">Указывает тип контента нового секрета в новом хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-152">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="4ce3a-153">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4ce3a-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4ce3a-154">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="4ce3a-154">application/x-pkcs12</span></span>
- <span data-ttu-id="4ce3a-155">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="4ce3a-155">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce3a-156">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="4ce3a-156">-SubjectName</span></span>
<span data-ttu-id="4ce3a-157">Указывает имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-157">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce3a-158">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="4ce3a-158">-ValidityInMonths</span></span>
<span data-ttu-id="4ce3a-159">Указывает число месяцев, на которое действителен сертификат.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-159">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce3a-160">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4ce3a-160">-VaultName</span></span>
<span data-ttu-id="4ce3a-161">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-161">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="4ce3a-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ce3a-162">-Confirm</span></span>
<span data-ttu-id="4ce3a-163">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ce3a-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ce3a-164">-WhatIf</span></span>
<span data-ttu-id="4ce3a-165">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ce3a-166">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ce3a-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce3a-167">CommonParameters</span></span>
<span data-ttu-id="4ce3a-168">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce3a-169">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ce3a-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce3a-170">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ce3a-170">INPUTS</span></span>

### <span data-ttu-id="4ce3a-171">Ничего</span><span class="sxs-lookup"><span data-stu-id="4ce3a-171">None</span></span>
<span data-ttu-id="4ce3a-172">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4ce3a-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4ce3a-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ce3a-173">OUTPUTS</span></span>

### <span data-ttu-id="4ce3a-174">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4ce3a-174">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4ce3a-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ce3a-175">NOTES</span></span>

## <span data-ttu-id="4ce3a-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ce3a-176">RELATED LINKS</span></span>

[<span data-ttu-id="4ce3a-177">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4ce3a-177">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="4ce3a-178">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4ce3a-178">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

