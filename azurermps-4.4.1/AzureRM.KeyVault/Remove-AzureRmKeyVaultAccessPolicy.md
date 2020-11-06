---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://go.microsoft.com/fwlink/?LinkId=690164
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 4e46c100984a9e50794130b3de6e30ce5f664ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568053"
---
# <span data-ttu-id="8623c-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8623c-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="8623c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8623c-102">SYNOPSIS</span></span>
<span data-ttu-id="8623c-103">Удаляет все разрешения для пользователя или приложения из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8623c-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8623c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8623c-104">SYNTAX</span></span>

### <span data-ttu-id="8623c-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8623c-105">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8623c-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8623c-106">ByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8623c-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="8623c-107">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8623c-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="8623c-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8623c-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="8623c-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8623c-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8623c-110">DESCRIPTION</span></span>
<span data-ttu-id="8623c-111">Командлет **Remove-AzureRmKeyVaultAccessPolicy** удаляет все разрешения для пользователя или приложения или для всех пользователей и приложений из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8623c-111">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="8623c-112">Даже если вы удалите все разрешения, владелец подписки Azure, которая имеет хранилище ключей, может добавить разрешения в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="8623c-112">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="8623c-113">Обратите внимание, что хотя указывать группу ресурсов необязательно для этого командлета, вы должны сделать это для лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="8623c-113">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="8623c-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8623c-114">EXAMPLES</span></span>

### <span data-ttu-id="8623c-115">Пример 1: удаление разрешений для пользователя</span><span class="sxs-lookup"><span data-stu-id="8623c-115">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="8623c-116">Эта команда удаляет все разрешения, которые пользователь PattiFuller@contoso.com имеет в хранилище ключей с именем Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8623c-116">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="8623c-117">Пример 2: удаление разрешений для приложения</span><span class="sxs-lookup"><span data-stu-id="8623c-117">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="8623c-118">Эта команда удаляет все разрешения, которые приложение имеет в хранилище ключей с именем Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8623c-118">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="8623c-119">В этом примере приложение идентифицируется с использованием имени субъекта-службы, зарегистрированного в Azure Active Directory http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="8623c-119">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="8623c-120">Пример 3: удаление разрешений для приложения с помощью идентификатора объекта</span><span class="sxs-lookup"><span data-stu-id="8623c-120">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="8623c-121">Эта команда удаляет все разрешения, которые приложение имеет в хранилище ключей с именем Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8623c-121">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="8623c-122">В этом примере приложение идентифицируется по ИДЕНТИФИКАТОРу объекта участника-службы.</span><span class="sxs-lookup"><span data-stu-id="8623c-122">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="8623c-123">Пример 4: удаление разрешений для поставщика ресурсов Microsoft. COMPUTE</span><span class="sxs-lookup"><span data-stu-id="8623c-123">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="8623c-124">Эта команда удаляет разрешения для поставщика ресурсов Microsoft. COMPUTE, чтобы получать секреты из Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8623c-124">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="8623c-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8623c-125">PARAMETERS</span></span>

### <span data-ttu-id="8623c-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8623c-126">-ApplicationId</span></span>
<span data-ttu-id="8623c-127">Для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="8623c-127">For future use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8623c-128">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="8623c-128">-EmailAddress</span></span>
<span data-ttu-id="8623c-129">Указывает адрес электронной почты пользователя, доступ к которому вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="8623c-129">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8623c-130">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="8623c-130">-EnabledForDeployment</span></span>
<span data-ttu-id="8623c-131">Включает поставщик ресурсов Microsoft. COMPUTE для извлечения секретов из этого ключа, если это временное хранилище ссылается на создание ресурсов (например, при создании виртуальной машины).</span><span class="sxs-lookup"><span data-stu-id="8623c-131">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8623c-132">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="8623c-132">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="8623c-133">Позволяет службе шифрования дисков Azure получить секретные ключи и их перетекание из этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8623c-133">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8623c-134">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="8623c-134">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="8623c-135">Позволяет диспетчеру ресурсов Azure получать секреты из этого хранилища ключей при ссылке на это хранилище ключей в развертывании шаблона.</span><span class="sxs-lookup"><span data-stu-id="8623c-135">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8623c-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8623c-136">-ObjectId</span></span>
<span data-ttu-id="8623c-137">Указывает идентификатор объекта пользователя или участника-службы в Azure Active Directory, для которого нужно удалить разрешения.</span><span class="sxs-lookup"><span data-stu-id="8623c-137">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8623c-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8623c-138">-PassThru</span></span>
<span data-ttu-id="8623c-139">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="8623c-139">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8623c-140">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8623c-140">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8623c-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8623c-141">-ResourceGroupName</span></span>
<span data-ttu-id="8623c-142">Указывает имя группы ресурсов, связанной с хранилищем ключей, для которого изменяется политика доступа.</span><span class="sxs-lookup"><span data-stu-id="8623c-142">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="8623c-143">Если он не указан, этот командлет осуществляет поиск в текущем подписке хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8623c-143">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8623c-144">-Намерено</span><span class="sxs-lookup"><span data-stu-id="8623c-144">-ServicePrincipalName</span></span>
<span data-ttu-id="8623c-145">Указывает имя субъекта-службы для приложения, разрешения которого вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="8623c-145">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="8623c-146">Укажите идентификатор приложения, который также называется ИДЕНТИФИКАТОРом клиента, зарегистрированный для приложения в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8623c-146">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8623c-147">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8623c-147">-UserPrincipalName</span></span>
<span data-ttu-id="8623c-148">Задает имя участника-пользователя, доступ к которому вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="8623c-148">Specifies the user principal name of the user whose access you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8623c-149">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8623c-149">-VaultName</span></span>
<span data-ttu-id="8623c-150">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8623c-150">Specifies the name of the key vault.</span></span>
<span data-ttu-id="8623c-151">Этот командлет удаляет разрешения для хранилища ключей, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="8623c-151">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8623c-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8623c-152">-Confirm</span></span>
<span data-ttu-id="8623c-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8623c-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8623c-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8623c-154">-WhatIf</span></span>
<span data-ttu-id="8623c-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8623c-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8623c-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8623c-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8623c-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8623c-157">-DefaultProfile</span></span>
<span data-ttu-id="8623c-158">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8623c-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8623c-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8623c-159">CommonParameters</span></span>
<span data-ttu-id="8623c-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8623c-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8623c-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8623c-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8623c-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8623c-162">INPUTS</span></span>

## <span data-ttu-id="8623c-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8623c-163">OUTPUTS</span></span>

### <span data-ttu-id="8623c-164">Microsoft. Azure. Commands. KeyVault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="8623c-164">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="8623c-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="8623c-165">NOTES</span></span>

## <span data-ttu-id="8623c-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8623c-166">RELATED LINKS</span></span>

[<span data-ttu-id="8623c-167">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8623c-167">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

