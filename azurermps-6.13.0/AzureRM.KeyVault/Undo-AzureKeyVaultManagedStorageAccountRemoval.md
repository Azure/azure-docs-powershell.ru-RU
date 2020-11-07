---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: a8e8bb9a4a006c30275f1de959181ad640a04f88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734649"
---
# <span data-ttu-id="4e406-101">Undo-AzureKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="4e406-101">Undo-AzureKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="4e406-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e406-102">SYNOPSIS</span></span>
<span data-ttu-id="4e406-103">Восстановление ранее удаленной учетной записи хранения, управляемой KeyVault.</span><span class="sxs-lookup"><span data-stu-id="4e406-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e406-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e406-104">SYNTAX</span></span>

### <span data-ttu-id="4e406-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e406-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e406-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4e406-106">InputObject</span></span>
```
Undo-AzureKeyVaultManagedStorageAccountRemoval
 [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e406-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e406-107">DESCRIPTION</span></span>
<span data-ttu-id="4e406-108">Команда **Undo-AzureKeyVaultManagedStorageAccountRemoval** восстанавливает ранее удаленную учетную запись хранения, при условии, что для этого хранилища включена функция обратимого удаления и что при восстановлении происходит попытка восстановления.</span><span class="sxs-lookup"><span data-stu-id="4e406-108">The **Undo-AzureKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="4e406-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e406-109">EXAMPLES</span></span>

### <span data-ttu-id="4e406-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e406-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName myVault -Name myAccount -InRemovedState
PS C:\> Undo-AzureKeyVaultManagedStorageAccountRemoval -VaultName myVault -Name myAccount

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

<span data-ttu-id="4e406-111">Эта последовательность команд определяет, существует ли указанная учетная запись хранения в удаленном состоянии. Следующая команда воспроизводит восстановление удаленной учетной записи хранения, переводя ее в активное состояние.</span><span class="sxs-lookup"><span data-stu-id="4e406-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="4e406-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e406-112">PARAMETERS</span></span>

### <span data-ttu-id="4e406-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e406-113">-DefaultProfile</span></span>
<span data-ttu-id="4e406-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e406-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e406-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e406-115">-InputObject</span></span>
<span data-ttu-id="4e406-116">Удален управляемый объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="4e406-116">Deleted Managed Storage Account object</span></span>

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

### <span data-ttu-id="4e406-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e406-117">-Name</span></span>
<span data-ttu-id="4e406-118">Имя учетной записи хранения, управляемой KeyVault.</span><span class="sxs-lookup"><span data-stu-id="4e406-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="4e406-119">Командлет создает полное доменное имя целевого объекта с имени хранилища, выбранной в данный момент среды и именем управляемой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="4e406-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

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

### <span data-ttu-id="4e406-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4e406-120">-VaultName</span></span>
<span data-ttu-id="4e406-121">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="4e406-121">Vault name.</span></span>
<span data-ttu-id="4e406-122">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="4e406-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="4e406-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e406-123">-Confirm</span></span>
<span data-ttu-id="4e406-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e406-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e406-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e406-125">-WhatIf</span></span>
<span data-ttu-id="4e406-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e406-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e406-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e406-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e406-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e406-128">CommonParameters</span></span>
<span data-ttu-id="4e406-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e406-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e406-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e406-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e406-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e406-131">INPUTS</span></span>

### <span data-ttu-id="4e406-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4e406-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="4e406-133">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4e406-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4e406-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e406-134">OUTPUTS</span></span>

### <span data-ttu-id="4e406-135">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4e406-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="4e406-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e406-136">NOTES</span></span>

## <span data-ttu-id="4e406-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e406-137">RELATED LINKS</span></span>
