---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 1eca5a380dc71a5bd801c21bb7e7f556fcff0d35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394468"
---
# <span data-ttu-id="bcfb1-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="bcfb1-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="bcfb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcfb1-102">SYNOPSIS</span></span>
<span data-ttu-id="bcfb1-103">Восстановление удаленной секретной секретной области в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="bcfb1-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="bcfb1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bcfb1-104">SYNTAX</span></span>

### <span data-ttu-id="bcfb1-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bcfb1-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcfb1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bcfb1-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcfb1-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcfb1-107">DESCRIPTION</span></span>
<span data-ttu-id="bcfb1-108">С **его нажатием** можно восстановить ранее удаленную секретную.</span><span class="sxs-lookup"><span data-stu-id="bcfb1-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="bcfb1-109">Восстановленная секретная будет активна и ее можно использовать для всех обычных секретных операций.</span><span class="sxs-lookup"><span data-stu-id="bcfb1-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="bcfb1-110">Для выполнения этой операции вызываемму вызываемму звоня необходимо разрешение на восстановление.</span><span class="sxs-lookup"><span data-stu-id="bcfb1-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="bcfb1-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bcfb1-111">EXAMPLES</span></span>

### <span data-ttu-id="bcfb1-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bcfb1-112">Example 1</span></span>
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

<span data-ttu-id="bcfb1-113">Эта команда восстановит секретный "МойСекрет", который ранее был удален, в активное состояние.</span><span class="sxs-lookup"><span data-stu-id="bcfb1-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="bcfb1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcfb1-114">PARAMETERS</span></span>

### <span data-ttu-id="bcfb1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcfb1-115">-DefaultProfile</span></span>
<span data-ttu-id="bcfb1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bcfb1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcfb1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcfb1-117">-InputObject</span></span>
<span data-ttu-id="bcfb1-118">Удаленный секретный объект</span><span class="sxs-lookup"><span data-stu-id="bcfb1-118">Deleted secret object</span></span>

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

### <span data-ttu-id="bcfb1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bcfb1-119">-Name</span></span>
<span data-ttu-id="bcfb1-120">Секретное имя.</span><span class="sxs-lookup"><span data-stu-id="bcfb1-120">Secret name.</span></span>
<span data-ttu-id="bcfb1-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span><span class="sxs-lookup"><span data-stu-id="bcfb1-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="bcfb1-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bcfb1-122">-VaultName</span></span>
<span data-ttu-id="bcfb1-123">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="bcfb1-123">Vault name.</span></span>
<span data-ttu-id="bcfb1-124">С его учетом именем и выбранной средой строится FQDN хранилища.</span><span class="sxs-lookup"><span data-stu-id="bcfb1-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="bcfb1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcfb1-125">-Confirm</span></span>
<span data-ttu-id="bcfb1-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bcfb1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcfb1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcfb1-127">-WhatIf</span></span>
<span data-ttu-id="bcfb1-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcfb1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcfb1-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bcfb1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcfb1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcfb1-130">CommonParameters</span></span>
<span data-ttu-id="bcfb1-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcfb1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcfb1-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcfb1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcfb1-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bcfb1-133">INPUTS</span></span>

### <span data-ttu-id="bcfb1-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bcfb1-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="bcfb1-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bcfb1-135">OUTPUTS</span></span>

### <span data-ttu-id="bcfb1-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="bcfb1-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="bcfb1-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bcfb1-137">NOTES</span></span>

## <span data-ttu-id="bcfb1-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcfb1-138">RELATED LINKS</span></span>

[<span data-ttu-id="bcfb1-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="bcfb1-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="bcfb1-140">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="bcfb1-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="bcfb1-141">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="bcfb1-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
