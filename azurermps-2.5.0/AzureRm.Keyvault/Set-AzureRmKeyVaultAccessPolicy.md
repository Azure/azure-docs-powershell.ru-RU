---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurermkeyvaultaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 413f0e22139abe26a2be34a607587042739df1d5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913314"
---
# <span data-ttu-id="b59b7-101">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b59b7-101">Set-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="b59b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b59b7-102">SYNOPSIS</span></span>
<span data-ttu-id="b59b7-103">Предоставление или изменение существующих разрешений для пользователя, приложения или группы безопасности для выполнения операций с помощью хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="b59b7-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b59b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b59b7-104">SYNTAX</span></span>

### <span data-ttu-id="b59b7-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b59b7-105">ByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b59b7-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="b59b7-106">ByUserPrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b59b7-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="b59b7-107">ByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b59b7-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="b59b7-108">ByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b59b7-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="b59b7-109">ForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b59b7-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b59b7-110">DESCRIPTION</span></span>
<span data-ttu-id="b59b7-111">Командлет **Set-AzureRmKeyVaultAccessPolicy** предоставляет или изменяет существующие разрешения для пользователя, приложения или группы безопасности для выполнения указанных операций с помощью хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="b59b7-111">The **Set-AzureRmKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="b59b7-112">Изменения, внесенные другими пользователями, приложениями или группами безопасности, не изменяются в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="b59b7-112">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="b59b7-113">Если вы настраиваете разрешения для группы безопасности, эта операция влияет только на пользователей в этой группе безопасности.</span><span class="sxs-lookup"><span data-stu-id="b59b7-113">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="b59b7-114">Следующие каталоги должны находиться в одном каталоге Azure:</span><span class="sxs-lookup"><span data-stu-id="b59b7-114">The following directories must all be the same Azure directory:</span></span> 
- <span data-ttu-id="b59b7-115">Каталог подписки Azure по умолчанию, в котором находится хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="b59b7-115">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="b59b7-116">Каталог Azure, содержащий пользователя или группу приложений, которым предоставляются разрешения.</span><span class="sxs-lookup"><span data-stu-id="b59b7-116">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="b59b7-117">Примеры ситуаций, когда эти условия не выполняются, и этот командлет не работает.</span><span class="sxs-lookup"><span data-stu-id="b59b7-117">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span> 

- <span data-ttu-id="b59b7-118">Авторизация пользователя из другой организации для управления вашим хранилищем ключей.</span><span class="sxs-lookup"><span data-stu-id="b59b7-118">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="b59b7-119">Каждая организация имеет собственный каталог.</span><span class="sxs-lookup"><span data-stu-id="b59b7-119">Each organization has its own directory.</span></span> 
- <span data-ttu-id="b59b7-120">У вашей учетной записи Azure есть несколько каталогов.</span><span class="sxs-lookup"><span data-stu-id="b59b7-120">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="b59b7-121">Если зарегистрировать приложение в каталоге, отличном от каталога по умолчанию, вы не сможете авторизовать это приложение для использования вашего хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="b59b7-121">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="b59b7-122">Приложение должно быть в каталоге по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b59b7-122">The application must be in the default directory.</span></span>

<span data-ttu-id="b59b7-123">Обратите внимание, что хотя указывать группу ресурсов необязательно для этого командлета, вы должны сделать это для лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="b59b7-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="b59b7-124">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b59b7-124">EXAMPLES</span></span>

### <span data-ttu-id="b59b7-125">Пример 1: предоставление разрешений пользователю для хранилища ключей и изменение разрешений</span><span class="sxs-lookup"><span data-stu-id="b59b7-125">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets 'set,delete'
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="b59b7-126">Первая команда предоставляет разрешения для пользователя в Azure Active Directory, PattiFuller@contoso.com для выполнения операций с ключами и секретами с помощью хранилища ключей с именем Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="b59b7-126">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="b59b7-127">Вторая команда изменяет разрешения, предоставленные PattiFuller@contoso.com первой командой, теперь позволяет получать секреты в дополнение к установке и удалению.</span><span class="sxs-lookup"><span data-stu-id="b59b7-127">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="b59b7-128">После этой команды разрешения на выполнение операций с клавишами остались неизменными.</span><span class="sxs-lookup"><span data-stu-id="b59b7-128">The permissions to key operations remain unchanged after this command.</span></span> <span data-ttu-id="b59b7-129">Параметр *PassThru* приводит к обновлению объекта, возвращаемого командлетом.</span><span class="sxs-lookup"><span data-stu-id="b59b7-129">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="b59b7-130">Последняя команда дополнительно изменяет существующие разрешения для PattiFuller@contoso.com удаления всех разрешений на выполнение операций с ключами.</span><span class="sxs-lookup"><span data-stu-id="b59b7-130">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="b59b7-131">После этой команды разрешения на выполнение операций с секретными действиями остаются неизменными.</span><span class="sxs-lookup"><span data-stu-id="b59b7-131">The permissions to secret operations remain unchanged after this command.</span></span> <span data-ttu-id="b59b7-132">Параметр *PassThru* приводит к обновлению объекта, возвращаемого командлетом.</span><span class="sxs-lookup"><span data-stu-id="b59b7-132">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="b59b7-133">Пример 2: предоставление разрешений на чтение и запись секретов для субъекта-службы приложения</span><span class="sxs-lookup"><span data-stu-id="b59b7-133">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="b59b7-134">Эта команда предоставляет приложению разрешения на доступ к хранилищу ключей с именем Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="b59b7-134">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span> 

