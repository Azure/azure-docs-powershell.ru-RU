---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: 7b56e7d251aee8887fe408237d17d275cb87034e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720602"
---
# <span data-ttu-id="3a627-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="3a627-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="3a627-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a627-102">SYNOPSIS</span></span>
<span data-ttu-id="3a627-103">Восстановление ранее удаленного определения SAS из управляемого KeyVault хранилища.</span><span class="sxs-lookup"><span data-stu-id="3a627-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="3a627-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a627-104">SYNTAX</span></span>

### <span data-ttu-id="3a627-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3a627-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a627-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3a627-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a627-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a627-107">DESCRIPTION</span></span>
<span data-ttu-id="3a627-108">Команда **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** восстанавливает ранее удаленное определение управляемого сопоставления безопасности хранилища при условии, что для этого хранилища включена функция обратимого удаления, и что попытка восстановления выполняется в течение интервала восстановления.</span><span class="sxs-lookup"><span data-stu-id="3a627-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="3a627-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a627-109">EXAMPLES</span></span>

### <span data-ttu-id="3a627-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3a627-110">Example 1</span></span>
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

<span data-ttu-id="3a627-111">Эта последовательность команд определяет, существует ли указанное определение SAS хранилища в удаленном состоянии. Следующая команда воспроизводит восстановление удаленного определения SAS, переводя его в активное состояние.</span><span class="sxs-lookup"><span data-stu-id="3a627-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="3a627-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a627-112">PARAMETERS</span></span>

### <span data-ttu-id="3a627-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="3a627-113">-AccountName</span></span>
<span data-ttu-id="3a627-114">Имя учетной записи хранения, управляемой KeyVault.</span><span class="sxs-lookup"><span data-stu-id="3a627-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="3a627-115">Командлет создает полное доменное имя управляемого определения SAS хранилища из имени хранилища, в настоящее время выбранной среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3a627-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

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

### <span data-ttu-id="3a627-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a627-116">-DefaultProfile</span></span>
<span data-ttu-id="3a627-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a627-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a627-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a627-118">-InputObject</span></span>
<span data-ttu-id="3a627-119">Удален объект определения SAS управляемого хранилища</span><span class="sxs-lookup"><span data-stu-id="3a627-119">Deleted managed storage SAS definition object</span></span>

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

### <span data-ttu-id="3a627-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3a627-120">-Name</span></span>
<span data-ttu-id="3a627-121">Имя определения SAS хранилища, управляемого KeyVault.</span><span class="sxs-lookup"><span data-stu-id="3a627-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="3a627-122">Командлет создает полное доменное имя целевого объекта с имени хранилища, в настоящее время выбранной среды, именем управляемой учетной записи хранения и именем определения SAS.</span><span class="sxs-lookup"><span data-stu-id="3a627-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

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

### <span data-ttu-id="3a627-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3a627-123">-VaultName</span></span>
<span data-ttu-id="3a627-124">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="3a627-124">Vault name.</span></span>
<span data-ttu-id="3a627-125">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="3a627-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="3a627-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a627-126">-Confirm</span></span>
<span data-ttu-id="3a627-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3a627-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a627-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a627-128">-WhatIf</span></span>
<span data-ttu-id="3a627-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3a627-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a627-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3a627-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a627-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a627-131">CommonParameters</span></span>
<span data-ttu-id="3a627-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a627-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a627-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a627-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a627-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a627-134">INPUTS</span></span>

### <span data-ttu-id="3a627-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3a627-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="3a627-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a627-136">OUTPUTS</span></span>

### <span data-ttu-id="3a627-137">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="3a627-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="3a627-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a627-138">NOTES</span></span>

## <span data-ttu-id="3a627-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a627-139">RELATED LINKS</span></span>
