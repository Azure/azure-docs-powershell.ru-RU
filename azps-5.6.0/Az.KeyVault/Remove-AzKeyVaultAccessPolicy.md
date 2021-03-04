---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 0062b345a78063028ffe0c0c983ab73af66cf674
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952616"
---
# <span data-ttu-id="cf26a-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cf26a-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="cf26a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf26a-102">SYNOPSIS</span></span>
<span data-ttu-id="cf26a-103">Удаляет все разрешения для пользователя или приложения из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="cf26a-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="cf26a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cf26a-104">SYNTAX</span></span>

### <span data-ttu-id="cf26a-105">ByUserPrincipalName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf26a-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf26a-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="cf26a-106">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf26a-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="cf26a-107">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf26a-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="cf26a-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf26a-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="cf26a-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf26a-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="cf26a-110">InputObjectByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf26a-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="cf26a-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf26a-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cf26a-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf26a-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="cf26a-113">InputObjectByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf26a-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="cf26a-114">InputObjectForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf26a-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="cf26a-115">ResourceIdByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf26a-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="cf26a-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf26a-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cf26a-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf26a-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="cf26a-118">ResourceIdByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf26a-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="cf26a-119">ResourceIdForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf26a-120">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf26a-120">DESCRIPTION</span></span>
<span data-ttu-id="cf26a-121">**Cmdlet Remove-AzKeyVaultAccessPolicy** удаляет все разрешения для пользователя или приложения или всех пользователей и приложений из хранилища ключа.</span><span class="sxs-lookup"><span data-stu-id="cf26a-121">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="cf26a-122">Даже если вы удалите все разрешения, владелец подписки Azure, которая содержит ключевое хранилище, может добавить разрешения в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="cf26a-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="cf26a-123">Обратите внимание на то, что хотя для этого cmdlet не требуется указывать группу ресурсов, это следует сделать для улучшения производительности.</span><span class="sxs-lookup"><span data-stu-id="cf26a-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="cf26a-124">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cf26a-124">EXAMPLES</span></span>

### <span data-ttu-id="cf26a-125">Пример 1. Удаление разрешений для пользователя</span><span class="sxs-lookup"><span data-stu-id="cf26a-125">Example 1: Remove permissions for a user</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     :
                                   Permissions to Certificates                : get, create
                                   Permissions to (Key Vault Managed) Storage :


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="cf26a-126">Эта команда удаляет все разрешения пользователя в хранилище ключей PattiFuller@contoso.com Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="cf26a-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="cf26a-127">Если задано значение -PassThru, возвращается объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="cf26a-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="cf26a-128">Пример 2. Удаление разрешений для приложения</span><span class="sxs-lookup"><span data-stu-id="cf26a-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="cf26a-129">Эта команда удаляет все разрешения приложения в хранилище ключей Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="cf26a-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="cf26a-130">В этом примере приложение идентифицируется с помощью имени директора-службы, зарегистрированного в Azure Active `http://payroll.contoso.com` Directory.</span><span class="sxs-lookup"><span data-stu-id="cf26a-130">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="cf26a-131">Пример 3. Удаление разрешений для приложения с помощью ИД объекта</span><span class="sxs-lookup"><span data-stu-id="cf26a-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="cf26a-132">Эта команда удаляет все разрешения приложения в хранилище ключей Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="cf26a-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="cf26a-133">В этом примере приложение идентифицируется идентификатором объекта, который является основной службой.</span><span class="sxs-lookup"><span data-stu-id="cf26a-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="cf26a-134">Пример 4. Удаление разрешений для поставщика ресурсов Microsoft.Comput</span><span class="sxs-lookup"><span data-stu-id="cf26a-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="cf26a-135">Эта команда удаляет разрешение поставщика ресурсов Microsoft.Compute на доступ к секретам Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="cf26a-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="cf26a-136">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf26a-136">PARAMETERS</span></span>

