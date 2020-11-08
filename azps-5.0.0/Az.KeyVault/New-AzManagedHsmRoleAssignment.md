---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 3b02bf3471546c9b6bc68d0ded109133341d20bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245303"
---
# <span data-ttu-id="e3deb-101">New-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e3deb-101">New-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="e3deb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3deb-102">SYNOPSIS</span></span>
<span data-ttu-id="e3deb-103">Назначает указанную роль RBAC указанному участнику в заданной области.</span><span class="sxs-lookup"><span data-stu-id="e3deb-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="e3deb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3deb-104">SYNTAX</span></span>

### <span data-ttu-id="e3deb-105">DefinitionNameSignInName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3deb-105">DefinitionNameSignInName (Default)</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3deb-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="e3deb-106">DefinitionNameApplicationId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3deb-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="e3deb-107">DefinitionNameObjectId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3deb-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="e3deb-108">DefinitionIdApplicationId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3deb-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="e3deb-109">DefinitionIdObjectId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3deb-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="e3deb-110">DefinitionIdSignInName</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3deb-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3deb-111">DESCRIPTION</span></span>
<span data-ttu-id="e3deb-112">Используйте `New-AzManagedHsmRoleAssignment` команду для предоставления доступа.</span><span class="sxs-lookup"><span data-stu-id="e3deb-112">Use the `New-AzManagedHsmRoleAssignment` command to grant access.</span></span>
<span data-ttu-id="e3deb-113">Доступ предоставляется путем назначения им соответствующей роли RBAC в области справа.</span><span class="sxs-lookup"><span data-stu-id="e3deb-113">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="e3deb-114">Необходимо указать тему назначения.</span><span class="sxs-lookup"><span data-stu-id="e3deb-114">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="e3deb-115">Чтобы указать пользователя, используйте параметры SignInName или Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="e3deb-115">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="e3deb-116">Чтобы указать группу безопасности, используйте параметр Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="e3deb-116">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="e3deb-117">Чтобы указать приложение Azure AD, используйте параметры ApplicationId или ObjectId.</span><span class="sxs-lookup"><span data-stu-id="e3deb-117">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="e3deb-118">Назначаемая роль должна быть указана с помощью параметра RoleDefinitionName PR RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="e3deb-118">The role that is being assigned must be specified using the RoleDefinitionName pr RoleDefinitionId parameter.</span></span> <span data-ttu-id="e3deb-119">Может быть указана область, для которой предоставляется доступ.</span><span class="sxs-lookup"><span data-stu-id="e3deb-119">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="e3deb-120">По умолчанию используется выбранная подписка.</span><span class="sxs-lookup"><span data-stu-id="e3deb-120">It defaults to the selected subscription.</span></span>

## <span data-ttu-id="e3deb-121">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3deb-121">EXAMPLES</span></span>

### <span data-ttu-id="e3deb-122">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e3deb-122">Example 1</span></span>
```powershell
PS C:\> New-AzManagedHsmRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com

RoleDefinitionName               DisplayName                    ObjectType Scope
------------------               -----------                    ---------- -----
Managed HSM Policy Administrator User 1 (user1@microsoft.com)   User       /
```

<span data-ttu-id="e3deb-123">В этом примере роли "управляемый Администратор политики HSM" назначаются пользователю " user1@microsoft.com " в верхней области.</span><span class="sxs-lookup"><span data-stu-id="e3deb-123">This example assigns role "Managed HSM Policy Administrator" to user "user1@microsoft.com" at top scope.</span></span>

## <span data-ttu-id="e3deb-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3deb-124">PARAMETERS</span></span>

### <span data-ttu-id="e3deb-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e3deb-125">-ApplicationId</span></span>
<span data-ttu-id="e3deb-126">Имя субъекта-службы приложения.</span><span class="sxs-lookup"><span data-stu-id="e3deb-126">The app SPN.</span></span>

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

### <span data-ttu-id="e3deb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3deb-127">-DefaultProfile</span></span>
<span data-ttu-id="e3deb-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3deb-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3deb-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="e3deb-129">-HsmName</span></span>
<span data-ttu-id="e3deb-130">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="e3deb-130">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3deb-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e3deb-131">-ObjectId</span></span>
<span data-ttu-id="e3deb-132">Идентификатор объекта пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="e3deb-132">The user or group object id.</span></span>

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

### <span data-ttu-id="e3deb-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e3deb-133">-RoleDefinitionId</span></span>
<span data-ttu-id="e3deb-134">Идентификатор роли, которой назначен участник.</span><span class="sxs-lookup"><span data-stu-id="e3deb-134">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="e3deb-135">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e3deb-135">-RoleDefinitionName</span></span>
<span data-ttu-id="e3deb-136">Имя роли RBAC, с которой нужно назначить участника.</span><span class="sxs-lookup"><span data-stu-id="e3deb-136">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="e3deb-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="e3deb-137">-Scope</span></span>
<span data-ttu-id="e3deb-138">Область, к которой относится назначение роли или определение (например, "/" или "/Keys" или "/keys/{keyName}").</span><span class="sxs-lookup"><span data-stu-id="e3deb-138">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="e3deb-139">"/" используется, если опущен.</span><span class="sxs-lookup"><span data-stu-id="e3deb-139">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="e3deb-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="e3deb-140">-SignInName</span></span>
<span data-ttu-id="e3deb-141">SignInName пользователя.</span><span class="sxs-lookup"><span data-stu-id="e3deb-141">The user SignInName.</span></span>

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

### <span data-ttu-id="e3deb-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3deb-142">-Confirm</span></span>
<span data-ttu-id="e3deb-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e3deb-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3deb-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3deb-144">-WhatIf</span></span>
<span data-ttu-id="e3deb-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e3deb-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3deb-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e3deb-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3deb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3deb-147">CommonParameters</span></span>
<span data-ttu-id="e3deb-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3deb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3deb-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3deb-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3deb-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3deb-150">INPUTS</span></span>

### <span data-ttu-id="e3deb-151">Ничего</span><span class="sxs-lookup"><span data-stu-id="e3deb-151">None</span></span>

## <span data-ttu-id="e3deb-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3deb-152">OUTPUTS</span></span>

### <span data-ttu-id="e3deb-153">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e3deb-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="e3deb-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3deb-154">NOTES</span></span>

## <span data-ttu-id="e3deb-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3deb-155">RELATED LINKS</span></span>