<span data-ttu-id="b59b7-135">Параметр *"* имя приложения" Указывает приложение.</span><span class="sxs-lookup"><span data-stu-id="b59b7-135">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="b59b7-136">Приложение должно быть зарегистрировано в службе Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b59b7-136">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="b59b7-137">Значение параметра "ИД *:" должно* быть либо именем субъекта-службы приложения, либо идентификатором GUID приложения.</span><span class="sxs-lookup"><span data-stu-id="b59b7-137">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>

<span data-ttu-id="b59b7-138">В этом примере задается имя субъекта-службы http://payroll.contoso.com , и команда предоставляет разрешения приложения на чтение и запись секретов.</span><span class="sxs-lookup"><span data-stu-id="b59b7-138">This example specifies the service principal name http://payroll.contoso.com, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="b59b7-139">Пример 3: предоставление разрешений на доступ к приложению с помощью идентификатора объекта</span><span class="sxs-lookup"><span data-stu-id="b59b7-139">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="b59b7-140">Эта команда предоставляет приложению разрешения на чтение и запись секретов.</span><span class="sxs-lookup"><span data-stu-id="b59b7-140">This command grants the application permissions to read and write secrets.</span></span>

<span data-ttu-id="b59b7-141">В этом примере приложение задается с помощью идентификатора объекта субъекта-службы приложения.</span><span class="sxs-lookup"><span data-stu-id="b59b7-141">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="b59b7-142">Пример 4: предоставление разрешений для основного имени пользователя</span><span class="sxs-lookup"><span data-stu-id="b59b7-142">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="b59b7-143">Эта команда предоставляет получение, список и задание разрешений для указанного основного имени пользователя, чтобы получить доступ к секретным данным.</span><span class="sxs-lookup"><span data-stu-id="b59b7-143">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="b59b7-144">Пример 5: включение секретных данных для получения из хранилища ключей с помощью поставщика ресурсов Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="b59b7-144">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="b59b7-145">Эта команда предоставляет доступ к зашифрованным данным из хранилища ключей Contoso03Vault с помощью поставщика ресурсов Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="b59b7-145">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="b59b7-146">Пример 6: предоставление разрешений группе безопасности</span><span class="sxs-lookup"><span data-stu-id="b59b7-146">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzureRmADGroup
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzureRmADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="b59b7-147">В первой команде используется командлет Get-AzureRmADGroup, чтобы получить все группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b59b7-147">The first command uses the Get-AzureRmADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="b59b7-148">На экране выводятся три возвращенные группы с именами **group1** , **group2** и **group3**.</span><span class="sxs-lookup"><span data-stu-id="b59b7-148">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="b59b7-149">У нескольких групп может быть одно и то же имя, но всегда есть уникальный ObjectId.</span><span class="sxs-lookup"><span data-stu-id="b59b7-149">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="b59b7-150">Если возвращено несколько групп с одним и тем же именем, используйте ObjectId в выходных данных, чтобы определить, какой из них вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="b59b7-150">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="b59b7-151">Затем вы можете использовать вывод этой команды с Set-AzureRmKeyVaultAccessPolicy для предоставления разрешений на доступ к group2 для вашего хранилища ключей с именем **myownvault**.</span><span class="sxs-lookup"><span data-stu-id="b59b7-151">You then use the output of this command with Set-AzureRmKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="b59b7-152">В этом примере выполняется перечисление групп с именем "group2" в той же командной строке.</span><span class="sxs-lookup"><span data-stu-id="b59b7-152">This example enumerates the groups named 'group2' inline in the same command line.</span></span>

