---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleAssignment.md
ms.openlocfilehash: 4ca9b3d731c4b4c0029dafa68a1f7e747c62dedb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567942"
---
# <span data-ttu-id="b5c20-101">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b5c20-101">Remove-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="b5c20-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5c20-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c20-103">Удаляет назначение роли указанному участнику, которому назначена определенная роль в определенной области.</span><span class="sxs-lookup"><span data-stu-id="b5c20-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5c20-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5c20-104">SYNTAX</span></span>

### <span data-ttu-id="b5c20-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b5c20-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c20-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5c20-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c20-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5c20-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c20-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5c20-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c20-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5c20-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c20-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5c20-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c20-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5c20-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c20-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5c20-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c20-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5c20-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c20-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5c20-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 -RoleDefinitionName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5c20-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5c20-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c20-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5c20-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzureRmRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5c20-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5c20-117">DESCRIPTION</span></span>
<span data-ttu-id="b5c20-118">Используйте Remove-AzureRmRoleAssignment unifiedgroup для отзыва доступа к любому участнику в заданной области и данной роли.</span><span class="sxs-lookup"><span data-stu-id="b5c20-118">Use the Remove-AzureRmRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>

<span data-ttu-id="b5c20-119">Объект назначения, т. е. участник должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="b5c20-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="b5c20-120">Участник может быть пользователем (используйте параметры SignInName или ObjectId для идентификации пользователя), группу безопасности (с помощью параметра ObjectId для идентификации группы) или участника-службы (используйте параметры программного обеспечения или ObjectId для идентификации ServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="b5c20-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>

<span data-ttu-id="b5c20-121">Роль, которой назначен участник, должна быть указана с помощью параметра RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="b5c20-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>

<span data-ttu-id="b5c20-122">Область назначения может быть указана, и, если она не задана, по умолчанию используется область подписки, то есть предпринимается попытка удалить назначение для указанного участника и роль в области подписки.</span><span class="sxs-lookup"><span data-stu-id="b5c20-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="b5c20-123">Область назначения может быть указана с помощью одного из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="b5c20-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="b5c20-124">помощью.</span><span class="sxs-lookup"><span data-stu-id="b5c20-124">a.</span></span>
<span data-ttu-id="b5c20-125">Scope — это полностью определенная область, начиная с/Subscriptions/ \<subscriptionId\> b.</span><span class="sxs-lookup"><span data-stu-id="b5c20-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="b5c20-126">ResourceGroupName — имя любой группы ресурсов в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="b5c20-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="b5c20-127">c++.</span><span class="sxs-lookup"><span data-stu-id="b5c20-127">c.</span></span>
<span data-ttu-id="b5c20-128">ResourceName, ResourceType, ResourceGroupName и (необязательно) ParentResource — определяет конкретный ресурс в подписке.</span><span class="sxs-lookup"><span data-stu-id="b5c20-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="b5c20-129">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5c20-129">EXAMPLES</span></span>

### <span data-ttu-id="b5c20-130">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b5c20-130">Example 1</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="b5c20-131">Удаляет назначение ролей для пользователей, которым john.doe@contoso.com назначена роль средства чтения в области resourcegroup Rg1.</span><span class="sxs-lookup"><span data-stu-id="b5c20-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="b5c20-132">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b5c20-132">Example 2</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="b5c20-133">Удаляет назначение роли участнику группы, определенному ObjectId и назначаемым роли читателя.</span><span class="sxs-lookup"><span data-stu-id="b5c20-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="b5c20-134">По умолчанию использует текущую подписку в качестве области, чтобы найти назначение для удаления.</span><span class="sxs-lookup"><span data-stu-id="b5c20-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="b5c20-135">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b5c20-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzureRmRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzureRmRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="b5c20-136">Удаляет первый объект назначения роли, извлеченный из Get-AzureRmRoleAssignment unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="b5c20-136">Removes the first role assignment object which is fetched from the Get-AzureRmRoleAssignment commandlet.</span></span>

## <span data-ttu-id="b5c20-137">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5c20-137">PARAMETERS</span></span>

### <span data-ttu-id="b5c20-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c20-138">-DefaultProfile</span></span>
<span data-ttu-id="b5c20-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b5c20-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5c20-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5c20-140">-InputObject</span></span>
<span data-ttu-id="b5c20-141">Объект назначения роли.</span><span class="sxs-lookup"><span data-stu-id="b5c20-141">Role Assignment object.</span></span>

