---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/import-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: 2903aa294830b8f9a39578374c1c108fe91c36e4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914465"
---
# <span data-ttu-id="24f0c-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="24f0c-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="24f0c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="24f0c-103">Импорт сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="24f0c-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24f0c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24f0c-104">SYNTAX</span></span>

### <span data-ttu-id="24f0c-105">ImportCertificateFromFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="24f0c-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24f0c-106">ImportWithPrivateKeyFromFile</span><span class="sxs-lookup"><span data-stu-id="24f0c-106">ImportWithPrivateKeyFromFile</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24f0c-107">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="24f0c-107">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24f0c-108">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="24f0c-108">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 -CertificateCollection <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24f0c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24f0c-109">DESCRIPTION</span></span>
<span data-ttu-id="24f0c-110">Командлет **Import-AzureKeyVaultCertificate** импортирует сертификат в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="24f0c-110">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>

<span data-ttu-id="24f0c-111">Вы можете создать сертификат для импорта с помощью одного из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="24f0c-111">You can create the certificate to import by using one of the following methods:</span></span>

- <span data-ttu-id="24f0c-112">Используйте командлет New-AzureKeyVaultCertificateSigningRequest, чтобы создать запрос на подписывание сертификата и отправить его в центр сертификации.</span><span class="sxs-lookup"><span data-stu-id="24f0c-112">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="24f0c-113">Используйте существующий файл пакета сертификата, например PFX или P12, который включает в себя сертификат и закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="24f0c-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="24f0c-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24f0c-114">EXAMPLES</span></span>

### <span data-ttu-id="24f0c-115">Пример 1: Импорт сертификата хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="24f0c-115">Example 1: Import a key vault certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password
Name        : importCert01
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
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="24f0c-116">Первая команда использует командлет ConvertTo-SecureString для создания защищенного пароля и сохраняет его в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="24f0c-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>

<span data-ttu-id="24f0c-117">Вторая команда импортирует сертификат с именем ImportCert01 в хранилище ключей CosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="24f0c-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="24f0c-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24f0c-118">PARAMETERS</span></span>

### <span data-ttu-id="24f0c-119">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="24f0c-119">-CertificateCollection</span></span>
<span data-ttu-id="24f0c-120">Указывает коллекцию сертификатов, которую нужно добавить в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="24f0c-120">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f0c-121">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="24f0c-121">-CertificateString</span></span>
<span data-ttu-id="24f0c-122">Указывает строку сертификата.</span><span class="sxs-lookup"><span data-stu-id="24f0c-122">Specifies a certificate string.</span></span>

```yaml
Type: String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f0c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f0c-123">-DefaultProfile</span></span>
<span data-ttu-id="24f0c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="24f0c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24f0c-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="24f0c-125">-FilePath</span></span>
<span data-ttu-id="24f0c-126">Задает путь к файлу сертификата, который импортируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="24f0c-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f0c-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="24f0c-127">-Name</span></span>
<span data-ttu-id="24f0c-128">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="24f0c-128">Specifies the certificate name.</span></span> <span data-ttu-id="24f0c-129">Этот командлет создает полное доменное имя (FQDN) сертификата из имени хранилища ключей, выбранной в данный момент среды и имени сертификата.</span><span class="sxs-lookup"><span data-stu-id="24f0c-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="24f0c-130">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="24f0c-130">-Password</span></span>
<span data-ttu-id="24f0c-131">Указывает пароль для файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="24f0c-131">Specifies the password for a certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ImportWithPrivateKeyFromFile, ImportWithPrivateKeyFromString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f0c-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="24f0c-132">-Tag</span></span>
<span data-ttu-id="24f0c-133">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="24f0c-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="24f0c-134">Например:</span><span class="sxs-lookup"><span data-stu-id="24f0c-134">For example:</span></span>

<span data-ttu-id="24f0c-135">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="24f0c-135">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24f0c-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="24f0c-136">-VaultName</span></span>
<span data-ttu-id="24f0c-137">Указывает имя хранилища ключей, в которое этот командлет импортирует сертификаты.</span><span class="sxs-lookup"><span data-stu-id="24f0c-137">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="24f0c-138">Этот командлет создает полное доменное имя (FQDN) для хранилища ключей, основываясь на имени и выбранной в данный момент среде.</span><span class="sxs-lookup"><span data-stu-id="24f0c-138">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="24f0c-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24f0c-139">-Confirm</span></span>
<span data-ttu-id="24f0c-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="24f0c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24f0c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24f0c-141">-WhatIf</span></span>
<span data-ttu-id="24f0c-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="24f0c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24f0c-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="24f0c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24f0c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f0c-144">CommonParameters</span></span>
<span data-ttu-id="24f0c-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24f0c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f0c-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24f0c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f0c-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24f0c-147">INPUTS</span></span>

## <span data-ttu-id="24f0c-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24f0c-148">OUTPUTS</span></span>

### <span data-ttu-id="24f0c-149">Microsoft. Azure. Commands. KeyVault. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="24f0c-149">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="24f0c-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="24f0c-150">NOTES</span></span>

## <span data-ttu-id="24f0c-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24f0c-151">RELATED LINKS</span></span>

[<span data-ttu-id="24f0c-152">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="24f0c-152">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
