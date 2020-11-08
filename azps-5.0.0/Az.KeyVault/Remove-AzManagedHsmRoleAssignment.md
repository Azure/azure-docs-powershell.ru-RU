---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 038049af40d84b678da12a57918328b3b0725127
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245288"
---
# <span data-ttu-id="32d94-101">Remove-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="32d94-101">Remove-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="32d94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32d94-102">SYNOPSIS</span></span>
<span data-ttu-id="32d94-103">Удаляет назначение роли указанному участнику, которому назначена определенная роль в определенной области.</span><span class="sxs-lookup"><span data-stu-id="32d94-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="32d94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32d94-104">SYNTAX</span></span>

### <span data-ttu-id="32d94-105">DefinitionNameSignInName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32d94-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32d94-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="32d94-106">DefinitionNameApplicationId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32d94-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="32d94-107">DefinitionNameObjectId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32d94-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="32d94-108">DefinitionIdApplicationId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32d94-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="32d94-109">DefinitionIdObjectId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32d94-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="32d94-110">DefinitionIdSignInName</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32d94-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="32d94-111">RemoveByNameParameterSet</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru]
 -RoleAssignmentName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32d94-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="32d94-112">InputObject</span></span>
```
Remove-AzManagedHsmRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32d94-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32d94-113">DESCRIPTION</span></span>
<span data-ttu-id="32d94-114">Используйте `Remove-AzManagedHsmRoleAssignment` командлет для отзыва доступа к любому участнику в заданной области и данной роли.</span><span class="sxs-lookup"><span data-stu-id="32d94-114">Use the `Remove-AzManagedHsmRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="32d94-115">Объект назначения, т. е. участник должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="32d94-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="32d94-116">Участник может быть пользователем (используйте параметры SignInName или ObjectId для идентификации пользователя), группу безопасности (используйте параметр ObjectId для идентификации группы) или участника-службы (используйте параметры ApplicationId или ObjectId для идентификации ServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="32d94-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="32d94-117">Роль, которой назначен участник, должна быть указана с помощью параметра RoleDefinitionName или RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="32d94-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="32d94-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32d94-118">EXAMPLES</span></span>

### <span data-ttu-id="32d94-119">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32d94-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzManagedHsmRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="32d94-120">В этом примере отменяется "роль управляемого" администратора политики HSM "" user1@microsoft.com в области "/Keys".</span><span class="sxs-lookup"><span data-stu-id="32d94-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="32d94-121">Пример 2</span><span class="sxs-lookup"><span data-stu-id="32d94-121">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzManagedHsmRoleAssignment
```

<span data-ttu-id="32d94-122">В этом примере все роли "" для всех областей "отменяются user1@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="32d94-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="32d94-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32d94-123">PARAMETERS</span></span>

### <span data-ttu-id="32d94-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="32d94-124">-ApplicationId</span></span>
<span data-ttu-id="32d94-125">Имя субъекта-службы приложения.</span><span class="sxs-lookup"><span data-stu-id="32d94-125">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameApplicationId, DefinitionIdApplicationId
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d94-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32d94-126">-DefaultProfile</span></span>
<span data-ttu-id="32d94-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32d94-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32d94-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="32d94-128">-HsmName</span></span>
<span data-ttu-id="32d94-129">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="32d94-129">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId, DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName, RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d94-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32d94-130">-InputObject</span></span>
<span data-ttu-id="32d94-131">Объект назначения роли.</span><span class="sxs-lookup"><span data-stu-id="32d94-131">Role assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32d94-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="32d94-132">-ObjectId</span></span>
<span data-ttu-id="32d94-133">Идентификатор объекта пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="32d94-133">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameObjectId, DefinitionIdObjectId
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d94-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32d94-134">-PassThru</span></span>
<span data-ttu-id="32d94-135">Возвращает значение "истина" при восстановлении HSM.</span><span class="sxs-lookup"><span data-stu-id="32d94-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="32d94-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="32d94-136">-RoleAssignmentName</span></span>
<span data-ttu-id="32d94-137">Имя назначения роли.</span><span class="sxs-lookup"><span data-stu-id="32d94-137">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d94-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="32d94-138">-RoleDefinitionId</span></span>
<span data-ttu-id="32d94-139">Идентификатор роли, которой назначен участник.</span><span class="sxs-lookup"><span data-stu-id="32d94-139">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName
Aliases: RoleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d94-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="32d94-140">-RoleDefinitionName</span></span>
<span data-ttu-id="32d94-141">Имя роли RBAC, с которой нужно назначить участника.</span><span class="sxs-lookup"><span data-stu-id="32d94-141">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d94-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="32d94-142">-Scope</span></span>
<span data-ttu-id="32d94-143">Область, к которой относится назначение роли или определение (например, "/" или "/Keys" или "/keys/{keyName}").</span><span class="sxs-lookup"><span data-stu-id="32d94-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="32d94-144">"/" используется, если опущен.</span><span class="sxs-lookup"><span data-stu-id="32d94-144">'/' is used when omitted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d94-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="32d94-145">-SignInName</span></span>
<span data-ttu-id="32d94-146">SignInName пользователя.</span><span class="sxs-lookup"><span data-stu-id="32d94-146">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionIdSignInName
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d94-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32d94-147">-Confirm</span></span>
<span data-ttu-id="32d94-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32d94-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32d94-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32d94-149">-WhatIf</span></span>
<span data-ttu-id="32d94-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="32d94-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32d94-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="32d94-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32d94-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d94-152">CommonParameters</span></span>
<span data-ttu-id="32d94-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32d94-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d94-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32d94-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d94-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32d94-155">INPUTS</span></span>

### <span data-ttu-id="32d94-156">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="32d94-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="32d94-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32d94-157">OUTPUTS</span></span>

### <span data-ttu-id="32d94-158">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="32d94-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="32d94-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="32d94-159">NOTES</span></span>

## <span data-ttu-id="32d94-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32d94-160">RELATED LINKS</span></span>
