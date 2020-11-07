---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: a0cf20ad9fafbae2ed6902226e396b3d732cee5c
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "93915514"
---
# <span data-ttu-id="01456-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="01456-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="01456-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01456-102">SYNOPSIS</span></span>
<span data-ttu-id="01456-103">Удаляет все разрешения для пользователя или приложения из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="01456-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="01456-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01456-104">SYNTAX</span></span>

### <span data-ttu-id="01456-105">ByUserPrincipalName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="01456-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01456-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="01456-106">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01456-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="01456-107">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01456-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="01456-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01456-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="01456-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01456-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="01456-110">InputObjectByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01456-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="01456-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01456-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="01456-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01456-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="01456-113">InputObjectByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01456-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="01456-114">InputObjectForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01456-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="01456-115">ResourceIdByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01456-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="01456-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01456-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="01456-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01456-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="01456-118">ResourceIdByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01456-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="01456-119">ResourceIdForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01456-120">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01456-120">DESCRIPTION</span></span>
<span data-ttu-id="01456-121">Командлет **Remove-AzKeyVaultAccessPolicy** удаляет все разрешения для пользователя или приложения или для всех пользователей и приложений из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="01456-121">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="01456-122">Даже если вы удалите все разрешения, владелец подписки Azure, которая имеет хранилище ключей, может добавить разрешения в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="01456-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="01456-123">Обратите внимание, что хотя указывать группу ресурсов необязательно для этого командлета, вы должны сделать это для лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="01456-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="01456-124">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01456-124">EXAMPLES</span></span>

### <span data-ttu-id="01456-125">Пример 1: удаление разрешений для пользователя</span><span class="sxs-lookup"><span data-stu-id="01456-125">Example 1: Remove permissions for a user</span></span>
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

<span data-ttu-id="01456-126">Эта команда удаляет все разрешения, которые пользователь PattiFuller@contoso.com имеет в хранилище ключей с именем Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="01456-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="01456-127">Если задано значение-PassThru, возвращается объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="01456-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="01456-128">Пример 2: удаление разрешений для приложения</span><span class="sxs-lookup"><span data-stu-id="01456-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="01456-129">Эта команда удаляет все разрешения, которые приложение имеет в хранилище ключей с именем Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="01456-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="01456-130">В этом примере приложение идентифицируется с использованием имени субъекта-службы, зарегистрированного в Azure Active Directory `http://payroll.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="01456-130">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="01456-131">Пример 3: удаление разрешений для приложения с помощью идентификатора объекта</span><span class="sxs-lookup"><span data-stu-id="01456-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="01456-132">Эта команда удаляет все разрешения, которые приложение имеет в хранилище ключей с именем Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="01456-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="01456-133">В этом примере приложение идентифицируется по ИДЕНТИФИКАТОРу объекта участника-службы.</span><span class="sxs-lookup"><span data-stu-id="01456-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="01456-134">Пример 4: удаление разрешений для поставщика ресурсов Microsoft. COMPUTE</span><span class="sxs-lookup"><span data-stu-id="01456-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="01456-135">Эта команда удаляет разрешения для поставщика ресурсов Microsoft. COMPUTE, чтобы получать секреты из Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="01456-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="01456-136">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01456-136">PARAMETERS</span></span>

### <span data-ttu-id="01456-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="01456-137">-ApplicationId</span></span>
<span data-ttu-id="01456-138">Указывает идентификатор приложения, разрешения которого нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="01456-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="01456-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01456-139">-DefaultProfile</span></span>
<span data-ttu-id="01456-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="01456-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01456-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="01456-141">-EmailAddress</span></span>
<span data-ttu-id="01456-142">Указывает адрес электронной почты пользователя, доступ к которому вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="01456-142">Specifies the user email address of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="01456-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="01456-143">-EnabledForDeployment</span></span>
<span data-ttu-id="01456-144">Если задано, отключение получения секретных данных от этого ключа в хранилище ключей поставщиком Microsoft. COMPUTE Resource provider при указании ссылки в разделе Создание ресурсов.</span><span class="sxs-lookup"><span data-stu-id="01456-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="01456-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="01456-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="01456-146">Запрещает получение секретных данных в этом хранилище ключей с помощью шифрования диска Azure.</span><span class="sxs-lookup"><span data-stu-id="01456-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="01456-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="01456-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="01456-148">Отключает получение секретных данных в этом хранилище с помощью диспетчера ресурсов Azure при указании ссылок в шаблонах.</span><span class="sxs-lookup"><span data-stu-id="01456-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="01456-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01456-149">-InputObject</span></span>
<span data-ttu-id="01456-150">Объект хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="01456-150">Key Vault object.</span></span>

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

### <span data-ttu-id="01456-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="01456-151">-ObjectId</span></span>
<span data-ttu-id="01456-152">Указывает идентификатор объекта пользователя или участника-службы в Azure Active Directory, для которого нужно удалить разрешения.</span><span class="sxs-lookup"><span data-stu-id="01456-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="01456-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01456-153">-PassThru</span></span>
<span data-ttu-id="01456-154">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="01456-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="01456-155">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="01456-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="01456-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01456-156">-ResourceGroupName</span></span>
<span data-ttu-id="01456-157">Указывает имя группы ресурсов, связанной с хранилищем ключей, для которого изменяется политика доступа.</span><span class="sxs-lookup"><span data-stu-id="01456-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="01456-158">Если он не указан, этот командлет осуществляет поиск в текущем подписке хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="01456-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

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

### <span data-ttu-id="01456-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01456-159">-ResourceId</span></span>
<span data-ttu-id="01456-160">Идентификатор ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="01456-160">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="01456-161">-Намерено</span><span class="sxs-lookup"><span data-stu-id="01456-161">-ServicePrincipalName</span></span>
<span data-ttu-id="01456-162">Указывает имя субъекта-службы для приложения, разрешения которого вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="01456-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="01456-163">Укажите идентификатор приложения, который также называется ИДЕНТИФИКАТОРом клиента, зарегистрированный для приложения в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="01456-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="01456-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="01456-164">-UserPrincipalName</span></span>
<span data-ttu-id="01456-165">Задает имя участника-пользователя, доступ к которому вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="01456-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="01456-166">-VaultName</span><span class="sxs-lookup"><span data-stu-id="01456-166">-VaultName</span></span>
<span data-ttu-id="01456-167">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="01456-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="01456-168">Этот командлет удаляет разрешения для хранилища ключей, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="01456-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="01456-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01456-169">-Confirm</span></span>
<span data-ttu-id="01456-170">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="01456-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01456-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01456-171">-WhatIf</span></span>
<span data-ttu-id="01456-172">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="01456-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01456-173">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="01456-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01456-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01456-174">CommonParameters</span></span>
<span data-ttu-id="01456-175">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01456-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01456-176">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01456-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01456-177">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01456-177">INPUTS</span></span>

### <span data-ttu-id="01456-178">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="01456-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="01456-179">System. String</span><span class="sxs-lookup"><span data-stu-id="01456-179">System.String</span></span>

## <span data-ttu-id="01456-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01456-180">OUTPUTS</span></span>

### <span data-ttu-id="01456-181">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="01456-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="01456-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="01456-182">NOTES</span></span>

## <span data-ttu-id="01456-183">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01456-183">RELATED LINKS</span></span>

[<span data-ttu-id="01456-184">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="01456-184">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

