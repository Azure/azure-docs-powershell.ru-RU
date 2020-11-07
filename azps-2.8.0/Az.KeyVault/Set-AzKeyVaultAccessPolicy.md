---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 55cdc385c5cdf291db15399f4fd587b9b10ce308
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "93915522"
---
# <span data-ttu-id="3868a-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3868a-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="3868a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3868a-102">SYNOPSIS</span></span>
<span data-ttu-id="3868a-103">Предоставление или изменение существующих разрешений для пользователя, приложения или группы безопасности для выполнения операций с помощью хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3868a-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="3868a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3868a-104">SYNTAX</span></span>

### <span data-ttu-id="3868a-105">ByUserPrincipalName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3868a-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3868a-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="3868a-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3868a-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3868a-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3868a-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3868a-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3868a-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="3868a-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3868a-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="3868a-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3868a-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3868a-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3868a-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3868a-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3868a-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3868a-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3868a-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="3868a-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3868a-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="3868a-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3868a-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3868a-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3868a-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3868a-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3868a-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3868a-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3868a-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="3868a-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3868a-120">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3868a-120">DESCRIPTION</span></span>
<span data-ttu-id="3868a-121">Командлет **Set-AzKeyVaultAccessPolicy** предоставляет или изменяет существующие разрешения для пользователя, приложения или группы безопасности для выполнения указанных операций с помощью хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3868a-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="3868a-122">Изменения, внесенные другими пользователями, приложениями или группами безопасности, не изменяются в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="3868a-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="3868a-123">Если вы настраиваете разрешения для группы безопасности, эта операция влияет только на пользователей в этой группе безопасности.</span><span class="sxs-lookup"><span data-stu-id="3868a-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="3868a-124">Следующие каталоги должны находиться в одном каталоге Azure:</span><span class="sxs-lookup"><span data-stu-id="3868a-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="3868a-125">Каталог подписки Azure по умолчанию, в котором находится хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="3868a-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="3868a-126">Каталог Azure, содержащий пользователя или группу приложений, которым предоставляются разрешения.</span><span class="sxs-lookup"><span data-stu-id="3868a-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="3868a-127">Примеры ситуаций, когда эти условия не выполняются, и этот командлет не работает.</span><span class="sxs-lookup"><span data-stu-id="3868a-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="3868a-128">Авторизация пользователя из другой организации для управления вашим хранилищем ключей.</span><span class="sxs-lookup"><span data-stu-id="3868a-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="3868a-129">Каждая организация имеет собственный каталог.</span><span class="sxs-lookup"><span data-stu-id="3868a-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="3868a-130">У вашей учетной записи Azure есть несколько каталогов.</span><span class="sxs-lookup"><span data-stu-id="3868a-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="3868a-131">Если зарегистрировать приложение в каталоге, отличном от каталога по умолчанию, вы не сможете авторизовать это приложение для использования вашего хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3868a-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="3868a-132">Приложение должно быть в каталоге по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3868a-132">The application must be in the default directory.</span></span>
<span data-ttu-id="3868a-133">Обратите внимание, что хотя указывать группу ресурсов необязательно для этого командлета, вы должны сделать это для лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="3868a-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="3868a-134">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3868a-134">EXAMPLES</span></span>

### <span data-ttu-id="3868a-135">Пример 1: предоставление разрешений пользователю для хранилища ключей и изменение разрешений</span><span class="sxs-lookup"><span data-stu-id="3868a-135">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
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