```yaml
Type: PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b5c20-142">-ObjectId</span></span>
<span data-ttu-id="b5c20-143">Azure AD ObjectId для пользователя, группы или участника-службы.</span><span class="sxs-lookup"><span data-stu-id="b5c20-143">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: Guid
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="b5c20-144">-ParentResource</span></span>
<span data-ttu-id="b5c20-145">Родительский ресурс в иерархии (ресурс, указанный с помощью параметра ResourceName), если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="b5c20-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="b5c20-146">Необходимо использовать совместно с параметрами ResourceGroupName, ResourceType и ResourceName для создания иерархической области в форме относительного URI, определяющего ресурс.</span><span class="sxs-lookup"><span data-stu-id="b5c20-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5c20-147">-PassThru</span></span>
<span data-ttu-id="b5c20-148">При указании показывает удаленное назначение роли</span><span class="sxs-lookup"><span data-stu-id="b5c20-148">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="b5c20-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5c20-149">-ResourceGroupName</span></span>
<span data-ttu-id="b5c20-150">Имя группы ресурсов, которой назначена роль.</span><span class="sxs-lookup"><span data-stu-id="b5c20-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="b5c20-151">Пытается удалить задание в указанной области группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5c20-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="b5c20-152">При использовании в сочетании с ResourceName, ResourceType и (необязательно) параметрами ParentResource команда создает иерархическую область в форме относительного URI, который определяет ресурс.</span><span class="sxs-lookup"><span data-stu-id="b5c20-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b5c20-153">-ResourceName</span></span>
<span data-ttu-id="b5c20-154">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="b5c20-154">The resource name.</span></span>
<span data-ttu-id="b5c20-155">Например, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="b5c20-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="b5c20-156">Необходимо использовать в сочетании с ResourceGroupName, ResourceType и (необязательно) параметрами ParentResource для создания иерархической области в форме относительного URI, определяющего ресурс, и удаления задания в этой области.</span><span class="sxs-lookup"><span data-stu-id="b5c20-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b5c20-157">-ResourceType</span></span>
<span data-ttu-id="b5c20-158">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="b5c20-158">The resource type.</span></span>
<span data-ttu-id="b5c20-159">Для таких, например, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="b5c20-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="b5c20-160">Необходимо использовать в сочетании с ResourceGroupName, ResourceName и (необязательно) параметрами ParentResource для создания иерархической области в форме относительного URI, определяющего ресурс, и удаления задания в этой области ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5c20-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b5c20-161">-RoleDefinitionId</span></span>
<span data-ttu-id="b5c20-162">Идентификатор роли RBAC, для которой необходимо удалить назначение.</span><span class="sxs-lookup"><span data-stu-id="b5c20-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

```yaml
Type: Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b5c20-163">-RoleDefinitionName</span></span>
<span data-ttu-id="b5c20-164">Имя роли RBAC, для которой необходимо удалить назначение, например читатель, участник, Администратор виртуальной сети и т. д.</span><span class="sxs-lookup"><span data-stu-id="b5c20-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-165">-Scope</span><span class="sxs-lookup"><span data-stu-id="b5c20-165">-Scope</span></span>
<span data-ttu-id="b5c20-166">Область назначения роли, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b5c20-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="b5c20-167">В формате относительных URI.</span><span class="sxs-lookup"><span data-stu-id="b5c20-167">In the format of relative URI.</span></span>
<span data-ttu-id="b5c20-168">Например, "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="b5c20-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="b5c20-169">Если не указано, будет выполнена попытка удаления роли на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="b5c20-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="b5c20-170">Если указан, она должна начинаться с "/Subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="b5c20-170">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-171">-Намерено</span><span class="sxs-lookup"><span data-stu-id="b5c20-171">-ServicePrincipalName</span></span>
<span data-ttu-id="b5c20-172">Значение программного приложения Azure AD</span><span class="sxs-lookup"><span data-stu-id="b5c20-172">The ServicePrincipalName of the Azure AD application</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="b5c20-173">-SignInName</span></span>
<span data-ttu-id="b5c20-174">Адрес электронной почты или имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="b5c20-174">The email address or the user principal name of the user.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5c20-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5c20-175">-Confirm</span></span>
<span data-ttu-id="b5c20-176">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b5c20-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5c20-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5c20-177">-WhatIf</span></span>
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

### <span data-ttu-id="b5c20-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c20-178">CommonParameters</span></span>
<span data-ttu-id="b5c20-179">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5c20-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c20-180">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5c20-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c20-181">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5c20-181">INPUTS</span></span>

### <span data-ttu-id="b5c20-182">Ничего</span><span class="sxs-lookup"><span data-stu-id="b5c20-182">None</span></span>
<span data-ttu-id="b5c20-183">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b5c20-183">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b5c20-184">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5c20-184">OUTPUTS</span></span>

### <span data-ttu-id="b5c20-185">System. Collections. Generic. List ' 1 [Microsoft. Azure. System. Resources. Authorization. PSRoleAssignment]</span><span class="sxs-lookup"><span data-stu-id="b5c20-185">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment]</span></span>

## <span data-ttu-id="b5c20-186">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5c20-186">NOTES</span></span>
<span data-ttu-id="b5c20-187">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="b5c20-187">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b5c20-188">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5c20-188">RELATED LINKS</span></span>

[<span data-ttu-id="b5c20-189">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b5c20-189">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="b5c20-190">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b5c20-190">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="b5c20-191">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b5c20-191">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

