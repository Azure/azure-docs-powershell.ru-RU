---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 20a36e35c509ecca889d4059bd7e74ccafa22dc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561743"
---
# <span data-ttu-id="26261-101">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="26261-101">Set-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="26261-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26261-102">SYNOPSIS</span></span>
<span data-ttu-id="26261-103">Предоставление или изменение существующих разрешений для пользователя, приложения или группы безопасности для выполнения операций с помощью хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="26261-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26261-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26261-104">SYNTAX</span></span>

### <span data-ttu-id="26261-105">ByUserPrincipalName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26261-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26261-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="26261-106">ByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26261-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="26261-107">ByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26261-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="26261-108">ByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26261-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="26261-109">ForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26261-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="26261-110">InputObjectByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26261-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="26261-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26261-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="26261-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26261-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="26261-113">InputObjectByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26261-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="26261-114">InputObjectForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26261-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26261-115">DESCRIPTION</span></span>
<span data-ttu-id="26261-116">Командлет **Set-AzureRmKeyVaultAccessPolicy** предоставляет или изменяет существующие разрешения для пользователя, приложения или группы безопасности для выполнения указанных операций с помощью хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="26261-116">The **Set-AzureRmKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="26261-117">Изменения, внесенные другими пользователями, приложениями или группами безопасности, не изменяются в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="26261-117">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="26261-118">Если вы настраиваете разрешения для группы безопасности, эта операция влияет только на пользователей в этой группе безопасности.</span><span class="sxs-lookup"><span data-stu-id="26261-118">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="26261-119">Следующие каталоги должны находиться в одном каталоге Azure:</span><span class="sxs-lookup"><span data-stu-id="26261-119">The following directories must all be the same Azure directory:</span></span> 
- <span data-ttu-id="26261-120">Каталог подписки Azure по умолчанию, в котором находится хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="26261-120">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="26261-121">Каталог Azure, содержащий пользователя или группу приложений, которым предоставляются разрешения.</span><span class="sxs-lookup"><span data-stu-id="26261-121">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="26261-122">Примеры ситуаций, когда эти условия не выполняются, и этот командлет не работает.</span><span class="sxs-lookup"><span data-stu-id="26261-122">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span> 

- <span data-ttu-id="26261-123">Авторизация пользователя из другой организации для управления вашим хранилищем ключей.</span><span class="sxs-lookup"><span data-stu-id="26261-123">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="26261-124">Каждая организация имеет собственный каталог.</span><span class="sxs-lookup"><span data-stu-id="26261-124">Each organization has its own directory.</span></span> 
- <span data-ttu-id="26261-125">У вашей учетной записи Azure есть несколько каталогов.</span><span class="sxs-lookup"><span data-stu-id="26261-125">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="26261-126">Если зарегистрировать приложение в каталоге, отличном от каталога по умолчанию, вы не сможете авторизовать это приложение для использования вашего хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="26261-126">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="26261-127">Приложение должно быть в каталоге по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="26261-127">The application must be in the default directory.</span></span>

<span data-ttu-id="26261-128">Обратите внимание, что хотя указывать группу ресурсов необязательно для этого командлета, вы должны сделать это для лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="26261-128">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="26261-129">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26261-129">EXAMPLES</span></span>

### <span data-ttu-id="26261-130">Пример 1: предоставление разрешений пользователю для хранилища ключей и изменение разрешений</span><span class="sxs-lookup"><span data-stu-id="26261-130">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="26261-131">Первая команда предоставляет разрешения для пользователя в Azure Active Directory, PattiFuller@contoso.com для выполнения операций с ключами и секретами с помощью хранилища ключей с именем Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="26261-131">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="26261-132">Вторая команда изменяет разрешения, предоставленные PattiFuller@contoso.com первой командой, теперь позволяет получать секреты в дополнение к установке и удалению.</span><span class="sxs-lookup"><span data-stu-id="26261-132">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="26261-133">После этой команды разрешения на выполнение операций с клавишами остались неизменными.</span><span class="sxs-lookup"><span data-stu-id="26261-133">The permissions to key operations remain unchanged after this command.</span></span> <span data-ttu-id="26261-134">Параметр *PassThru* приводит к обновлению объекта, возвращаемого командлетом.</span><span class="sxs-lookup"><span data-stu-id="26261-134">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="26261-135">Последняя команда дополнительно изменяет существующие разрешения для PattiFuller@contoso.com удаления всех разрешений на выполнение операций с ключами.</span><span class="sxs-lookup"><span data-stu-id="26261-135">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="26261-136">После этой команды разрешения на выполнение операций с секретными действиями остаются неизменными.</span><span class="sxs-lookup"><span data-stu-id="26261-136">The permissions to secret operations remain unchanged after this command.</span></span> <span data-ttu-id="26261-137">Параметр *PassThru* приводит к обновлению объекта, возвращаемого командлетом.</span><span class="sxs-lookup"><span data-stu-id="26261-137">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="26261-138">Пример 2: предоставление разрешений на чтение и запись секретов для субъекта-службы приложения</span><span class="sxs-lookup"><span data-stu-id="26261-138">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="26261-139">Эта команда предоставляет приложению разрешения на доступ к хранилищу ключей с именем Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="26261-139">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span> 