<span data-ttu-id="3868a-136">Первая команда предоставляет разрешения для пользователя в Azure Active Directory, PattiFuller@contoso.com для выполнения операций с ключами и секретами с помощью хранилища ключей с именем Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="3868a-136">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="3868a-137">Параметр *PassThru* приводит к обновлению объекта, возвращаемого командлетом.</span><span class="sxs-lookup"><span data-stu-id="3868a-137">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="3868a-138">Вторая команда изменяет разрешения, предоставленные PattiFuller@contoso.com первой командой, теперь позволяет получать секреты в дополнение к установке и удалению.</span><span class="sxs-lookup"><span data-stu-id="3868a-138">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="3868a-139">После этой команды разрешения на выполнение операций с клавишами остались неизменными.</span><span class="sxs-lookup"><span data-stu-id="3868a-139">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="3868a-140">Последняя команда дополнительно изменяет существующие разрешения для PattiFuller@contoso.com удаления всех разрешений на выполнение операций с ключами.</span><span class="sxs-lookup"><span data-stu-id="3868a-140">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="3868a-141">После этой команды разрешения на выполнение операций с секретными действиями остаются неизменными.</span><span class="sxs-lookup"><span data-stu-id="3868a-141">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="3868a-142">Пример 2: предоставление разрешений на чтение и запись секретов для субъекта-службы приложения</span><span class="sxs-lookup"><span data-stu-id="3868a-142">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="3868a-143">Эта команда предоставляет приложению разрешения на доступ к хранилищу ключей с именем Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="3868a-143">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="3868a-144">Параметр *"* имя приложения" Указывает приложение.</span><span class="sxs-lookup"><span data-stu-id="3868a-144">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="3868a-145">Приложение должно быть зарегистрировано в службе Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3868a-145">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="3868a-146">Значение параметра "ИД *:" должно* быть либо именем субъекта-службы приложения, либо идентификатором GUID приложения.</span><span class="sxs-lookup"><span data-stu-id="3868a-146">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="3868a-147">В этом примере задается имя субъекта-службы `http://payroll.contoso.com` , и команда предоставляет разрешения приложения на чтение и запись секретов.</span><span class="sxs-lookup"><span data-stu-id="3868a-147">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="3868a-148">Пример 3: предоставление разрешений на доступ к приложению с помощью идентификатора объекта</span><span class="sxs-lookup"><span data-stu-id="3868a-148">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="3868a-149">Эта команда предоставляет приложению разрешения на чтение и запись секретов.</span><span class="sxs-lookup"><span data-stu-id="3868a-149">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="3868a-150">В этом примере приложение задается с помощью идентификатора объекта субъекта-службы приложения.</span><span class="sxs-lookup"><span data-stu-id="3868a-150">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="3868a-151">Пример 4: предоставление разрешений для основного имени пользователя</span><span class="sxs-lookup"><span data-stu-id="3868a-151">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="3868a-152">Эта команда предоставляет получение, список и задание разрешений для указанного основного имени пользователя, чтобы получить доступ к секретным данным.</span><span class="sxs-lookup"><span data-stu-id="3868a-152">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="3868a-153">Пример 5: включение секретных данных для получения из хранилища ключей с помощью поставщика ресурсов Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="3868a-153">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="3868a-154">Эта команда предоставляет доступ к зашифрованным данным из хранилища ключей Contoso03Vault с помощью поставщика ресурсов Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="3868a-154">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="3868a-155">Пример 6: предоставление разрешений группе безопасности</span><span class="sxs-lookup"><span data-stu-id="3868a-155">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="3868a-156">В первой команде используется командлет Get-AzADGroup, чтобы получить все группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3868a-156">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="3868a-157">На экране выводятся три возвращенные группы с именами **group1** , **group2** и **group3**.</span><span class="sxs-lookup"><span data-stu-id="3868a-157">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="3868a-158">У нескольких групп может быть одно и то же имя, но всегда есть уникальный ObjectId.</span><span class="sxs-lookup"><span data-stu-id="3868a-158">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="3868a-159">Если возвращено несколько групп с одним и тем же именем, используйте ObjectId в выходных данных, чтобы определить, какой из них вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="3868a-159">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="3868a-160">Затем вы можете использовать вывод этой команды с Set-AzKeyVaultAccessPolicy для предоставления разрешений на доступ к group2 для вашего хранилища ключей с именем **myownvault**.</span><span class="sxs-lookup"><span data-stu-id="3868a-160">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="3868a-161">В этом примере выполняется перечисление групп с именем "group2" в той же командной строке.</span><span class="sxs-lookup"><span data-stu-id="3868a-161">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="3868a-162">В возвращаемом списке может быть несколько групп с именем "group2".</span><span class="sxs-lookup"><span data-stu-id="3868a-162">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="3868a-163">В этом примере первый элемент, обозначенный индексом 0, выбирается \[ \] в списке "возвращено".</span><span class="sxs-lookup"><span data-stu-id="3868a-163">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="3868a-164">Пример 7: предоставление службе Azure Information Protection доступа к ключу клиента, управляемому клиентом (BYOK)</span><span class="sxs-lookup"><span data-stu-id="3868a-164">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="3868a-165">Эта команда авторизует защиту данных Azure на использование управляемого пользователем ключа (например, "сделать свой ключ" или "BYOK") в качестве ключа клиента для защиты данных Azure.</span><span class="sxs-lookup"><span data-stu-id="3868a-165">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="3868a-166">При выполнении этой команды укажите свое собственное имя хранилища ключей, но необходимо указать параметр «код *продукта» (* GUID **00000012-0000-0000-C000-000000000000)** и задать разрешения в этом примере.</span><span class="sxs-lookup"><span data-stu-id="3868a-166">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="3868a-167">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3868a-167">PARAMETERS</span></span>

