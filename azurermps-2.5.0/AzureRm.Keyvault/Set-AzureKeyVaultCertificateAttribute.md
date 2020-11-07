---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateattribute
schema: 2.0.0
ms.openlocfilehash: 9f7c08f42026c6cc5d321ae78687a903c8393904
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913321"
---
# <span data-ttu-id="21ff7-101">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="21ff7-101">Set-AzureKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="21ff7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="21ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="21ff7-103">Изменяет редактируемые атрибуты сертификата.</span><span class="sxs-lookup"><span data-stu-id="21ff7-103">Modifies editable attributes of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21ff7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="21ff7-104">SYNTAX</span></span>

```
Set-AzureKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21ff7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21ff7-105">DESCRIPTION</span></span>
<span data-ttu-id="21ff7-106">Командлет **Set-AzureKeyVaultCertificateAttribute** изменяет редактируемые атрибуты сертификата.</span><span class="sxs-lookup"><span data-stu-id="21ff7-106">The **Set-AzureKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="21ff7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="21ff7-107">EXAMPLES</span></span>

### <span data-ttu-id="21ff7-108">Пример 1: изменение тегов, связанных с сертификатом</span><span class="sxs-lookup"><span data-stu-id="21ff7-108">Example 1: Modify the tags associated with a certificate</span></span>
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

<span data-ttu-id="21ff7-109">В первой команде массив пар "ключ-значение" назначается переменной $Tags.</span><span class="sxs-lookup"><span data-stu-id="21ff7-109">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="21ff7-110">Вторая команда задает в качестве значения тегов сертификата с именем TestCert01 $Tags.</span><span class="sxs-lookup"><span data-stu-id="21ff7-110">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="21ff7-111">Последняя команда отображает сертификат TestCert01 с помощью командлета Get-AzureKeyVaultCertificate, чтобы проверить операцию.</span><span class="sxs-lookup"><span data-stu-id="21ff7-111">The final command displays the TestCert01 certificate by using the Get-AzureKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="21ff7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="21ff7-112">PARAMETERS</span></span>

### <span data-ttu-id="21ff7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21ff7-113">-DefaultProfile</span></span>
<span data-ttu-id="21ff7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="21ff7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21ff7-115">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="21ff7-115">-Enable</span></span>
<span data-ttu-id="21ff7-116">Указывает, нужно ли включать или отключать сертификат.</span><span class="sxs-lookup"><span data-stu-id="21ff7-116">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="21ff7-117">Укажите $True, чтобы включить или отключить или $False.</span><span class="sxs-lookup"><span data-stu-id="21ff7-117">Specify $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="21ff7-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="21ff7-118">-Name</span></span>
<span data-ttu-id="21ff7-119">Указывает имя сертификата, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="21ff7-119">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="21ff7-120">Этот командлет создает полное доменное имя сертификата на основе имени хранилища ключей, текущей выбранной среды, имени сертификата и версии сертификата.</span><span class="sxs-lookup"><span data-stu-id="21ff7-120">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

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

### <span data-ttu-id="21ff7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21ff7-121">-PassThru</span></span>
<span data-ttu-id="21ff7-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="21ff7-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="21ff7-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="21ff7-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="21ff7-124">-Тег</span><span class="sxs-lookup"><span data-stu-id="21ff7-124">-Tag</span></span>
<span data-ttu-id="21ff7-125">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="21ff7-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="21ff7-126">Например:</span><span class="sxs-lookup"><span data-stu-id="21ff7-126">For example:</span></span>

<span data-ttu-id="21ff7-127">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="21ff7-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="21ff7-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="21ff7-128">-VaultName</span></span>
<span data-ttu-id="21ff7-129">Указывает имя хранилища ключей, в котором этот командлет изменяет сертификат.</span><span class="sxs-lookup"><span data-stu-id="21ff7-129">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="21ff7-130">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени и выбранной в данный момент среде.</span><span class="sxs-lookup"><span data-stu-id="21ff7-130">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="21ff7-131">-Version</span><span class="sxs-lookup"><span data-stu-id="21ff7-131">-Version</span></span>
<span data-ttu-id="21ff7-132">Определяет версию сертификата.</span><span class="sxs-lookup"><span data-stu-id="21ff7-132">Specifies the version of a certificate.</span></span>
<span data-ttu-id="21ff7-133">Этот командлет создает полное доменное имя сертификата на основе имени хранилища ключей, текущей выбранной среды, имени сертификата и версии сертификата.</span><span class="sxs-lookup"><span data-stu-id="21ff7-133">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

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

### <span data-ttu-id="21ff7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21ff7-134">-Confirm</span></span>
<span data-ttu-id="21ff7-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="21ff7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21ff7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21ff7-136">-WhatIf</span></span>
<span data-ttu-id="21ff7-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="21ff7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21ff7-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="21ff7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21ff7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ff7-139">CommonParameters</span></span>
<span data-ttu-id="21ff7-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="21ff7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ff7-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21ff7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ff7-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="21ff7-142">INPUTS</span></span>

## <span data-ttu-id="21ff7-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="21ff7-143">OUTPUTS</span></span>

### <span data-ttu-id="21ff7-144">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="21ff7-144">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="21ff7-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="21ff7-145">NOTES</span></span>

## <span data-ttu-id="21ff7-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21ff7-146">RELATED LINKS</span></span>

[<span data-ttu-id="21ff7-147">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="21ff7-147">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)
