---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
ms.openlocfilehash: fc954dcf2ce3b9a1c066b3986bbc0bbea302ea2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405660"
---
# <span data-ttu-id="cc018-101">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cc018-101">Remove-AzRoleAssignment</span></span>

## <span data-ttu-id="cc018-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc018-102">SYNOPSIS</span></span>
<span data-ttu-id="cc018-103">Удаляет назначение роли для указанного директора, которому назначена определенная роль в определенной области.</span><span class="sxs-lookup"><span data-stu-id="cc018-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="cc018-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cc018-104">SYNTAX</span></span>

### <span data-ttu-id="cc018-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cc018-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc018-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc018-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc018-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc018-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc018-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc018-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc018-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc018-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc018-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc018-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc018-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc018-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc018-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc018-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc018-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc018-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc018-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc018-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc018-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc018-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc018-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc018-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc018-117">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc018-117">DESCRIPTION</span></span>
<span data-ttu-id="cc018-118">С помощью Remove-AzRoleAssignment управления можно отоблескать доступ к любой основной деятельности в заданной области и данной роли.</span><span class="sxs-lookup"><span data-stu-id="cc018-118">Use the Remove-AzRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>
<span data-ttu-id="cc018-119">Объект назначения, то есть основной должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="cc018-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="cc018-120">Основным может быть пользователь (с помощью параметров SignInName или ObjectId для идентификации пользователя), группа безопасности (с помощью параметра ObjectId для идентификации группы) или задача службы (для определения параметра ServicePrincipalName или ObjectId используется параметр ServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="cc018-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>
<span data-ttu-id="cc018-121">Роль, которая назначена основной, должна быть указана с помощью параметра RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="cc018-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="cc018-122">Область назначения может быть указана и, если не указана, по умолчанию задана область действия подписки, т. е. оно попытается удалить назначение указанному основному заданию и роли в области подписки.</span><span class="sxs-lookup"><span data-stu-id="cc018-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="cc018-123">Область назначения можно укакручить с помощью одного из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="cc018-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="cc018-124">а)</span><span class="sxs-lookup"><span data-stu-id="cc018-124">a.</span></span>
<span data-ttu-id="cc018-125">Область: это вся полнейская область, начиная с \<subscriptionId\> /subscriptions/b.</span><span class="sxs-lookup"><span data-stu-id="cc018-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="cc018-126">ResourceGroupName — имя любой группы ресурсов в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="cc018-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="cc018-127">в.</span><span class="sxs-lookup"><span data-stu-id="cc018-127">c.</span></span>
<span data-ttu-id="cc018-128">ResourceName, ResourceType, ResourceGroupName и (необязательно) ParentResource — определяет определенный ресурс в подписке.</span><span class="sxs-lookup"><span data-stu-id="cc018-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="cc018-129">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cc018-129">EXAMPLES</span></span>

### <span data-ttu-id="cc018-130">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cc018-130">Example 1</span></span>
```
PS C:\> Remove-AzRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="cc018-131">Удаляет назначение ролей для тех, кому назначена роль "Читатель" в области "Группа ресурсов john.doe@contoso.com rg1".</span><span class="sxs-lookup"><span data-stu-id="cc018-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="cc018-132">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cc018-132">Example 2</span></span>
```
PS C:\> Remove-AzRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="cc018-133">Удаляет назначение роли для группы, которая была определена объективным объектом и назначена роли "Читатель".</span><span class="sxs-lookup"><span data-stu-id="cc018-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="cc018-134">По умолчанию для удаления задания используется текущая подписка.</span><span class="sxs-lookup"><span data-stu-id="cc018-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="cc018-135">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cc018-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="cc018-136">Удаляет первый объект назначения роли, извлеченный Get-AzRoleAssignment командлета.</span><span class="sxs-lookup"><span data-stu-id="cc018-136">Removes the first role assignment object which is fetched from the Get-AzRoleAssignment commandlet.</span></span>

## <span data-ttu-id="cc018-137">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc018-137">PARAMETERS</span></span>

### <span data-ttu-id="cc018-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc018-138">-DefaultProfile</span></span>
<span data-ttu-id="cc018-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cc018-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc018-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc018-140">-InputObject</span></span>
<span data-ttu-id="cc018-141">Объект "Назначение ролей".</span><span class="sxs-lookup"><span data-stu-id="cc018-141">Role Assignment object.</span></span>

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

### <span data-ttu-id="cc018-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cc018-142">-ObjectId</span></span>
<span data-ttu-id="cc018-143">ОбъектId Azure AD пользователя, группы или основной службы.</span><span class="sxs-lookup"><span data-stu-id="cc018-143">Azure AD ObjectId of the user, group or service principal.</span></span>

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

### <span data-ttu-id="cc018-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="cc018-144">-ParentResource</span></span>
<span data-ttu-id="cc018-145">Родительский ресурс в иерархии (из ресурса, указанного с помощью параметра ResourceName), если он имеется.</span><span class="sxs-lookup"><span data-stu-id="cc018-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="cc018-146">Необходимо использовать в сочетании с параметрами ResourceGroupName, ResourceType и ResourceName, чтобы создать иерархическую область в виде относительного URI, определяемого ресурсом.</span><span class="sxs-lookup"><span data-stu-id="cc018-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

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

