---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificate.md
ms.openlocfilehash: 4984ce5dde65be9e715a7e34a10e5671902b53cc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911188"
---
# <span data-ttu-id="72f40-101">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="72f40-101">Add-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="72f40-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72f40-102">SYNOPSIS</span></span>
<span data-ttu-id="72f40-103">Добавляет сертификат в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="72f40-103">Adds a certificate to a key vault.</span></span>

## <span data-ttu-id="72f40-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72f40-104">SYNTAX</span></span>

```
Add-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72f40-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72f40-105">DESCRIPTION</span></span>
<span data-ttu-id="72f40-106">Командлет **Add-AzKeyVaultCertificate** запускает процесс регистрации сертификата в хранилище ключей Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="72f40-106">The **Add-AzKeyVaultCertificate** cmdlet starts the process of enrolling for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="72f40-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72f40-107">EXAMPLES</span></span>

### <span data-ttu-id="72f40-108">Пример 1: Добавление сертификата</span><span class="sxs-lookup"><span data-stu-id="72f40-108">Example 1: Add a certificate</span></span>
```
PS C:\>$Policy = New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
PS C:\> Add-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -CertificatePolicy $Policy

Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : PS C:\>Get-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : completed
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : PS C:\>Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        :
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="72f40-109">В первой команде для создания политики сертификата используется командлет New-AzKeyVaultCertificatePolicy, а затем он сохраняется в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="72f40-109">The first command uses the New-AzKeyVaultCertificatePolicy cmdlet to create a certificate policy, and then stores it in the $Policy variable.</span></span>

<span data-ttu-id="72f40-110">Вторая команда использует **Add-AzKeyVaultCertificate** , чтобы запустить процесс для создания сертификата.</span><span class="sxs-lookup"><span data-stu-id="72f40-110">The second command uses **Add-AzKeyVaultCertificate** to start the process to create a certificate.</span></span>

<span data-ttu-id="72f40-111">Третья команда использует командлет Get-AzKeyVaultCertificateOperation для опроса операции, чтобы убедиться, что она завершена.</span><span class="sxs-lookup"><span data-stu-id="72f40-111">The third command uses the Get-AzKeyVaultCertificateOperation cmdlet to poll the operation to verify that it's complete.</span></span>

<span data-ttu-id="72f40-112">В последней команде для получения сертификата используется командлет Get-AzKeyVaultCertificate.</span><span class="sxs-lookup"><span data-stu-id="72f40-112">The final command uses the Get-AzKeyVaultCertificate cmdlet to get the certificate.</span></span>

## <span data-ttu-id="72f40-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72f40-113">PARAMETERS</span></span>

### <span data-ttu-id="72f40-114">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="72f40-114">-CertificatePolicy</span></span>
<span data-ttu-id="72f40-115">Указывает объект **KeyVaultCertificatePolicy** .</span><span class="sxs-lookup"><span data-stu-id="72f40-115">Specifies a **KeyVaultCertificatePolicy** object.</span></span>

```yaml
Type: KeyVaultCertificatePolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72f40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72f40-116">-DefaultProfile</span></span>
<span data-ttu-id="72f40-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="72f40-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72f40-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="72f40-118">-Name</span></span>
<span data-ttu-id="72f40-119">Указывает имя добавляемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="72f40-119">Specifies the name of the certificate to add.</span></span>

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

### <span data-ttu-id="72f40-120">-Тег</span><span class="sxs-lookup"><span data-stu-id="72f40-120">-Tag</span></span>
<span data-ttu-id="72f40-121">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="72f40-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="72f40-122">Например:</span><span class="sxs-lookup"><span data-stu-id="72f40-122">For example:</span></span>

<span data-ttu-id="72f40-123">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="72f40-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72f40-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="72f40-124">-VaultName</span></span>
<span data-ttu-id="72f40-125">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="72f40-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="72f40-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72f40-126">-Confirm</span></span>
<span data-ttu-id="72f40-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="72f40-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72f40-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72f40-128">-WhatIf</span></span>
<span data-ttu-id="72f40-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="72f40-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72f40-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="72f40-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72f40-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72f40-131">CommonParameters</span></span>
<span data-ttu-id="72f40-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72f40-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72f40-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72f40-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72f40-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72f40-134">INPUTS</span></span>

### <span data-ttu-id="72f40-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="72f40-135">None</span></span>
<span data-ttu-id="72f40-136">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="72f40-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72f40-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72f40-137">OUTPUTS</span></span>

### <span data-ttu-id="72f40-138">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="72f40-138">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="72f40-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="72f40-139">NOTES</span></span>

## <span data-ttu-id="72f40-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72f40-140">RELATED LINKS</span></span>

[<span data-ttu-id="72f40-141">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="72f40-141">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="72f40-142">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="72f40-142">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="72f40-143">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="72f40-143">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)
