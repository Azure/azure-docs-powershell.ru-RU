---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: f3a1e4d1e938b84a434c07451f3d2294e203f440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567752"
---
# <span data-ttu-id="72a80-101">Get-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="72a80-101">Get-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="72a80-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72a80-102">SYNOPSIS</span></span>
<span data-ttu-id="72a80-103">Получение управляемых учетных записей хранилища Azure для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="72a80-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72a80-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72a80-104">SYNTAX</span></span>

### <span data-ttu-id="72a80-105">ByAccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="72a80-105">ByAccountName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72a80-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="72a80-106">ByInputObject</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72a80-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="72a80-107">ByResourceId</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72a80-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72a80-108">DESCRIPTION</span></span>
<span data-ttu-id="72a80-109">Возвращает управляемую учетную запись хранилища Azure с основным хранилищем, если указано имя учетной записи, а ключи учетной записи управляются указанным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="72a80-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="72a80-110">Если имя учетной записи не указано, перечисляются все учетные записи, для которых управление ключами задается указанным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="72a80-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="72a80-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72a80-111">EXAMPLES</span></span>

### <span data-ttu-id="72a80-112">Пример 1: список всех учетных записей хранения с управляемым хранилищем</span><span class="sxs-lookup"><span data-stu-id="72a80-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault'

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

<span data-ttu-id="72a80-113">Выводит все учетные записи, для которых управление ключами является хранилищем "myvault".</span><span class="sxs-lookup"><span data-stu-id="72a80-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="72a80-114">Пример 2: получение учетной записи хранилища с управляемым хранилищем ключей</span><span class="sxs-lookup"><span data-stu-id="72a80-114">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'

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

<span data-ttu-id="72a80-115">Получение сведений об учетной записи хранения ключа управляемого хранилища для "mystorageaccount", если ее ключи управляются хранилищем "myvault"</span><span class="sxs-lookup"><span data-stu-id="72a80-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="72a80-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72a80-116">PARAMETERS</span></span>

### <span data-ttu-id="72a80-117">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="72a80-117">-AccountName</span></span>
<span data-ttu-id="72a80-118">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="72a80-118">Key Vault managed storage account name.</span></span> <span data-ttu-id="72a80-119">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="72a80-119">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="72a80-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72a80-120">-DefaultProfile</span></span>
<span data-ttu-id="72a80-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="72a80-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72a80-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72a80-122">-InputObject</span></span>
<span data-ttu-id="72a80-123">Объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="72a80-123">Vault object.</span></span>

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

### <span data-ttu-id="72a80-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="72a80-124">-InRemovedState</span></span>
<span data-ttu-id="72a80-125">Указывает, нужно ли отображать ранее удаленные учетные записи хранения в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="72a80-125">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="72a80-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72a80-126">-ResourceId</span></span>
<span data-ttu-id="72a80-127">Идентификатор ресурса хранилища.</span><span class="sxs-lookup"><span data-stu-id="72a80-127">Vault resource id.</span></span>

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

### <span data-ttu-id="72a80-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="72a80-128">-VaultName</span></span>
<span data-ttu-id="72a80-129">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="72a80-129">Vault name.</span></span>
<span data-ttu-id="72a80-130">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="72a80-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="72a80-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72a80-131">CommonParameters</span></span>
<span data-ttu-id="72a80-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72a80-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72a80-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72a80-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72a80-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72a80-134">INPUTS</span></span>

### <span data-ttu-id="72a80-135">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="72a80-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="72a80-136">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="72a80-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="72a80-137">System. String</span><span class="sxs-lookup"><span data-stu-id="72a80-137">System.String</span></span>

## <span data-ttu-id="72a80-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72a80-138">OUTPUTS</span></span>

### <span data-ttu-id="72a80-139">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="72a80-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="72a80-140">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="72a80-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="72a80-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="72a80-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="72a80-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="72a80-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="72a80-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="72a80-143">NOTES</span></span>

## <span data-ttu-id="72a80-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72a80-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

