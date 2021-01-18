---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: eeaea44ec387dc7739a97b5026054186ff817ab3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505137"
---
# <span data-ttu-id="ca3d4-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca3d4-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="ca3d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca3d4-102">SYNOPSIS</span></span>
<span data-ttu-id="ca3d4-103">Предоставляет или изменяет существующие разрешения для пользователя, приложения или группы безопасности на выполнение операций с хранилищем ключа.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="ca3d4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ca3d4-104">SYNTAX</span></span>

### <span data-ttu-id="ca3d4-105">ByUserPrincipalName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ca3d4-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca3d4-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="ca3d4-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca3d4-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ca3d4-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca3d4-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ca3d4-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca3d4-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="ca3d4-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca3d4-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="ca3d4-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca3d4-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ca3d4-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca3d4-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ca3d4-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca3d4-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ca3d4-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca3d4-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="ca3d4-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca3d4-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="ca3d4-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca3d4-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ca3d4-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca3d4-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ca3d4-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca3d4-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ca3d4-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca3d4-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="ca3d4-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca3d4-120">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca3d4-120">DESCRIPTION</span></span>
<span data-ttu-id="ca3d4-121">**Cmdlet Set-AzKeyVaultAccessPolicy** предоставляет или изменяет существующие разрешения для пользователя, приложения или группы безопасности на выполнение указанных операций с хранилищем ключа.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="ca3d4-122">При этом не изменяются разрешения других пользователей, приложений и групп безопасности в хранилище ключа.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="ca3d4-123">Если вы устанавливаете разрешения для группы безопасности, эта операция затрагивает только ее пользователей.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="ca3d4-124">Все следующие каталоги должны быть в одном каталоге Azure:</span><span class="sxs-lookup"><span data-stu-id="ca3d4-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="ca3d4-125">Стандартный каталог подписки Azure, в котором находится хранилище ключа.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="ca3d4-126">Каталог Azure, содержащий пользователя или группу приложений, на которые вы предоставляете разрешения.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="ca3d4-127">Примеры сценариев, когда эти условия не выполнены и этот cmdlet не работает:</span><span class="sxs-lookup"><span data-stu-id="ca3d4-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="ca3d4-128">Разрешение пользователю из другой организации управлять вашим хранилищем ключей.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="ca3d4-129">У каждой организации есть собственный каталог.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="ca3d4-130">Учетная запись Azure имеет несколько каталогов.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="ca3d4-131">Если вы зарегистрировали приложение в другом каталоге, который не является каталогом по умолчанию, вы не сможете разрешить этому приложению использовать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="ca3d4-132">Приложение должно быть в каталоге по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-132">The application must be in the default directory.</span></span>
<span data-ttu-id="ca3d4-133">Обратите внимание на то, что хотя для этого cmdlet не требуется указывать группу ресурсов, это следует сделать для улучшения производительности.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

> [!NOTE]
> <span data-ttu-id="ca3d4-134">При предоставлении разрешений на доступ к политике доступа с помощью принципов обслуживания необходимо использовать `-BypassObjectIdValidation` параметр.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-134">When using a service principal to grant access policy permissions, you must use the `-BypassObjectIdValidation` parameter.</span></span>

## <span data-ttu-id="ca3d4-135">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ca3d4-135">EXAMPLES</span></span>