<span data-ttu-id="26261-140">Параметр *"* имя приложения" Указывает приложение.</span><span class="sxs-lookup"><span data-stu-id="26261-140">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="26261-141">Приложение должно быть зарегистрировано в службе Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="26261-141">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="26261-142">Значение параметра "ИД *:" должно* быть либо именем субъекта-службы приложения, либо идентификатором GUID приложения.</span><span class="sxs-lookup"><span data-stu-id="26261-142">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>

<span data-ttu-id="26261-143">В этом примере задается имя субъекта-службы http://payroll.contoso.com , и команда предоставляет разрешения приложения на чтение и запись секретов.</span><span class="sxs-lookup"><span data-stu-id="26261-143">This example specifies the service principal name http://payroll.contoso.com, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="26261-144">Пример 3: предоставление разрешений на доступ к приложению с помощью идентификатора объекта</span><span class="sxs-lookup"><span data-stu-id="26261-144">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="26261-145">Эта команда предоставляет приложению разрешения на чтение и запись секретов.</span><span class="sxs-lookup"><span data-stu-id="26261-145">This command grants the application permissions to read and write secrets.</span></span>

<span data-ttu-id="26261-146">В этом примере приложение задается с помощью идентификатора объекта субъекта-службы приложения.</span><span class="sxs-lookup"><span data-stu-id="26261-146">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="26261-147">Пример 4: предоставление разрешений для основного имени пользователя</span><span class="sxs-lookup"><span data-stu-id="26261-147">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="26261-148">Эта команда предоставляет получение, список и задание разрешений для указанного основного имени пользователя, чтобы получить доступ к секретным данным.</span><span class="sxs-lookup"><span data-stu-id="26261-148">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="26261-149">Пример 5: включение секретных данных для получения из хранилища ключей с помощью поставщика ресурсов Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="26261-149">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="26261-150">Эта команда предоставляет доступ к зашифрованным данным из хранилища ключей Contoso03Vault с помощью поставщика ресурсов Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="26261-150">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="26261-151">Пример 6: предоставление разрешений группе безопасности</span><span class="sxs-lookup"><span data-stu-id="26261-151">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzureRmADGroup
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzureRmADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="26261-152">В первой команде используется командлет Get-AzureRmADGroup, чтобы получить все группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="26261-152">The first command uses the Get-AzureRmADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="26261-153">На экране выводятся три возвращенные группы с именами **group1** , **group2** и **group3**.</span><span class="sxs-lookup"><span data-stu-id="26261-153">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="26261-154">У нескольких групп может быть одно и то же имя, но всегда есть уникальный ObjectId.</span><span class="sxs-lookup"><span data-stu-id="26261-154">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="26261-155">Если возвращено несколько групп с одним и тем же именем, используйте ObjectId в выходных данных, чтобы определить, какой из них вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="26261-155">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="26261-156">Затем вы можете использовать вывод этой команды с Set-AzureRmKeyVaultAccessPolicy для предоставления разрешений на доступ к group2 для вашего хранилища ключей с именем **myownvault**.</span><span class="sxs-lookup"><span data-stu-id="26261-156">You then use the output of this command with Set-AzureRmKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="26261-157">В этом примере выполняется перечисление групп с именем "group2" в той же командной строке.</span><span class="sxs-lookup"><span data-stu-id="26261-157">This example enumerates the groups named 'group2' inline in the same command line.</span></span>

