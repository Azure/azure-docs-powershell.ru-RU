---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 89299823-3382-402D-9458-519466748051
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: e94a93be6070a6800ef7528004d8b64ab28fc6fd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913358"
---
# <span data-ttu-id="82f80-101">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="82f80-101">Add-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="82f80-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82f80-102">SYNOPSIS</span></span>
<span data-ttu-id="82f80-103">Добавляет сертификат в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="82f80-103">Adds a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82f80-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82f80-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82f80-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82f80-105">DESCRIPTION</span></span>
<span data-ttu-id="82f80-106">Командлет **Add-AzureKeyVaultCertificate** запускает процесс регистрации сертификата в хранилище ключей Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="82f80-106">The **Add-AzureKeyVaultCertificate** cmdlet starts the process of enrolling for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="82f80-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82f80-107">EXAMPLES</span></span>

### <span data-ttu-id="82f80-108">Пример 1: Добавление сертификата</span><span class="sxs-lookup"><span data-stu-id="82f80-108">Example 1: Add a certificate</span></span>
```
PS C:\>$Policy = New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
PS C:\> Add-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -CertificatePolicy $Policy

Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : PS C:\>Get-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : completed
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : PS C:\>Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="82f80-109">В первой команде для создания политики сертификата используется командлет New-AzureKeyVaultCertificatePolicy, а затем он сохраняется в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="82f80-109">The first command uses the New-AzureKeyVaultCertificatePolicy cmdlet to create a certificate policy, and then stores it in the $Policy variable.</span></span>

<span data-ttu-id="82f80-110">Вторая команда использует **Add-AzureKeyVaultCertificate** , чтобы запустить процесс для создания сертификата.</span><span class="sxs-lookup"><span data-stu-id="82f80-110">The second command uses **Add-AzureKeyVaultCertificate** to start the process to create a certificate.</span></span>

<span data-ttu-id="82f80-111">Третья команда использует командлет Get-AzureKeyVaultCertificateOperation для опроса операции, чтобы убедиться, что она завершена.</span><span class="sxs-lookup"><span data-stu-id="82f80-111">The third command uses the Get-AzureKeyVaultCertificateOperation cmdlet to poll the operation to verify that it's complete.</span></span>

<span data-ttu-id="82f80-112">В последней команде для получения сертификата используется командлет Get-AzureKeyVaultCertificate.</span><span class="sxs-lookup"><span data-stu-id="82f80-112">The final command uses the Get-AzureKeyVaultCertificate cmdlet to get the certificate.</span></span>

## <span data-ttu-id="82f80-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82f80-113">PARAMETERS</span></span>

### <span data-ttu-id="82f80-114">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="82f80-114">-CertificatePolicy</span></span>
<span data-ttu-id="82f80-115">Указывает объект **KeyVaultCertificatePolicy** .</span><span class="sxs-lookup"><span data-stu-id="82f80-115">Specifies a **KeyVaultCertificatePolicy** object.</span></span>

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

### <span data-ttu-id="82f80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82f80-116">-DefaultProfile</span></span>
<span data-ttu-id="82f80-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="82f80-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82f80-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="82f80-118">-Name</span></span>
<span data-ttu-id="82f80-119">Указывает имя добавляемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="82f80-119">Specifies the name of the certificate to add.</span></span>

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

### <span data-ttu-id="82f80-120">-Тег</span><span class="sxs-lookup"><span data-stu-id="82f80-120">-Tag</span></span>
<span data-ttu-id="82f80-121">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="82f80-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="82f80-122">Например:</span><span class="sxs-lookup"><span data-stu-id="82f80-122">For example:</span></span>

<span data-ttu-id="82f80-123">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="82f80-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="82f80-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="82f80-124">-VaultName</span></span>
<span data-ttu-id="82f80-125">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="82f80-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="82f80-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82f80-126">-Confirm</span></span>
<span data-ttu-id="82f80-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="82f80-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82f80-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82f80-128">-WhatIf</span></span>
<span data-ttu-id="82f80-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="82f80-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82f80-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="82f80-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82f80-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f80-131">CommonParameters</span></span>
<span data-ttu-id="82f80-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82f80-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82f80-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82f80-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f80-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82f80-134">INPUTS</span></span>

## <span data-ttu-id="82f80-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82f80-135">OUTPUTS</span></span>

### <span data-ttu-id="82f80-136">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="82f80-136">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="82f80-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="82f80-137">NOTES</span></span>

## <span data-ttu-id="82f80-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82f80-138">RELATED LINKS</span></span>

[<span data-ttu-id="82f80-139">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="82f80-139">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="82f80-140">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="82f80-140">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="82f80-141">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="82f80-141">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
