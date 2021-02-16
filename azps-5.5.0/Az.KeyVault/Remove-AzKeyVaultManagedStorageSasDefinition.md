---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 392c8aa5259419851d3cb85967ddf85afa3c94de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226417"
---
# <span data-ttu-id="011fc-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="011fc-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="011fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="011fc-102">SYNOPSIS</span></span>
<span data-ttu-id="011fc-103">Удаляет определения SAS хранилища Azure, управляемые хранилищем.</span><span class="sxs-lookup"><span data-stu-id="011fc-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="011fc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="011fc-104">SYNTAX</span></span>

### <span data-ttu-id="011fc-105">ByDefinitionName (Default)</span><span class="sxs-lookup"><span data-stu-id="011fc-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="011fc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="011fc-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="011fc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="011fc-107">DESCRIPTION</span></span>
<span data-ttu-id="011fc-108">Удаляет определения SAS хранилища Azure, управляемые хранилищем.</span><span class="sxs-lookup"><span data-stu-id="011fc-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="011fc-109">При этом также удаляется секрет, используемый для получения маркера SAS для этого определения SAS.</span><span class="sxs-lookup"><span data-stu-id="011fc-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="011fc-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="011fc-110">EXAMPLES</span></span>

### <span data-ttu-id="011fc-111">Пример 1. Удаление определения SAS хранилища Azure, управляемого ключом.</span><span class="sxs-lookup"><span data-stu-id="011fc-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="011fc-112">Удаляет определение SAS хранилища, связанное с учетной записью mystorageaccount в хранилище myvault.</span><span class="sxs-lookup"><span data-stu-id="011fc-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="011fc-113">Пример 2. Удаление определения SAS хранилища Azure, управляемого хранилищем Azure, без подтверждения пользователем.</span><span class="sxs-lookup"><span data-stu-id="011fc-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru -Force

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="011fc-114">Удаляет определение SAS хранилища, связанное с учетной записью mystorageaccount в хранилище myvault.</span><span class="sxs-lookup"><span data-stu-id="011fc-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="011fc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="011fc-115">PARAMETERS</span></span>

### <span data-ttu-id="011fc-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="011fc-116">-AccountName</span></span>
<span data-ttu-id="011fc-117">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="011fc-117">Storage account name.</span></span>
<span data-ttu-id="011fc-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span><span class="sxs-lookup"><span data-stu-id="011fc-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="011fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="011fc-119">-DefaultProfile</span></span>
<span data-ttu-id="011fc-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="011fc-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="011fc-121">-Force</span><span class="sxs-lookup"><span data-stu-id="011fc-121">-Force</span></span>
<span data-ttu-id="011fc-122">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="011fc-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="011fc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="011fc-123">-InputObject</span></span>
<span data-ttu-id="011fc-124">Объект ManagedStorageSasDefinition.</span><span class="sxs-lookup"><span data-stu-id="011fc-124">ManagedStorageSasDefinition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="011fc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="011fc-125">-Name</span></span>
<span data-ttu-id="011fc-126">Имя определения sas хранилища.</span><span class="sxs-lookup"><span data-stu-id="011fc-126">Storage sas definition name.</span></span>
<span data-ttu-id="011fc-127">Cmdlet конструировать FQDN определения sas хранилища из имени хранилища, выбранной среды, имени учетной записи хранения и имени определения sas.</span><span class="sxs-lookup"><span data-stu-id="011fc-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="011fc-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="011fc-128">-PassThru</span></span>
<span data-ttu-id="011fc-129">По умолчанию cmdlet не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="011fc-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="011fc-130">Если этот переключатель задан, возвращается удаленная учетная запись управляемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="011fc-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="011fc-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="011fc-131">-VaultName</span></span>
<span data-ttu-id="011fc-132">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="011fc-132">Vault name.</span></span>
<span data-ttu-id="011fc-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="011fc-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="011fc-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="011fc-134">-Confirm</span></span>
<span data-ttu-id="011fc-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="011fc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="011fc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="011fc-136">-WhatIf</span></span>
<span data-ttu-id="011fc-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="011fc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="011fc-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="011fc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="011fc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="011fc-139">CommonParameters</span></span>
<span data-ttu-id="011fc-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="011fc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="011fc-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="011fc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="011fc-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="011fc-142">INPUTS</span></span>

### <span data-ttu-id="011fc-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="011fc-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="011fc-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="011fc-144">OUTPUTS</span></span>

### <span data-ttu-id="011fc-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="011fc-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="011fc-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="011fc-146">NOTES</span></span>

## <span data-ttu-id="011fc-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="011fc-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