### <span data-ttu-id="ca3d4-136">Пример 1. Предоставление пользователям разрешений для хранилища ключей и изменение разрешений</span><span class="sxs-lookup"><span data-stu-id="ca3d4-136">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :
```

<span data-ttu-id="ca3d4-137">Первая команда предоставляет пользователю в Azure Active Directory разрешения на выполнение операций с ключами и секретами с ключным хранилищем PattiFuller@contoso.com Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-137">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="ca3d4-138">В *результате с помощью параметра PassThru* обновленный объект возвращается этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-138">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="ca3d4-139">Вторая команда изменяет разрешения, предоставленные в первой команде, чтобы теперь можно было не только устанавливать и удалять секрет, но и PattiFuller@contoso.com получать секрет.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-139">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="ca3d4-140">Разрешения для ключевых операций остаются без изменений после этой команды.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-140">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="ca3d4-141">Итоговая команда еще больше изменяет существующие разрешения на удаление всех PattiFuller@contoso.com разрешений для ключевых операций.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-141">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="ca3d4-142">Разрешения на секретные операции остаются без изменений после этой команды.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-142">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="ca3d4-143">Пример 2. Предоставление разрешений для директора службы приложений на чтение и написание секретов</span><span class="sxs-lookup"><span data-stu-id="ca3d4-143">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="ca3d4-144">Эта команда предоставляет разрешения для приложения для key vault под названием Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-144">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="ca3d4-145">Параметр *ServicePrincipalName* определяет приложение.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-145">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="ca3d4-146">Приложение должно быть зарегистрировано в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-146">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="ca3d4-147">Значением параметра *ServicePrincipalName* должно быть либо имя основной службы приложения, либо GUID его кодов.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-147">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="ca3d4-148">В этом примере указывается имя директора-службы и команда предоставляет приложению разрешения на чтение `http://payroll.contoso.com` и написание секретов.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-148">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="ca3d4-149">Пример 3. Предоставление разрешений для приложения с использованием ИД объекта</span><span class="sxs-lookup"><span data-stu-id="ca3d4-149">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="ca3d4-150">Эта команда предоставляет приложению разрешения на чтение и написание секретов.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-150">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="ca3d4-151">В этом примере приложение указывается с использованием ИД объекта, который является основной службой приложения.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-151">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="ca3d4-152">Пример 4. Предоставление разрешений для имени директора пользователя</span><span class="sxs-lookup"><span data-stu-id="ca3d4-152">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="ca3d4-153">Эта команда предоставляет права доступа к секретам указанного имени пользователя, а также разрешения на его получение, список и настройка.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-153">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="ca3d4-154">Пример 5. Включить секретную информацию, извлекаемую поставщиком ресурсов Microsoft.Compute из ключного хранилища</span><span class="sxs-lookup"><span data-stu-id="ca3d4-154">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="ca3d4-155">Эта команда предоставляет разрешения на получение секретов из хранилища ключей Contoso03Vault поставщиком ресурсов Microsoft.Compute.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-155">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="ca3d4-156">Пример 6. Предоставление разрешений группе безопасности</span><span class="sxs-lookup"><span data-stu-id="ca3d4-156">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="ca3d4-157">Первая команда использует Get-AzADGroup для получения всех групп Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-157">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="ca3d4-158">В выходных данных будут возвращены 3 группы, **группа1,** **группа2** и **группа3.**</span><span class="sxs-lookup"><span data-stu-id="ca3d4-158">From the output, you see 3 groups returned, named **group1**, **group2**, and **group3**.</span></span> <span data-ttu-id="ca3d4-159">Несколько групп могут иметь одно и то же имя, но всегда иметь уникальный ObjectId.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-159">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="ca3d4-160">Если возвращается несколько групп с одинаковыми именами, используйте ObjectId в результатах для определения нужной группы.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-160">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="ca3d4-161">Затем используйте выходные данные этой команды вместе с командой Set-AzKeyVaultAccessPolicy, чтобы предоставить разрешения для хранилища ключей **(myownvault)** на группу 2.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-161">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="ca3d4-162">В этом примере группы с именем "группа2" многут в одной командной строке.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-162">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="ca3d4-163">В возвращаемом списке может быть несколько групп с именем "группа2".</span><span class="sxs-lookup"><span data-stu-id="ca3d4-163">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="ca3d4-164">В этом примере выбирается первый из них, обозначенный индексом \[ 0 \] в возвращаемом списке.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-164">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="ca3d4-165">Пример 7. Предоставление Azure Information Protection доступа к ключу клиента, управляемому клиентом (BYOK)</span><span class="sxs-lookup"><span data-stu-id="ca3d4-165">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="ca3d4-166">Эта команда разрешает Azure Information Protection использовать управляемый клиентом ключ (собственный ключ, или СЦЕНАРИЙ BYOK) в качестве ключа клиента Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-166">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="ca3d4-167">При запуске этой команды укажите имя своего сейфа ключа, но необходимо указать параметр *ServicePrincipalName* с GUID **00000012-0000-0000-c000-000000000000** и указать разрешения в примере.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-167">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="ca3d4-168">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca3d4-168">PARAMETERS</span></span>

