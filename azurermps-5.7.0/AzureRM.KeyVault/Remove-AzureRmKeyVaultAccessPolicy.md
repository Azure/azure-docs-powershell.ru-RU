---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: ca175d0873b74d8b13d1755f3d0986580c5853ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566173"
---
# <span data-ttu-id="dcd39-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd39-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="dcd39-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dcd39-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd39-103">Удаляет все разрешения для пользователя или приложения из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="dcd39-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcd39-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dcd39-104">SYNTAX</span></span>

### <span data-ttu-id="dcd39-105">ByUserPrincipalName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dcd39-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dcd39-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="dcd39-106">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dcd39-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="dcd39-107">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dcd39-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="dcd39-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd39-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="dcd39-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd39-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="dcd39-110">InputObjectByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd39-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="dcd39-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd39-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="dcd39-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd39-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="dcd39-113">InputObjectByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd39-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="dcd39-114">InputObjectForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcd39-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcd39-115">DESCRIPTION</span></span>
<span data-ttu-id="dcd39-116">Командлет **Remove-AzureRmKeyVaultAccessPolicy** удаляет все разрешения для пользователя или приложения или для всех пользователей и приложений из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="dcd39-116">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="dcd39-117">Даже если вы удалите все разрешения, владелец подписки Azure, которая имеет хранилище ключей, может добавить разрешения в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="dcd39-117">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="dcd39-118">Обратите внимание, что хотя указывать группу ресурсов необязательно для этого командлета, вы должны сделать это для лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="dcd39-118">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="dcd39-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dcd39-119">EXAMPLES</span></span>

### <span data-ttu-id="dcd39-120">Пример 1: удаление разрешений для пользователя</span><span class="sxs-lookup"><span data-stu-id="dcd39-120">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="dcd39-121">Эта команда удаляет все разрешения, которые пользователь PattiFuller@contoso.com имеет в хранилище ключей с именем Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="dcd39-121">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="dcd39-122">Пример 2: удаление разрешений для приложения</span><span class="sxs-lookup"><span data-stu-id="dcd39-122">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="dcd39-123">Эта команда удаляет все разрешения, которые приложение имеет в хранилище ключей с именем Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="dcd39-123">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="dcd39-124">В этом примере приложение идентифицируется с использованием имени субъекта-службы, зарегистрированного в Azure Active Directory http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="dcd39-124">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="dcd39-125">Пример 3: удаление разрешений для приложения с помощью идентификатора объекта</span><span class="sxs-lookup"><span data-stu-id="dcd39-125">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="dcd39-126">Эта команда удаляет все разрешения, которые приложение имеет в хранилище ключей с именем Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="dcd39-126">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="dcd39-127">В этом примере приложение идентифицируется по ИДЕНТИФИКАТОРу объекта участника-службы.</span><span class="sxs-lookup"><span data-stu-id="dcd39-127">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="dcd39-128">Пример 4: удаление разрешений для поставщика ресурсов Microsoft. COMPUTE</span><span class="sxs-lookup"><span data-stu-id="dcd39-128">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="dcd39-129">Эта команда удаляет разрешения для поставщика ресурсов Microsoft. COMPUTE, чтобы получать секреты из Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="dcd39-129">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="dcd39-130">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dcd39-130">PARAMETERS</span></span>

### <span data-ttu-id="dcd39-131">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="dcd39-131">-ApplicationId</span></span>
<span data-ttu-id="dcd39-132">Указывает идентификатор приложения, разрешения которого нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="dcd39-132">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="dcd39-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcd39-133">-DefaultProfile</span></span>
<span data-ttu-id="dcd39-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dcd39-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcd39-135">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="dcd39-135">-EmailAddress</span></span>
<span data-ttu-id="dcd39-136">Указывает адрес электронной почты пользователя, доступ к которому вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="dcd39-136">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByEmail, InputObjectByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd39-137">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="dcd39-137">-EnabledForDeployment</span></span>
<span data-ttu-id="dcd39-138">Если задано, отключение получения секретных данных от этого ключа в хранилище ключей поставщиком Microsoft. COMPUTE Resource provider при указании ссылки в разделе Создание ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dcd39-138">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="dcd39-139">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="dcd39-139">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="dcd39-140">Запрещает получение секретных данных в этом хранилище ключей с помощью шифрования диска Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd39-140">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="dcd39-141">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="dcd39-141">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="dcd39-142">Отключает получение секретных данных в этом хранилище с помощью диспетчера ресурсов Azure при указании ссылок в шаблонах.</span><span class="sxs-lookup"><span data-stu-id="dcd39-142">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="dcd39-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcd39-143">-InputObject</span></span>
<span data-ttu-id="dcd39-144">Объект хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="dcd39-144">Key Vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd39-145">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dcd39-145">-ObjectId</span></span>
<span data-ttu-id="dcd39-146">Указывает идентификатор объекта пользователя или участника-службы в Azure Active Directory, для которого нужно удалить разрешения.</span><span class="sxs-lookup"><span data-stu-id="dcd39-146">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="dcd39-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcd39-147">-PassThru</span></span>
<span data-ttu-id="dcd39-148">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="dcd39-148">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dcd39-149">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="dcd39-149">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dcd39-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcd39-150">-ResourceGroupName</span></span>
<span data-ttu-id="dcd39-151">Указывает имя группы ресурсов, связанной с хранилищем ключей, для которого изменяется политика доступа.</span><span class="sxs-lookup"><span data-stu-id="dcd39-151">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="dcd39-152">Если он не указан, этот командлет осуществляет поиск в текущем подписке хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="dcd39-152">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd39-153">-Намерено</span><span class="sxs-lookup"><span data-stu-id="dcd39-153">-ServicePrincipalName</span></span>
<span data-ttu-id="dcd39-154">Указывает имя субъекта-службы для приложения, разрешения которого вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="dcd39-154">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="dcd39-155">Укажите идентификатор приложения, который также называется ИДЕНТИФИКАТОРом клиента, зарегистрированный для приложения в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dcd39-155">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="dcd39-156">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="dcd39-156">-UserPrincipalName</span></span>
<span data-ttu-id="dcd39-157">Задает имя участника-пользователя, доступ к которому вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="dcd39-157">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="dcd39-158">-VaultName</span><span class="sxs-lookup"><span data-stu-id="dcd39-158">-VaultName</span></span>
<span data-ttu-id="dcd39-159">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="dcd39-159">Specifies the name of the key vault.</span></span>
<span data-ttu-id="dcd39-160">Этот командлет удаляет разрешения для хранилища ключей, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="dcd39-160">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd39-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcd39-161">-Confirm</span></span>
<span data-ttu-id="dcd39-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dcd39-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcd39-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcd39-163">-WhatIf</span></span>
<span data-ttu-id="dcd39-164">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dcd39-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcd39-165">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dcd39-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcd39-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd39-166">CommonParameters</span></span>
<span data-ttu-id="dcd39-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dcd39-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd39-168">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcd39-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd39-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dcd39-169">INPUTS</span></span>

### <span data-ttu-id="dcd39-170">Ничего</span><span class="sxs-lookup"><span data-stu-id="dcd39-170">None</span></span>
<span data-ttu-id="dcd39-171">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="dcd39-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dcd39-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcd39-172">OUTPUTS</span></span>

### <span data-ttu-id="dcd39-173">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd39-173">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="dcd39-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="dcd39-174">NOTES</span></span>

## <span data-ttu-id="dcd39-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcd39-175">RELATED LINKS</span></span>

[<span data-ttu-id="dcd39-176">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd39-176">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