<span data-ttu-id="b59b7-153">В возвращаемом списке может быть несколько групп с именем "group2".</span><span class="sxs-lookup"><span data-stu-id="b59b7-153">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="b59b7-154">В этом примере первый элемент, обозначенный индексом 0, выбирается \[ \] в списке "возвращено".</span><span class="sxs-lookup"><span data-stu-id="b59b7-154">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="b59b7-155">Пример 7: предоставление службе Azure Information Protection доступа к ключу клиента, управляемому клиентом (BYOK)</span><span class="sxs-lookup"><span data-stu-id="b59b7-155">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="b59b7-156">Эта команда авторизует защиту данных Azure на использование управляемого пользователем ключа (например, "сделать свой ключ" или "BYOK") в качестве ключа клиента для защиты данных Azure.</span><span class="sxs-lookup"><span data-stu-id="b59b7-156">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>

<span data-ttu-id="b59b7-157">При выполнении этой команды укажите свое собственное имя хранилища ключей, но необходимо указать параметр «код *продукта» (* GUID **00000012-0000-0000-C000-000000000000)** и задать разрешения в этом примере.</span><span class="sxs-lookup"><span data-stu-id="b59b7-157">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="b59b7-158">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b59b7-158">PARAMETERS</span></span>

### <span data-ttu-id="b59b7-159">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b59b7-159">-ApplicationId</span></span>
<span data-ttu-id="b59b7-160">Для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="b59b7-160">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59b7-161">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="b59b7-161">-BypassObjectIdValidation</span></span>
<span data-ttu-id="b59b7-162">Позволяет указать идентификатор объекта, не проверяя, существует ли этот объект в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b59b7-162">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>

<span data-ttu-id="b59b7-163">Используйте этот параметр только в том случае, если вы хотите предоставить доступ к своему хранилищу ключей ИДЕНТИФИКАТОРу объекта, который ссылается на делегированную группу безопасности из другого клиента Azure.</span><span class="sxs-lookup"><span data-stu-id="b59b7-163">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59b7-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b59b7-164">-DefaultProfile</span></span>
<span data-ttu-id="b59b7-165">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b59b7-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b59b7-166">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="b59b7-166">-EmailAddress</span></span>
<span data-ttu-id="b59b7-167">Указывает адрес электронной почты пользователя, которому нужно предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="b59b7-167">Specifies the user email address of the user to whom to grant permissions.</span></span>

<span data-ttu-id="b59b7-168">Этот адрес электронной почты должен содержаться в каталоге, связанном с текущей подпиской, и быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="b59b7-168">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: String
Parameter Sets: ByEmailAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59b7-169">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="b59b7-169">-EnabledForDeployment</span></span>
<span data-ttu-id="b59b7-170">Включает поставщик ресурсов Microsoft. COMPUTE для извлечения секретов из этого ключа, если это временное хранилище ссылается на создание ресурсов (например, при создании виртуальной машины).</span><span class="sxs-lookup"><span data-stu-id="b59b7-170">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59b7-171">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="b59b7-171">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="b59b7-172">Позволяет службе шифрования дисков Azure получить секретные ключи и их перетекание из этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="b59b7-172">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59b7-173">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="b59b7-173">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="b59b7-174">Позволяет диспетчеру ресурсов Azure получать секреты из этого хранилища ключей при ссылке на это хранилище ключей в развертывании шаблона.</span><span class="sxs-lookup"><span data-stu-id="b59b7-174">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59b7-175">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b59b7-175">-ObjectId</span></span>
<span data-ttu-id="b59b7-176">Указывает идентификатор объекта пользователя или участника-службы в Azure Active Directory, для которого требуется предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="b59b7-176">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59b7-177">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b59b7-177">-PassThru</span></span>
<span data-ttu-id="b59b7-178">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b59b7-178">Returns an object representing the item with which you are working.</span></span>