### <span data-ttu-id="ca3d4-169">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ca3d4-169">-ApplicationId</span></span>
<span data-ttu-id="ca3d4-170">Для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-170">For future use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d4-171">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="ca3d4-171">-BypassObjectIdValidation</span></span>
<span data-ttu-id="ca3d4-172">Позволяет указать ИД объекта без проверки его существования в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-172">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="ca3d4-173">Используйте этот параметр только в том случае, если вы хотите предоставить доступ к сейфу ключа объекту, который ссылается на делегированную группу безопасности из другого клиента Azure.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-173">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d4-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca3d4-174">-DefaultProfile</span></span>
<span data-ttu-id="ca3d4-175">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ca3d4-175">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca3d4-176">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="ca3d4-176">-EmailAddress</span></span>
<span data-ttu-id="ca3d4-177">Определяет адрес электронной почты пользователя, которому нужно предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-177">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="ca3d4-178">Этот адрес электронной почты должен существовать в каталоге, связанном с текущей подпиской, и быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-178">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress, ResourceIdByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d4-179">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="ca3d4-179">-EnabledForDeployment</span></span>
<span data-ttu-id="ca3d4-180">Позволяет поставщику ресурсов Microsoft.Compute извлекать секрет из этого ключевого сейфа, когда на него ссылается создание ресурсов, например при создании виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-180">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d4-181">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="ca3d4-181">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="ca3d4-182">Позволяет службе шифрования дисков Azure получать секрет и отобирать ключи из этого key vault.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-182">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d4-183">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="ca3d4-183">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="ca3d4-184">Позволяет Диспетчеру ресурсов Azure получать секрет из этого сейфа ключа, если на него ссылается развертывание шаблонов.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-184">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d4-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca3d4-185">-InputObject</span></span>
<span data-ttu-id="ca3d4-186">Объект Key Vault</span><span class="sxs-lookup"><span data-stu-id="ca3d4-186">Key Vault Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d4-187">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ca3d4-187">-ObjectId</span></span>
<span data-ttu-id="ca3d4-188">Определяет ИД объекта пользователя или основной службы в Azure Active Directory, для которого нужно предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-188">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d4-189">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca3d4-189">-PassThru</span></span>
<span data-ttu-id="ca3d4-190">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-190">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ca3d4-191">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-191">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ca3d4-192">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="ca3d4-192">-PermissionsToCertificates</span></span>
<span data-ttu-id="ca3d4-193">Указывает массив разрешений на сертификат, которые необходимо предоставить пользователю или основной службе.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-193">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="ca3d4-194">Допустимые значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="ca3d4-194">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="ca3d4-195">Все</span><span class="sxs-lookup"><span data-stu-id="ca3d4-195">All</span></span>
- <span data-ttu-id="ca3d4-196">Получить</span><span class="sxs-lookup"><span data-stu-id="ca3d4-196">Get</span></span>
- <span data-ttu-id="ca3d4-197">Список</span><span class="sxs-lookup"><span data-stu-id="ca3d4-197">List</span></span>
- <span data-ttu-id="ca3d4-198">Удалить</span><span class="sxs-lookup"><span data-stu-id="ca3d4-198">Delete</span></span>
- <span data-ttu-id="ca3d4-199">"Создать"</span><span class="sxs-lookup"><span data-stu-id="ca3d4-199">Create</span></span>
- <span data-ttu-id="ca3d4-200">Импорт</span><span class="sxs-lookup"><span data-stu-id="ca3d4-200">Import</span></span>
- <span data-ttu-id="ca3d4-201">Обновление</span><span class="sxs-lookup"><span data-stu-id="ca3d4-201">Update</span></span>
- <span data-ttu-id="ca3d4-202">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="ca3d4-202">Managecontacts</span></span>
- <span data-ttu-id="ca3d4-203">Getissuers</span><span class="sxs-lookup"><span data-stu-id="ca3d4-203">Getissuers</span></span>
- <span data-ttu-id="ca3d4-204">Listissuers</span><span class="sxs-lookup"><span data-stu-id="ca3d4-204">Listissuers</span></span>
- <span data-ttu-id="ca3d4-205">Setissuers</span><span class="sxs-lookup"><span data-stu-id="ca3d4-205">Setissuers</span></span>
- <span data-ttu-id="ca3d4-206">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="ca3d4-206">Deleteissuers</span></span>
- <span data-ttu-id="ca3d4-207">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="ca3d4-207">Manageissuers</span></span>
- <span data-ttu-id="ca3d4-208">"Восстановить"</span><span class="sxs-lookup"><span data-stu-id="ca3d4-208">Recover</span></span>
- <span data-ttu-id="ca3d4-209">Резервное копирование</span><span class="sxs-lookup"><span data-stu-id="ca3d4-209">Backup</span></span>
- <span data-ttu-id="ca3d4-210">"Восстановить"</span><span class="sxs-lookup"><span data-stu-id="ca3d4-210">Restore</span></span>
- <span data-ttu-id="ca3d4-211">Очистка</span><span class="sxs-lookup"><span data-stu-id="ca3d4-211">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d4-212">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="ca3d4-212">-PermissionsToKeys</span></span>
<span data-ttu-id="ca3d4-213">Указывает массив разрешений на операцию ключа, которые необходимо предоставить пользователю или основной службе.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-213">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="ca3d4-214">Допустимые значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="ca3d4-214">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="ca3d4-215">Все</span><span class="sxs-lookup"><span data-stu-id="ca3d4-215">All</span></span>
- <span data-ttu-id="ca3d4-216">Расшифровать</span><span class="sxs-lookup"><span data-stu-id="ca3d4-216">Decrypt</span></span>
- <span data-ttu-id="ca3d4-217">Шифровать</span><span class="sxs-lookup"><span data-stu-id="ca3d4-217">Encrypt</span></span>
- <span data-ttu-id="ca3d4-218">Unw простоЕКоматурие</span><span class="sxs-lookup"><span data-stu-id="ca3d4-218">UnwrapKey</span></span>
- <span data-ttu-id="ca3d4-219">WrapKey</span><span class="sxs-lookup"><span data-stu-id="ca3d4-219">WrapKey</span></span>
- <span data-ttu-id="ca3d4-220">Проверить</span><span class="sxs-lookup"><span data-stu-id="ca3d4-220">Verify</span></span>
- <span data-ttu-id="ca3d4-221">Подписать</span><span class="sxs-lookup"><span data-stu-id="ca3d4-221">Sign</span></span>
- <span data-ttu-id="ca3d4-222">Получить</span><span class="sxs-lookup"><span data-stu-id="ca3d4-222">Get</span></span>
- <span data-ttu-id="ca3d4-223">Список</span><span class="sxs-lookup"><span data-stu-id="ca3d4-223">List</span></span>
- <span data-ttu-id="ca3d4-224">Обновление</span><span class="sxs-lookup"><span data-stu-id="ca3d4-224">Update</span></span>
- <span data-ttu-id="ca3d4-225">"Создать"</span><span class="sxs-lookup"><span data-stu-id="ca3d4-225">Create</span></span>
- <span data-ttu-id="ca3d4-226">Импорт</span><span class="sxs-lookup"><span data-stu-id="ca3d4-226">Import</span></span>
- <span data-ttu-id="ca3d4-227">Удалить</span><span class="sxs-lookup"><span data-stu-id="ca3d4-227">Delete</span></span>
- <span data-ttu-id="ca3d4-228">Резервное копирование</span><span class="sxs-lookup"><span data-stu-id="ca3d4-228">Backup</span></span>
- <span data-ttu-id="ca3d4-229">"Восстановить"</span><span class="sxs-lookup"><span data-stu-id="ca3d4-229">Restore</span></span>
- <span data-ttu-id="ca3d4-230">"Восстановить"</span><span class="sxs-lookup"><span data-stu-id="ca3d4-230">Recover</span></span>
- <span data-ttu-id="ca3d4-231">Очистка</span><span class="sxs-lookup"><span data-stu-id="ca3d4-231">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d4-232">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="ca3d4-232">-PermissionsToSecrets</span></span>
<span data-ttu-id="ca3d4-233">Определяет массив разрешений на секретную операцию, которые необходимо предоставить пользователю или основному службе.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-233">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="ca3d4-234">Допустимые значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="ca3d4-234">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="ca3d4-235">Все</span><span class="sxs-lookup"><span data-stu-id="ca3d4-235">All</span></span>
- <span data-ttu-id="ca3d4-236">Получить</span><span class="sxs-lookup"><span data-stu-id="ca3d4-236">Get</span></span>
- <span data-ttu-id="ca3d4-237">Список</span><span class="sxs-lookup"><span data-stu-id="ca3d4-237">List</span></span>
- <span data-ttu-id="ca3d4-238">Set</span><span class="sxs-lookup"><span data-stu-id="ca3d4-238">Set</span></span>
- <span data-ttu-id="ca3d4-239">Удалить</span><span class="sxs-lookup"><span data-stu-id="ca3d4-239">Delete</span></span>
- <span data-ttu-id="ca3d4-240">Резервное копирование</span><span class="sxs-lookup"><span data-stu-id="ca3d4-240">Backup</span></span>
- <span data-ttu-id="ca3d4-241">"Восстановить"</span><span class="sxs-lookup"><span data-stu-id="ca3d4-241">Restore</span></span>
- <span data-ttu-id="ca3d4-242">"Восстановить"</span><span class="sxs-lookup"><span data-stu-id="ca3d4-242">Recover</span></span>
- <span data-ttu-id="ca3d4-243">Очистка</span><span class="sxs-lookup"><span data-stu-id="ca3d4-243">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d4-244">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="ca3d4-244">-PermissionsToStorage</span></span>
<span data-ttu-id="ca3d4-245">Определяет учетную запись хранения и разрешения на операции определения SaS, которые можно предоставить пользователю или основной службе.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-245">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="ca3d4-246">Допустимые значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="ca3d4-246">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="ca3d4-247">все</span><span class="sxs-lookup"><span data-stu-id="ca3d4-247">all</span></span>
- <span data-ttu-id="ca3d4-248">Получить</span><span class="sxs-lookup"><span data-stu-id="ca3d4-248">get</span></span>
- <span data-ttu-id="ca3d4-249">список</span><span class="sxs-lookup"><span data-stu-id="ca3d4-249">list</span></span>
- <span data-ttu-id="ca3d4-250">удалить</span><span class="sxs-lookup"><span data-stu-id="ca3d4-250">delete</span></span>
- <span data-ttu-id="ca3d4-251">set</span><span class="sxs-lookup"><span data-stu-id="ca3d4-251">set</span></span>
- <span data-ttu-id="ca3d4-252">обновление</span><span class="sxs-lookup"><span data-stu-id="ca3d4-252">update</span></span>
- <span data-ttu-id="ca3d4-253">regeneratekey</span><span class="sxs-lookup"><span data-stu-id="ca3d4-253">regeneratekey</span></span>
- <span data-ttu-id="ca3d4-254">getsas</span><span class="sxs-lookup"><span data-stu-id="ca3d4-254">getsas</span></span>
- <span data-ttu-id="ca3d4-255">listsas</span><span class="sxs-lookup"><span data-stu-id="ca3d4-255">listsas</span></span>
- <span data-ttu-id="ca3d4-256">deletesas</span><span class="sxs-lookup"><span data-stu-id="ca3d4-256">deletesas</span></span>
- <span data-ttu-id="ca3d4-257">setsas</span><span class="sxs-lookup"><span data-stu-id="ca3d4-257">setsas</span></span>
- <span data-ttu-id="ca3d4-258">восстановить</span><span class="sxs-lookup"><span data-stu-id="ca3d4-258">recover</span></span>
- <span data-ttu-id="ca3d4-259">резервное копирование</span><span class="sxs-lookup"><span data-stu-id="ca3d4-259">backup</span></span>
- <span data-ttu-id="ca3d4-260">восстановить</span><span class="sxs-lookup"><span data-stu-id="ca3d4-260">restore</span></span>
- <span data-ttu-id="ca3d4-261">очистка</span><span class="sxs-lookup"><span data-stu-id="ca3d4-261">purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d4-262">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca3d4-262">-ResourceGroupName</span></span>
<span data-ttu-id="ca3d4-263">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-263">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d4-264">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca3d4-264">-ResourceId</span></span>
<span data-ttu-id="ca3d4-265">Key Vault Resource Id</span><span class="sxs-lookup"><span data-stu-id="ca3d4-265">Key Vault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d4-266">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ca3d4-266">-ServicePrincipalName</span></span>
<span data-ttu-id="ca3d4-267">Указывает имя основной службы приложения, для которого необходимо предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-267">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="ca3d4-268">Укажите ИД приложения, также известный как ИД клиента, зарегистрированный для приложения в AzureActive Directory.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-268">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="ca3d4-269">Приложение с именем основной службы, указанным этим параметром, должно быть зарегистрировано в каталоге Azure, который содержит текущую подписку.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-269">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName, ResourceIdByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d4-270">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ca3d4-270">-UserPrincipalName</span></span>
<span data-ttu-id="ca3d4-271">Определяет имя пользователя, которому необходимо предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-271">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="ca3d4-272">Это имя пользователя должно существовать в каталоге, связанном с текущей подпиской.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-272">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName, ResourceIdByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d4-273">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ca3d4-273">-VaultName</span></span>
<span data-ttu-id="ca3d4-274">Указывает имя сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-274">Specifies the name of a key vault.</span></span>
<span data-ttu-id="ca3d4-275">Этот cmdlet изменяет политику доступа для хранилища ключей, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-275">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d4-276">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca3d4-276">-Confirm</span></span>
<span data-ttu-id="ca3d4-277">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-277">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca3d4-278">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca3d4-278">-WhatIf</span></span>
<span data-ttu-id="ca3d4-279">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-279">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca3d4-280">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-280">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca3d4-281">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca3d4-281">CommonParameters</span></span>
<span data-ttu-id="ca3d4-282">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca3d4-282">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca3d4-283">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca3d4-283">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca3d4-284">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca3d4-284">INPUTS</span></span>

### <span data-ttu-id="ca3d4-285">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ca3d4-285">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="ca3d4-286">System.String</span><span class="sxs-lookup"><span data-stu-id="ca3d4-286">System.String</span></span>

## <span data-ttu-id="ca3d4-287">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ca3d4-287">OUTPUTS</span></span>

### <span data-ttu-id="ca3d4-288">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ca3d4-288">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="ca3d4-289">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ca3d4-289">NOTES</span></span>

## <span data-ttu-id="ca3d4-290">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca3d4-290">RELATED LINKS</span></span>

[<span data-ttu-id="ca3d4-291">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="ca3d4-291">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="ca3d4-292">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca3d4-292">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

