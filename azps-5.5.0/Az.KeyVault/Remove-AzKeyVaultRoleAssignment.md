---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: 9e2dd07ac0346cacb99bbcc2e05d47b57ac8ccd6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214508"
---
# <span data-ttu-id="b02f6-101">Remove-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b02f6-101">Remove-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="b02f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b02f6-102">SYNOPSIS</span></span>
<span data-ttu-id="b02f6-103">Удаляет назначение роли для указанного директора, которому назначена определенная роль в определенной области.</span><span class="sxs-lookup"><span data-stu-id="b02f6-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="b02f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b02f6-104">SYNTAX</span></span>

### <span data-ttu-id="b02f6-105">DefinitionNameSignInName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b02f6-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b02f6-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="b02f6-106">DefinitionNameApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b02f6-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="b02f6-107">DefinitionNameObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b02f6-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="b02f6-108">DefinitionIdApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b02f6-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="b02f6-109">DefinitionIdObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b02f6-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="b02f6-110">DefinitionIdSignInName</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b02f6-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b02f6-111">RemoveByNameParameterSet</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02f6-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="b02f6-112">InputObject</span></span>
```
Remove-AzKeyVaultRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b02f6-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b02f6-113">DESCRIPTION</span></span>
<span data-ttu-id="b02f6-114">Используйте этот cmdlet, чтобы отоблескить доступ к любой основной деятельности на заданной области и `Remove-AzKeyVaultRoleAssignment` в заданной роли.</span><span class="sxs-lookup"><span data-stu-id="b02f6-114">Use the `Remove-AzKeyVaultRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="b02f6-115">Объект назначения, то есть основной должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="b02f6-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="b02f6-116">Основным может быть пользователь (с помощью параметров SignInName или ObjectId для идентификации пользователя), группа безопасности (с помощью параметра ObjectId для идентификации группы) или principal-служба (используйте параметры ApplicationId или ObjectId для определения параметра ServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="b02f6-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="b02f6-117">Роль, которая назначена основной, должна быть указана с помощью параметра RoleDefinitionName или RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="b02f6-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="b02f6-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b02f6-118">EXAMPLES</span></span>

### <span data-ttu-id="b02f6-119">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b02f6-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="b02f6-120">В этом примере отменяется роль "Администратор управляемой политики HSM" для области user1@microsoft.com "/keys".</span><span class="sxs-lookup"><span data-stu-id="b02f6-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="b02f6-121">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b02f6-121">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzKeyVaultRoleAssignment
```

<span data-ttu-id="b02f6-122">В этом примере отменяется отзыв всех ролей user1@microsoft.com "" для всех областей.</span><span class="sxs-lookup"><span data-stu-id="b02f6-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="b02f6-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b02f6-123">PARAMETERS</span></span>

### <span data-ttu-id="b02f6-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b02f6-124">-ApplicationId</span></span>
<span data-ttu-id="b02f6-125">SpN приложения.</span><span class="sxs-lookup"><span data-stu-id="b02f6-125">The app SPN.</span></span>

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

### <span data-ttu-id="b02f6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b02f6-126">-DefaultProfile</span></span>
<span data-ttu-id="b02f6-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b02f6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b02f6-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="b02f6-128">-HsmName</span></span>
<span data-ttu-id="b02f6-129">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="b02f6-129">Name of the HSM.</span></span>

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

### <span data-ttu-id="b02f6-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b02f6-130">-InputObject</span></span>
<span data-ttu-id="b02f6-131">Объект назначения роли.</span><span class="sxs-lookup"><span data-stu-id="b02f6-131">Role assignment object.</span></span>

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

### <span data-ttu-id="b02f6-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b02f6-132">-ObjectId</span></span>
<span data-ttu-id="b02f6-133">ИД объекта пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="b02f6-133">The user or group object id.</span></span>

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

### <span data-ttu-id="b02f6-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b02f6-134">-PassThru</span></span>
<span data-ttu-id="b02f6-135">Возвращается истина при восстановлении HSM.</span><span class="sxs-lookup"><span data-stu-id="b02f6-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="b02f6-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="b02f6-136">-RoleAssignmentName</span></span>
<span data-ttu-id="b02f6-137">Имя назначения роли.</span><span class="sxs-lookup"><span data-stu-id="b02f6-137">Name of the role assignment.</span></span>

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

### <span data-ttu-id="b02f6-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b02f6-138">-RoleDefinitionId</span></span>
<span data-ttu-id="b02f6-139">ИД роли, назначенной основной роли.</span><span class="sxs-lookup"><span data-stu-id="b02f6-139">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="b02f6-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b02f6-140">-RoleDefinitionName</span></span>
<span data-ttu-id="b02f6-141">Имя роли, с помощью которого можно назначить главную функцию.</span><span class="sxs-lookup"><span data-stu-id="b02f6-141">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="b02f6-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="b02f6-142">-Scope</span></span>
<span data-ttu-id="b02f6-143">Область применения назначения роли или определения, например "/", "/" или "/keys" или '/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="b02f6-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="b02f6-144">"/" используется в опущении.</span><span class="sxs-lookup"><span data-stu-id="b02f6-144">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="b02f6-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="b02f6-145">-SignInName</span></span>
<span data-ttu-id="b02f6-146">Пользователь SignInName.</span><span class="sxs-lookup"><span data-stu-id="b02f6-146">The user SignInName.</span></span>

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

### <span data-ttu-id="b02f6-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b02f6-147">-Confirm</span></span>
<span data-ttu-id="b02f6-148">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b02f6-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b02f6-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b02f6-149">-WhatIf</span></span>
<span data-ttu-id="b02f6-150">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b02f6-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b02f6-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b02f6-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b02f6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b02f6-152">CommonParameters</span></span>
<span data-ttu-id="b02f6-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b02f6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b02f6-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b02f6-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b02f6-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b02f6-155">INPUTS</span></span>

### <span data-ttu-id="b02f6-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b02f6-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="b02f6-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b02f6-157">OUTPUTS</span></span>

### <span data-ttu-id="b02f6-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b02f6-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="b02f6-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b02f6-159">NOTES</span></span>

## <span data-ttu-id="b02f6-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b02f6-160">RELATED LINKS</span></span>
