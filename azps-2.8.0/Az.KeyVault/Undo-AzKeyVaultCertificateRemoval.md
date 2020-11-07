---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: ff8404b3a437d27b84501ba56bc79daa09a9b8f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720610"
---
# <span data-ttu-id="b4ec3-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="b4ec3-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="b4ec3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ec3-103">Восстановление удаленного сертификата из хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="b4ec3-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="b4ec3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4ec3-104">SYNTAX</span></span>

### <span data-ttu-id="b4ec3-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b4ec3-105">Default (Default)</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4ec3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b4ec3-106">InputObject</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4ec3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4ec3-107">DESCRIPTION</span></span>
<span data-ttu-id="b4ec3-108">Командлет **Undo-AzKeyVaultCertificateRemoval** восстановит ранее удаленный сертификат.</span><span class="sxs-lookup"><span data-stu-id="b4ec3-108">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="b4ec3-109">Восстановленный сертификат будет активен и может использоваться для всех операций.</span><span class="sxs-lookup"><span data-stu-id="b4ec3-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="b4ec3-110">Для выполнения этой операции вызывающему объекту должно быть предоставлено разрешение "Recover".</span><span class="sxs-lookup"><span data-stu-id="b4ec3-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="b4ec3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4ec3-111">EXAMPLES</span></span>

### <span data-ttu-id="b4ec3-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b4ec3-112">Example 1</span></span>
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

<span data-ttu-id="b4ec3-113">Эта команда восстановит сертификат "MyCertificate", который ранее был удален, в активное и пригодное для использования состояние.</span><span class="sxs-lookup"><span data-stu-id="b4ec3-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="b4ec3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4ec3-114">PARAMETERS</span></span>

### <span data-ttu-id="b4ec3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ec3-115">-DefaultProfile</span></span>
<span data-ttu-id="b4ec3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b4ec3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4ec3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4ec3-117">-InputObject</span></span>
<span data-ttu-id="b4ec3-118">Удаленный объект сертификата</span><span class="sxs-lookup"><span data-stu-id="b4ec3-118">Deleted Certificate object</span></span>

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

### <span data-ttu-id="b4ec3-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b4ec3-119">-Name</span></span>
<span data-ttu-id="b4ec3-120">Имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="b4ec3-120">Certificate name.</span></span>
<span data-ttu-id="b4ec3-121">Командлет создает полное доменное имя сертификата из имени хранилища, выбранной в данный момент среды и имени сертификата.</span><span class="sxs-lookup"><span data-stu-id="b4ec3-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="b4ec3-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b4ec3-122">-VaultName</span></span>
<span data-ttu-id="b4ec3-123">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="b4ec3-123">Vault name.</span></span>
<span data-ttu-id="b4ec3-124">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="b4ec3-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b4ec3-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4ec3-125">-Confirm</span></span>
<span data-ttu-id="b4ec3-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b4ec3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4ec3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4ec3-127">-WhatIf</span></span>
<span data-ttu-id="b4ec3-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b4ec3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4ec3-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b4ec3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4ec3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ec3-130">CommonParameters</span></span>
<span data-ttu-id="b4ec3-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4ec3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ec3-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4ec3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ec3-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4ec3-133">INPUTS</span></span>

### <span data-ttu-id="b4ec3-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b4ec3-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="b4ec3-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4ec3-135">OUTPUTS</span></span>

### <span data-ttu-id="b4ec3-136">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b4ec3-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="b4ec3-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4ec3-137">NOTES</span></span>

## <span data-ttu-id="b4ec3-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4ec3-138">RELATED LINKS</span></span>

[<span data-ttu-id="b4ec3-139">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b4ec3-139">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="b4ec3-140">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b4ec3-140">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