<span data-ttu-id="b59b7-179">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b59b7-179">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b59b7-180">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="b59b7-180">-PermissionsToCertificates</span></span>
<span data-ttu-id="b59b7-181">Задает массив разрешений на доступ к сертификату, предоставляемый пользователю или участнику службы.</span><span class="sxs-lookup"><span data-stu-id="b59b7-181">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="b59b7-182">Допустимые значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="b59b7-182">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="b59b7-183">Получить</span><span class="sxs-lookup"><span data-stu-id="b59b7-183">Get</span></span>
- <span data-ttu-id="b59b7-184">Список</span><span class="sxs-lookup"><span data-stu-id="b59b7-184">List</span></span>
- <span data-ttu-id="b59b7-185">Удаление</span><span class="sxs-lookup"><span data-stu-id="b59b7-185">Delete</span></span>
- <span data-ttu-id="b59b7-186">Заново</span><span class="sxs-lookup"><span data-stu-id="b59b7-186">Create</span></span>
- <span data-ttu-id="b59b7-187">Импортируем</span><span class="sxs-lookup"><span data-stu-id="b59b7-187">Import</span></span>
- <span data-ttu-id="b59b7-188">Обновление</span><span class="sxs-lookup"><span data-stu-id="b59b7-188">Update</span></span>
- <span data-ttu-id="b59b7-189">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="b59b7-189">Managecontacts</span></span>
- <span data-ttu-id="b59b7-190">Поставщики</span><span class="sxs-lookup"><span data-stu-id="b59b7-190">Getissuers</span></span>
- <span data-ttu-id="b59b7-191">Listissuers</span><span class="sxs-lookup"><span data-stu-id="b59b7-191">Listissuers</span></span>
- <span data-ttu-id="b59b7-192">Setissuers</span><span class="sxs-lookup"><span data-stu-id="b59b7-192">Setissuers</span></span>
- <span data-ttu-id="b59b7-193">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="b59b7-193">Deleteissuers</span></span>
- <span data-ttu-id="b59b7-194">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="b59b7-194">Manageissuers</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59b7-195">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="b59b7-195">-PermissionsToKeys</span></span>
<span data-ttu-id="b59b7-196">Задает массив разрешений на операцию с ключом для предоставления пользователю или участнику службы.</span><span class="sxs-lookup"><span data-stu-id="b59b7-196">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="b59b7-197">Допустимые значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="b59b7-197">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="b59b7-198">Расшифровки</span><span class="sxs-lookup"><span data-stu-id="b59b7-198">Decrypt</span></span>
- <span data-ttu-id="b59b7-199">EFS</span><span class="sxs-lookup"><span data-stu-id="b59b7-199">Encrypt</span></span>
- <span data-ttu-id="b59b7-200">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="b59b7-200">UnwrapKey</span></span>
- <span data-ttu-id="b59b7-201">WrapKey</span><span class="sxs-lookup"><span data-stu-id="b59b7-201">WrapKey</span></span>
- <span data-ttu-id="b59b7-202">Подтвержда</span><span class="sxs-lookup"><span data-stu-id="b59b7-202">Verify</span></span>
- <span data-ttu-id="b59b7-203">Рядом</span><span class="sxs-lookup"><span data-stu-id="b59b7-203">Sign</span></span>
- <span data-ttu-id="b59b7-204">Получить</span><span class="sxs-lookup"><span data-stu-id="b59b7-204">Get</span></span>
- <span data-ttu-id="b59b7-205">Список</span><span class="sxs-lookup"><span data-stu-id="b59b7-205">List</span></span>
- <span data-ttu-id="b59b7-206">Обновление</span><span class="sxs-lookup"><span data-stu-id="b59b7-206">Update</span></span>
- <span data-ttu-id="b59b7-207">Заново</span><span class="sxs-lookup"><span data-stu-id="b59b7-207">Create</span></span>
- <span data-ttu-id="b59b7-208">Импортируем</span><span class="sxs-lookup"><span data-stu-id="b59b7-208">Import</span></span>
- <span data-ttu-id="b59b7-209">Удаление</span><span class="sxs-lookup"><span data-stu-id="b59b7-209">Delete</span></span>
- <span data-ttu-id="b59b7-210">Копирование</span><span class="sxs-lookup"><span data-stu-id="b59b7-210">Backup</span></span>
- <span data-ttu-id="b59b7-211">Восстановление</span><span class="sxs-lookup"><span data-stu-id="b59b7-211">Restore</span></span>
- <span data-ttu-id="b59b7-212">Устранения</span><span class="sxs-lookup"><span data-stu-id="b59b7-212">Recover</span></span>
- <span data-ttu-id="b59b7-213">Меня</span><span class="sxs-lookup"><span data-stu-id="b59b7-213">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59b7-214">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="b59b7-214">-PermissionsToSecrets</span></span>
<span data-ttu-id="b59b7-215">Задает массив разрешений на секретную операцию для предоставления пользователю или участнику службы.</span><span class="sxs-lookup"><span data-stu-id="b59b7-215">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="b59b7-216">Допустимые значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="b59b7-216">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="b59b7-217">Получить</span><span class="sxs-lookup"><span data-stu-id="b59b7-217">Get</span></span>
- <span data-ttu-id="b59b7-218">Список</span><span class="sxs-lookup"><span data-stu-id="b59b7-218">List</span></span>
- <span data-ttu-id="b59b7-219">Свои</span><span class="sxs-lookup"><span data-stu-id="b59b7-219">Set</span></span>
- <span data-ttu-id="b59b7-220">Удаление</span><span class="sxs-lookup"><span data-stu-id="b59b7-220">Delete</span></span>
- <span data-ttu-id="b59b7-221">Копирование</span><span class="sxs-lookup"><span data-stu-id="b59b7-221">Backup</span></span>
- <span data-ttu-id="b59b7-222">Восстановление</span><span class="sxs-lookup"><span data-stu-id="b59b7-222">Restore</span></span>
- <span data-ttu-id="b59b7-223">Устранения</span><span class="sxs-lookup"><span data-stu-id="b59b7-223">Recover</span></span>
- <span data-ttu-id="b59b7-224">Меня</span><span class="sxs-lookup"><span data-stu-id="b59b7-224">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59b7-225">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="b59b7-225">-PermissionsToStorage</span></span>
<span data-ttu-id="b59b7-226">Задает управляемую учетную запись хранения и разрешения операций определения SaS, предоставляемые пользователю или участнику службы.</span><span class="sxs-lookup"><span data-stu-id="b59b7-226">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59b7-227">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b59b7-227">-ResourceGroupName</span></span>
<span data-ttu-id="b59b7-228">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b59b7-228">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59b7-229">-Намерено</span><span class="sxs-lookup"><span data-stu-id="b59b7-229">-ServicePrincipalName</span></span>
<span data-ttu-id="b59b7-230">Указывает имя субъекта-службы для приложения, которому нужно предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="b59b7-230">Specifies the service principal name of the application to which to grant permissions.</span></span>

