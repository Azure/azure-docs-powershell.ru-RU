---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: c09218b960fb6c11b685106a3cb90bfdfd2f546a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222241"
---
# <span data-ttu-id="7320a-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="7320a-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="7320a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7320a-102">SYNOPSIS</span></span>
<span data-ttu-id="7320a-103">Получает определения SAS хранилища, управляемые ключом хранилища.</span><span class="sxs-lookup"><span data-stu-id="7320a-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="7320a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7320a-104">SYNTAX</span></span>

### <span data-ttu-id="7320a-105">ByDefinitionName (Default)</span><span class="sxs-lookup"><span data-stu-id="7320a-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7320a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7320a-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7320a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7320a-107">DESCRIPTION</span></span>
<span data-ttu-id="7320a-108">Возвращает определение SAS хранилища, управляемое хранилищем, если задано имя определения.</span><span class="sxs-lookup"><span data-stu-id="7320a-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="7320a-109">Если имя определения не указано, в списке будут перечислены все определения SAS, связанные с указанной учетной записью хранилища, управляемой хранилищем ключа.</span><span class="sxs-lookup"><span data-stu-id="7320a-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="7320a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7320a-110">EXAMPLES</span></span>

### <span data-ttu-id="7320a-111">Пример 1. Список всех определений SAS хранилища, управляемого хранилищем</span><span class="sxs-lookup"><span data-stu-id="7320a-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="7320a-112">Список всех определений SAS, связанных с key Vault Managed Storage Account "mystorageaccount", управляемых хранилищем myvault.</span><span class="sxs-lookup"><span data-stu-id="7320a-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="7320a-113">Пример 2. Получить учетную запись хранения в key Vault</span><span class="sxs-lookup"><span data-stu-id="7320a-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'accountsas'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Secret Id   : https://myvault.vault.azure.net/secrets/mystorageaccount-accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="7320a-114">Получает сведения об учетных записях определения SAS, связанных с ключевой учетной записью хранения mystorageaccount, управляемой хранилищем myvault.</span><span class="sxs-lookup"><span data-stu-id="7320a-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="7320a-115">Пример 3. Список всех определений SAS хранилища, управляемых хранилищем, с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="7320a-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name "account*"

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas1
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas1
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas2
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas2
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="7320a-116">Список всех определений SAS, связанных с key Vault Managed Storage Account "mystorageaccount", управляемых хранилищем myvault, которое начинается с "account".</span><span class="sxs-lookup"><span data-stu-id="7320a-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="7320a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7320a-117">PARAMETERS</span></span>

### <span data-ttu-id="7320a-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7320a-118">-AccountName</span></span>
<span data-ttu-id="7320a-119">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="7320a-119">Vault name.</span></span>
<span data-ttu-id="7320a-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="7320a-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="7320a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7320a-121">-DefaultProfile</span></span>
<span data-ttu-id="7320a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7320a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7320a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7320a-123">-InputObject</span></span>
<span data-ttu-id="7320a-124">Объект ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="7320a-124">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7320a-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="7320a-125">-InRemovedState</span></span>
<span data-ttu-id="7320a-126">Определяет, нужно ли показывать ранее удаленные определения sas хранилища в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7320a-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="7320a-127">-Name</span><span class="sxs-lookup"><span data-stu-id="7320a-127">-Name</span></span>
<span data-ttu-id="7320a-128">Имя определения sas хранилища.</span><span class="sxs-lookup"><span data-stu-id="7320a-128">Storage sas definition name.</span></span>
<span data-ttu-id="7320a-129">Cmdlet конструировать FQDN определения sas хранилища из имени хранилища, выбранной среды, имени учетной записи хранения и имени определения sas.</span><span class="sxs-lookup"><span data-stu-id="7320a-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7320a-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7320a-130">-VaultName</span></span>
<span data-ttu-id="7320a-131">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="7320a-131">Vault name.</span></span>
<span data-ttu-id="7320a-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="7320a-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="7320a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7320a-133">CommonParameters</span></span>
<span data-ttu-id="7320a-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7320a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7320a-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7320a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7320a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7320a-136">INPUTS</span></span>

### <span data-ttu-id="7320a-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7320a-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="7320a-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7320a-138">OUTPUTS</span></span>

### <span data-ttu-id="7320a-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7320a-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="7320a-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="7320a-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="7320a-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="7320a-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="7320a-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7320a-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="7320a-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7320a-143">NOTES</span></span>

## <span data-ttu-id="7320a-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7320a-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

