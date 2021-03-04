---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 552a696a31b8c5fb26a1c6a17434ef53380d0491
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001480"
---
# <span data-ttu-id="9a040-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a040-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="9a040-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a040-102">SYNOPSIS</span></span>
<span data-ttu-id="9a040-103">Получает основные учетные записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="9a040-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="9a040-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9a040-104">SYNTAX</span></span>

### <span data-ttu-id="9a040-105">ByAccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a040-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a040-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9a040-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a040-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9a040-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a040-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a040-108">DESCRIPTION</span></span>
<span data-ttu-id="9a040-109">Получает учетную запись хранилища Azure, управлия ключом, если задано имя учетной записи и управление ключами учетной записи происходит в указанном хранилище.</span><span class="sxs-lookup"><span data-stu-id="9a040-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="9a040-110">Если имя учетной записи не указано, будут перечислены все учетные записи, ключами которых управляет указанный сейф.</span><span class="sxs-lookup"><span data-stu-id="9a040-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="9a040-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9a040-111">EXAMPLES</span></span>

### <span data-ttu-id="9a040-112">Пример 1. Список всех ключевых учетных записей хранилища, управляемых хранилищем</span><span class="sxs-lookup"><span data-stu-id="9a040-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="9a040-113">Список всех учетных записей, ключами которых управляет хранилище Myvault.</span><span class="sxs-lookup"><span data-stu-id="9a040-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="9a040-114">Пример 2. Получить учетную запись хранения в key Vault</span><span class="sxs-lookup"><span data-stu-id="9a040-114">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/maddie1/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="9a040-115">Подробные сведения о учетной записи хранилища mystorageaccount, если ключами управляет хранилище "myvault".</span><span class="sxs-lookup"><span data-stu-id="9a040-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="9a040-116">Пример 3. Список всех ключевых учетных записей хранилища, управляемых хранилищем, с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="9a040-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name "test*"

Id                  : https://myvault.vault.azure.net:443/storage/test1
Vault Name          : myvault
AccountName         : test1
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test1
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :

Id                  : https://myvault.vault.azure.net:443/storage/test2
Vault Name          : myvault
AccountName         : test2
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test2
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="9a040-117">Список всех учетных записей, ключами которых управляет хранилище Myvault, которые начинаются с "test"</span><span class="sxs-lookup"><span data-stu-id="9a040-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="9a040-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a040-118">PARAMETERS</span></span>

### <span data-ttu-id="9a040-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9a040-119">-AccountName</span></span>
<span data-ttu-id="9a040-120">Имя учетной записи управляемого хранилища в key Vault.</span><span class="sxs-lookup"><span data-stu-id="9a040-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="9a040-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span><span class="sxs-lookup"><span data-stu-id="9a040-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="9a040-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a040-122">-DefaultProfile</span></span>
<span data-ttu-id="9a040-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9a040-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a040-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a040-124">-InputObject</span></span>
<span data-ttu-id="9a040-125">Объект Vault.</span><span class="sxs-lookup"><span data-stu-id="9a040-125">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a040-126">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="9a040-126">-InRemovedState</span></span>
<span data-ttu-id="9a040-127">Указывает, следует ли показывать ранее удаленные учетные записи хранения в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9a040-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="9a040-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a040-128">-ResourceId</span></span>
<span data-ttu-id="9a040-129">ИД ресурса хранилища.</span><span class="sxs-lookup"><span data-stu-id="9a040-129">Vault resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a040-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9a040-130">-VaultName</span></span>
<span data-ttu-id="9a040-131">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="9a040-131">Vault name.</span></span>
<span data-ttu-id="9a040-132">С его учетом именем и выбранной средой строится FQDN хранилища.</span><span class="sxs-lookup"><span data-stu-id="9a040-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a040-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a040-133">CommonParameters</span></span>
<span data-ttu-id="9a040-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a040-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a040-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a040-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a040-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a040-136">INPUTS</span></span>

### <span data-ttu-id="9a040-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="9a040-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="9a040-138">System.String</span><span class="sxs-lookup"><span data-stu-id="9a040-138">System.String</span></span>

## <span data-ttu-id="9a040-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a040-139">OUTPUTS</span></span>

### <span data-ttu-id="9a040-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9a040-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="9a040-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a040-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="9a040-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9a040-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="9a040-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a040-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="9a040-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9a040-144">NOTES</span></span>

## <span data-ttu-id="9a040-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a040-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