<span data-ttu-id="26261-158">В возвращаемом списке может быть несколько групп с именем "group2".</span><span class="sxs-lookup"><span data-stu-id="26261-158">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="26261-159">В этом примере первый элемент, обозначенный индексом 0, выбирается \[ \] в списке "возвращено".</span><span class="sxs-lookup"><span data-stu-id="26261-159">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="26261-160">Пример 7: предоставление службе Azure Information Protection доступа к ключу клиента, управляемому клиентом (BYOK)</span><span class="sxs-lookup"><span data-stu-id="26261-160">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="26261-161">Эта команда авторизует защиту данных Azure на использование управляемого пользователем ключа (например, "сделать свой ключ" или "BYOK") в качестве ключа клиента для защиты данных Azure.</span><span class="sxs-lookup"><span data-stu-id="26261-161">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>

<span data-ttu-id="26261-162">При выполнении этой команды укажите свое собственное имя хранилища ключей, но необходимо указать параметр «код *продукта» (* GUID **00000012-0000-0000-C000-000000000000)** и задать разрешения в этом примере.</span><span class="sxs-lookup"><span data-stu-id="26261-162">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="26261-163">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26261-163">PARAMETERS</span></span>

### <span data-ttu-id="26261-164">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="26261-164">-ApplicationId</span></span>
<span data-ttu-id="26261-165">Для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="26261-165">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26261-166">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="26261-166">-BypassObjectIdValidation</span></span>
<span data-ttu-id="26261-167">Позволяет указать идентификатор объекта, не проверяя, существует ли этот объект в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="26261-167">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>

<span data-ttu-id="26261-168">Используйте этот параметр только в том случае, если вы хотите предоставить доступ к своему хранилищу ключей ИДЕНТИФИКАТОРу объекта, который ссылается на делегированную группу безопасности из другого клиента Azure.</span><span class="sxs-lookup"><span data-stu-id="26261-168">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26261-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26261-169">-DefaultProfile</span></span>
<span data-ttu-id="26261-170">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="26261-170">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26261-171">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="26261-171">-EmailAddress</span></span>
<span data-ttu-id="26261-172">Указывает адрес электронной почты пользователя, которому нужно предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="26261-172">Specifies the user email address of the user to whom to grant permissions.</span></span>

<span data-ttu-id="26261-173">Этот адрес электронной почты должен содержаться в каталоге, связанном с текущей подпиской, и быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="26261-173">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26261-174">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="26261-174">-EnabledForDeployment</span></span>
<span data-ttu-id="26261-175">Включает поставщик ресурсов Microsoft. COMPUTE для извлечения секретов из этого ключа, если это временное хранилище ссылается на создание ресурсов (например, при создании виртуальной машины).</span><span class="sxs-lookup"><span data-stu-id="26261-175">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26261-176">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="26261-176">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="26261-177">Позволяет службе шифрования дисков Azure получить секретные ключи и их перетекание из этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="26261-177">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26261-178">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="26261-178">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="26261-179">Позволяет диспетчеру ресурсов Azure получать секреты из этого хранилища ключей при ссылке на это хранилище ключей в развертывании шаблона.</span><span class="sxs-lookup"><span data-stu-id="26261-179">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26261-180">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26261-180">-InputObject</span></span>
<span data-ttu-id="26261-181">Объект хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="26261-181">Key Vault Object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26261-182">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="26261-182">-ObjectId</span></span>
<span data-ttu-id="26261-183">Указывает идентификатор объекта пользователя или участника-службы в Azure Active Directory, для которого требуется предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="26261-183">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26261-184">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26261-184">-PassThru</span></span>
<span data-ttu-id="26261-185">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="26261-185">Returns an object representing the item with which you are working.</span></span>

