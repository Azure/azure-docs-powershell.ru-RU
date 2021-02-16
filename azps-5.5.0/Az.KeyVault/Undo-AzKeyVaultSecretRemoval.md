---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 9513cba1532ec70acb77cdf97d19de25db36434f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100416147"
---
# <span data-ttu-id="f0811-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="f0811-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="f0811-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0811-102">SYNOPSIS</span></span>
<span data-ttu-id="f0811-103">Восстановление удаленной секретной секретной области в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="f0811-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="f0811-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f0811-104">SYNTAX</span></span>

### <span data-ttu-id="f0811-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0811-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0811-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f0811-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0811-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0811-107">DESCRIPTION</span></span>
<span data-ttu-id="f0811-108">С **его нажатием** можно восстановить ранее удаленную секретную.</span><span class="sxs-lookup"><span data-stu-id="f0811-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="f0811-109">Восстановленная секретная будет активна и ее можно использовать для всех обычных секретных операций.</span><span class="sxs-lookup"><span data-stu-id="f0811-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="f0811-110">Для выполнения этой операции вызываемму вызываемму звоня необходимо разрешение на восстановление.</span><span class="sxs-lookup"><span data-stu-id="f0811-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="f0811-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f0811-111">EXAMPLES</span></span>

### <span data-ttu-id="f0811-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0811-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'

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

<span data-ttu-id="f0811-113">Эта команда восстановит секретный "МойСекрет", который ранее был удален, в активное и можное состояние.</span><span class="sxs-lookup"><span data-stu-id="f0811-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="f0811-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0811-114">PARAMETERS</span></span>

### <span data-ttu-id="f0811-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0811-115">-DefaultProfile</span></span>
<span data-ttu-id="f0811-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f0811-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0811-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0811-117">-InputObject</span></span>
<span data-ttu-id="f0811-118">Удаленный секретный объект</span><span class="sxs-lookup"><span data-stu-id="f0811-118">Deleted secret object</span></span>

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

### <span data-ttu-id="f0811-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f0811-119">-Name</span></span>
<span data-ttu-id="f0811-120">Секретное имя.</span><span class="sxs-lookup"><span data-stu-id="f0811-120">Secret name.</span></span>
<span data-ttu-id="f0811-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span><span class="sxs-lookup"><span data-stu-id="f0811-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="f0811-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f0811-122">-VaultName</span></span>
<span data-ttu-id="f0811-123">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="f0811-123">Vault name.</span></span>
<span data-ttu-id="f0811-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="f0811-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f0811-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0811-125">-Confirm</span></span>
<span data-ttu-id="f0811-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f0811-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0811-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0811-127">-WhatIf</span></span>
<span data-ttu-id="f0811-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0811-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0811-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f0811-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0811-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0811-130">CommonParameters</span></span>
<span data-ttu-id="f0811-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0811-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0811-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0811-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0811-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0811-133">INPUTS</span></span>

### <span data-ttu-id="f0811-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f0811-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="f0811-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f0811-135">OUTPUTS</span></span>

### <span data-ttu-id="f0811-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f0811-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="f0811-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f0811-137">NOTES</span></span>

## <span data-ttu-id="f0811-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0811-138">RELATED LINKS</span></span>

[<span data-ttu-id="f0811-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f0811-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)


[<span data-ttu-id="f0811-140">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f0811-140">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
