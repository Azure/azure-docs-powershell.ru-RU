---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: bb44bc8f5e4537691d1e5d5493a29111ceaf42a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506258"
---
# <span data-ttu-id="412ae-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="412ae-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="412ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="412ae-102">SYNOPSIS</span></span>
<span data-ttu-id="412ae-103">Восстановление ранее удаленного определения SAS хранилища, управляемого KeyVault.</span><span class="sxs-lookup"><span data-stu-id="412ae-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="412ae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="412ae-104">SYNTAX</span></span>

### <span data-ttu-id="412ae-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="412ae-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="412ae-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="412ae-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="412ae-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="412ae-107">DESCRIPTION</span></span>
<span data-ttu-id="412ae-108">Команда **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** восстанавливает ранее удаленное определение SAS хранилища, если для этого хранилища включено soft delete и что попытка восстановления происходит во время интервала восстановления.</span><span class="sxs-lookup"><span data-stu-id="412ae-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="412ae-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="412ae-109">EXAMPLES</span></span>

### <span data-ttu-id="412ae-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="412ae-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName myVault -AccountName myAccount -Name mySasName -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageSasDefinitionRemoval -VaultName myVault -AccountName myAccount -Name mySasName

Id          : https://myvault.vault.azure.net:443/storage/myaccount/sas/mysasname
Secret Id   : https://myvault.vault.azure.net/secrets/myaccount-mysasname
Vault Name  : myVault
AccountName : myAccount
Name        : mySasName
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="412ae-111">Эта последовательность команд определяет, существует ли указанное определение SAS хранилища в хранилище в удаленном состоянии. После этого удаленная команда восстановит определение sas и снова активна.</span><span class="sxs-lookup"><span data-stu-id="412ae-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="412ae-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="412ae-112">PARAMETERS</span></span>

### <span data-ttu-id="412ae-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="412ae-113">-AccountName</span></span>
<span data-ttu-id="412ae-114">Имя учетной записи хранения, управляемой KeyVault.</span><span class="sxs-lookup"><span data-stu-id="412ae-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="412ae-115">С его учетной записью можно определить SAS управляемого хранилища из имени хранилища, выбранной среды и имени учетной записи управляемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="412ae-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="412ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="412ae-116">-DefaultProfile</span></span>
<span data-ttu-id="412ae-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="412ae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="412ae-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="412ae-118">-InputObject</span></span>
<span data-ttu-id="412ae-119">Удален объект определения SAS для управляемого хранилища</span><span class="sxs-lookup"><span data-stu-id="412ae-119">Deleted managed storage SAS definition object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="412ae-120">-Name</span><span class="sxs-lookup"><span data-stu-id="412ae-120">-Name</span></span>
<span data-ttu-id="412ae-121">Имя определения SAS хранилища, управляемого KeyVault.</span><span class="sxs-lookup"><span data-stu-id="412ae-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="412ae-122">С его учетной записью можно определить FQDN конечного хранилища из имени хранилища, выбранной среды, имени учетной записи управляемого хранилища и имени определения SAS.</span><span class="sxs-lookup"><span data-stu-id="412ae-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="412ae-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="412ae-123">-VaultName</span></span>
<span data-ttu-id="412ae-124">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="412ae-124">Vault name.</span></span>
<span data-ttu-id="412ae-125">С его учетом именем и выбранной средой строится FQDN хранилища.</span><span class="sxs-lookup"><span data-stu-id="412ae-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="412ae-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="412ae-126">-Confirm</span></span>
<span data-ttu-id="412ae-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="412ae-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="412ae-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="412ae-128">-WhatIf</span></span>
<span data-ttu-id="412ae-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="412ae-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="412ae-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="412ae-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="412ae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="412ae-131">CommonParameters</span></span>
<span data-ttu-id="412ae-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="412ae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="412ae-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="412ae-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="412ae-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="412ae-134">INPUTS</span></span>

### <span data-ttu-id="412ae-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="412ae-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="412ae-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="412ae-136">OUTPUTS</span></span>

### <span data-ttu-id="412ae-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="412ae-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="412ae-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="412ae-138">NOTES</span></span>

## <span data-ttu-id="412ae-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="412ae-139">RELATED LINKS</span></span>