<span data-ttu-id="26261-186">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="26261-186">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26261-187">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="26261-187">-PermissionsToCertificates</span></span>
<span data-ttu-id="26261-188">Задает массив разрешений на доступ к сертификату, предоставляемый пользователю или участнику службы.</span><span class="sxs-lookup"><span data-stu-id="26261-188">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="26261-189">Допустимые значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="26261-189">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="26261-190">Получить</span><span class="sxs-lookup"><span data-stu-id="26261-190">Get</span></span>
- <span data-ttu-id="26261-191">Список</span><span class="sxs-lookup"><span data-stu-id="26261-191">List</span></span>
- <span data-ttu-id="26261-192">Удаление</span><span class="sxs-lookup"><span data-stu-id="26261-192">Delete</span></span>
- <span data-ttu-id="26261-193">Заново</span><span class="sxs-lookup"><span data-stu-id="26261-193">Create</span></span>
- <span data-ttu-id="26261-194">Импортируем</span><span class="sxs-lookup"><span data-stu-id="26261-194">Import</span></span>
- <span data-ttu-id="26261-195">Обновление</span><span class="sxs-lookup"><span data-stu-id="26261-195">Update</span></span>
- <span data-ttu-id="26261-196">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="26261-196">Managecontacts</span></span>
- <span data-ttu-id="26261-197">Поставщики</span><span class="sxs-lookup"><span data-stu-id="26261-197">Getissuers</span></span>
- <span data-ttu-id="26261-198">Listissuers</span><span class="sxs-lookup"><span data-stu-id="26261-198">Listissuers</span></span>
- <span data-ttu-id="26261-199">Setissuers</span><span class="sxs-lookup"><span data-stu-id="26261-199">Setissuers</span></span>
- <span data-ttu-id="26261-200">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="26261-200">Deleteissuers</span></span>
- <span data-ttu-id="26261-201">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="26261-201">Manageissuers</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26261-202">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="26261-202">-PermissionsToKeys</span></span>
<span data-ttu-id="26261-203">Задает массив разрешений на операцию с ключом для предоставления пользователю или участнику службы.</span><span class="sxs-lookup"><span data-stu-id="26261-203">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="26261-204">Допустимые значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="26261-204">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="26261-205">Расшифровки</span><span class="sxs-lookup"><span data-stu-id="26261-205">Decrypt</span></span>
- <span data-ttu-id="26261-206">EFS</span><span class="sxs-lookup"><span data-stu-id="26261-206">Encrypt</span></span>
- <span data-ttu-id="26261-207">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="26261-207">UnwrapKey</span></span>
- <span data-ttu-id="26261-208">WrapKey</span><span class="sxs-lookup"><span data-stu-id="26261-208">WrapKey</span></span>
- <span data-ttu-id="26261-209">Подтвержда</span><span class="sxs-lookup"><span data-stu-id="26261-209">Verify</span></span>
- <span data-ttu-id="26261-210">Рядом</span><span class="sxs-lookup"><span data-stu-id="26261-210">Sign</span></span>
- <span data-ttu-id="26261-211">Получить</span><span class="sxs-lookup"><span data-stu-id="26261-211">Get</span></span>
- <span data-ttu-id="26261-212">Список</span><span class="sxs-lookup"><span data-stu-id="26261-212">List</span></span>
- <span data-ttu-id="26261-213">Обновление</span><span class="sxs-lookup"><span data-stu-id="26261-213">Update</span></span>
- <span data-ttu-id="26261-214">Заново</span><span class="sxs-lookup"><span data-stu-id="26261-214">Create</span></span>
- <span data-ttu-id="26261-215">Импортируем</span><span class="sxs-lookup"><span data-stu-id="26261-215">Import</span></span>
- <span data-ttu-id="26261-216">Удаление</span><span class="sxs-lookup"><span data-stu-id="26261-216">Delete</span></span>
- <span data-ttu-id="26261-217">Копирование</span><span class="sxs-lookup"><span data-stu-id="26261-217">Backup</span></span>
- <span data-ttu-id="26261-218">Восстановление</span><span class="sxs-lookup"><span data-stu-id="26261-218">Restore</span></span>
- <span data-ttu-id="26261-219">Устранения</span><span class="sxs-lookup"><span data-stu-id="26261-219">Recover</span></span>
- <span data-ttu-id="26261-220">Меня</span><span class="sxs-lookup"><span data-stu-id="26261-220">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26261-221">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="26261-221">-PermissionsToSecrets</span></span>
<span data-ttu-id="26261-222">Задает массив разрешений на секретную операцию для предоставления пользователю или участнику службы.</span><span class="sxs-lookup"><span data-stu-id="26261-222">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="26261-223">Допустимые значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="26261-223">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="26261-224">Получить</span><span class="sxs-lookup"><span data-stu-id="26261-224">Get</span></span>
- <span data-ttu-id="26261-225">Список</span><span class="sxs-lookup"><span data-stu-id="26261-225">List</span></span>
- <span data-ttu-id="26261-226">Свои</span><span class="sxs-lookup"><span data-stu-id="26261-226">Set</span></span>
- <span data-ttu-id="26261-227">Удаление</span><span class="sxs-lookup"><span data-stu-id="26261-227">Delete</span></span>
- <span data-ttu-id="26261-228">Копирование</span><span class="sxs-lookup"><span data-stu-id="26261-228">Backup</span></span>
- <span data-ttu-id="26261-229">Восстановление</span><span class="sxs-lookup"><span data-stu-id="26261-229">Restore</span></span>
- <span data-ttu-id="26261-230">Устранения</span><span class="sxs-lookup"><span data-stu-id="26261-230">Recover</span></span>
- <span data-ttu-id="26261-231">Меня</span><span class="sxs-lookup"><span data-stu-id="26261-231">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26261-232">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="26261-232">-PermissionsToStorage</span></span>
<span data-ttu-id="26261-233">Задает управляемую учетную запись хранения и разрешения операций определения SaS, предоставляемые пользователю или участнику службы.</span><span class="sxs-lookup"><span data-stu-id="26261-233">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26261-234">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26261-234">-ResourceGroupName</span></span>
<span data-ttu-id="26261-235">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26261-235">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26261-236">-Намерено</span><span class="sxs-lookup"><span data-stu-id="26261-236">-ServicePrincipalName</span></span>
<span data-ttu-id="26261-237">Указывает имя субъекта-службы для приложения, которому нужно предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="26261-237">Specifies the service principal name of the application to which to grant permissions.</span></span>

