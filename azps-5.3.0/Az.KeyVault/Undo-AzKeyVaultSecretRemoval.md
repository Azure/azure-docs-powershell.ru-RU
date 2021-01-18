---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 1eca5a380dc71a5bd801c21bb7e7f556fcff0d35
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518330"
---
# <span data-ttu-id="ebc7e-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="ebc7e-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="ebc7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebc7e-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc7e-103">Восстановление удаленной секретной секретной фигуры в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="ebc7e-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="ebc7e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ebc7e-104">SYNTAX</span></span>

### <span data-ttu-id="ebc7e-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ebc7e-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebc7e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ebc7e-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebc7e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebc7e-107">DESCRIPTION</span></span>
<span data-ttu-id="ebc7e-108">С **его нажатием** можно восстановить ранее удаленную секретную.</span><span class="sxs-lookup"><span data-stu-id="ebc7e-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="ebc7e-109">Восстановленная секретная будет активна и ее можно использовать для всех обычных секретных операций.</span><span class="sxs-lookup"><span data-stu-id="ebc7e-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="ebc7e-110">Для выполнения этой операции вызываемму вызываемму звоня необходимо разрешение на восстановление.</span><span class="sxs-lookup"><span data-stu-id="ebc7e-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="ebc7e-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ebc7e-111">EXAMPLES</span></span>

### <span data-ttu-id="ebc7e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ebc7e-112">Example 1</span></span>
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

<span data-ttu-id="ebc7e-113">Эта команда восстановит секретный "МойСекрет", который ранее был удален, в активное и можное состояние.</span><span class="sxs-lookup"><span data-stu-id="ebc7e-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="ebc7e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebc7e-114">PARAMETERS</span></span>

### <span data-ttu-id="ebc7e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc7e-115">-DefaultProfile</span></span>
<span data-ttu-id="ebc7e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ebc7e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebc7e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebc7e-117">-InputObject</span></span>
<span data-ttu-id="ebc7e-118">Удаленный секретный объект</span><span class="sxs-lookup"><span data-stu-id="ebc7e-118">Deleted secret object</span></span>

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

### <span data-ttu-id="ebc7e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ebc7e-119">-Name</span></span>
<span data-ttu-id="ebc7e-120">Секретное имя.</span><span class="sxs-lookup"><span data-stu-id="ebc7e-120">Secret name.</span></span>
<span data-ttu-id="ebc7e-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span><span class="sxs-lookup"><span data-stu-id="ebc7e-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="ebc7e-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ebc7e-122">-VaultName</span></span>
<span data-ttu-id="ebc7e-123">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="ebc7e-123">Vault name.</span></span>
<span data-ttu-id="ebc7e-124">С его учетом именем и выбранной средой строится FQDN хранилища.</span><span class="sxs-lookup"><span data-stu-id="ebc7e-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ebc7e-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebc7e-125">-Confirm</span></span>
<span data-ttu-id="ebc7e-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebc7e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebc7e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebc7e-127">-WhatIf</span></span>
<span data-ttu-id="ebc7e-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebc7e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebc7e-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ebc7e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebc7e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc7e-130">CommonParameters</span></span>
<span data-ttu-id="ebc7e-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebc7e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc7e-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebc7e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc7e-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebc7e-133">INPUTS</span></span>

### <span data-ttu-id="ebc7e-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ebc7e-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="ebc7e-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ebc7e-135">OUTPUTS</span></span>

### <span data-ttu-id="ebc7e-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ebc7e-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="ebc7e-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ebc7e-137">NOTES</span></span>

## <span data-ttu-id="ebc7e-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebc7e-138">RELATED LINKS</span></span>

[<span data-ttu-id="ebc7e-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ebc7e-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="ebc7e-140">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ebc7e-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="ebc7e-141">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ebc7e-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
