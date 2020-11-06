---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
ms.openlocfilehash: 4aac9e7079451eebda0c77ae663666fbd55dc9e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557323"
---
# <span data-ttu-id="81505-101">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="81505-101">Set-AzureKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="81505-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81505-102">SYNOPSIS</span></span>
<span data-ttu-id="81505-103">Изменяет редактируемые атрибуты сертификата.</span><span class="sxs-lookup"><span data-stu-id="81505-103">Modifies editable attributes of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81505-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81505-104">SYNTAX</span></span>

### <span data-ttu-id="81505-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="81505-105">ByName (Default)</span></span>
```
Set-AzureKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81505-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="81505-106">ByInputObject</span></span>
```
Set-AzureKeyVaultCertificateAttribute [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81505-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81505-107">DESCRIPTION</span></span>
<span data-ttu-id="81505-108">Командлет **Set-AzureKeyVaultCertificateAttribute** изменяет редактируемые атрибуты сертификата.</span><span class="sxs-lookup"><span data-stu-id="81505-108">The **Set-AzureKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="81505-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81505-109">EXAMPLES</span></span>

### <span data-ttu-id="81505-110">Пример 1: изменение тегов, связанных с сертификатом</span><span class="sxs-lookup"><span data-stu-id="81505-110">Example 1: Modify the tags associated with a certificate</span></span>
```
PS C:\>$Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Set-AzureKeyVaultCertificateAttribute -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags
PS C:\> Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : "TestCert01"
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                5A2EF60501F241D6A4336841B36FEA41

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                A565D568082FEE2BE33B356ECC3703C2E9886555

Id          : https://ContosoKV01.vault.azure.net:443/certificates/tt02
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/tt02
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/tt02
Thumbprint  : A565D568082FEE2BE33B356ECC3703C2E9886555
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="81505-111">В первой команде массив пар "ключ-значение" назначается переменной $Tags.</span><span class="sxs-lookup"><span data-stu-id="81505-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="81505-112">Вторая команда задает в качестве значения тегов сертификата с именем TestCert01 $Tags.</span><span class="sxs-lookup"><span data-stu-id="81505-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="81505-113">Последняя команда отображает сертификат TestCert01 с помощью командлета Get-AzureKeyVaultCertificate, чтобы проверить операцию.</span><span class="sxs-lookup"><span data-stu-id="81505-113">The final command displays the TestCert01 certificate by using the Get-AzureKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="81505-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81505-114">PARAMETERS</span></span>

### <span data-ttu-id="81505-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81505-115">-DefaultProfile</span></span>
<span data-ttu-id="81505-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="81505-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81505-117">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="81505-117">-Enable</span></span>
<span data-ttu-id="81505-118">Указывает, нужно ли включать или отключать сертификат.</span><span class="sxs-lookup"><span data-stu-id="81505-118">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="81505-119">Укажите $True, чтобы включить или отключить или $False.</span><span class="sxs-lookup"><span data-stu-id="81505-119">Specify $True to enable or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81505-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81505-120">-InputObject</span></span>
<span data-ttu-id="81505-121">Объект сертификата</span><span class="sxs-lookup"><span data-stu-id="81505-121">Certificate object</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81505-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="81505-122">-Name</span></span>
<span data-ttu-id="81505-123">Указывает имя сертификата, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="81505-123">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="81505-124">Этот командлет создает полное доменное имя сертификата на основе имени хранилища ключей, текущей выбранной среды, имени сертификата и версии сертификата.</span><span class="sxs-lookup"><span data-stu-id="81505-124">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81505-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81505-125">-PassThru</span></span>
<span data-ttu-id="81505-126">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="81505-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="81505-127">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="81505-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="81505-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="81505-128">-Tag</span></span>
<span data-ttu-id="81505-129">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="81505-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="81505-130">Например:</span><span class="sxs-lookup"><span data-stu-id="81505-130">For example:</span></span>

<span data-ttu-id="81505-131">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="81505-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="81505-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="81505-132">-VaultName</span></span>
<span data-ttu-id="81505-133">Указывает имя хранилища ключей, в котором этот командлет изменяет сертификат.</span><span class="sxs-lookup"><span data-stu-id="81505-133">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="81505-134">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени и выбранной в данный момент среде.</span><span class="sxs-lookup"><span data-stu-id="81505-134">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81505-135">-Version</span><span class="sxs-lookup"><span data-stu-id="81505-135">-Version</span></span>
<span data-ttu-id="81505-136">Определяет версию сертификата.</span><span class="sxs-lookup"><span data-stu-id="81505-136">Specifies the version of a certificate.</span></span>
<span data-ttu-id="81505-137">Этот командлет создает полное доменное имя сертификата на основе имени хранилища ключей, текущей выбранной среды, имени сертификата и версии сертификата.</span><span class="sxs-lookup"><span data-stu-id="81505-137">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81505-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81505-138">-Confirm</span></span>
<span data-ttu-id="81505-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="81505-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81505-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81505-140">-WhatIf</span></span>
<span data-ttu-id="81505-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="81505-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81505-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="81505-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81505-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81505-143">CommonParameters</span></span>
<span data-ttu-id="81505-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81505-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81505-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81505-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81505-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81505-146">INPUTS</span></span>

### <span data-ttu-id="81505-147">Ничего</span><span class="sxs-lookup"><span data-stu-id="81505-147">None</span></span>
<span data-ttu-id="81505-148">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="81505-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="81505-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81505-149">OUTPUTS</span></span>

### <span data-ttu-id="81505-150">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="81505-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="81505-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="81505-151">NOTES</span></span>

## <span data-ttu-id="81505-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81505-152">RELATED LINKS</span></span>

[<span data-ttu-id="81505-153">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="81505-153">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)