### <span data-ttu-id="3868a-168">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3868a-168">-ApplicationId</span></span>
<span data-ttu-id="3868a-169">Для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="3868a-169">For future use.</span></span>

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

### <span data-ttu-id="3868a-170">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="3868a-170">-BypassObjectIdValidation</span></span>
<span data-ttu-id="3868a-171">Позволяет указать идентификатор объекта, не проверяя, существует ли этот объект в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3868a-171">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="3868a-172">Используйте этот параметр только в том случае, если вы хотите предоставить доступ к своему хранилищу ключей ИДЕНТИФИКАТОРу объекта, который ссылается на делегированную группу безопасности из другого клиента Azure.</span><span class="sxs-lookup"><span data-stu-id="3868a-172">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

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

### <span data-ttu-id="3868a-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3868a-173">-DefaultProfile</span></span>
<span data-ttu-id="3868a-174">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3868a-174">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3868a-175">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="3868a-175">-EmailAddress</span></span>
<span data-ttu-id="3868a-176">Указывает адрес электронной почты пользователя, которому нужно предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="3868a-176">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="3868a-177">Этот адрес электронной почты должен содержаться в каталоге, связанном с текущей подпиской, и быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="3868a-177">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

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

### <span data-ttu-id="3868a-178">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="3868a-178">-EnabledForDeployment</span></span>
<span data-ttu-id="3868a-179">Включает поставщик ресурсов Microsoft. COMPUTE для извлечения секретов из этого ключа, если это временное хранилище ссылается на создание ресурсов (например, при создании виртуальной машины).</span><span class="sxs-lookup"><span data-stu-id="3868a-179">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="3868a-180">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="3868a-180">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="3868a-181">Позволяет службе шифрования дисков Azure получить секретные ключи и их перетекание из этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3868a-181">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="3868a-182">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="3868a-182">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="3868a-183">Позволяет диспетчеру ресурсов Azure получать секреты из этого хранилища ключей при ссылке на это хранилище ключей в развертывании шаблона.</span><span class="sxs-lookup"><span data-stu-id="3868a-183">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="3868a-184">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3868a-184">-InputObject</span></span>
<span data-ttu-id="3868a-185">Объект хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="3868a-185">Key Vault Object</span></span>

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

