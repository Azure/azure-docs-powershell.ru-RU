---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: 33024ce7002975848a98ff8bdfd6188196a96e6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734448"
---
# <span data-ttu-id="4a0a9-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="4a0a9-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="4a0a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a0a9-102">SYNOPSIS</span></span>
<span data-ttu-id="4a0a9-103">Восстановление удаленного сертификата из хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a0a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a0a9-104">SYNTAX</span></span>

### <span data-ttu-id="4a0a9-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a0a9-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a0a9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4a0a9-106">InputObject</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a0a9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a0a9-107">DESCRIPTION</span></span>
<span data-ttu-id="4a0a9-108">Командлет **Undo-AzureKeyVaultCertificateRemoval** восстановит ранее удаленный сертификат.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-108">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="4a0a9-109">Восстановленный сертификат будет активен и может использоваться для всех операций.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="4a0a9-110">Для выполнения этой операции вызывающему объекту должно быть предоставлено разрешение "Recover".</span><span class="sxs-lookup"><span data-stu-id="4a0a9-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="4a0a9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a0a9-111">EXAMPLES</span></span>

### <span data-ttu-id="4a0a9-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4a0a9-112">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="4a0a9-113">Эта команда восстановит сертификат "MyCertificate", который ранее был удален, в активное и пригодное для использования состояние.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="4a0a9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a0a9-114">PARAMETERS</span></span>

### <span data-ttu-id="4a0a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a0a9-115">-DefaultProfile</span></span>
<span data-ttu-id="4a0a9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4a0a9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a0a9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a0a9-117">-InputObject</span></span>
<span data-ttu-id="4a0a9-118">Удаленный объект сертификата</span><span class="sxs-lookup"><span data-stu-id="4a0a9-118">Deleted Certificate object</span></span>

```yaml
Type: PSDeletedKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0a9-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4a0a9-119">-Name</span></span>
<span data-ttu-id="4a0a9-120">Имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-120">Certificate name.</span></span>
<span data-ttu-id="4a0a9-121">Командлет создает полное доменное имя сертификата из имени хранилища, выбранной в данный момент среды и имени сертификата.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0a9-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4a0a9-122">-VaultName</span></span>
<span data-ttu-id="4a0a9-123">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-123">Vault name.</span></span>
<span data-ttu-id="4a0a9-124">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0a9-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a0a9-125">-Confirm</span></span>
<span data-ttu-id="4a0a9-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a0a9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a0a9-127">-WhatIf</span></span>
<span data-ttu-id="4a0a9-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a0a9-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a0a9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a0a9-130">CommonParameters</span></span>
<span data-ttu-id="4a0a9-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a0a9-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a0a9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a0a9-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a0a9-133">INPUTS</span></span>

### <span data-ttu-id="4a0a9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4a0a9-134">System.String</span></span>

## <span data-ttu-id="4a0a9-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a0a9-135">OUTPUTS</span></span>

### <span data-ttu-id="4a0a9-136">Microsoft. Azure. Commands. KeyVault. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="4a0a9-136">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="4a0a9-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a0a9-137">NOTES</span></span>

## <span data-ttu-id="4a0a9-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a0a9-138">RELATED LINKS</span></span>

[<span data-ttu-id="4a0a9-139">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4a0a9-139">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="4a0a9-140">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4a0a9-140">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
