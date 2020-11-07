---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: 3e2da64d467d71721255afa12211530e7c0d9f08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900169"
---
# <span data-ttu-id="0f4fe-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0f4fe-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="0f4fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f4fe-102">SYNOPSIS</span></span>
<span data-ttu-id="0f4fe-103">Удаляет сертификат из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="0f4fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f4fe-104">SYNTAX</span></span>

### <span data-ttu-id="0f4fe-105">ByVaultNameAndName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f4fe-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f4fe-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="0f4fe-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f4fe-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f4fe-107">DESCRIPTION</span></span>
<span data-ttu-id="0f4fe-108">Командлет **Remove-AzKeyVaultCertificate** Удаляет сертификат из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-108">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="0f4fe-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f4fe-109">EXAMPLES</span></span>

### <span data-ttu-id="0f4fe-110">Пример 1: Удаление сертификата</span><span class="sxs-lookup"><span data-stu-id="0f4fe-110">Example 1: Remove a certificate</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       4/11/2018 4:28:39 PM

                     [Not After]
                       10/11/2018 4:38:39 PM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contosokv01.vault.azure.net:443/keys/selfsigned01/968c3920884a435abf8faea11f565456
SecretId           : https://contosokv01.vault.azure.net:443/secrets/selfsigned01/968c3920884a435abf8faea11f565456
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Purgeable
ScheduledPurgeDate :
DeletedDate        :
Enabled            : True
Expires            : 10/11/2018 11:38:39 PM
NotBefore          : 4/11/2018 11:28:39 PM
Created            : 4/11/2018 11:38:39 PM
Updated            : 4/11/2018 11:38:39 PM
Tags               :
VaultName          : ContosoKV01
Name               : SelfSigned01
Version            : 968c3920884a435abf8faea11f565456
Id                 : https://contosokv01.vault.azure.net:443/certificates/selfsigned01/968c3920884a435abf8faea11f565456
```

<span data-ttu-id="0f4fe-111">Эта команда удаляет сертификат с именем SelfSigned01 из хранилища ключей с именем ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="0f4fe-112">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="0f4fe-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="0f4fe-113">Таким образом, командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="0f4fe-114">Пример 2: Удаление удаленного сертификата из хранилища ключей без возможности восстановления</span><span class="sxs-lookup"><span data-stu-id="0f4fe-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="0f4fe-115">Эта команда окончательно удаляет сертификат с именем "MyCert" из хранилища ключей с именем "contoso".</span><span class="sxs-lookup"><span data-stu-id="0f4fe-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="0f4fe-116">Для выполнения этого командлета требуется разрешение на очистку, которое должно быть ранее и явно предоставлено пользователю в этом хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="0f4fe-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f4fe-117">PARAMETERS</span></span>

### <span data-ttu-id="0f4fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f4fe-118">-DefaultProfile</span></span>
<span data-ttu-id="0f4fe-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0f4fe-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f4fe-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0f4fe-120">-Force</span></span>
<span data-ttu-id="0f4fe-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f4fe-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f4fe-122">-InputObject</span></span>
<span data-ttu-id="0f4fe-123">Объект сертификата.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-123">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f4fe-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="0f4fe-124">-InRemovedState</span></span>
<span data-ttu-id="0f4fe-125">Если он указан, окончательно удаляет ранее удаленный сертификат.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="0f4fe-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f4fe-126">-Name</span></span>
<span data-ttu-id="0f4fe-127">Указывает имя сертификата, который этот командлет удаляет из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="0f4fe-128">Этот командлет создает полное доменное имя (FQDN) сертификата на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f4fe-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f4fe-129">-PassThru</span></span>
<span data-ttu-id="0f4fe-130">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0f4fe-131">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0f4fe-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0f4fe-132">-VaultName</span></span>
<span data-ttu-id="0f4fe-133">Указывает имя хранилища ключей, из которого этот командлет удаляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="0f4fe-134">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f4fe-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f4fe-135">-Confirm</span></span>
<span data-ttu-id="0f4fe-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f4fe-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f4fe-137">-WhatIf</span></span>
<span data-ttu-id="0f4fe-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f4fe-139">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f4fe-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f4fe-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f4fe-141">CommonParameters</span></span>
<span data-ttu-id="0f4fe-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f4fe-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f4fe-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f4fe-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f4fe-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f4fe-144">INPUTS</span></span>

### <span data-ttu-id="0f4fe-145">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0f4fe-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="0f4fe-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f4fe-146">OUTPUTS</span></span>

### <span data-ttu-id="0f4fe-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0f4fe-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="0f4fe-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f4fe-148">NOTES</span></span>

## <span data-ttu-id="0f4fe-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f4fe-149">RELATED LINKS</span></span>

[<span data-ttu-id="0f4fe-150">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0f4fe-150">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="0f4fe-151">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0f4fe-151">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="0f4fe-152">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0f4fe-152">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="0f4fe-153">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="0f4fe-153">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