### <span data-ttu-id="3868a-186">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3868a-186">-ObjectId</span></span>
<span data-ttu-id="3868a-187">Указывает идентификатор объекта пользователя или участника-службы в Azure Active Directory, для которого требуется предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="3868a-187">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="3868a-188">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3868a-188">-PassThru</span></span>
<span data-ttu-id="3868a-189">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="3868a-189">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3868a-190">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3868a-190">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3868a-191">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="3868a-191">-PermissionsToCertificates</span></span>
<span data-ttu-id="3868a-192">Задает массив разрешений на доступ к сертификату, предоставляемый пользователю или участнику службы.</span><span class="sxs-lookup"><span data-stu-id="3868a-192">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="3868a-193">Допустимые значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="3868a-193">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="3868a-194">Получить</span><span class="sxs-lookup"><span data-stu-id="3868a-194">Get</span></span>
- <span data-ttu-id="3868a-195">Список</span><span class="sxs-lookup"><span data-stu-id="3868a-195">List</span></span>
- <span data-ttu-id="3868a-196">Удаление</span><span class="sxs-lookup"><span data-stu-id="3868a-196">Delete</span></span>
- <span data-ttu-id="3868a-197">Заново</span><span class="sxs-lookup"><span data-stu-id="3868a-197">Create</span></span>
- <span data-ttu-id="3868a-198">Импортируем</span><span class="sxs-lookup"><span data-stu-id="3868a-198">Import</span></span>
- <span data-ttu-id="3868a-199">Обновление</span><span class="sxs-lookup"><span data-stu-id="3868a-199">Update</span></span>
- <span data-ttu-id="3868a-200">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="3868a-200">Managecontacts</span></span>
- <span data-ttu-id="3868a-201">Поставщики</span><span class="sxs-lookup"><span data-stu-id="3868a-201">Getissuers</span></span>
- <span data-ttu-id="3868a-202">Listissuers</span><span class="sxs-lookup"><span data-stu-id="3868a-202">Listissuers</span></span>
- <span data-ttu-id="3868a-203">Setissuers</span><span class="sxs-lookup"><span data-stu-id="3868a-203">Setissuers</span></span>
- <span data-ttu-id="3868a-204">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="3868a-204">Deleteissuers</span></span>
- <span data-ttu-id="3868a-205">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="3868a-205">Manageissuers</span></span>
- <span data-ttu-id="3868a-206">Устранения</span><span class="sxs-lookup"><span data-stu-id="3868a-206">Recover</span></span>
- <span data-ttu-id="3868a-207">Копирование</span><span class="sxs-lookup"><span data-stu-id="3868a-207">Backup</span></span>
- <span data-ttu-id="3868a-208">Восстановление</span><span class="sxs-lookup"><span data-stu-id="3868a-208">Restore</span></span>
- <span data-ttu-id="3868a-209">Меня</span><span class="sxs-lookup"><span data-stu-id="3868a-209">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3868a-210">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="3868a-210">-PermissionsToKeys</span></span>
<span data-ttu-id="3868a-211">Задает массив разрешений на операцию с ключом для предоставления пользователю или участнику службы.</span><span class="sxs-lookup"><span data-stu-id="3868a-211">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="3868a-212">Допустимые значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="3868a-212">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="3868a-213">Расшифровки</span><span class="sxs-lookup"><span data-stu-id="3868a-213">Decrypt</span></span>
- <span data-ttu-id="3868a-214">EFS</span><span class="sxs-lookup"><span data-stu-id="3868a-214">Encrypt</span></span>
- <span data-ttu-id="3868a-215">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="3868a-215">UnwrapKey</span></span>
- <span data-ttu-id="3868a-216">WrapKey</span><span class="sxs-lookup"><span data-stu-id="3868a-216">WrapKey</span></span>
- <span data-ttu-id="3868a-217">Подтвержда</span><span class="sxs-lookup"><span data-stu-id="3868a-217">Verify</span></span>
- <span data-ttu-id="3868a-218">Рядом</span><span class="sxs-lookup"><span data-stu-id="3868a-218">Sign</span></span>
- <span data-ttu-id="3868a-219">Получить</span><span class="sxs-lookup"><span data-stu-id="3868a-219">Get</span></span>
- <span data-ttu-id="3868a-220">Список</span><span class="sxs-lookup"><span data-stu-id="3868a-220">List</span></span>
- <span data-ttu-id="3868a-221">Обновление</span><span class="sxs-lookup"><span data-stu-id="3868a-221">Update</span></span>
- <span data-ttu-id="3868a-222">Заново</span><span class="sxs-lookup"><span data-stu-id="3868a-222">Create</span></span>
- <span data-ttu-id="3868a-223">Импортируем</span><span class="sxs-lookup"><span data-stu-id="3868a-223">Import</span></span>
- <span data-ttu-id="3868a-224">Удаление</span><span class="sxs-lookup"><span data-stu-id="3868a-224">Delete</span></span>
- <span data-ttu-id="3868a-225">Копирование</span><span class="sxs-lookup"><span data-stu-id="3868a-225">Backup</span></span>
- <span data-ttu-id="3868a-226">Восстановление</span><span class="sxs-lookup"><span data-stu-id="3868a-226">Restore</span></span>
- <span data-ttu-id="3868a-227">Устранения</span><span class="sxs-lookup"><span data-stu-id="3868a-227">Recover</span></span>
- <span data-ttu-id="3868a-228">Меня</span><span class="sxs-lookup"><span data-stu-id="3868a-228">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3868a-229">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="3868a-229">-PermissionsToSecrets</span></span>
<span data-ttu-id="3868a-230">Задает массив разрешений на секретную операцию для предоставления пользователю или участнику службы.</span><span class="sxs-lookup"><span data-stu-id="3868a-230">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="3868a-231">Допустимые значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="3868a-231">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="3868a-232">Получить</span><span class="sxs-lookup"><span data-stu-id="3868a-232">Get</span></span>
- <span data-ttu-id="3868a-233">Список</span><span class="sxs-lookup"><span data-stu-id="3868a-233">List</span></span>
- <span data-ttu-id="3868a-234">Свои</span><span class="sxs-lookup"><span data-stu-id="3868a-234">Set</span></span>
- <span data-ttu-id="3868a-235">Удаление</span><span class="sxs-lookup"><span data-stu-id="3868a-235">Delete</span></span>
- <span data-ttu-id="3868a-236">Копирование</span><span class="sxs-lookup"><span data-stu-id="3868a-236">Backup</span></span>
- <span data-ttu-id="3868a-237">Восстановление</span><span class="sxs-lookup"><span data-stu-id="3868a-237">Restore</span></span>
- <span data-ttu-id="3868a-238">Устранения</span><span class="sxs-lookup"><span data-stu-id="3868a-238">Recover</span></span>
- <span data-ttu-id="3868a-239">Меня</span><span class="sxs-lookup"><span data-stu-id="3868a-239">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3868a-240">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="3868a-240">-PermissionsToStorage</span></span>
<span data-ttu-id="3868a-241">Задает управляемую учетную запись хранения и разрешения операций определения SaS, предоставляемые пользователю или участнику службы.</span><span class="sxs-lookup"><span data-stu-id="3868a-241">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3868a-242">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3868a-242">-ResourceGroupName</span></span>
<span data-ttu-id="3868a-243">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3868a-243">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3868a-244">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3868a-244">-ResourceId</span></span>
<span data-ttu-id="3868a-245">Идентификатор ресурса для хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="3868a-245">Key Vault Resource Id</span></span>

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