<span data-ttu-id="b59b7-231">Укажите идентификатор приложения, который также называется ИДЕНТИФИКАТОРом клиента, зарегистрированный для приложения в AzureActive Directory.</span><span class="sxs-lookup"><span data-stu-id="b59b7-231">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="b59b7-232">Приложение с именем субъекта-службы, которое указывает этот параметр, должно быть зарегистрировано в каталоге Azure, содержащем текущую подписку.</span><span class="sxs-lookup"><span data-stu-id="b59b7-232">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59b7-233">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="b59b7-233">-UserPrincipalName</span></span>
<span data-ttu-id="b59b7-234">Указывает имя участника-пользователя, которому нужно предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="b59b7-234">Specifies the user principal name of the user to whom to grant permissions.</span></span>

<span data-ttu-id="b59b7-235">Это имя участника-пользователя должно существовать в каталоге, связанном с текущей подпиской.</span><span class="sxs-lookup"><span data-stu-id="b59b7-235">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59b7-236">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b59b7-236">-VaultName</span></span>
<span data-ttu-id="b59b7-237">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="b59b7-237">Specifies the name of a key vault.</span></span>

<span data-ttu-id="b59b7-238">Этот командлет изменяет политику доступа для хранилища ключей, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b59b7-238">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59b7-239">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b59b7-239">-Confirm</span></span>
<span data-ttu-id="b59b7-240">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b59b7-240">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b59b7-241">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b59b7-241">-WhatIf</span></span>
<span data-ttu-id="b59b7-242">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b59b7-242">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b59b7-243">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b59b7-243">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b59b7-244">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b59b7-244">CommonParameters</span></span>
<span data-ttu-id="b59b7-245">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b59b7-245">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b59b7-246">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b59b7-246">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b59b7-247">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b59b7-247">INPUTS</span></span>

### <span data-ttu-id="b59b7-248">String, GUID, String [], переключатель</span><span class="sxs-lookup"><span data-stu-id="b59b7-248">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="b59b7-249">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b59b7-249">OUTPUTS</span></span>

### <span data-ttu-id="b59b7-250">Microsoft. Azure. Commands. KeyVault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="b59b7-250">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="b59b7-251">Пуск</span><span class="sxs-lookup"><span data-stu-id="b59b7-251">NOTES</span></span>

## <span data-ttu-id="b59b7-252">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b59b7-252">RELATED LINKS</span></span>

[<span data-ttu-id="b59b7-253">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b59b7-253">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="b59b7-254">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b59b7-254">Remove-AzureRmKeyVaultAccessPolicy</span></span>](./Remove-AzureRmKeyVaultAccessPolicy.md)

