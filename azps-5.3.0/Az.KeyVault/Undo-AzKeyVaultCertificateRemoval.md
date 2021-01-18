---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 7e9af7cd775726fc57b78f3fdead20f36dca13cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506257"
---
# <span data-ttu-id="972c5-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="972c5-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="972c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="972c5-102">SYNOPSIS</span></span>
<span data-ttu-id="972c5-103">Восстановление удаленного сертификата из хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="972c5-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="972c5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="972c5-104">SYNTAX</span></span>

### <span data-ttu-id="972c5-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="972c5-105">Default (Default)</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="972c5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="972c5-106">InputObject</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="972c5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="972c5-107">DESCRIPTION</span></span>
<span data-ttu-id="972c5-108">Для восстановления ранее удаленного сертификата будет восстановлен ранее удаленный cmdlet **Undo-AzKeyVaultCertificateRemoval.**</span><span class="sxs-lookup"><span data-stu-id="972c5-108">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="972c5-109">Восстановленный сертификат будет активен и может использоваться для всех операций.</span><span class="sxs-lookup"><span data-stu-id="972c5-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="972c5-110">Для выполнения этой операции вызываемму вызываемму звоня необходимо разрешение на восстановление.</span><span class="sxs-lookup"><span data-stu-id="972c5-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="972c5-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="972c5-111">EXAMPLES</span></span>

### <span data-ttu-id="972c5-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="972c5-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/24/2018 10:58:13 AM

                [Not After]
                  11/24/2018 10:08:13 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/mycertificate/7fe415d5518240c1a6fce89986b8d334
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/mycertificate/7fe415d5518240c1a6fce89986b8d334
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Recoverable+Purgeable
Enabled       : True
Expires       : 11/24/2018 6:08:13 PM
NotBefore     : 5/24/2018 5:58:13 PM
Created       : 5/24/2018 6:08:13 PM
Updated       : 5/24/2018 6:08:13 PM
Tags          :
VaultName     : MyKeyVault
Name          : MyCertificate
Version       : 7fe415d5518240c1a6fce89986b8d334
Id            : https://mykeyvault.vault.azure.net:443/certificates/mycertificate/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="972c5-113">Эта команда восстановит сертификат MyCertificate, который ранее был удален, в активное состояние.</span><span class="sxs-lookup"><span data-stu-id="972c5-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="972c5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="972c5-114">PARAMETERS</span></span>

### <span data-ttu-id="972c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="972c5-115">-DefaultProfile</span></span>
<span data-ttu-id="972c5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="972c5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="972c5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="972c5-117">-InputObject</span></span>
<span data-ttu-id="972c5-118">Удаленный объект сертификата</span><span class="sxs-lookup"><span data-stu-id="972c5-118">Deleted Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="972c5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="972c5-119">-Name</span></span>
<span data-ttu-id="972c5-120">Имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="972c5-120">Certificate name.</span></span>
<span data-ttu-id="972c5-121">Cmdlet конструировать FQDN сертификата из имени сейфа, выбранной среды и имени сертификата.</span><span class="sxs-lookup"><span data-stu-id="972c5-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972c5-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="972c5-122">-VaultName</span></span>
<span data-ttu-id="972c5-123">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="972c5-123">Vault name.</span></span>
<span data-ttu-id="972c5-124">С его учетом именем и выбранной средой строится FQDN хранилища.</span><span class="sxs-lookup"><span data-stu-id="972c5-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972c5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="972c5-125">-Confirm</span></span>
<span data-ttu-id="972c5-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="972c5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="972c5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="972c5-127">-WhatIf</span></span>
<span data-ttu-id="972c5-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="972c5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="972c5-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="972c5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="972c5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="972c5-130">CommonParameters</span></span>
<span data-ttu-id="972c5-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="972c5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="972c5-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="972c5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="972c5-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="972c5-133">INPUTS</span></span>

### <span data-ttu-id="972c5-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="972c5-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="972c5-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="972c5-135">OUTPUTS</span></span>

### <span data-ttu-id="972c5-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="972c5-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="972c5-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="972c5-137">NOTES</span></span>

## <span data-ttu-id="972c5-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="972c5-138">RELATED LINKS</span></span>

[<span data-ttu-id="972c5-139">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="972c5-139">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="972c5-140">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="972c5-140">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