<span data-ttu-id="26261-238">Укажите идентификатор приложения, который также называется ИДЕНТИФИКАТОРом клиента, зарегистрированный для приложения в AzureActive Directory.</span><span class="sxs-lookup"><span data-stu-id="26261-238">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="26261-239">Приложение с именем субъекта-службы, которое указывает этот параметр, должно быть зарегистрировано в каталоге Azure, содержащем текущую подписку.</span><span class="sxs-lookup"><span data-stu-id="26261-239">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26261-240">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="26261-240">-UserPrincipalName</span></span>
<span data-ttu-id="26261-241">Указывает имя участника-пользователя, которому нужно предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="26261-241">Specifies the user principal name of the user to whom to grant permissions.</span></span>

<span data-ttu-id="26261-242">Это имя участника-пользователя должно существовать в каталоге, связанном с текущей подпиской.</span><span class="sxs-lookup"><span data-stu-id="26261-242">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26261-243">-VaultName</span><span class="sxs-lookup"><span data-stu-id="26261-243">-VaultName</span></span>
<span data-ttu-id="26261-244">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="26261-244">Specifies the name of a key vault.</span></span>

<span data-ttu-id="26261-245">Этот командлет изменяет политику доступа для хранилища ключей, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="26261-245">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26261-246">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26261-246">-Confirm</span></span>
<span data-ttu-id="26261-247">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="26261-247">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26261-248">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26261-248">-WhatIf</span></span>
<span data-ttu-id="26261-249">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="26261-249">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26261-250">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="26261-250">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26261-251">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26261-251">CommonParameters</span></span>
<span data-ttu-id="26261-252">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26261-252">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26261-253">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26261-253">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26261-254">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26261-254">INPUTS</span></span>

### <span data-ttu-id="26261-255">String, GUID, String [], переключатель</span><span class="sxs-lookup"><span data-stu-id="26261-255">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="26261-256">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26261-256">OUTPUTS</span></span>

### <span data-ttu-id="26261-257">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="26261-257">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="26261-258">Пуск</span><span class="sxs-lookup"><span data-stu-id="26261-258">NOTES</span></span>

## <span data-ttu-id="26261-259">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26261-259">RELATED LINKS</span></span>

[<span data-ttu-id="26261-260">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="26261-260">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="26261-261">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="26261-261">Remove-AzureRmKeyVaultAccessPolicy</span></span>](./Remove-AzureRmKeyVaultAccessPolicy.md)

