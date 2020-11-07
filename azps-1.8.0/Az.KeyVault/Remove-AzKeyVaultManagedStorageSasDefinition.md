---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 0fe20196f805f292ecc6b351fbb9138c6617bb4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900145"
---
# <span data-ttu-id="4984b-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="4984b-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="4984b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4984b-102">SYNOPSIS</span></span>
<span data-ttu-id="4984b-103">Удаляет определения SAS из хранилища ключей для управляемых хранилищ Azure.</span><span class="sxs-lookup"><span data-stu-id="4984b-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="4984b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4984b-104">SYNTAX</span></span>

### <span data-ttu-id="4984b-105">ByDefinitionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4984b-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4984b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4984b-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4984b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4984b-107">DESCRIPTION</span></span>
<span data-ttu-id="4984b-108">Удаляет определения SAS из хранилища ключей для управляемых хранилищ Azure.</span><span class="sxs-lookup"><span data-stu-id="4984b-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="4984b-109">Кроме того, он удаляет секрет, используемый для получения маркера SAS для этого определения SAS.</span><span class="sxs-lookup"><span data-stu-id="4984b-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="4984b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4984b-110">EXAMPLES</span></span>

### <span data-ttu-id="4984b-111">Пример 1: Удаление определения SAS хранилища управляемых хранилищ Azure с помощью хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="4984b-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="4984b-112">Удаляет из хранилища ключей определение SAS "mysasdef", связанного с учетной записью "mystorageaccount" в хранилище "myvault".</span><span class="sxs-lookup"><span data-stu-id="4984b-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="4984b-113">Пример 2: Удаление определения управляемого хранилища Azure с хранилищем ключей без подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="4984b-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru -Force

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="4984b-114">Удаляет из хранилища ключей определение SAS "mysasdef", связанного с учетной записью "mystorageaccount" в хранилище "myvault".</span><span class="sxs-lookup"><span data-stu-id="4984b-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="4984b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4984b-115">PARAMETERS</span></span>

### <span data-ttu-id="4984b-116">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="4984b-116">-AccountName</span></span>
<span data-ttu-id="4984b-117">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="4984b-117">Storage account name.</span></span>
<span data-ttu-id="4984b-118">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="4984b-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

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

### <span data-ttu-id="4984b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4984b-119">-DefaultProfile</span></span>
<span data-ttu-id="4984b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4984b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4984b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4984b-121">-Force</span></span>
<span data-ttu-id="4984b-122">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4984b-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4984b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4984b-123">-InputObject</span></span>
<span data-ttu-id="4984b-124">Объект ManagedStorageSasDefinition.</span><span class="sxs-lookup"><span data-stu-id="4984b-124">ManagedStorageSasDefinition object.</span></span>

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

### <span data-ttu-id="4984b-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4984b-125">-Name</span></span>
<span data-ttu-id="4984b-126">Имя определения SAS хранилища.</span><span class="sxs-lookup"><span data-stu-id="4984b-126">Storage sas definition name.</span></span>
<span data-ttu-id="4984b-127">Командлет создает полное доменное имя определения SAS хранилища из имени хранилища, выбранной среды, имени учетной записи хранения и имени определения SAS.</span><span class="sxs-lookup"><span data-stu-id="4984b-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="4984b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4984b-128">-PassThru</span></span>
<span data-ttu-id="4984b-129">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="4984b-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4984b-130">Если этот параметр указан, командлет возвращает управляемую учетную запись хранения, которая была удалена.</span><span class="sxs-lookup"><span data-stu-id="4984b-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="4984b-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4984b-131">-VaultName</span></span>
<span data-ttu-id="4984b-132">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="4984b-132">Vault name.</span></span>
<span data-ttu-id="4984b-133">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="4984b-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="4984b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4984b-134">-Confirm</span></span>
<span data-ttu-id="4984b-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4984b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4984b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4984b-136">-WhatIf</span></span>
<span data-ttu-id="4984b-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4984b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4984b-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4984b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4984b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4984b-139">CommonParameters</span></span>
<span data-ttu-id="4984b-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4984b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4984b-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4984b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4984b-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4984b-142">INPUTS</span></span>

### <span data-ttu-id="4984b-143">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4984b-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="4984b-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4984b-144">OUTPUTS</span></span>

### <span data-ttu-id="4984b-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="4984b-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="4984b-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="4984b-146">NOTES</span></span>

## <span data-ttu-id="4984b-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4984b-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

