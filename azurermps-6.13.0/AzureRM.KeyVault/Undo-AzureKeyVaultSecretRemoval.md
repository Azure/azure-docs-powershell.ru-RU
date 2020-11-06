---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: ecc22deb6be4f8fe85b66454091f6bfbd01d3a80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564383"
---
# <span data-ttu-id="76613-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="76613-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="76613-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76613-102">SYNOPSIS</span></span>
<span data-ttu-id="76613-103">Восстановление удаленного секрета из хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="76613-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76613-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76613-104">SYNTAX</span></span>

### <span data-ttu-id="76613-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76613-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76613-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="76613-106">InputObject</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76613-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76613-107">DESCRIPTION</span></span>
<span data-ttu-id="76613-108">Командлет **Undo-AzureKeyVaultSecretRemoval** восстановит ранее удаленный секрет.</span><span class="sxs-lookup"><span data-stu-id="76613-108">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="76613-109">Восстановленный секрет будет активен и может использоваться для всех обычных секретных операций.</span><span class="sxs-lookup"><span data-stu-id="76613-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="76613-110">Для выполнения этой операции вызывающему объекту должно быть предоставлено разрешение "Recover".</span><span class="sxs-lookup"><span data-stu-id="76613-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="76613-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76613-111">EXAMPLES</span></span>

### <span data-ttu-id="76613-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="76613-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'

Vault Name   : MyKeyVault
Name         : MySecret
Version      : f622abc7b1394092812f1eb0f85dc91c
Id           : https://mykeyvault.vault.azure.net:443/secrets/mysecret/f622abc7b1394092812f1eb0f85dc91c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/19/2018 5:56:02 PM
Updated      : 4/26/2018 7:48:40 PM
Content Type :
Tags         :
```

<span data-ttu-id="76613-113">Эта команда восстановит секретный "MySecret", который ранее был удален, в активное и пригодное для использования состояние.</span><span class="sxs-lookup"><span data-stu-id="76613-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="76613-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76613-114">PARAMETERS</span></span>

### <span data-ttu-id="76613-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76613-115">-DefaultProfile</span></span>
<span data-ttu-id="76613-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="76613-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76613-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76613-117">-InputObject</span></span>
<span data-ttu-id="76613-118">Удален секретный объект</span><span class="sxs-lookup"><span data-stu-id="76613-118">Deleted secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76613-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="76613-119">-Name</span></span>
<span data-ttu-id="76613-120">Имя секрета.</span><span class="sxs-lookup"><span data-stu-id="76613-120">Secret name.</span></span>
<span data-ttu-id="76613-121">Командлет создает полное доменное имя секрета из имени хранилища, выбранного в настоящее время среды и имени секрета.</span><span class="sxs-lookup"><span data-stu-id="76613-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76613-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="76613-122">-VaultName</span></span>
<span data-ttu-id="76613-123">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="76613-123">Vault name.</span></span>
<span data-ttu-id="76613-124">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="76613-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="76613-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76613-125">-Confirm</span></span>
<span data-ttu-id="76613-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="76613-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76613-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76613-127">-WhatIf</span></span>
<span data-ttu-id="76613-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="76613-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76613-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="76613-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76613-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76613-130">CommonParameters</span></span>
<span data-ttu-id="76613-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76613-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76613-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76613-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76613-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76613-133">INPUTS</span></span>

### <span data-ttu-id="76613-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="76613-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="76613-135">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="76613-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="76613-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76613-136">OUTPUTS</span></span>

### <span data-ttu-id="76613-137">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="76613-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="76613-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="76613-138">NOTES</span></span>

## <span data-ttu-id="76613-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76613-139">RELATED LINKS</span></span>

[<span data-ttu-id="76613-140">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="76613-140">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="76613-141">Add-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="76613-141">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="76613-142">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="76613-142">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