### <span data-ttu-id="cf26a-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="cf26a-137">-ApplicationId</span></span>
<span data-ttu-id="cf26a-138">Определяет ИД приложения, разрешения которого нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="cf26a-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="cf26a-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf26a-139">-DefaultProfile</span></span>
<span data-ttu-id="cf26a-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cf26a-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf26a-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="cf26a-141">-EmailAddress</span></span>
<span data-ttu-id="cf26a-142">Указывает адрес электронной почты пользователя, доступ которого вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="cf26a-142">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmail, InputObjectByEmail, ResourceIdByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf26a-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="cf26a-143">-EnabledForDeployment</span></span>
<span data-ttu-id="cf26a-144">При этом при создании ресурсов отключается инижа секретов из этого ключевого хранилища поставщиком ресурсов Microsoft.Compute.</span><span class="sxs-lookup"><span data-stu-id="cf26a-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="cf26a-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="cf26a-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="cf26a-146">При этом отключает истику секретов из этого хранилища ключа с помощью шифрования диска Azure.</span><span class="sxs-lookup"><span data-stu-id="cf26a-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="cf26a-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="cf26a-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="cf26a-148">При указании в шаблонах отключено инижай секретов из этого сейфа с помощью Диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="cf26a-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="cf26a-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf26a-149">-InputObject</span></span>
<span data-ttu-id="cf26a-150">Объект Key Vault.</span><span class="sxs-lookup"><span data-stu-id="cf26a-150">Key Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf26a-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cf26a-151">-ObjectId</span></span>
<span data-ttu-id="cf26a-152">Определяет ИД объекта пользователя или основной службы в Azure Active Directory, для которого нужно удалить разрешения.</span><span class="sxs-lookup"><span data-stu-id="cf26a-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="cf26a-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf26a-153">-PassThru</span></span>
<span data-ttu-id="cf26a-154">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="cf26a-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cf26a-155">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cf26a-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cf26a-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf26a-156">-ResourceGroupName</span></span>
<span data-ttu-id="cf26a-157">Указывает имя группы ресурсов, связанной с хранилищем ключа, для которого была изменена политика доступа.</span><span class="sxs-lookup"><span data-stu-id="cf26a-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="cf26a-158">Если он не задан, этот cmdlet выполняет поиск ключевого сейфа в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="cf26a-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf26a-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf26a-159">-ResourceId</span></span>
<span data-ttu-id="cf26a-160">ИД ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="cf26a-160">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmail, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf26a-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="cf26a-161">-ServicePrincipalName</span></span>
<span data-ttu-id="cf26a-162">Указывает имя директора-службы приложения, разрешения которого вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="cf26a-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="cf26a-163">Укажите ИД приложения, также известный как ИД клиента, зарегистрированный для приложения в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cf26a-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="cf26a-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cf26a-164">-UserPrincipalName</span></span>
<span data-ttu-id="cf26a-165">Указывает имя пользователя, доступ которого вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="cf26a-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="cf26a-166">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cf26a-166">-VaultName</span></span>
<span data-ttu-id="cf26a-167">Указывает имя сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="cf26a-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="cf26a-168">Этот cmdlet удаляет разрешения для хранилища ключей, указанные этим параметром.</span><span class="sxs-lookup"><span data-stu-id="cf26a-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf26a-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf26a-169">-Confirm</span></span>
<span data-ttu-id="cf26a-170">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cf26a-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf26a-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf26a-171">-WhatIf</span></span>
<span data-ttu-id="cf26a-172">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf26a-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf26a-173">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cf26a-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf26a-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf26a-174">CommonParameters</span></span>
<span data-ttu-id="cf26a-175">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf26a-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf26a-176">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf26a-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf26a-177">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf26a-177">INPUTS</span></span>

### <span data-ttu-id="cf26a-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="cf26a-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="cf26a-179">System.String</span><span class="sxs-lookup"><span data-stu-id="cf26a-179">System.String</span></span>

## <span data-ttu-id="cf26a-180">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cf26a-180">OUTPUTS</span></span>

### <span data-ttu-id="cf26a-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="cf26a-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="cf26a-182">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cf26a-182">NOTES</span></span>

## <span data-ttu-id="cf26a-183">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf26a-183">RELATED LINKS</span></span>

[<span data-ttu-id="cf26a-184">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cf26a-184">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

