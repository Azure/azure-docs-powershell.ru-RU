---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultCertificate.md
ms.openlocfilehash: 732d8dc7cfe3c0f8a3bec6eb3157b65bc8437e44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564376"
---
# <span data-ttu-id="0f786-101">Update-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0f786-101">Update-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="0f786-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f786-102">SYNOPSIS</span></span>
<span data-ttu-id="0f786-103">Изменяет редактируемые атрибуты сертификата.</span><span class="sxs-lookup"><span data-stu-id="0f786-103">Modifies editable attributes of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f786-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f786-104">SYNTAX</span></span>

### <span data-ttu-id="0f786-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f786-105">ByName (Default)</span></span>
```
Update-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f786-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0f786-106">ByInputObject</span></span>
```
Update-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f786-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f786-107">DESCRIPTION</span></span>
<span data-ttu-id="0f786-108">Командлет **Update-AzureKeyVaultCertificate** изменяет редактируемые атрибуты сертификата.</span><span class="sxs-lookup"><span data-stu-id="0f786-108">The **Update-AzureKeyVaultCertificate** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="0f786-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f786-109">EXAMPLES</span></span>

### <span data-ttu-id="0f786-110">Пример 1: изменение тегов, связанных с сертификатом</span><span class="sxs-lookup"><span data-stu-id="0f786-110">Example 1: Modify the tags associated with a certificate</span></span>
```powershell
PS C:\> $Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Update-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags -PassThru

Name        : TestCert01
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Id          : https://ContosoKV01.vault.azure.net:443/certificates/TestCert01
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/TestCert01
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/TestCert01
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="0f786-111">В первой команде массив пар "ключ-значение" назначается переменной $Tags.</span><span class="sxs-lookup"><span data-stu-id="0f786-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="0f786-112">Вторая команда задает в качестве значения тегов сертификата с именем TestCert01 $Tags.</span><span class="sxs-lookup"><span data-stu-id="0f786-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

## <span data-ttu-id="0f786-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f786-113">PARAMETERS</span></span>

### <span data-ttu-id="0f786-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f786-114">-DefaultProfile</span></span>
<span data-ttu-id="0f786-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f786-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f786-116">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="0f786-116">-Enable</span></span>
<span data-ttu-id="0f786-117">Если указано, включите сертификат, если значение равно true.</span><span class="sxs-lookup"><span data-stu-id="0f786-117">If present, enable a certificate if value is true.</span></span>
<span data-ttu-id="0f786-118">Отключение сертификата, если значение равно false.</span><span class="sxs-lookup"><span data-stu-id="0f786-118">Disable a certificate if value is false.</span></span>
<span data-ttu-id="0f786-119">Если не указано, существующее значение состояния Enabled или Disabled сертификата останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="0f786-119">If not specified, the existing value of the certificate's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f786-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f786-120">-InputObject</span></span>
<span data-ttu-id="0f786-121">Объект сертификата</span><span class="sxs-lookup"><span data-stu-id="0f786-121">Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f786-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f786-122">-Name</span></span>
<span data-ttu-id="0f786-123">Имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="0f786-123">Certificate name.</span></span>
<span data-ttu-id="0f786-124">Командлет создает полное доменное имя секрета из имени хранилища, выбранного в настоящее время среды и имени секрета.</span><span class="sxs-lookup"><span data-stu-id="0f786-124">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f786-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f786-125">-PassThru</span></span>
<span data-ttu-id="0f786-126">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="0f786-126">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="0f786-127">Если этот параметр указан, возвращают объект сертификата.</span><span class="sxs-lookup"><span data-stu-id="0f786-127">If this switch is specified, return certificate object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f786-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="0f786-128">-Tag</span></span>
<span data-ttu-id="0f786-129">Хэш-таблица, представляющая Теги сертификата.</span><span class="sxs-lookup"><span data-stu-id="0f786-129">A hashtable representing certificate tags.</span></span>
<span data-ttu-id="0f786-130">Если он не указан, существующие теги Sertificate остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="0f786-130">If not specified, the existing tags of the sertificate remain unchanged.</span></span>
<span data-ttu-id="0f786-131">Удалите тег, указав пустую хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="0f786-131">Remove a tag by specifying an empty Hashtable.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f786-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0f786-132">-VaultName</span></span>
<span data-ttu-id="0f786-133">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="0f786-133">Vault name.</span></span>
<span data-ttu-id="0f786-134">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="0f786-134">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f786-135">-Version</span><span class="sxs-lookup"><span data-stu-id="0f786-135">-Version</span></span>
<span data-ttu-id="0f786-136">Версия сертификата.</span><span class="sxs-lookup"><span data-stu-id="0f786-136">Certificate version.</span></span>
<span data-ttu-id="0f786-137">Командлет создает полное доменное имя сертификата из имени хранилища, выбранной в данный момент среды, имени сертификата и версии сертификата.</span><span class="sxs-lookup"><span data-stu-id="0f786-137">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment, certificate name and certificate version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f786-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f786-138">-Confirm</span></span>
<span data-ttu-id="0f786-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0f786-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f786-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f786-140">-WhatIf</span></span>
<span data-ttu-id="0f786-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0f786-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f786-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0f786-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f786-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f786-143">CommonParameters</span></span>
<span data-ttu-id="0f786-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f786-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f786-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f786-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f786-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f786-146">INPUTS</span></span>

### <span data-ttu-id="0f786-147">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0f786-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="0f786-148">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0f786-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0f786-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f786-149">OUTPUTS</span></span>

### <span data-ttu-id="0f786-150">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0f786-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="0f786-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f786-151">NOTES</span></span>

## <span data-ttu-id="0f786-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f786-152">RELATED LINKS</span></span>