### <span data-ttu-id="3868a-246">-Намерено</span><span class="sxs-lookup"><span data-stu-id="3868a-246">-ServicePrincipalName</span></span>
<span data-ttu-id="3868a-247">Указывает имя субъекта-службы для приложения, которому нужно предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="3868a-247">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="3868a-248">Укажите идентификатор приложения, который также называется ИДЕНТИФИКАТОРом клиента, зарегистрированный для приложения в AzureActive Directory.</span><span class="sxs-lookup"><span data-stu-id="3868a-248">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="3868a-249">Приложение с именем субъекта-службы, которое указывает этот параметр, должно быть зарегистрировано в каталоге Azure, содержащем текущую подписку.</span><span class="sxs-lookup"><span data-stu-id="3868a-249">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="3868a-250">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3868a-250">-UserPrincipalName</span></span>
<span data-ttu-id="3868a-251">Указывает имя участника-пользователя, которому нужно предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="3868a-251">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="3868a-252">Это имя участника-пользователя должно существовать в каталоге, связанном с текущей подпиской.</span><span class="sxs-lookup"><span data-stu-id="3868a-252">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="3868a-253">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3868a-253">-VaultName</span></span>
<span data-ttu-id="3868a-254">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3868a-254">Specifies the name of a key vault.</span></span>
<span data-ttu-id="3868a-255">Этот командлет изменяет политику доступа для хранилища ключей, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3868a-255">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="3868a-256">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3868a-256">-Confirm</span></span>
<span data-ttu-id="3868a-257">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3868a-257">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3868a-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3868a-258">-WhatIf</span></span>
<span data-ttu-id="3868a-259">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3868a-259">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3868a-260">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3868a-260">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3868a-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3868a-261">CommonParameters</span></span>
<span data-ttu-id="3868a-262">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3868a-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3868a-263">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3868a-263">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3868a-264">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3868a-264">INPUTS</span></span>

### <span data-ttu-id="3868a-265">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3868a-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="3868a-266">System. String</span><span class="sxs-lookup"><span data-stu-id="3868a-266">System.String</span></span>

## <span data-ttu-id="3868a-267">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3868a-267">OUTPUTS</span></span>

### <span data-ttu-id="3868a-268">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3868a-268">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="3868a-269">Пуск</span><span class="sxs-lookup"><span data-stu-id="3868a-269">NOTES</span></span>

## <span data-ttu-id="3868a-270">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3868a-270">RELATED LINKS</span></span>

[<span data-ttu-id="3868a-271">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="3868a-271">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="3868a-272">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3868a-272">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

