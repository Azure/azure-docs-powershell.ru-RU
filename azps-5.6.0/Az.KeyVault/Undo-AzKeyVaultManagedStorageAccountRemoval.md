---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: 289adecd07837134fed9279758cf1142d30183a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010467"
---
# <span data-ttu-id="6315f-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="6315f-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="6315f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6315f-102">SYNOPSIS</span></span>
<span data-ttu-id="6315f-103">Восстановление ранее удаленной учетной записи хранения, управляемой KeyVault.</span><span class="sxs-lookup"><span data-stu-id="6315f-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

## <span data-ttu-id="6315f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6315f-104">SYNTAX</span></span>

### <span data-ttu-id="6315f-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6315f-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6315f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6315f-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6315f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6315f-107">DESCRIPTION</span></span>
<span data-ttu-id="6315f-108">Команда **Undo-AzKeyVaultManagedStorageAccountRemoval** восстанавливает ранее удаленную учетную запись управляемого хранилища, если для этого хранилища включено soft delete и что попытка восстановления происходит во время интервала восстановления.</span><span class="sxs-lookup"><span data-stu-id="6315f-108">The **Undo-AzKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="6315f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6315f-109">EXAMPLES</span></span>

### <span data-ttu-id="6315f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6315f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName myVault -Name myAccount -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageAccountRemoval -VaultName myVault -Name myAccount

Id                  : https://myvault.vault.azure.net:443/storage/myaccount
Vault Name          : myVault
AccountName         : myAccount
Account Resource Id : /subscriptions/8bc48661-1801-4b7a-8ca1-6a3cadfb4870/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/myaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="6315f-111">Эта последовательность команд определяет, существует ли указанная учетная запись хранения в хранилище в удаленном состоянии. После этого удаленная учетная запись хранилища будет восстановлена, а затем снова активна.</span><span class="sxs-lookup"><span data-stu-id="6315f-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="6315f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6315f-112">PARAMETERS</span></span>

### <span data-ttu-id="6315f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6315f-113">-DefaultProfile</span></span>
<span data-ttu-id="6315f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6315f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6315f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6315f-115">-InputObject</span></span>
<span data-ttu-id="6315f-116">Удален объект учетной записи управляемого хранения</span><span class="sxs-lookup"><span data-stu-id="6315f-116">Deleted Managed Storage Account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6315f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6315f-117">-Name</span></span>
<span data-ttu-id="6315f-118">Имя учетной записи хранения, управляемой KeyVault.</span><span class="sxs-lookup"><span data-stu-id="6315f-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="6315f-119">С его учетной записью можно создать FQDN целевого хранилища из имени хранилища, выбранной в текущий момент среды и учетной записи управляемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="6315f-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6315f-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6315f-120">-VaultName</span></span>
<span data-ttu-id="6315f-121">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="6315f-121">Vault name.</span></span>
<span data-ttu-id="6315f-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="6315f-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="6315f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6315f-123">-Confirm</span></span>
<span data-ttu-id="6315f-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6315f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6315f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6315f-125">-WhatIf</span></span>
<span data-ttu-id="6315f-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6315f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6315f-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6315f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6315f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6315f-128">CommonParameters</span></span>
<span data-ttu-id="6315f-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6315f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6315f-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6315f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6315f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6315f-131">INPUTS</span></span>

### <span data-ttu-id="6315f-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6315f-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="6315f-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6315f-133">OUTPUTS</span></span>

### <span data-ttu-id="6315f-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6315f-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="6315f-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6315f-135">NOTES</span></span>

## <span data-ttu-id="6315f-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6315f-136">RELATED LINKS</span></span>