### <span data-ttu-id="cc018-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc018-147">-PassThru</span></span>
<span data-ttu-id="cc018-148">Отображение удаленного назначения роли, если он задан.</span><span class="sxs-lookup"><span data-stu-id="cc018-148">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="cc018-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc018-149">-ResourceGroupName</span></span>
<span data-ttu-id="cc018-150">Имя группы ресурсов, которая назначена роли.</span><span class="sxs-lookup"><span data-stu-id="cc018-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="cc018-151">Пытается удалить назначение в указанной области действия группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc018-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="cc018-152">При использовании в сочетании с параметрами ResourceName, ResourceType и (необязательно)ParentResource команда формирует иерархическую область в виде относительного URI, определяемого ресурсом.</span><span class="sxs-lookup"><span data-stu-id="cc018-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="cc018-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="cc018-153">-ResourceName</span></span>
<span data-ttu-id="cc018-154">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="cc018-154">The resource name.</span></span>
<span data-ttu-id="cc018-155">Например, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="cc018-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="cc018-156">Необходимо использовать в сочетании с параметрами ResourceGroupName, ResourceType и (необязательно)ParentResource, чтобы построить иерархическую область в виде относительного URI, определяемого ресурсом, и удаления назначения в этой области.</span><span class="sxs-lookup"><span data-stu-id="cc018-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

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

### <span data-ttu-id="cc018-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="cc018-157">-ResourceType</span></span>
<span data-ttu-id="cc018-158">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="cc018-158">The resource type.</span></span>
<span data-ttu-id="cc018-159">Например, Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="cc018-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="cc018-160">Необходимо использовать в сочетании с параметрами ResourceGroupName, ResourceName и (необязательно)ParentResource для создания иерархической области в виде относительного URI, определяемого ресурсом, и удаления назначения из этой области.</span><span class="sxs-lookup"><span data-stu-id="cc018-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

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

### <span data-ttu-id="cc018-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="cc018-161">-RoleDefinitionId</span></span>
<span data-ttu-id="cc018-162">ИД роли "СДБ", для которой нужно удалить назначение.</span><span class="sxs-lookup"><span data-stu-id="cc018-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

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

### <span data-ttu-id="cc018-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="cc018-163">-RoleDefinitionName</span></span>
<span data-ttu-id="cc018-164">Имя роли СДВ, для которой нужно удалить назначение, например "Читатель", "Участник", "Виртуальный администратор сети" и т. д.</span><span class="sxs-lookup"><span data-stu-id="cc018-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="cc018-165">-Scope</span><span class="sxs-lookup"><span data-stu-id="cc018-165">-Scope</span></span>
<span data-ttu-id="cc018-166">Область удаления назначения роли.</span><span class="sxs-lookup"><span data-stu-id="cc018-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="cc018-167">В формате относительного URI.</span><span class="sxs-lookup"><span data-stu-id="cc018-167">In the format of relative URI.</span></span>
<span data-ttu-id="cc018-168">Например: "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="cc018-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="cc018-169">Если не указано, будет предпринята попытка удалить роль на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="cc018-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="cc018-170">Если указано, оно должно начинаться с "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="cc018-170">If specified, it should start with "/subscriptions/{id}".</span></span>

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

### <span data-ttu-id="cc018-171">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="cc018-171">-ServicePrincipalName</span></span>
<span data-ttu-id="cc018-172">Имя ServicePrincipalName приложения Azure AD</span><span class="sxs-lookup"><span data-stu-id="cc018-172">The ServicePrincipalName of the Azure AD application</span></span>

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

### <span data-ttu-id="cc018-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="cc018-173">-SignInName</span></span>
<span data-ttu-id="cc018-174">Адрес электронной почты или имя директора пользователя.</span><span class="sxs-lookup"><span data-stu-id="cc018-174">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="cc018-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc018-175">-Confirm</span></span>
<span data-ttu-id="cc018-176">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc018-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc018-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc018-177">-WhatIf</span></span>
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

### <span data-ttu-id="cc018-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc018-178">CommonParameters</span></span>
<span data-ttu-id="cc018-179">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc018-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc018-180">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc018-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc018-181">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc018-181">INPUTS</span></span>

### <span data-ttu-id="cc018-182">System.String</span><span class="sxs-lookup"><span data-stu-id="cc018-182">System.String</span></span>

### <span data-ttu-id="cc018-183">System.Guid</span><span class="sxs-lookup"><span data-stu-id="cc018-183">System.Guid</span></span>

### <span data-ttu-id="cc018-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cc018-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="cc018-185">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc018-185">OUTPUTS</span></span>

### <span data-ttu-id="cc018-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cc018-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="cc018-187">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cc018-187">NOTES</span></span>
<span data-ttu-id="cc018-188">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="cc018-188">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="cc018-189">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc018-189">RELATED LINKS</span></span>

[<span data-ttu-id="cc018-190">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cc018-190">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="cc018-191">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cc018-191">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="cc018-192">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cc018-192">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

