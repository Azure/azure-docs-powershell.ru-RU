---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 6a687f67741a8d4925e3253c9f787532501ad186
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250221"
---
# <span data-ttu-id="6446e-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6446e-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="6446e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6446e-102">SYNOPSIS</span></span>
<span data-ttu-id="6446e-103">Импорт сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="6446e-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="6446e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6446e-104">SYNTAX</span></span>

### <span data-ttu-id="6446e-105">ImportCertificateFromFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6446e-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6446e-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="6446e-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6446e-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="6446e-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6446e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6446e-108">DESCRIPTION</span></span>
<span data-ttu-id="6446e-109">Командлет **Import-AzKeyVaultCertificate** импортирует сертификат в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="6446e-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="6446e-110">Вы можете создать сертификат для импорта с помощью одного из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="6446e-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="6446e-111">Используется `Add-AzKeyVaultCertificate` для создания запроса подписи сертификата и его отправки в центр сертификации.</span><span class="sxs-lookup"><span data-stu-id="6446e-111">Use `Add-AzKeyVaultCertificate` to create a certificate signing request and submit it to a certificate authority.</span></span> <span data-ttu-id="6446e-112">Обнаружить https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request</span><span class="sxs-lookup"><span data-stu-id="6446e-112">See https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request</span></span>
- <span data-ttu-id="6446e-113">Используйте существующий файл пакета сертификата, например PFX или P12, который включает в себя сертификат и закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="6446e-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="6446e-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6446e-114">EXAMPLES</span></span>

### <span data-ttu-id="6446e-115">Пример 1: Импорт сертификата хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="6446e-115">Example 1: Import a key vault certificate</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password

Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="6446e-116">Первая команда использует командлет ConvertTo-SecureString для создания защищенного пароля и сохраняет его в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="6446e-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="6446e-117">Вторая команда импортирует сертификат с именем ImportCert01 в хранилище ключей CosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="6446e-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="6446e-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6446e-118">PARAMETERS</span></span>

### <span data-ttu-id="6446e-119">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="6446e-119">-CertificateCollection</span></span>
<span data-ttu-id="6446e-120">Указывает коллекцию сертификатов, которую нужно добавить в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="6446e-120">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: System.Security.Cryptography.X509Certificates.X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6446e-121">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="6446e-121">-CertificateString</span></span>
<span data-ttu-id="6446e-122">Указывает строку сертификата.</span><span class="sxs-lookup"><span data-stu-id="6446e-122">Specifies a certificate string.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6446e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6446e-123">-DefaultProfile</span></span>
<span data-ttu-id="6446e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6446e-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6446e-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="6446e-125">-FilePath</span></span>
<span data-ttu-id="6446e-126">Задает путь к файлу сертификата, который импортируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6446e-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6446e-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6446e-127">-Name</span></span>
<span data-ttu-id="6446e-128">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="6446e-128">Specifies the certificate name.</span></span> <span data-ttu-id="6446e-129">Этот командлет создает полное доменное имя (FQDN) сертификата из имени хранилища ключей, выбранной в данный момент среды и имени сертификата.</span><span class="sxs-lookup"><span data-stu-id="6446e-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6446e-130">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="6446e-130">-Password</span></span>
<span data-ttu-id="6446e-131">Указывает пароль для файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="6446e-131">Specifies the password for a certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6446e-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="6446e-132">-Tag</span></span>
<span data-ttu-id="6446e-133">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="6446e-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6446e-134">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="6446e-134">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6446e-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6446e-135">-VaultName</span></span>
<span data-ttu-id="6446e-136">Указывает имя хранилища ключей, в которое этот командлет импортирует сертификаты.</span><span class="sxs-lookup"><span data-stu-id="6446e-136">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="6446e-137">Этот командлет создает полное доменное имя (FQDN) для хранилища ключей, основываясь на имени и выбранной в данный момент среде.</span><span class="sxs-lookup"><span data-stu-id="6446e-137">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6446e-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6446e-138">-Confirm</span></span>
<span data-ttu-id="6446e-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6446e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6446e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6446e-140">-WhatIf</span></span>
<span data-ttu-id="6446e-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6446e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6446e-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6446e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6446e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6446e-143">CommonParameters</span></span>
<span data-ttu-id="6446e-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6446e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6446e-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6446e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6446e-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6446e-146">INPUTS</span></span>

### <span data-ttu-id="6446e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="6446e-147">System.String</span></span>

### <span data-ttu-id="6446e-148">System. Security. Cryptography. X509Certificates. X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="6446e-148">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="6446e-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6446e-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6446e-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6446e-150">OUTPUTS</span></span>

### <span data-ttu-id="6446e-151">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6446e-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="6446e-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="6446e-152">NOTES</span></span>

## <span data-ttu-id="6446e-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6446e-153">RELATED LINKS</span></span>

[<span data-ttu-id="6446e-154">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6446e-154">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="6446e-155">Создание и слияние CSR в ключевом хранилище</span><span class="sxs-lookup"><span data-stu-id="6446e-155">Creating and merging CSR in Key Vault</span></span>](https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request)