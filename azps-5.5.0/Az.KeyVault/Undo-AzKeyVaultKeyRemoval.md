---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: d6637b8c180dd2ef25bdba5326f0a42a364bc8ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219521"
---
# <span data-ttu-id="1faa5-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="1faa5-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="1faa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1faa5-102">SYNOPSIS</span></span>
<span data-ttu-id="1faa5-103">Восстановление удаленного ключа в сейфе ключа в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="1faa5-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="1faa5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1faa5-104">SYNTAX</span></span>

### <span data-ttu-id="1faa5-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1faa5-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1faa5-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="1faa5-106">HsmInteractive</span></span>
```
Undo-AzKeyVaultKeyRemoval -HsmName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1faa5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="1faa5-107">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1faa5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1faa5-108">DESCRIPTION</span></span>
<span data-ttu-id="1faa5-109">Для восстановления ранее удаленного ключа будет восстановлен ранее удаленный **cmdlet Undo-AzKeyVaultKeyRemoval.**</span><span class="sxs-lookup"><span data-stu-id="1faa5-109">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="1faa5-110">Восстановленный ключ будет активен и может использоваться для всех обычных операций.</span><span class="sxs-lookup"><span data-stu-id="1faa5-110">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="1faa5-111">Для выполнения этой операции вызываемму вызываемму звоня необходимо разрешение на восстановление.</span><span class="sxs-lookup"><span data-stu-id="1faa5-111">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="1faa5-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1faa5-112">EXAMPLES</span></span>

### <span data-ttu-id="1faa5-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1faa5-113">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'

Vault Name     : MyKeyVault
Name           : MyKey
Version        : 1af807cc331a49d0b52b7c75e1b2366e
Id             : https://mykeybault.vault.azure.net:443/keys/mykey/1af807cc331a49d0b52b7c75e1b2366e
Enabled        : True
Expires        :
Not Before     :
Created        : 5/24/2018 8:32:27 PM
Updated        : 5/24/2018 8:32:27 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="1faa5-114">Эта команда восстановит ранее удаленный ключ MyKey в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="1faa5-114">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="1faa5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1faa5-115">PARAMETERS</span></span>

### <span data-ttu-id="1faa5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1faa5-116">-DefaultProfile</span></span>
<span data-ttu-id="1faa5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1faa5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1faa5-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="1faa5-118">-HsmName</span></span>
<span data-ttu-id="1faa5-119">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="1faa5-119">HSM name.</span></span> <span data-ttu-id="1faa5-120">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="1faa5-120">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1faa5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1faa5-121">-InputObject</span></span>
<span data-ttu-id="1faa5-122">Удаленный ключевой объект</span><span class="sxs-lookup"><span data-stu-id="1faa5-122">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1faa5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1faa5-123">-Name</span></span>
<span data-ttu-id="1faa5-124">Имя ключа.</span><span class="sxs-lookup"><span data-stu-id="1faa5-124">Key name.</span></span>
<span data-ttu-id="1faa5-125">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span><span class="sxs-lookup"><span data-stu-id="1faa5-125">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1faa5-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1faa5-126">-VaultName</span></span>
<span data-ttu-id="1faa5-127">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="1faa5-127">Vault name.</span></span>
<span data-ttu-id="1faa5-128">С его учетом именем и выбранной средой строится FQDN хранилища.</span><span class="sxs-lookup"><span data-stu-id="1faa5-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="1faa5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1faa5-129">-Confirm</span></span>
<span data-ttu-id="1faa5-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1faa5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1faa5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1faa5-131">-WhatIf</span></span>
<span data-ttu-id="1faa5-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1faa5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1faa5-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1faa5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1faa5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1faa5-134">CommonParameters</span></span>
<span data-ttu-id="1faa5-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1faa5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1faa5-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1faa5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1faa5-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1faa5-137">INPUTS</span></span>

### <span data-ttu-id="1faa5-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1faa5-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="1faa5-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1faa5-139">OUTPUTS</span></span>

### <span data-ttu-id="1faa5-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1faa5-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="1faa5-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1faa5-141">NOTES</span></span>

## <span data-ttu-id="1faa5-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1faa5-142">RELATED LINKS</span></span>

[<span data-ttu-id="1faa5-143">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1faa5-143">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="1faa5-144">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1faa5-144">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="1faa5-145">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1faa5-145">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

