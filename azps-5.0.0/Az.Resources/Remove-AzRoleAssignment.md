---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
ms.openlocfilehash: fc954dcf2ce3b9a1c066b3986bbc0bbea302ea2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249827"
---
# <span data-ttu-id="d9e5f-101">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d9e5f-101">Remove-AzRoleAssignment</span></span>

## <span data-ttu-id="d9e5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9e5f-102">SYNOPSIS</span></span>
<span data-ttu-id="d9e5f-103">Удаляет назначение роли указанному участнику, которому назначена определенная роль в определенной области.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="d9e5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9e5f-104">SYNTAX</span></span>

### <span data-ttu-id="d9e5f-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d9e5f-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9e5f-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9e5f-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9e5f-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9e5f-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9e5f-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9e5f-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9e5f-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9e5f-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9e5f-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9e5f-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9e5f-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9e5f-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9e5f-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9e5f-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9e5f-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9e5f-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9e5f-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9e5f-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9e5f-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9e5f-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9e5f-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9e5f-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9e5f-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9e5f-117">DESCRIPTION</span></span>
<span data-ttu-id="d9e5f-118">Используйте Remove-AzRoleAssignment unifiedgroup для отзыва доступа к любому участнику в заданной области и данной роли.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-118">Use the Remove-AzRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>
<span data-ttu-id="d9e5f-119">Объект назначения, т. е. участник должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="d9e5f-120">Участник может быть пользователем (используйте параметры SignInName или ObjectId для идентификации пользователя), группу безопасности (с помощью параметра ObjectId для идентификации группы) или участника-службы (используйте параметры программного обеспечения или ObjectId для идентификации ServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>
<span data-ttu-id="d9e5f-121">Роль, которой назначен участник, должна быть указана с помощью параметра RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="d9e5f-122">Область назначения может быть указана, и, если она не задана, по умолчанию используется область подписки, то есть предпринимается попытка удалить назначение для указанного участника и роль в области подписки.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="d9e5f-123">Область назначения может быть указана с помощью одного из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="d9e5f-124">помощью.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-124">a.</span></span>
<span data-ttu-id="d9e5f-125">Scope — это полностью определенная область, начиная с/Subscriptions/ \<subscriptionId\> b.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="d9e5f-126">ResourceGroupName — имя любой группы ресурсов в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="d9e5f-127">c++.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-127">c.</span></span>
<span data-ttu-id="d9e5f-128">ResourceName, ResourceType, ResourceGroupName и (необязательно) ParentResource — определяет конкретный ресурс в подписке.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="d9e5f-129">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9e5f-129">EXAMPLES</span></span>

### <span data-ttu-id="d9e5f-130">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d9e5f-130">Example 1</span></span>
```
PS C:\> Remove-AzRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="d9e5f-131">Удаляет назначение ролей для пользователей, которым john.doe@contoso.com назначена роль средства чтения в области resourcegroup Rg1.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="d9e5f-132">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d9e5f-132">Example 2</span></span>
```
PS C:\> Remove-AzRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="d9e5f-133">Удаляет назначение роли участнику группы, определенному ObjectId и назначаемым роли читателя.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="d9e5f-134">По умолчанию использует текущую подписку в качестве области, чтобы найти назначение для удаления.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="d9e5f-135">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d9e5f-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="d9e5f-136">Удаляет первый объект назначения роли, извлеченный из Get-AzRoleAssignment unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-136">Removes the first role assignment object which is fetched from the Get-AzRoleAssignment commandlet.</span></span>

## <span data-ttu-id="d9e5f-137">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9e5f-137">PARAMETERS</span></span>

### <span data-ttu-id="d9e5f-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9e5f-138">-DefaultProfile</span></span>
<span data-ttu-id="d9e5f-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d9e5f-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9e5f-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9e5f-140">-InputObject</span></span>
<span data-ttu-id="d9e5f-141">Объект назначения роли.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-141">Role Assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e5f-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d9e5f-142">-ObjectId</span></span>
<span data-ttu-id="d9e5f-143">Azure AD ObjectId для пользователя, группы или участника-службы.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-143">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e5f-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="d9e5f-144">-ParentResource</span></span>
<span data-ttu-id="d9e5f-145">Родительский ресурс в иерархии (ресурс, указанный с помощью параметра ResourceName), если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="d9e5f-146">Необходимо использовать совместно с параметрами ResourceGroupName, ResourceType и ResourceName для создания иерархической области в форме относительного URI, определяющего ресурс.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e5f-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9e5f-147">-PassThru</span></span>
<span data-ttu-id="d9e5f-148">При указании показывает удаленное назначение роли</span><span class="sxs-lookup"><span data-stu-id="d9e5f-148">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="d9e5f-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9e5f-149">-ResourceGroupName</span></span>
<span data-ttu-id="d9e5f-150">Имя группы ресурсов, которой назначена роль.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="d9e5f-151">Пытается удалить задание в указанной области группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="d9e5f-152">При использовании в сочетании с ResourceName, ResourceType и (необязательно) параметрами ParentResource команда создает иерархическую область в форме относительного URI, который определяет ресурс.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e5f-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d9e5f-153">-ResourceName</span></span>
<span data-ttu-id="d9e5f-154">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-154">The resource name.</span></span>
<span data-ttu-id="d9e5f-155">Например, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="d9e5f-156">Необходимо использовать в сочетании с ResourceGroupName, ResourceType и (необязательно) параметрами ParentResource для создания иерархической области в форме относительного URI, определяющего ресурс, и удаления задания в этой области.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e5f-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d9e5f-157">-ResourceType</span></span>
<span data-ttu-id="d9e5f-158">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-158">The resource type.</span></span>
<span data-ttu-id="d9e5f-159">Для таких, например, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="d9e5f-160">Необходимо использовать в сочетании с ResourceGroupName, ResourceName и (необязательно) параметрами ParentResource для создания иерархической области в форме относительного URI, определяющего ресурс, и удаления задания в этой области ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e5f-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="d9e5f-161">-RoleDefinitionId</span></span>
<span data-ttu-id="d9e5f-162">Идентификатор роли RBAC, для которой необходимо удалить назначение.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e5f-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d9e5f-163">-RoleDefinitionName</span></span>
<span data-ttu-id="d9e5f-164">Имя роли RBAC, для которой необходимо удалить назначение, например читатель, участник, Администратор виртуальной сети и т. д.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e5f-165">-Scope</span><span class="sxs-lookup"><span data-stu-id="d9e5f-165">-Scope</span></span>
<span data-ttu-id="d9e5f-166">Область назначения роли, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="d9e5f-167">В формате относительных URI.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-167">In the format of relative URI.</span></span>
<span data-ttu-id="d9e5f-168">Например, "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="d9e5f-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="d9e5f-169">Если не указано, будет выполнена попытка удаления роли на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="d9e5f-170">Если указан, она должна начинаться с "/Subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="d9e5f-170">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e5f-171">-Намерено</span><span class="sxs-lookup"><span data-stu-id="d9e5f-171">-ServicePrincipalName</span></span>
<span data-ttu-id="d9e5f-172">Значение программного приложения Azure AD</span><span class="sxs-lookup"><span data-stu-id="d9e5f-172">The ServicePrincipalName of the Azure AD application</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e5f-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="d9e5f-173">-SignInName</span></span>
<span data-ttu-id="d9e5f-174">Адрес электронной почты или имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-174">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e5f-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9e5f-175">-Confirm</span></span>
<span data-ttu-id="d9e5f-176">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9e5f-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9e5f-177">-WhatIf</span></span>
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

### <span data-ttu-id="d9e5f-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9e5f-178">CommonParameters</span></span>
<span data-ttu-id="d9e5f-179">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9e5f-180">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9e5f-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9e5f-181">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9e5f-181">INPUTS</span></span>

### <span data-ttu-id="d9e5f-182">System. String</span><span class="sxs-lookup"><span data-stu-id="d9e5f-182">System.String</span></span>

### <span data-ttu-id="d9e5f-183">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d9e5f-183">System.Guid</span></span>

### <span data-ttu-id="d9e5f-184">Microsoft. Azure. Commands. Resources. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d9e5f-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="d9e5f-185">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9e5f-185">OUTPUTS</span></span>

### <span data-ttu-id="d9e5f-186">Microsoft. Azure. Commands. Resources. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d9e5f-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="d9e5f-187">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9e5f-187">NOTES</span></span>
<span data-ttu-id="d9e5f-188">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="d9e5f-188">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d9e5f-189">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9e5f-189">RELATED LINKS</span></span>

[<span data-ttu-id="d9e5f-190">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d9e5f-190">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="d9e5f-191">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d9e5f-191">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="d9e5f-192">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d9e5f-192">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

