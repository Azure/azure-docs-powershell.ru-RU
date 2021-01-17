---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: ee90ab1b4ba22f1a5c40427f7fc435c75cef992d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395772"
---
# <span data-ttu-id="4f16f-101">New-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4f16f-101">New-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="4f16f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f16f-102">SYNOPSIS</span></span>
<span data-ttu-id="4f16f-103">Назначает указанную роль СРБ указанной основной в указанной области.</span><span class="sxs-lookup"><span data-stu-id="4f16f-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="4f16f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4f16f-104">SYNTAX</span></span>

### <span data-ttu-id="4f16f-105">DefinitionNameSignInName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4f16f-105">DefinitionNameSignInName (Default)</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f16f-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="4f16f-106">DefinitionNameApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f16f-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="4f16f-107">DefinitionNameObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f16f-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="4f16f-108">DefinitionIdApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f16f-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="4f16f-109">DefinitionIdObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f16f-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="4f16f-110">DefinitionIdSignInName</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f16f-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f16f-111">DESCRIPTION</span></span>
<span data-ttu-id="4f16f-112">Чтобы предоставить `New-AzKeyVaultRoleAssignment` доступ, используйте команду.</span><span class="sxs-lookup"><span data-stu-id="4f16f-112">Use the `New-AzKeyVaultRoleAssignment` command to grant access.</span></span>
<span data-ttu-id="4f16f-113">Access предоставляется путем назначения им соответствующей роли RBAC в нужной области.</span><span class="sxs-lookup"><span data-stu-id="4f16f-113">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="4f16f-114">Необходимо у указывается тема задания.</span><span class="sxs-lookup"><span data-stu-id="4f16f-114">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="4f16f-115">Чтобы указать пользователя, используйте параметры SignInName или Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="4f16f-115">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="4f16f-116">Чтобы указать группу безопасности, используйте параметр Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="4f16f-116">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="4f16f-117">Чтобы указать приложение Azure AD, используйте параметры ApplicationId или ObjectId.</span><span class="sxs-lookup"><span data-stu-id="4f16f-117">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="4f16f-118">Роль, которая должна быть назначена, должна быть указана с помощью параметра RoleDefinitionName pr RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="4f16f-118">The role that is being assigned must be specified using the RoleDefinitionName pr RoleDefinitionId parameter.</span></span> <span data-ttu-id="4f16f-119">Может быть указана область, для которой предоставляется доступ.</span><span class="sxs-lookup"><span data-stu-id="4f16f-119">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="4f16f-120">По умолчанию выбранная подписка.</span><span class="sxs-lookup"><span data-stu-id="4f16f-120">It defaults to the selected subscription.</span></span>

## <span data-ttu-id="4f16f-121">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4f16f-121">EXAMPLES</span></span>

### <span data-ttu-id="4f16f-122">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4f16f-122">Example 1</span></span>
```powershell
PS C:\> New-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com

RoleDefinitionName               DisplayName                    ObjectType Scope
------------------               -----------                    ---------- -----
Managed HSM Policy Administrator User 1 (user1@microsoft.com)   User       /
```

<span data-ttu-id="4f16f-123">В этом примере роль "Администратор управляемой политики HSM" назначается пользователю " user1@microsoft.com в верхней области действия.</span><span class="sxs-lookup"><span data-stu-id="4f16f-123">This example assigns role "Managed HSM Policy Administrator" to user "user1@microsoft.com" at top scope.</span></span>

## <span data-ttu-id="4f16f-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f16f-124">PARAMETERS</span></span>

### <span data-ttu-id="4f16f-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4f16f-125">-ApplicationId</span></span>
<span data-ttu-id="4f16f-126">SpN приложения.</span><span class="sxs-lookup"><span data-stu-id="4f16f-126">The app SPN.</span></span>

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

### <span data-ttu-id="4f16f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f16f-127">-DefaultProfile</span></span>
<span data-ttu-id="4f16f-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4f16f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f16f-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="4f16f-129">-HsmName</span></span>
<span data-ttu-id="4f16f-130">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="4f16f-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="4f16f-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4f16f-131">-ObjectId</span></span>
<span data-ttu-id="4f16f-132">ИД объекта пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="4f16f-132">The user or group object id.</span></span>

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

### <span data-ttu-id="4f16f-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="4f16f-133">-RoleDefinitionId</span></span>
<span data-ttu-id="4f16f-134">ИД роли, назначенной основной роли.</span><span class="sxs-lookup"><span data-stu-id="4f16f-134">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="4f16f-135">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="4f16f-135">-RoleDefinitionName</span></span>
<span data-ttu-id="4f16f-136">Имя роли, с помощью которого можно назначить главную функцию.</span><span class="sxs-lookup"><span data-stu-id="4f16f-136">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="4f16f-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="4f16f-137">-Scope</span></span>
<span data-ttu-id="4f16f-138">Область применения назначения роли или определения, например "/", "/" или "/keys" или "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="4f16f-138">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="4f16f-139">"/" используется в опущении.</span><span class="sxs-lookup"><span data-stu-id="4f16f-139">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="4f16f-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="4f16f-140">-SignInName</span></span>
<span data-ttu-id="4f16f-141">Пользователь SignInName.</span><span class="sxs-lookup"><span data-stu-id="4f16f-141">The user SignInName.</span></span>

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

### <span data-ttu-id="4f16f-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f16f-142">-Confirm</span></span>
<span data-ttu-id="4f16f-143">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4f16f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f16f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f16f-144">-WhatIf</span></span>
<span data-ttu-id="4f16f-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f16f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f16f-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4f16f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f16f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f16f-147">CommonParameters</span></span>
<span data-ttu-id="4f16f-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f16f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f16f-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f16f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f16f-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f16f-150">INPUTS</span></span>

### <span data-ttu-id="4f16f-151">Нет</span><span class="sxs-lookup"><span data-stu-id="4f16f-151">None</span></span>

## <span data-ttu-id="4f16f-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4f16f-152">OUTPUTS</span></span>

### <span data-ttu-id="4f16f-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4f16f-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="4f16f-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4f16f-154">NOTES</span></span>

## <span data-ttu-id="4f16f-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f16f-155">RELATED LINKS</span></span>
