---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: 3d854d6b820f6c2e23d99e3397173ec45d5b7697
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219516"
---
# <span data-ttu-id="8a709-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="8a709-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="8a709-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a709-102">SYNOPSIS</span></span>
<span data-ttu-id="8a709-103">Восстановление ранее удаленной учетной записи хранения, управляемой KeyVault.</span><span class="sxs-lookup"><span data-stu-id="8a709-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

## <span data-ttu-id="8a709-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8a709-104">SYNTAX</span></span>

### <span data-ttu-id="8a709-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8a709-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a709-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8a709-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a709-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a709-107">DESCRIPTION</span></span>
<span data-ttu-id="8a709-108">Команда **Undo-AzKeyVaultManagedStorageAccountRemoval** восстанавливает ранее удаленную учетную запись управляемого хранилища, если для этого хранилища включено soft delete и что попытка восстановления происходит во время интервала восстановления.</span><span class="sxs-lookup"><span data-stu-id="8a709-108">The **Undo-AzKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="8a709-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8a709-109">EXAMPLES</span></span>

### <span data-ttu-id="8a709-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8a709-110">Example 1</span></span>
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

<span data-ttu-id="8a709-111">Эта последовательность команд определяет, существует ли указанная учетная запись хранения в хранилище в удаленном состоянии. После этого удаленная учетная запись хранилища будет восстановлена, а затем снова активна.</span><span class="sxs-lookup"><span data-stu-id="8a709-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="8a709-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a709-112">PARAMETERS</span></span>

### <span data-ttu-id="8a709-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a709-113">-DefaultProfile</span></span>
<span data-ttu-id="8a709-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a709-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a709-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a709-115">-InputObject</span></span>
<span data-ttu-id="8a709-116">Удален объект учетной записи управляемого хранения</span><span class="sxs-lookup"><span data-stu-id="8a709-116">Deleted Managed Storage Account object</span></span>

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

### <span data-ttu-id="8a709-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8a709-117">-Name</span></span>
<span data-ttu-id="8a709-118">Имя учетной записи хранения KeyVault.</span><span class="sxs-lookup"><span data-stu-id="8a709-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="8a709-119">С его учетной записью можно создать FQDN целевого хранилища из имени хранилища, выбранной в текущий момент среды и учетной записи управляемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="8a709-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

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

### <span data-ttu-id="8a709-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8a709-120">-VaultName</span></span>
<span data-ttu-id="8a709-121">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="8a709-121">Vault name.</span></span>
<span data-ttu-id="8a709-122">С его учетом именем и выбранной средой строится FQDN хранилища.</span><span class="sxs-lookup"><span data-stu-id="8a709-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8a709-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a709-123">-Confirm</span></span>
<span data-ttu-id="8a709-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a709-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a709-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a709-125">-WhatIf</span></span>
<span data-ttu-id="8a709-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a709-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a709-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8a709-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a709-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a709-128">CommonParameters</span></span>
<span data-ttu-id="8a709-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a709-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a709-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a709-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a709-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a709-131">INPUTS</span></span>

### <span data-ttu-id="8a709-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8a709-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="8a709-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8a709-133">OUTPUTS</span></span>

### <span data-ttu-id="8a709-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8a709-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="8a709-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8a709-135">NOTES</span></span>

## <span data-ttu-id="8a709-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a709-136">RELATED LINKS</span></span>
