---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 6e7cbaf9ed6e9f0d9751e8e16004891a7fcbb056
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065159"
---
# <span data-ttu-id="8fe6c-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fe6c-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="8fe6c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8fe6c-102">SYNOPSIS</span></span>
<span data-ttu-id="8fe6c-103">Получение управляемых учетных записей хранилища Azure для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="8fe6c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8fe6c-104">SYNTAX</span></span>

### <span data-ttu-id="8fe6c-105">ByAccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8fe6c-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fe6c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8fe6c-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fe6c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8fe6c-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fe6c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fe6c-108">DESCRIPTION</span></span>
<span data-ttu-id="8fe6c-109">Возвращает управляемую учетную запись хранилища Azure с основным хранилищем, если указано имя учетной записи, а ключи учетной записи управляются указанным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="8fe6c-110">Если имя учетной записи не указано, перечисляются все учетные записи, для которых управление ключами задается указанным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="8fe6c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8fe6c-111">EXAMPLES</span></span>

### <span data-ttu-id="8fe6c-112">Пример 1: список всех учетных записей хранения с управляемым хранилищем</span><span class="sxs-lookup"><span data-stu-id="8fe6c-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
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

<span data-ttu-id="8fe6c-113">Выводит все учетные записи, для которых управление ключами является хранилищем "myvault".</span><span class="sxs-lookup"><span data-stu-id="8fe6c-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="8fe6c-114">Пример 2: получение учетной записи хранилища с управляемым хранилищем ключей</span><span class="sxs-lookup"><span data-stu-id="8fe6c-114">Example 2: Get a Key Vault managed Storage Account</span></span>
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

<span data-ttu-id="8fe6c-115">Получение сведений об учетной записи хранения ключа управляемого хранилища для "mystorageaccount", если ее ключи управляются хранилищем "myvault"</span><span class="sxs-lookup"><span data-stu-id="8fe6c-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="8fe6c-116">Пример 3. Перечислите все учетные записи хранилища с управляемым хранилищем с помощью фильтрации.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
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

<span data-ttu-id="8fe6c-117">Список всех учетных записей, чьи ключи управляются хранилищем "myvault" и начинается с "Test".</span><span class="sxs-lookup"><span data-stu-id="8fe6c-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="8fe6c-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8fe6c-118">PARAMETERS</span></span>

### <span data-ttu-id="8fe6c-119">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="8fe6c-119">-AccountName</span></span>
<span data-ttu-id="8fe6c-120">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="8fe6c-121">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe6c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fe6c-122">-DefaultProfile</span></span>
<span data-ttu-id="8fe6c-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8fe6c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fe6c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fe6c-124">-InputObject</span></span>
<span data-ttu-id="8fe6c-125">Объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-125">Vault object.</span></span>

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

### <span data-ttu-id="8fe6c-126">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="8fe6c-126">-InRemovedState</span></span>
<span data-ttu-id="8fe6c-127">Указывает, нужно ли отображать ранее удаленные учетные записи хранения в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="8fe6c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fe6c-128">-ResourceId</span></span>
<span data-ttu-id="8fe6c-129">Идентификатор ресурса хранилища.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-129">Vault resource id.</span></span>

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

### <span data-ttu-id="8fe6c-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8fe6c-130">-VaultName</span></span>
<span data-ttu-id="8fe6c-131">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-131">Vault name.</span></span>
<span data-ttu-id="8fe6c-132">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8fe6c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe6c-133">CommonParameters</span></span>
<span data-ttu-id="8fe6c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8fe6c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fe6c-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fe6c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe6c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8fe6c-136">INPUTS</span></span>

### <span data-ttu-id="8fe6c-137">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8fe6c-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="8fe6c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8fe6c-138">System.String</span></span>

## <span data-ttu-id="8fe6c-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fe6c-139">OUTPUTS</span></span>

### <span data-ttu-id="8fe6c-140">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8fe6c-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="8fe6c-141">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fe6c-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="8fe6c-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8fe6c-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="8fe6c-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fe6c-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="8fe6c-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="8fe6c-144">NOTES</span></span>

## <span data-ttu-id="8fe6c-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8fe6c-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

